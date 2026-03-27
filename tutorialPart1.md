Section 1: Getting Started
1. The Terminal
Here’s what nobody tells you about Claude Code: it doesn’t live in a browser.

It lives in the terminal. The text-based interface on your computer where you type commands and things happen.

The terminal looks intimidating. Blank screen. Blinking cursor. No buttons, no menus, no drag-and-drop.

But here’s what you get in return: instead of clicking through 15 browser tabs, copying text between windows, and manually doing everything yourself... you type 1 sentence and Claude does the work because it has access to your COMPUTER, your files, your images, and the internet, plus you give it access to apps you use daily like Google Suite, Airtable, Notion, Blotato, etc.

Before: 15 windows open, copying and pasting between ChatGPT, your files, your browser, your spreadsheet.

After: 1 window. You type what you want. Claude reads your files, makes the changes, and shows you what it did.

How to find it: on Mac, open Launchpad, type “Terminal”, hit enter. On Windows, search for “Command Prompt.”

Set up your playground: once you have the terminal open, paste these 2 lines one at a time, to create a practice folder and enter it:

mkdir ~/playground

cd ~/playground

This is your playground for the rest of this tutorial. Everything Claude creates will live here.

2. Installation + Pricing
Before you type claude, you need to install it.

Open your terminal and paste this:

Mac/Linux: curl -fsSL https://claude.ai/install.sh | bash

Windows PowerShell: irm https://claude.ai/install.ps1 | iex

Hit enter. Done.

Full instructions at code.claude.com/docs/en/quickstart.

3 ways to pay:

- Max plan ($100/month, or $200/month for more): flat monthly fee, unlimited usage. Best if you’re using it daily for business.

- Pro plan ($20/month): monthly subscription, limited usage. Good for getting started.

If you’re a business owner who’ll use this every day, go Max. Don’t think about it. The ROI shows up in the first week. I’ve been on Max $200/month for a very long time and cancelled many other subscriptions as a result.

PASTE THIS INTO CLAUDE (your first prompt after installing):

What are you and what do you have access to on my computer? Give me the 30-second version.

3. File Access
This is the concept where Claude Code stops being a chatbot and starts being useful.

Claude Code reads and edits files on your computer. With your permission.

Not “paste your document into a chat window” like ChatGPT. It SEES your actual files. Your proposals, your spreadsheets, your client folders. And it edits them directly.

Before: copy-pasting your proposal into ChatGPT, losing all the formatting, getting a generic response.

After: “read my proposal.docx and tighten the executive summary” and Claude opens the file, reads it, and rewrites the section IN your document. You don’t have to copy-paste or drag-and-drop because Claude can just find it and update it directly.

PASTE THIS INTO CLAUDE:

Analyze the latest CSV in my downloads folder.

Claude can also CREATE files, not just read them. Try this next:

PASTE THIS INTO CLAUDE:

Create a file containing your analysis.

Open the file to check it out :)

4. Image + PDF Reading
Besides text, Claude Code sees images, screenshots, PDFs, diagrams, photos of whiteboards, mockups, receipts. Drop a file in and it reads it.

Take a screenshot of an error message and paste it. Drag in a PDF invoice. Share a photo of your whiteboard brainstorm. Claude reads it all and works with it like text.

Before: manually retyping what’s on a screenshot or PDF. Or describing an image to ChatGPT and hoping it understands.

After: drop in the image. Claude sees it, reads it, and acts on it.

PASTE INTO CLAUDE: take a screenshot of anything, drop it into your Claude session, and ask Claude to describe it.

---

Section 2: Your First Real Tasks
5. Tool Use (Claude ACTS, Not Chats)
This is the paradigm shift. Forget everything you know about chatbots.

Claude Code doesn’t chat. It ACTS.

It reads files, edits documents, runs commands, searches your folders, fetches web pages, connects to your apps. Each action is a “tool.” You see them happening in real time as Claude works.

Here’s what a tool call looks like in practice: you ask Claude to find invoices. It uses the search tool to scan every file in your folder. Then it uses the read tool to open each match. Then it uses the write tool to create a summary document.

