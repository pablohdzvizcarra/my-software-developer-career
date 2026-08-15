---
name: history-updater-agent
description: Analyzes a 50-day archive file and generates/appends a concise summary entry to the History table in README.md. Use when archiving a 50-day period or updating the repository's historical log table.
---

# History Table Updater Skill

This skill guides the assistant in reading a 50-day journal archive file, extracting high-level topics and milestones, and updating the History table in `README.md`.

## Role & Purpose

Act as a technical writer and maintainer that synthesizes an archive file's content into a concise, well-formatted row in the `## History` table located in `README.md`.

## Workflow

### 1. Identify Target Archive File
- Locate or request the target 50-day archive file (e.g., `day2001-2500/day2451-2500.md` or `dayXXXX-XXXX/dayXXXX-XXXX.md`).
- Read the archive file content thoroughly.

### 2. Analyze Content & Extract Key Information
From the daily entries across the 50-day block, extract:
- **Days Range**: The start and end day range (e.g., `2451-2500`).
- **Main Topics / Technologies**: Dominant languages, architectural concepts, protocols, frameworks, and tools used during this period (comma-separated, concise).
- **Highlights**: Standout accomplishments, milestones, major applications or clones built, books finished, or career changes (concise summary).
- **Link**: Markdown link relative to `README.md` pointing to the archive file (e.g., `[View](./day2001-2500/day2451-2500.md)`).

### 3. Read and Locate the History Table in `README.md`
- Read `README.md` to locate the `## History` table.
- Verify existing rows to prevent duplicate entries for the same day range.

### 4. Format & Append Table Row
- Format the markdown table row following the established table structure:
  ```markdown
  | <Days> | <Main Topics / Technologies> | <Highlights> | [View](./<directory>/<filename>.md) |
  ```
- Append the row at the bottom of the History table (maintaining row order and placement above any subsequent sections or dividers like `****`).

### 5. Verify & Confirm
- Verify that the relative path in the link is valid.
- Confirm table alignment and Markdown formatting.
- Summarize the newly added row and link for the user.
