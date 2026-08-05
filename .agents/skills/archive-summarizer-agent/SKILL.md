---
name: archive-summarizer-agent
description: Summarizes and formats a 50-day journal archive file. Converts Day headers (### to ##), generates a top-level summary title and overview paragraph, and prepends them to the archive document. Use when processing or formatting a new dayXXX-XXX.md archive file.
---

# Archive Summarizer Skill

This skill guides the assistant in processing, summarizing, and re-formatting 50-day journal archive files (e.g., `day2351-2400/day2351-2400.md` or similar range files).

## Role & Purpose
Act as a technical writer that analyzes a completed 50-day archive block, extracts key technical themes and milestones, converts header levels to maintain proper Markdown hierarchy, and prepends a top-level header and summary overview.

## Workflow

### 1. Identify Target Archive File
- Determine or ask for the target 50-day archive file path (e.g., `day2351-2400/day2351-2400.md`).
- Read the archive file content thoroughly.

### 2. Extract Key Themes & Milestones
- Analyze the daily entries to identify dominant technical topics (e.g., Systems Programming, Java Concurrency, AI Agents, Operating Systems).
- Note major projects completed or milestone concepts mastered.

### 3. Generate Top-Level Summary
- **Header 1 (`#`) Title**: Synthesize a descriptive title for the 50-day block (e.g., `# Days 2351-2400: Advanced Distributed Systems & Agent Design`).
- **Summary Paragraph**: Write a brief overview (1–3 sentences) summarizing the main concepts learned and accomplishments achieved during this timeframe.

### 4. Update Markdown Header Hierarchy
- Change all daily entry headers from Header 3 (`### Day XXX: ...`) to Header 2 (`## Day XXX: ...`) so they sit cleanly under the new Header 1.

### 5. Prepend Summary to File
- Prepend the Header 1 title and summary paragraph to the very top of the archive file.
