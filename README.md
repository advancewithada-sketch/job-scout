# The Job Scout

## Make it yours

This is a starting point, not a finished product. It was built for one person's work, and every rule in it is meant to be changed to fit yours. Nothing in here is precious.

- Fill in the `[BRACKETED]` placeholders in [`PROMPT.md`](PROMPT.md) with your own details.
- Read [`FEATURES.md`](FEATURES.md). It explains each feature, why it's there, and which part of the prompt to edit to turn it off, loosen it or swap it.
- Edit the prompt in plain words. If a rule doesn't fit how you work, rewrite it or delete it.
- Run it once by hand after every change and read what comes back.

An agent that reads the job boards every morning, checks each posting against your real resume and your pay floor, and hands you an outline for the ones worth your time. It never applies for you. You still write the letter.

This repo walks the same five steps as the guide, with the prompts already written out in [`PROMPT.md`](PROMPT.md).

## The dashboard: Marketing HQ

This agent reports into one section of **Marketing HQ**, a single dashboard where all of the marketing agents land. The whole dashboard is free in its own repo: [marketing-hq](https://github.com/advancewithada-sketch/marketing-hq). Open it locally to see every section with sample data, or publish it as a Claude artifact with a database and point this agent at it.

## Features

- Checks every posting against your real resume and a pay bar
- Skips roles it has already shown you
- Only roles posted in the last 7 days
- Never applies for you

**Who it's for:** anyone job-hunting alongside running a business.

**What it replaces:** doom-scrolling job boards and rewriting the resume for every posting.

## You need

- A paid Claude plan, and Claude able to use a browser on your computer (Claude in Chrome or the browser in the Claude desktop app).
- About 20 minutes to set up. A few minutes each morning to read what it found.
- Your current resume, the roles you want, and the lowest rate you'd say yes to.

## What it does

1. Searches LinkedIn jobs from the last few days, one plain search per phrase you give it.
2. Opens each posting and reads it properly before judging it.
3. Applies your four rules and nothing else, and keeps and flags anything it's unsure about.
4. For each role that passes: title, company, location, date posted, link, pay as stated, an honest fit check against your resume, and whether the posting asks for anything unusual.
5. Lists every role it dropped, with the rule number it failed and the actual figure if it was pay. That list is how you catch it being too strict.
6. When a role makes you lean in: tailors your resume to one page using only what's already in it, and gives you a cover letter outline in bullets, not a letter.

## What stays yours

- Deciding whether a role is worth your week.
- Writing the letter. The outline is there so you don't start from a blank page, not so you skip the writing.
- Clicking apply.

## What it will never do

- Click Apply or Easy Apply, message anyone, sign in, enter a password or solve a CAPTCHA. If a site needs you, it stops and tells you.
- Invent a salary, a date, a requirement or a link. If the posting doesn't say it, the field stays blank.
- Add a job, a title, a number or a skill to your resume that you didn't give it. It only reorders, cuts and rewords.
- Invent a fifth reason to drop a role.

## Set it up (five steps)

### 1. Write your rules

The scout is only as good as the reasons it's allowed to say no. Give it a short list and nothing else. Anything it's unsure about, it keeps and flags, because a posting you skim past costs you ten seconds and a posting it throws away could cost you the job.

Write down four things before you open Claude: the kind of work (full-time, part-time, contract, fractional, and which ones are a no), how fresh a posting has to be (seven days is a good start), your pay floor (postings with no pay listed get kept and flagged), and every role title you'd answer to. That's the whole list. Industry, company size, how senior it sounds, whether the job board says you're a match: none of those are reasons to drop a role. You decide those yourself. [`rules.example.md`](rules.example.md) shows the shape.

### 2. Make the scout

In Claude, make a new project and call it **Job Scout**. Upload your current resume to the project's files. Paste the "Project instructions" prompt from [`PROMPT.md`](PROMPT.md) into the project's instructions, with your rules from step 1 filled in. Save. Every new chat inside this project already knows your rules and resume, so you never have to paste them again.

### 3. Run your first scan

Sign in to LinkedIn in the browser Claude uses first. Then start a chat inside the Job Scout project and paste the "First scan" prompt. Read the dropped list the first few times. If it threw away something you'd have wanted, tell it which rule it misread and it'll do better next time.

### 4. Make it daily

Once a scan looks right, set it to run on its own. In Claude, create a scheduled task for weekday mornings and use the "Morning scan, scheduled" prompt. It reads LinkedIn in your browser, so your computer needs to be on with Claude open when it runs. Each morning it gives you the new roles that passed (skipping ones you already saw), the roles now older than your freshness window so you can let them go, and the day's dropped list with rule numbers.

### 5. Get ready to apply

When a role makes you lean in, paste the posting link into the Job Scout project with the "One-page resume" prompt, then the "Cover letter outline" prompt. The resume only moves things around and trims, so nothing in there is a lie you have to defend in an interview. If the posting wants something your resume doesn't show, you hear about it and decide whether to address it. The outline is bullets and questions, no finished sentences, so the letter still sounds like you because you still wrote it.

## Files

| File | What it is |
| --- | --- |
| `FEATURES.md` | Each feature, why it's there, and which part of the prompt to edit to change it |
| `PROMPT.md` | All five prompts from the guide, with `[bracket]` placeholders for your details |
| `rules.example.md` | The shape of the four rules and the search phrases you fill in |

## Shared as-is

This is the scout exactly as it runs for one Fractional COO, with personal details taken out. No support, no roadmap. Fork it and make it yours.

Made by Ada from [theoptimized.ceo](https://www.theoptimized.ceo).
