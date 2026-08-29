# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a **course deliverables repository** (Track 1, Day 27 — AI Team Lab), not a software project. Team Mixue's project is **VLearn AI Tutor** (an AI tutoring product with LTI 1.3 LMS integration). All content is in **Vietnamese** — keep any edits in Vietnamese unless asked otherwise.

Contents:
- `README.md` — the main submission: team info, 90-day goals, and 4 Artefacts (Stakeholder Map & Strategy, Conclusion-First Pitch & RACI, AI Team Architecture & Resourcing, Team Health & 30-Day Growth Plan), each followed by a Gate verification checklist (Gate 0–5).
- `Day27_AI-Team-Lab_TeamMixue.html` / `.pdf` and `Day27_AI-Team-Lab_Mixue.pdf` — the formatted 4-page submission document (one page per Artefact).
- `Reflection/` — individual reflection reports named `<FullName>_<StudentID>.md`.
- `export_pdf.py` — regenerates the HTML deliverable and exports it to PDF.

## Regenerating the PDF Deliverable

`export_pdf.py` is self-contained: it embeds the full HTML as the `HTML_TEMPLATE` string constant, overwrites `Day27_AI-Team-Lab_TeamMixue.html` with it, prints to PDF, and copies the result to `Day27_AI-Team-Lab_Mixue.pdf`.

```
python export_pdf.py    # requires pypdf (pip install pypdf) and Edge or Chrome
```

Important caveats:
- **The HTML template inside `export_pdf.py` is the source of truth**, not the `.html` file — the script rewrites the `.html` on every run. Edit `HTML_TEMPLATE` in the script, then rerun to regenerate both HTML and PDFs.
- The browser lookup uses **Windows paths only** (`C:\Program Files\...\msedge.exe`/`chrome.exe`). On macOS, add the Chrome/Edge path (e.g. `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome`) to `edge_paths` before running.
- The PDF must remain **exactly 4 pages** (one page per Artefact); `.page` blocks in the template CSS are fixed-height A4 sections with `overflow: hidden` — content that overflows is silently clipped, so verify page count after edits (the script prints it).

## Consistency Rules for Content Edits

The four Artefacts are cross-checked against each other (Gate 5's "Consistency Check" section in README.md). When changing any number or owner, keep these links intact across ALL files (README, HTML template, PDFs, reflections):
- Stakeholders in Artefact 1 ↔ pitch target and RACI roles in Artefact 2.
- Capability gaps (Artefact 3) ↔ lowest team-health scores (Artefact 4).
- Growth-plan owners (Sơn, Tấn, Hưng) ↔ RACI Accountable/Responsible assignments.
- Key recurring figures: accuracy ≥ 92%, hallucination < 5%, cost ≤ 1.200 VNĐ/session, gross margin ≥ 58%, TTF-End-User ≤ 7 days, Partner Activation ≥ 70%.

Each team member's student ID format is `<Name>_<2Axxxxxx>.md` in `Reflection/`; the README's Reflection section links to those files.

## Known Issues (as of 2026-08-29)

- **README.md broken reflection links**: the entries for Lê Đăng Tấn and Nguyễn Quang Sơn in the Reflection section both point to `Reflection/PhamTienHung_2A202601800.md` instead of their own files — `Reflection/` currently only contains reports for Phạm Tiến Hưng and Nguyễn Minh Quang. Don't treat those README links as ground truth; if those members' reports are added, fix the links.
- The two PDFs are binary outputs of `export_pdf.py` — never edit them by hand; change `HTML_TEMPLATE` and rerun the script.
