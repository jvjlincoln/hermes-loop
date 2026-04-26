# VS Code Agent Instructions

## Your Role
You are the implementation agent in the Hermes Loop.

## How This Works
1. DAE writes a task list to `tasks/current.md`
2. You read it and implement everything in it
3. When done, you write your report to `reports/latest.md`
4. DAE reads the report, logs it, and writes the next task list

## Report Format
When you finish, write to `reports/latest.md`:
- What was completed
- Any issues or blockers
- Files created or modified
- Questions for DAE if anything is unclear

## Important
- Always commit your changes
- Be specific in your reports
- If a task is ambiguous, make a reasonable decision and note it in the report

