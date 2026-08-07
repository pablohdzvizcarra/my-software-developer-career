---
name: completed-books-agent
description: Extracts finished/completed books from daily journal entries (such as README.md or dayXXX-XXX/ archive files) and updates or registers them in the completed-books.md table. Use when processing journal entries to track completed books.
---

# Completed Books Tracker Skill

This skill guides the assistant in analyzing daily journal entry files, identifying completed books, and recording them in `completed-books.md`.

## Role & Purpose
Act as a book tracking agent that scans daily journal entries (in `README.md` or 50-day archive files like `day1001-1500/day1001-1050.md`), identifies books that have been completed by the user, and maintains a structured Markdown table in `completed-books.md`.

## Workflow

### 1. Identify Target Journal File(s)
- Determine or ask for the target journal file or range (e.g., `README.md`, `day1001-1500/day1001-1050.md`).

### 2. Scan & Extract Finished Books
- Scan the file for entries mentioning reading activity.
- Look for completion indicators, such as:
  - "finish reading", "finished reading", "finish that read"
  - "completed the book", "read the book", "finished the book"
- **Distinguish** completed books from books currently in progress or planned (e.g., "start to read", "continue with my book", "when I finish").
- For each completed book, extract:
  - **Day / Date**: The Day number (e.g., `Day 1047 - 1048` or `Day 1050`).
  - **Book Title**: The title of the book.
  - **Topic / Key Takeaways**: A short summary of what the entry notes about the book or key learning.
  - **Source Entry**: Relative path to the journal file containing the entry.

### 3. Maintain `completed-books.md`
- Read `completed-books.md`. If it does not exist, initialize it with:

```markdown
# Completed Books

| Day / Date | Book Title | Topic / Key Takeaways | Source Entry |
| --- | --- | --- | --- |
```

- Check existing table rows to avoid duplicate entries for the same book and day.
- Append new entries using the standard format:

```markdown
| Day / Date | Book Title | Topic / Key Takeaways | Source Entry |
```

### 4. Verify & Confirm
- Verify that `completed-books.md` remains well-formatted and sorted (chronologically or by Day number).
- Summarize the newly added books for the user with markdown links to the source entry and `completed-books.md`.
