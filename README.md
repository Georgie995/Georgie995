# Hi, I'm Georgi 👋

I'm a post-production data I/O and archive specialist in London, moving into technical operations.

My day-to-day has been ingest, LTO/LTFS tape archive, checksum and manifest verification, and file delivery to cloud storage. That means making sure what arrives, what gets archived and what gets delivered is exactly what it should be, and working out the root cause when it isn't.

## How I work with AI

I build tools with AI coding assistants, and I say so openly. My part is:

- **specifying** what to build, from real failures I've handled;
- **testing** it, and reviewing its output the way an operator would;
- **understanding** it well enough to explain every part.

Each project documents its design decisions and what I did versus what the AI did.

## Projects

| Project | What it does | Status |
|---|---|---|
| [manifest-doctor](https://github.com/Georgie995/manifest-doctor) | Checks a delivery against its checksum manifest and explains *why* files don't match: an extra wrapper folder, Mac vs Windows file names, a file listed twice with different checksums. JSON/CSV/Markdown reports, 148 tests. | Published |
| delivery-ops-hub | An n8n workflow that receives verification reports by webhook, alerts on failures and keeps an audit log | Next |
| ai-triage | Uses an LLM to draft plain-English summaries of verification reports, with automated checks that catch invented or missing findings | Planned |

## What I'm looking for

Technical roles that value operational judgement and AI-assisted work: technical operations, support or implementation engineering, solutions engineering, and AI workflow or operations roles. London or remote UK.

## Toolbox

**Daily work:** checksums and manifests (MD5, SHA-256), LTO/LTFS, rclone to S3, Terminal/CLI, Bash and shell (.sh) scripts, media asset management and tracking systems

**Building with:** Python (AI-assisted), Git, pytest, JSON, SQL basics, SQLite

**Learning now:** n8n, REST APIs and webhooks, LLM APIs
