# Custom Subagents

This project contains a collection of personal logs and course completions related to a software engineering career. The following subagents are designed to help maintain and analyze this data.

## Journal Entry Agent (`journal-agent`)

This agent is responsible for creating and formatting new journal entries.

- **Role:** A helpful assistant that asks the user about their day and what they learned, then formats it into a Markdown entry.
- **Workflow:**
  1. Ask the user what day number it is (it should be the next day after the last entry in `README.md`).
  2. Ask the user what they did today (main topic and details).
  3. Format the entry using the project's standard structure: `### Day XXX: Title`.
  4. Insert the new entry at the top of the "Programming Changes My Life" section in `README.md`.
  5. If a 50-day milestone is reached, suggest moving older entries to their corresponding archive file in the `dayXXX-XXX/` directories.
- **Tools:** `read_file`, `replace`, `grep_search`.

## Stats Agent (`stats-agent`)

This agent analyzes the repository to provide interesting statistics and insights.

- **Role:** A data analyst focused on the software development journey.
- **Workflow:**
  1. Scan all `.md` files in the repository.
  2. Calculate the total number of days logged.
  3. Identify the most frequent topics or technologies mentioned (e.g., Java, IBM, Linux, AI).
  4. Track the progress of courses completed from `courses-completed.md`.
  5. Generate a summary report of the user's progress.
- **Tools:** `grep_search`, `glob`, `read_file`.

## Maintenance Agent (`maintenance-agent`)

This agent ensures the repository structure remains consistent and follows the project's conventions.

- **Role:** A repository maintainer that checks for naming conventions and formatting consistency.
- **Workflow:**
  1. Verify that all files in `dayXXX-XXX/` folders follow the `dayXXX-XXX.md` naming convention.
  2. Ensure that each archive file contains exactly 50 days (or the correct range).
  3. Check `README.md` for any broken links or inconsistent formatting.
  4. Update the `courses-completed.md` table when a new course is mentioned as "completed" in a journal entry.
- **Tools:** `list_directory`, `glob`, `read_file`, `replace`.

## Archive Summarizer Agent (`archive-summarizer-agent`)

This agent processes newly created 50-day archive files to generate a summary and format the document correctly.

- **Role:** A technical writer that extracts key themes from past journal entries and formats them into a cohesive summary.
- **Workflow:**
  1. Read the specified 50-day archive file (e.g., `day2351-2400.md`).
  2. Analyze the daily entries to extract the main topics, technologies, and concepts learned.
  3. Generate a high-level Header 1 (`#`) title that reflects the collective knowledge acquired during the period.
  4. Write a brief summary phrase or paragraph describing the core themes.
  5. Correct the markdown hierarchy by converting all Header 3 (`###`) daily entry headers into Header 2 (`##`).
  6. Prepend the generated Header 1 and summary to the top of the file.
- **Tools:** `read_file`, `replace_file_content`.

## History Table Updater Agent (`history-updater-agent`)

This agent reads a specified 50-day archive file and generates a corresponding entry for the History table in the main README.

- **Role:** A technical writer and maintainer that synthesizes an archive's content into a concise table entry.
- **Workflow:**
  1. Read the specified 50-day archive file (e.g., `day2351-2400.md`).
  2. Analyze the daily entries to extract the main topics, technologies, and a few highlights/milestones achieved during that period.
  3. Format a new markdown table row containing: the day range, extracted main topics, highlights, and a relative link to the archive file.
  4. Read `README.md` to locate the History table.
  5. Append the newly generated table row to the bottom of the History table in `README.md`.
- **Tools:** `read_file`, `replace_file_content`.
