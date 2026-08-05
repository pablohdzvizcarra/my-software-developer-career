# Custom Subagents

This project contains a collection of personal logs and course completions related to a software engineering career. The following subagents are designed to help maintain and analyze this data.

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
