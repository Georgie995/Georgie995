# Hi, I'm Georgi 👋

I'm a post-production data I/O and archive specialist in London, moving into technical operations.

My day-to-day has been ingest, LTO/LTFS tape archive, checksum and manifest verification, and file delivery to cloud storage. That means making sure what arrives, what gets archived and what gets delivered is exactly what it should be, and working out the root cause when it isn't.

## How I work with AI

I build tools with AI coding assistants, and I say so openly. My part is:

- **specifying** what to build, from real failures I've handled;
- **deciding** the safety rules and design choices, which are mine and are logged in each project;
- **testing** it, and reviewing its output the way an operator would.

I build quickly with AI, then study the core tools in depth. I'm currently learning manifest-doctor line by line, then delivery-ops-hub.

Each project documents its design decisions and what I did versus what the AI did.

## Projects

| Project | What it does | Status |
|---|---|---|
| [manifest-doctor](https://github.com/Georgie995/manifest-doctor) | Checks a delivery against its checksum manifest and explains *why* files don't match: an extra wrapper folder, Mac vs Windows file names, a file listed twice with different checksums. JSON/CSV/Markdown reports, 162 tests. | Published |
| [delivery-ops-hub](https://github.com/Georgie995/delivery-ops-hub) | An n8n workflow that receives verification results and job-watch events by webhook, logs every check and builds alerts for problems. Never silent when a check can't run or an alert can't be sent (outbox and resend). Alerts demonstrated as Teams cards in dry-run mode. | Published |
| [ai-triage](https://github.com/Georgie995/ai-triage) | Uses Claude to draft plain-English notes on delivery verification reports, then checks every draft against the report (9 checks: nothing invented, dropped or softened; advice only from my own playbook). Includes a 20-case test harness with cost guard. | Published (live AI evaluation pending) |
| [job-watch](https://github.com/Georgie995/job-watch) | Watches long tape restores and cloud transfers, and alerts once when a job finishes, fails, stalls or starts moving again. It never stops the job. Shows which file is copying and how far along it is, instead of listing folders blindly. Alerts go through delivery-ops-hub. 37 tests with fake jobs. | Published (real Linux run pending) |
| [delivery-desk](https://github.com/Georgie995/delivery-desk) | Joins my three delivery tools into one flow. One command checks a delivery, sends the alert, adds ai-triage's checked summary and, when problems are found, starts an incident note. A second command turns my filled-in note into an email for my manager, with my cause and fix copied word for word. It never sends anything or changes the delivery. 76 tests. | Published |
| [ClearSum](https://github.com/Georgie995/clearsum) | The desktop app version of delivery-desk, for people who don't use the command line: drag in a delivery and its checksum manifest, get a plain-language answer, and turn any problems into an email for your manager. Calm "Paper" design, secrets kept in Windows Credential Manager, a downloadable Windows build, 113 tests including real checks driven through the window. | Published (v0.1.0 download) |

## What I'm looking for

Technical roles that value operational judgement and AI-assisted work: technical operations, support or implementation engineering, solutions engineering, and AI workflow or operations roles. London or remote UK.

## Toolbox

**Daily work:** checksums and manifests (MD5, SHA-256), LTO/LTFS, rclone to S3, Terminal/CLI, Bash and shell (.sh) scripts, media asset management and tracking systems

**Building with:** Python (AI-assisted), Git, pytest, JSON, SQL basics, SQLite, n8n (self-hosted in Docker), webhooks and REST, Windows desktop apps (pywebview, PyInstaller)

**Learning now:** LLM APIs: the Anthropic Python SDK integration is built and tested against a stand-in; first live evaluation run pending
