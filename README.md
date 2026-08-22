Casey
A working title — no permanent name has been chosen yet.
Casey is a case management tool for solo and small-firm attorneys, built entirely as a single-file app through conversation with Claude (Anthropic's AI) — no traditional coding involved. It runs as a Claude artifact: no install, no separate account, no backend to stand up.
This started as a personal project and is being shared for other attorneys to try, stress-test, and give feedback on. It is not a finished commercial product — see Important disclaimers before putting any real client information into it.
---
What it does
Case tracking
Overview — case summary, scope, priority, active/closed status, next deadline, and free-form notes (click directly into any notes field to edit)
Case Status — a customizable, phase-by-phase to-do tracker for litigation matters, with:
Sub-tasks per to-do item
Deadlines, with "auto-complete when this date arrives" and "mark as important" options
Conditional/locked steps that unlock once a prior step is checked off
A fully customizable phase list — add, rename, reorder, or remove phases; renaming cascades automatically to every case, its history, and any templates that use it
Claims — track claims per case, including which party or parties each one is brought against
Docket — a manual docket log (entry number, date, name, filer)
Contacts — contacts grouped into reorderable sections by role
Activity Log — calls, meetings, hearings, and more, with date, start time, duration, attendees, and notes
Timeline — a per-case month calendar pulling together that case's to-do deadlines, activity entries, and docket entries; click any entry to jump straight to the relevant tab
Dashboard & Calendar
Dashboard shows your highest-priority cases (counts configurable) and a "This week" view of what's due day by day — optionally including weekends and/or activity log entries
A full Calendar view combining deadlines and activity entries across every open case
Every entry in either view is clickable and jumps straight to the right case and tab
Templates
Case templates — pre-fill a phase-by-phase to-do list (with sub-tasks) for new litigation matters
Claim templates — pre-fill a claim's title and notes
Import / Export
Organized into one window with three tabs:
Data — printable case snapshots, full backup/restore, and case data export/import (choose a subset)
CSV — spreadsheet templates and import for cases, activity log entries, and docket entries
Templates — export/import for case templates and claim templates
Security & access
Optional password lock screen with auto-lock after a configurable period of inactivity
A blocking disclaimer/release screen shown on every load (see below)
Please read the security section below — the password lock is a deterrent, not encryption
Customization
Settings is organized into four tabs: Display (font, dark mode, date format, color theme), Dashboard (thresholds, per-priority limits, "This week" options), Security (password/auto-lock), and User (your name and firm name)
Four color themes, each with light and dark variants: Parchment (default), Slate, Ink & Ivory, and Sage
Flip the sidebar to the right side of the screen if you prefer
Getting oriented
A Help window with a full reference, organized by area of the app
A short, skippable guided tour on first launch, plus optional contextual "first time here?" tours in a handful of key windows — all of which can be turned off at once
A sample data loader (4 example cases across different matter types, priorities, and phases) so you can explore the app without entering real data first
---
Important disclaimers — please read
Casey shows a disclaimer and requires an explicit acknowledgment every time it loads. The short version:
This is not a vetted commercial product. No company stands behind it, no support contract, no warranty of any kind.
It provides no security or confidentiality protection beyond whatever the platform it runs on already provides. The optional password lock is a basic deterrent, not encryption — it will not stop someone with browser developer tools.
Using this with real client information may implicate attorney-client privilege, work product protection, or your jurisdiction's rules of professional conduct, depending on the AI platform's data handling policies for the account tier in use. Evaluate this independently before entering anything privileged or confidential.
It doesn't replace your actual docketing or conflicts system. Deadlines are entered manually — there is no court-rules engine and no conflict-of-interest checking.
There's no document storage. You can't attach PDFs, filings, or exhibits — this is structured data and notes only.
The full disclaimer text is in the app itself and in `case-docket.html`'s disclaimer screen. It was drafted collaboratively and has not been independently reviewed by outside counsel — treat it as a starting point, not a finished legal instrument, if you plan to rely on it.
---
How to use it
Casey runs as a Claude artifact — a self-contained app that lives inside a Claude conversation.
Get the `.html` file from this repository.
Paste its contents into a new conversation with Claude (claude.ai or the Claude app) and ask Claude to render it as an artifact — or open the file directly in a browser for a quick look at the interface.
For your data to actually persist between sessions, it needs to be running as a real Claude artifact on an account with persistent storage enabled. As of this writing, persistent artifact storage is available on Pro, Max, Team, and Enterprise plans, not Free — check Anthropic's current documentation, since this changes over time.
If you're evaluating this for real practice use rather than just trying it out, that's worth a conversation with your own IT/compliance setup — an Enterprise plan with a signed Data Processing Addendum would be the appropriate starting point, not a default consumer plan.
---
Tech details
Single HTML file — HTML, CSS, and vanilla JavaScript, no framework, no build step, no external dependencies aside from Google Fonts
Data is stored via Claude's artifact storage API, scoped privately to your account
No network calls other than font loading — nothing phones home
---
Feedback
This is being shared specifically to get feedback from attorneys who'd actually use something like this day to day. Issues, pull requests, and comments are all welcome — especially anything that feels unsafe, unclear, or missing from a real-practice standpoint.
---
