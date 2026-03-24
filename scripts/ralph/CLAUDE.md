# Ralph Agent — Portfolio

You are an autonomous coding agent working on a single-file HTML portfolio page.

## Project

- **Main file:** `C:/Users/aless/Desktop/Portfolio/index.html` (all CSS and JS are inline)
- **Working directory:** `C:/Users/aless/Desktop/Portfolio/`
- **Git repo:** initialized, commit after each story

## Your Task

1. Read `prd.json` in the same directory as this file
2. Read `progress.txt` (Codebase Patterns section first)
3. Pick the **highest priority** user story where `passes: false`
4. Implement that single story by **editing index.html** (use Edit tool — never rewrite the whole file)
5. Quality check: review the changed CSS/JS/HTML block and confirm it is syntactically correct and logically sound — no typecheck or test commands exist for this project
6. Commit ALL changes: `git -C "C:/Users/aless/Desktop/Portfolio" add -A && git -C "C:/Users/aless/Desktop/Portfolio" commit -m "feat: [Story ID] - [Story Title]"`
7. Update `prd.json` to set `passes: true` for the completed story
8. Append progress to `progress.txt`

## Editing Rules

- Use Edit tool for targeted changes — never Write the whole file
- CSS changes: target the specific rule in the `<style>` block
- HTML changes: target the specific element
- JS changes: target the specific function

## Progress Report Format

APPEND to progress.txt:
```
## [Story ID]
- What changed
- Files changed
- Learnings:
  - Any patterns discovered or gotchas
---
```

## Stop Condition

If ALL stories have `passes: true`, output:
<promise>COMPLETE</promise>

Otherwise end your response normally.
