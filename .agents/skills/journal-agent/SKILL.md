---
name: journal-agent
description: Automates creating, formatting, inserting, and archiving daily journal entries in README.md based on the repository's standard day structure. Use when the user wants to log a new day entry or create a journal entry.
---

# Journal Entry Skill

This skill guides the assistant in creating, formatting, inserting, and archiving daily journal entries in `README.md`.

## Role & Purpose
Act as a helpful assistant that interacts with the user to gather details about their day, formats the entry according to the project standard, and inserts it into `README.md`.

## Workflow

### 1. Identify Next Day Number
- Read `README.md` and find the top/latest entry header under `## Programming Changes My` (e.g., `### Day 2486: Agent Orchestrator`).
- Calculate the default next day number (`Last Day + 1`).
- Confirm the day number with the user or use the calculated next day number.

### 2. Gather Entry Content
Ask the user (or extract from user input):
- **Day Number**: (Confirm next day number)
- **Title**: Concise title representing the primary topic of the day.
- **Main Topic & Details**: What was learned, built, or reflected upon.

### 3. Format Entry Standard
Format the entry strictly using the standard Markdown structure:

```markdown
### Day XXX: <Title>

<Details paragraph>
```

### 4. Insert into `README.md`
- Open `README.md`.
- Locate the `## Programming Changes My` section header.
- Insert the new `### Day XXX: <Title>` block immediately beneath `## Programming Changes My` (above the previous day's entry).

### 5. Milestone & Archiving Recommendation
- Check if a 50-day milestone has been reached (e.g. Day 2500, or when older entries exceed the current 50-day range).
- If a milestone is reached, notify the user and suggest archiving older entries to their corresponding `dayXXX-XXX/` directory file.
