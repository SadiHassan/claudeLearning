# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run setup          # First-time setup: install deps + Prisma generate + migrate
npm run dev            # Start dev server with Turbopack (http://localhost:3000)
npm run dev:daemon     # Start dev server in background, logs to logs.txt
npm run build          # Production build
npm run lint           # ESLint
npm test               # Run Vitest tests
npm test -- --run      # Run tests once (no watch mode)
npx vitest run src/path/to/file.test.ts  # Run a single test file
npm run db:reset       # Reset and re-run all migrations (destructive)
```

The dev server requires `NODE_OPTIONS='--require ./node-compat.cjs'` (already embedded in the npm scripts).

## Architecture

**UIGen** is an AI-powered React component generator with live preview. Users describe a component in chat; Claude generates it into a virtual file system; a sandboxed iframe renders the result in real time.

### Request flow

1. User sends a chat message from `src/app/[projectId]/page.tsx`
2. `POST /api/chat` (`src/app/api/chat/route.ts`) reconstructs a `VirtualFileSystem` from the serialized project state, calls `streamText` (Vercel AI SDK) with Claude, and streams back the response
3. Claude calls two tools: `str_replace_editor` (create/edit files) and `file_manager` (rename/delete/list) — both operate on the in-memory `VirtualFileSystem`
4. On finish, if authenticated the project's `messages` and `data` (serialized VFS) are saved to SQLite via Prisma
5. The frontend renders the VFS contents in a Monaco editor and a live iframe preview

### Key abstractions

- **`VirtualFileSystem`** (`src/lib/file-system.ts`) — in-memory tree of `FileNode`s; no files ever touch disk during generation. Serialized as `Record<string, FileNode>` in the `Project.data` JSON column.
- **`getLanguageModel()`** (`src/lib/provider.ts`) — returns `anthropic("claude-haiku-4-5")` when `ANTHROPIC_API_KEY` is set, or a `MockLanguageModel` otherwise. The mock simulates multi-step tool use without an API key.
- **Tools** (`src/lib/tools/`) — `str_replace_editor` and `file_manager` are built as closures over a `VirtualFileSystem` instance per request.
- **Prompts** (`src/lib/prompts/generation.tsx`) — system prompt for component generation.
- **Auth** (`src/lib/auth.ts`) — JWT-based sessions via `jose`; passwords hashed with `bcrypt`. Middleware (`src/middleware.ts`) gates protected routes.
- **Anonymous users** — `src/lib/anon-work-tracker.ts` tracks guest-created projects in localStorage so they can be claimed after sign-up.

### Data model

Prisma with SQLite (`prisma/dev.db`). Two models:
- `User` — email/password accounts
- `Project` — stores `messages` (JSON array) and `data` (serialized VFS JSON); `userId` is nullable for anonymous projects

### Frontend contexts

- `src/lib/contexts/file-system-context.tsx` — shares the client-side VFS state across components
- `src/lib/contexts/chat-context.tsx` — manages chat message state and streaming

### JSX preview

`src/lib/transform/jsx-transformer.ts` transforms JSX to runnable JS (using `@babel/standalone`) for the live iframe preview.
