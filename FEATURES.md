# The Job Scout: features and how to change them

Every feature below is a few lines in [`PROMPT.md`](PROMPT.md). Change the words and you change the behaviour. Run a scan by hand after any edit and read the dropped list.

## Checks every posting against your real resume and a pay bar

**What it does.** The project instructions (step 2) tell the scout to read your resume before judging fit, and give each passing role a fit check: what in your resume matches, anything the posting requires that you may not have, and anything that gave it pause. Rule 3 drops a role only when the confirmed pay is at or below your floor. A posting with no pay listed is kept and flagged.

**Why it's there.** The scout is only as good as the reasons it's allowed to say no. When unsure, it keeps the role, because a posting you skim past costs you ten seconds and a posting it throws away could cost you the job.

**How to change it.**
- Change your floor: edit `[YOUR LOWEST HOURLY RATE]` in rule 3.
- Turn the pay rule off: delete rule 3 and change "There are four" to "There are three".
- Drop postings with no pay listed: change "If no pay is listed, KEEP it and flag it" to "drop it". Expect to lose roles you would have wanted.
- A longer or shorter fit check: change "in 2 to 4 honest sentences".

## Skips roles it has already shown you

**What it does.** The "Morning scan, scheduled" prompt in [`PROMPT.md`](PROMPT.md) tells the scout to skip any role it already gave you in an earlier scan. It also lists roles from earlier scans that are now older than your freshness window, so you can let them go.

**Why it's there.** No reason is written down beyond what it does.

**How to change it.**
- Get a daily reminder until you've looked at each role: add a line to the morning scan prompt such as: "Keep a list of roles I have acknowledged. Until I acknowledge a role, list it again each morning under 'Still waiting for you'."
- See repeats again: delete "Skip any role you already gave me in an earlier scan."
- Stop the aged-out list: delete item 2 of the morning scan's report.

## Only roles posted in the last 7 days

**What it does.** Rule 2 drops anything posted more than [7] days ago. The first scan and the morning scan search the last [7] days, and the morning scan lists roles that have aged out so you can let them go.

**Why it's there.** Seven days is a good start for how fresh a posting has to be.

**How to change it.** Change every [7] in [`PROMPT.md`](PROMPT.md) to the same number: rule 2, step 3 and step 4. A longer window means more roles each morning; a shorter one means fewer.

## Never applies for you

**What it does.** The hard lines in the project instructions and in the morning scan: never click Apply or Easy Apply, never message anyone, never sign in, enter a password or solve a CAPTCHA. If a site needs you, it stops and tells you. The resume and cover letter prompts (step 5) only reorder, cut and reword what is already true, and give you an outline in bullets, not a letter.

**Why it's there.** Deciding whether a role is worth your week, writing the letter and clicking apply stay yours. The outline is there so you don't start from a blank page, not so you skip the writing.

**How to change it.**
- Want a draft letter instead of an outline: change "Keep it to bullets. Don't write sentences for me to copy." in the cover letter prompt. The letter will sound less like you.
- Keep the sign-in, password and CAPTCHA lines whatever else you change.