Tools are built into Claude Code. MCP (concept #25) lets you add MORE tools by connecting external apps like Airtable, Google Drive, and Slack. The difference: tools are what Claude does on your computer. MCP extends those tools to the internet.

Before: AI gives advice and YOU do the work. “Here are the steps to update your spreadsheet...”

After: AI does the work and you review. “Here’s your updated spreadsheet. I changed 47 rows.” You SEE each tool call happening as it works.

PASTE THIS INTO CLAUDE:

Look through my Downloads folder, list every file by type (PDF, image, spreadsheet, etc), and create a new file summary.md with your organization suggestions. Show me each step as you go.

Now, you’ll see Claude READING, then THINKING, then WRITING.

6. How to Talk to Claude Code
The #1 mistake: vague prompts.

“Help me with my marketing” = garbage in, garbage out.

“Write a 3-email welcome sequence for my dog walking business. Casual tone, mention our GPS tracking feature, each email under 200 words, include a CTA to book a free walk” = RESULTS.

Be specific. Say what you want AND what you don’t want. Give constraints. Name files. The more specific your ask, the more specific the result.

Tag specific files with @ to make sure Claude reads the right ones. Type @ and autocomplete shows your files. @budget_2024.xlsx pulls in your budget. @client_list.csv pulls in your client list. It’s like tagging someone in a group chat, but for files.

And here’s a power move: instead of trying to write the perfect prompt, let Claude help you write it.

Before: vague prompts, vague results, frustration, “AI doesn’t work.”

After: specific asks, specific results, shipped work, “how did I live without this?”

PASTE THIS INTO CLAUDE:

I need you to write a cold email to a local pet store pitching a partnership. Ask me clarifying questions, one at a time, until you’re 95% confident you can complete the task.

7. CLAUDE.md (Your AI’s Instruction Manual)
This is where Claude Code gets PERSONAL.

A CLAUDE.md file is a document you write once, and Claude reads it at the start of EVERY conversation. It’s your AI employee’s job description.

“Here’s how my business works. Here are my brand rules. Here’s what I NEVER want you to do. Here are the tools I use. Here’s my writing style.”

Teach it once, it knows every time. No more repeating yourself every conversation.

In Claude Code, you don’t even need to know how to create files. Say: “create a file called CLAUDE.md with these 3 rules” and tell it your rules. Done.

Before: “Remember, I want you to...” every single conversation. “I TOLD you yesterday, don’t use this format!”

After: write it once in CLAUDE.md. Claude follows your rules from now on. Forever.

PASTE THIS INTO CLAUDE:

Create a CLAUDE.md file based on everything you’ve learned about my preferences and how I work. Ask me clarifying questions about anything critical.

8. Plan Mode
If you learn ONE thing from this newsletter, make it this.

Plan mode means Claude writes out its full approach BEFORE making any changes. You review the plan, adjust it, approve it... THEN it builds.

It’s like getting a proposal from a contractor before they start demolishing your kitchen. You see what they’ll do, how they’ll do it, and what it’ll cost. Then you say “go.”

90% planning, 10% building.

Without plan mode, Claude rewrites half your files and you have no idea what happened. With plan mode, you’re the boss reviewing a proposal. I personally spend MOST of my time in plan mode for mission-critical activities, such as coding.

Before: Claude makes 47 changes and you have no idea what happened or why.

After: you see the plan, approve each step, stay in control. THEN it executes. Fast and right. As best practice, you should continue watching what Claude actually does in case it goes down the wrong rabbit hole, and you need to interrupt it.

press Shift+Tab until you see “plan”, then PASTE THIS INTO CLAUDE:

Reorganize all the files in my Downloads folder into subfolders by file type. Watch Claude write out the full plan for your approval before moving a single file.

Next, review the plan. You can select text in the plan and add comments, just like collaborating on Google Docs. Claude will read your feedback and improve the plan.

---

Section 3: How Claude’s Brain Works
9. Context Window
Think of Claude’s memory as a whiteboard.

Everything you say, every file it reads, every response it gives... all goes on the whiteboard.

The whiteboard is big. But it’s not infinite.

When it fills up, older stuff gets summarized to make room. Like taking a photo of the whiteboard before erasing part of it to write more.

This is why Claude sometimes “forgets” what you said 20 minutes ago. The whiteboard filled up and your early notes got compressed. Your early notes blend in with everything else, and it gets increasingly hard to understand what was truly important among all your notes.

Understanding this changes how you use Claude Code. Long, rambling conversations fill the whiteboard fast. Short, focused sessions keep it clean.

PASTE THIS INTO CLAUDE:

/usage (after a few back-and-forths, to see how full your whiteboard is)

10. Tokens + Cost Management
Tokens are how AI measures text. Every word you send and every word Claude sends back costs tokens. There’s a max per conversation (the whiteboard size).

Type /usage to see your spending. It shows input tokens (what you sent) vs output tokens (what Claude sent back). Type / and click “Account & usage” for a fuller breakdown.

4 ways to keep costs down:

1. Switch to a cheaper brain for simple tasks. You have 3 brains to choose from (next concept). Use the expensive one for big tasks, the cheap one for quick questions.

2. Use /clear between unrelated tasks. Don’t let old context pile up.

3. Use /compact during long sessions. Compresses the whiteboard without losing key details.

4. Install the context-mode plugin. It significantly reduces context usage by managing what Claude reads more efficiently. Run these 2 commands: /plugin marketplace add mksglu/context-mode then /plugin install context-mode@context-mode. Full details at github.com/mksglu/context-mode.

11. Model Selection (Picking the Right Brain)
Claude Code gives you 3 brains:

- Opus: the smartest, most thorough, most expensive. Use it for complex projects, big rewrites, anything where quality matters more than speed.

- Sonnet: fast, capable, affordable. Your daily driver. Use it for everyday tasks, quick edits, routine work.

- Haiku: cheap and quick. Use it for simple questions, quick lookups, anything where speed matters more than depth.

You switch mid-conversation based on the task. Building a full marketing strategy? Opus. Renaming a file? Haiku.

PASTE THIS INTO CLAUDE:

type /model, switch to Haiku, and paste: Research Etsy shops selling handmade candles. Then switch to Opus and paste the same prompt. Compare the quality AND check /usage after each. Same task, different brain, different price.

---

Section 4: Managing Conversations
12. /compact
Summarizes your conversation into a condensed version, freeing up whiteboard space WITHOUT losing the key points.

Remember the whiteboard from concept #9? /compact is like taking a photo of the whiteboard, erasing it, and writing a tight summary. You keep the important stuff, lose the fluff, and now you have room for more work.

IN CLAUDE:

/compact (after a long conversation, then ask: Summarize everything we’ve done so far in 3 bullet points. Claude still knows the key details, but the whiteboard is clean.)

13. /clear
Wipes your current conversation. Clean slate.

Use it when you’re switching to a totally different task. If you were working on email sequences and now you want to brainstorm product names, type /clear first. Old context confuses new work.

IN CLAUDE:

/clear (after finishing a task, then start fresh: Brainstorm 5 product names for an AI-powered dog walking app. Notice how Claude doesn’t reference anything from your previous conversation.)

14. Session Management
Each conversation is a session. Close the terminal, come back tomorrow, pick up where you left off.

Type claude --resume and you’re back in your last session. Your work doesn’t disappear.

Start fresh sessions for new topics. Resume old sessions for ongoing work.

Before: losing your entire conversation when you close the window.

After: pick up tomorrow exactly where you stopped.

Close Claude Code, reopen Terminal, type claude --resume, then paste: Where did we leave off?

---

Section 5: Controlling Claude
15. Permission Modes + Settings
You control how much freedom Claude has. Like setting parental controls, but for your AI employee.

From “ask me before every single edit” (safe, slow, good for learning) to “do whatever you need” (fast, you trust it, good for routine tasks).

Press Shift+Tab to cycle through modes. When you’re new, keep the guardrails tight. As you build trust, loosen them.

You also configure default settings. Your default permission level, preferred model, and other preferences all live in one place. Set your defaults once and every new session starts the way you want.

Before: Claude running wild making changes you didn’t approve. Or asking permission for every tiny thing.

After: you set your comfort level and it matches your pace. Every session starts with your preferred defaults.

PASTE THIS INTO CLAUDE:

Show me my current settings and explain what each one does in plain English. Then recommend the best defaults for a business owner who’s been using Claude Code for a day.

16. Effort Levels
Tell Claude how hard to think.

Low effort for quick answers (”what time zone is Denver in?”). High effort for complex problems (”restructure my entire pricing strategy”).

You don’t always need full brain power. Effort levels let you get fast answers for simple stuff and deep analysis for hard stuff. Change it anytime by typing /model and using the left/right arrow keys to adjust the effort slider.

There’s also a keyword: type “ultrathink” in your prompt and Claude maxes out its reasoning for one response. It’ll think through every edge case before answering. Also, it’s RAINBOW COLORED!!

Before: waiting 30 seconds for Claude to overthink a simple question.

After: low effort for quick stuff, ultrathink for the complex stuff.

IN CLAUDE:

type /model, use the left arrow key to set effort to low, then ask What’s 15% of $847? Then open /model again, set effort to high, and paste:

ultrathink: I run a freelance consulting business making $12k/month with 60% margins. Map out 3 paths to $50k/month with pros, cons, and timeline for each. Compare the depth.

In VSCode, there’s a nice shortcut - you can just type /effort.

17. Interrupt + Redirect
Press Escape anytime to stop Claude mid-task.

Like telling an employee “stop, new priority.” Claude stops immediately and waits for your next instruction. No work is lost. You pivot.

Before: watching Claude spend 2 minutes doing the wrong thing because you gave a bad instruction.

After: Escape, correct course, keep moving. Instant pivot.

PASTE THIS INTO CLAUDE:

Write me a 500-word blog post about... then immediately press Escape before it finishes. Now paste: Scratch the blog post. Give me 10 Instagram caption ideas for my real estate listings instead. Instant pivot.

---

Section 6: Reviewing Work + Teaching Claude
18. Visual Studio Code
You’ve been using the terminal for a few days. You’re getting comfortable. Now let me show you something better for REVIEWING Claude’s work.

VS Code is a free app (it says “code editor,” but don’t let the name scare you).

It’s like fancy Google Docs, so you and Claude Code can collaborate and review files together!

FUNNNNN :D

It shows your files with nice formatting, tabs, and a sidebar. Claude Code runs right inside it.

When Claude edits 5 files, you want to SEE what changed. VS Code shows you exactly which lines were added, removed, or modified. Color-coded. Side by side.

The terminal is great for giving AI instructions. VS Code is great for giving instructions AND reviewing the results.

Before: squinting at the terminal trying to figure out what Claude changed.

After: VS Code shows every change, highlighted, in context. You review like a boss and approve.

NEXT STEPS: download VS Code (free), install the Claude Code extension, open our playground folder, click the orange Claude Code extension to open it.

Then paste: “Rewrite the analysis to be half the length and twice as casual.”

Now look at VS Code’s left sidebar. You can see the updated analysis right there. You can highlight words or sentences and Claude is context-aware of the feedback you’re giving.

On the left sidebar, if you click the Claude Code icon, you’ll see ALL your Claude sessions including your local Claude Code session, as well as your web-based Claude.ai sessions!

Disadvantages of Visual Studio Code include:

- the official Claude Chrome VSCode extension sometimes doesn’t have features yet, such as remote control and btw at time of this writing, however you can always launch a terminal within VSCode

- terminal will have the least bugs in general; Claude Code VSCode extension sometimes has weird quirks or freezes

- it may be unnecessary/heavy if you don’t need to heavily review your AI employee’s outputs

---

19. Memory
Think of CLAUDE.md (concept #7) and Memory as two different things.

CLAUDE.md is your instruction manual. Your playbook/SOP for a project. You write it. It’s like handing a new employee a job description on day 1: “here’s how we do things, here are the tools, here are the rules.” It loads every conversation automatically. You can also have a global CLAUDE.md that’s like a “meta instruction manual” applying to all projects.

Memory is Claude’s personal notebook. Claude writes it (or you tell it to). It’s like an employee jotting down notes after meetings: “boss prefers casual tone, last time I used formal language she corrected me, the database field is called ‘Video URL’ not ‘Drive URL’.”

Put the system in CLAUDE.md: API references, account IDs, workflow steps, project structure. Stuff you’d put in a wiki.

Let preferences accumulate in memory: your writing style, corrections you’ve given, context about ongoing work. Stuff you’d tell a coworker once and expect them to remember.

If you find yourself repeating the same correction, tell Claude “remember this.” If it’s a rule every conversation needs from line 1, put it in CLAUDE.md.

Before: repeating your preferences every conversation. “I TOLD you yesterday!”

After: correct Claude once. It writes it down. It never forgets.

PASTE THIS INTO CLAUDE:

Remember: I prefer short, casual emails. My business is a dog walking app in Denver. I always sign off with “Cheers” not “Best regards.”

(start a new session and paste: Write a follow-up email to a client named Sarah about her golden retriever Max. See if it remembers.)

20. Project Scope vs Global Scope
Your dog walking app has different rules than your Etsy candle shop. But your name and preferences are the same everywhere.

Project scope: settings applying ONLY to your current project folder. Each project gets its own CLAUDE.md, its own rules, its own playbook.

Global scope: settings following you everywhere. Your name, your writing style, your preferences.

Think of it like having different employee handbooks for different departments, but 1 company-wide policy covering all of them.

Before: your blog project rules bleeding into your app project.

After: each project has its own playbook. Global preferences stay consistent.

PASTE THIS INTO CLAUDE:

Create a CLAUDE.md for this project with rules tailored to what we’re doing here. Also show me what’s in my global settings so I know what applies everywhere. Ask me clarifying questions to customize how to organize this for my needs.

---

Section 7: Skills + Automation
21. Slash Commands
Type “/” in Claude Code and a menu pops up. Quick actions you’ll use all the time:

/help, /clear, /compact, /model, /usage.

There are also 2 hidden gems most people miss:

- /insights shows you patterns in how you’ve been using Claude Code. What’s working, what’s not, where you’re spending the most tokens. It’s your personal performance dashboard.

- /btw lets you give Claude a side note without interrupting its current task. Claude is halfway through rewriting your proposal and you realize “oh, I forgot to mention, use my new phone number.” Type /btw use 555-1234 as my phone number and Claude absorbs it without losing its place. As of March 13 2026, this command is currently available in terminal, not yet in the VSCode Claude Code extension.

IN CLAUDE: type “/” and scroll through everything. Try /insights to see your personal usage patterns so far.

22. Skills (Your Custom Workflows)
THIS is where Claude Code goes from useful to life-changing.

I frequently hear from folks who followed my Claude Code tutorials: “MIND BLOWING!!”

A skill is a set of instructions saved as a file. They can be chained together. They can do complex things. Type /skill-name and an entire workflow runs.

Claude Code will always interpret your prompt, then determine what skill(s), if any, it should use. Or you can trigger the skill manually by typing /skill-name.

Here’s what my /crosspost skill does with 1 command:

1. Searches Google Drive for my latest finished videos (file access + tool use)

2. Downloads each video to my computer temporarily (file system tools)

3. Transcribes the audio using Whisper, a speech-to-text tool running locally on my machine (terminal commands)

4. Matches each transcript to its topic in my Airtable database (MCP connection to Airtable)

5. Reads my brand voice rules from my CLAUDE.md and writing templates (file access + context)

6. Writes 3 types of captions per video: a long SEO description for TikTok/YouTube/Instagram/Facebook, a short conversational tweet for Twitter/Threads/Bluesky, and a standalone text post for Substack (AI writing with constraints)

7. Runs every caption through a quality gate blocking banned words, checking character limits, catching vague references, and rejecting formatting I don’t use (hooks, concept #23)

8. Shows me all the captions in a review file so I approve them before anything goes live (plan mode philosophy, draft approval)

9. Publishes to 7 platforms simultaneously via Blotato’s API (MCP tool calls, parallel subagents)

10. Stores the Substack caption in Airtable for my n8n automation to pick up and post later (MCP + external automation)

11. Updates my Airtable database with the transcript, captions, post date, and status for every video (MCP + record keeping)

12. Renames the original files on Google Drive so I know they’ve been posted (file management via API)

13. Create DM automations by launching Claude Chrome extension, cloning DM automation templates, and swapping out the keyword and links.

1 command. 8 platforms. 12 steps.

All the concepts you’ve learned working together!

And it does this in parallel with subagents. If I have 5 videos, it spawns 5 mini-Claudes to transcribe them all at once, then 5 more to publish them all at once. What would take me 3 hours takes 10 minutes.

THIS is what a skill looks like at full power.

A markdown file with instructions turning Claude Code into your AI employee.

You don’t need to start this complex. Your first skill should be dead simple.

A /weekly-recap skill. It reads all the files you changed this week, summarizes what you worked on, and drafts a 3-paragraph update email for your team or clients. File access + AI writing + your CLAUDE.md voice rules. Concepts you already know.

1 command. Every Friday. Done in 30 seconds.

Later, when you add MCP connections (concept #25) and Perplexity (concept #26), your skills get WILD. A /fact-check skill reads your content line by line, searches the internet for primary sources, and flags anything unverified. But start simple.

Before: writing the same 500-word prompt every time you want to run a recurring workflow.

After: /skill-name and the entire thing runs. Build it once, use it forever. Improve it over time.

PASTE THIS INTO CLAUDE:

Create a skill called “weekly-recap”. It should read all files modified in the last 7 days, summarize what changed and why, and draft a short update email in my voice. Make it something I’d run every Friday. Now you have /weekly-recap forever.

23. Hooks (Automated Guardrails)
Hooks are scripts running automatically before or after Claude takes an action. Guardrails you don’t need to remember.

In my /crosspost skill, I have a quality gate hook. Every time Claude tries to publish a post, the hook automatically intercepts it and checks:

- Are there any banned punctuation marks? (I block specific ones from my brand voice.)

- Are there banned words? (40+ words I’ve banned.)

- Is the caption over the platform’s character limit?

- Is there missing media for platforms needing it?

- Does the text reference “this website” without naming the specific website?

If ANY check fails, the hook blocks the post. Claude has to fix the issue and try again. This happens automatically. I don’t need to remember to check. The guardrail is built in.

You also get a desktop notification when long tasks finish, so you don’t need to stare at the screen waiting.

You set up hooks by telling Claude what you want. Claude creates the hook for you.

Before: forgetting to proofread, shipping typos, breaking your own brand rules.

After: automated quality checks every single time. You set the rules, hooks enforce them.

PASTE THIS INTO CLAUDE:

Set up a hook so my Mac sends me a desktop notification every time you finish a long task. I want to hear a sound when you’re done so I don’t need to watch the screen.

---

Section 8: Connecting Claude to the Real World
24. Web Browsing
Claude reads any webpage you give it.

Paste a URL and it fetches the page, reads the content, and works with it. Competitor pricing pages, blog posts, documentation, job listings, recipes... anything public on the internet.

Here’s what makes this different from ChatGPT: Claude Code reads the page AND takes action. It doesn’t stop at a summary. It writes a comparison doc, saves it to your project folder, and moves on to the next task.

Before: manually copying website text into a chat window, losing formatting, missing sections.

After: Claude fetches the page, pulls the data, creates a file with the analysis, and saves it. You review the finished document.

PASTE THIS INTO CLAUDE (swap the URL for a real one):

Read https://www.blotato.com, pull out their pricing tiers and top features, then create a file called competitor_analysis.md comparing them to 2 other competitors.

25. MCP Servers (From Consultant to Employee)
MCP stands for Model Context Protocol. In plain English: it’s the bridge between Claude and your real tools.

Remember tools (concept #5)? Those are what Claude does on your computer: reading files, searching folders, running commands. MCP extends this to the INTERNET. It connects Claude to apps like Google Drive, Slack, Notion, Airtable, Stripe, Perplexity, and your email.

Without MCP, Claude says “go update your Airtable.” With MCP, Claude UPDATES your Airtable.

My /crosspost skill uses 3 MCP connections: Airtable (to read topics and update records), Blotato (to publish to 7 social platforms), and Google Drive (to find and download videos). Claude talks directly to these tools. No copy-pasting. No switching tabs.

Before: Claude says “here’s what you should update in your spreadsheet.” And YOU do it.

After: Claude updates the spreadsheet, confirms the change, and moves to the next task.

PASTE THIS INTO CLAUDE:

Help me connect my first MCP server. Walk me through adding Airtable step by step. I’ve never done this before.

Once you’ve connected Airtable MCP, try asking Claude to read or update items in your Airtable!

Type /mcp to see all your current MCP servers.

26. Perplexity MCP (AI-Powered Web Research)
Web browsing (#24) lets Claude read pages you point it to. Perplexity MCP lets Claude RESEARCH the entire internet with verified sources. I personally use Perplexity MCP ALL THE TIME instead of Claude’s native internet capabilities.

This step is optional, but I highly recommend it.

Instead of “read this 1 link,” it’s “go research this topic, find the 10 best verified sources, and tell me where you got each fact.”

This is the upgrade from reading 1 article to having a research assistant who reads 50 and gives you the summary with citations.

Note: Perplexity has its own pricing (free tier + paid plans at perplexity.ai). Check their site for current numbers.

Before: Claude reads the 1 page you gave it.

After: Claude finds the best sources using Perplexity MCP tailored to research, synthesizes sources, and cites every piece of info.

PASTE THIS INTO CLAUDE (after adding Perplexity MCP):

Create a skill called ‘fact-check’. It should read whatever content I provide, go line by line, and use Perplexity MCP to find primary sources backing every claim, and flag anything unverified. Each claim gets a verdict: confirmed, unverified, or wrong. With citations.

---

Section 9: Agents, Remote Control + Scheduling
27. Subagents (Automatic Parallel Workers)
When you give Claude a task with multiple independent parts, it automatically spawns mini-Claudes to handle them in parallel. You don’t need to ask for it. You don’t need to set it up. Claude decides on its own when parallel work would be faster.

“Research these 5 competitors” becomes 5 agents working simultaneously instead of 1 going through them 1 by 1.

In my /crosspost skill, if I have 5 new videos, Claude spawns 5 transcription agents at once. All 5 videos get transcribed simultaneously. Then 5 more to publish them all at once. What used to be sequential is now parallel.

You’ll see it happening in the output. Multiple tasks running at the same time. No configuration needed.

Before: watching Claude research competitors sequentially for 10 minutes.

After: 5 agents, 2 minutes, same work. Automatically.

PASTE THIS INTO CLAUDE:

I need you to deeply research 5 companies for me. For EACH company, spawn a separate agent to visit their website, read their pricing page, read their features page, read at least 2 customer reviews, and write a full 1-page competitive analysis saved as a separate file. The companies: Notion, Airtable, Monday.com, ClickUp, and Asana.

Sit back and watch it spawn 5 agents working simultaneously!

It will say “Agent: Research XX competitive analysis” 5 times :) these are your AI employees working in parallel.

28. Remote Control (Use Claude From Your Phone)
Start a Claude Code session on your computer, then continue it from the Claude mobile app on your phone. Walk away from your desk. Keep working from the couch, a coffee shop, anywhere.

Your computer does all the heavy lifting. The phone is the remote control.

As of March 13 2026, remote control is available in terminal, but NOT in Visual Studio Code’s official Claude Chrome extension.

Pro tip: you can always open a terminal within VSCode!

How to set it up:

1. Make sure you’re on Claude Code v2.1.51+ (type claude --version to check, claude update to upgrade)

2. Type claude remote-control in Terminal (or /rc inside an existing session)

3. A QR code appears on screen. Scan it with your phone camera.

4. The Claude mobile app opens directly to your session. You’re connected.

Everything stays on your machine. The phone is a window into your local session.

To enable this by default: type /config inside Claude Code, find “Enable Remote Control for all sessions”, toggle it on. Now every session is accessible from your phone automatically.

Before: need to be at your desk to use Claude Code.

After: start a task at your desk, continue it from your phone while walking the dog or ruminating on the toilet. CEO mode.

IN CLAUDE:

/remote-control (scan the QR code with your phone, then send a message from the Claude app to confirm it works)

29. Scheduled Tasks (/loop)
Schedule Claude to run tasks on a recurring timer using /loop.

/loop 1h check if any new files were added to my Google Drive

/loop 1d pull my marketing data from Airtable and summarize

You write the interval and the task in plain English. Claude runs it automatically in the background. Type Show me all my scheduled tasks to see what’s running and cancel anything you don’t need.

2 things to know: tasks in the terminal only run while your session is open (close the terminal, they stop). And they auto-expire after 3 days as a safety net.

For permanent recurring tasks, you’d have to use the Claude Code Desktop app, which has other limitations. Personally, this is why I still use n8n for its orchestration layer, especially with n8n-mcp which allows Claude Code to create and fix all my n8n automations.

Before: manually pulling the same report every morning.

After: /loop 1d summarize yesterday’s sales and it’s waiting for you when you sit down.

PASTE THIS INTO CLAUDE:

/loop 1h check my Downloads folder for new PDF invoices and list them with the total amount.

30. Version Control with Git
Every time Claude makes changes, you want a save point you can roll back to. That’s git. It’s already built into Claude Code.

Git is LOCAL. It saves versions on your computer. Think of it like a timeline of every change Claude ever made. You can rewind to any point. Nothing gets lost.

GitHub is the OPTIONAL cloud layer on top. It backs up your project online, lets you share it with a developer, and lets them review what Claude did. If you work with a team or want cloud backup, it’s worth setting up. But if you’re working solo, local git is all you need to start.

Claude Code works with both natively. Save versions, create branches, roll back mistakes, open pull requests for your developer to review... all from the terminal.

Before: Claude makes changes and you pray nothing breaks. No undo button.

After: every change is saved, documented, and reversible. You roll back to any previous version in seconds.

PASTE THIS INTO CLAUDE:

Save all the changes we’ve made today as a new version with a description of what changed.

---

Where to Start (Don’t Learn All 30 at Once)
The shiny object trap is the #1 waste of time. Master 5 concepts before adding the next 5.

Your first week (concepts 1-8):

1. Install it and open the terminal

2. Give it a file and watch it read + edit

3. Watch the tools work in real time (concept 5)

4. Create a CLAUDE.md with 3 rules for your main project

5. Use Plan mode for your first real task

After a week (concepts 9-20):

- Learn how the whiteboard works and manage your costs

- Switch between models to save money

- Set up memory so Claude remembers your preferences

- Build your first skill (start with something simple)

- Try VS Code for reviewing changes

After a month (concepts 21-30):

- Connect your first MCP server (Airtable, Notion, or Google Drive)

- Add Perplexity MCP and create a /fact-check skill

- Install the context-mode plugin to reduce token usage

- Set up remote control to use Claude from your phone

- Schedule a recurring task with /loop

- Save your work with git so you can roll back anytime

- Check /insights to see what’s working and optimize your usage

- Browse prebuilt skills

Speaking of prebuilt skills... hundreds of free ones already exist on GitHub. Browsing these repos is one of the best ways to learn what’s possible AND save yourself the work of building from scratch:

- anthropics/skills: Anthropic’s official skills (docs, PDFs, slides, web apps, API builders)

- hesreallyhim/awesome-claude-code: a directory of the entire Claude Code ecosystem

- alirezarezvani/claude-skills: 180+ skills for engineering, marketing, compliance

Simply drop the URL into Claude Code and tell it to set up the 3 most relevant skills for your needs :)

Just my one /crosspost skill saves me 10+ hours every week. And I keep making it better. Finetuned to my exact use case. Build once, reuse forever, improve over time.

Start today. Open the terminal. Type `claude`. Build something.

If you LOVE this newsletter, please SHARE it to help teach more people for FREE!

---