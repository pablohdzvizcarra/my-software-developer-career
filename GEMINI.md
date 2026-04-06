# Project: My Software Developer Career

This repository is a comprehensive personal chronicle of a journey in software engineering, spanning over 2300 days of continuous learning and professional growth. It serves as a daily log, a course tracker, and a knowledge base for technical insights.

## Project Overview

- **Purpose:** To document daily learning, reflect on technical decisions, and track professional evolution.
- **Nature:** Non-code project (primarily Markdown-based documentation).
- **Key Topics:** Java, C, Operating Systems, Networking, Distributed Systems, Data Structures & Algorithms, and AI.

## Directory Structure

- `README.md`: The main entry point containing the most recent journal entries (under "Programming Changes My Life") and a high-level history table.
- `dayXXX-500/`, `day501-1000/`, etc.: Archive directories containing 50-day blocks of journal entries (e.g., `day0-50.md`, `day51-100.md`).
- `courses-completed.md`: A tracking table for finished educational courses.
- `AGENTS.md`: Definitions for custom subagents designed to manage this repository.
- `resources/`: Technical documents and reference materials (e.g., PDFs).

## Development & Maintenance Conventions

### Journaling

- **Frequency:** Daily entries.
- **Formatting:** Each entry starts with `### Day XXX: Title`.
- **Archiving:** When a 50-day milestone is reached, entries are moved from `README.md` to the corresponding archive file in the `dayXXXX-XXXX/` folders.

### Subagents (as defined in `AGENTS.md`)

- `journal-agent`: Automates the creation and formatting of new daily entries.
- `stats-agent`: Provides analytics on topics, technologies, and progress.
- `maintenance-agent`: Ensures structural consistency and updates tracking tables.

### Quality Control

- **Spellcheck:** A GitHub Action is configured (`.github/workflows/blank.yml`) using `spellcheck_ignore.txt`.
- **Links:** Maintainers should ensure internal links in the `README.md` history table remain valid after archiving.

## Usage for Gemini

When interacting with this repository, Gemini should:

1. **Reference History:** Use the archived `dayXXX-XXX.md` files to provide context on the user's past learning and technical background.
2. **Maintain Structure:** Adhere to the `### Day XXX: Title` format when suggesting new entries.
3. **Update Stats:** Consider the data in `courses-completed.md` when discussing the user's expertise levels.
