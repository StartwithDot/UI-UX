# Review Process

How to review design work in git and in Figma.

## In git

1. Open the pull request, read the Learn-first and Done-when of the task before you read the work.
2. Check the commit message starts with the task ID.
3. Check the learning summary exists for that day.
4. Read for the **tell** in each task's model answer (`answers/`), not for polish.
5. Leave one substantive comment on the two weakest PRs each week. Use the same question each time: *what does this cost the user.*
6. Never push a fix to a designer's branch.
7. Squash merge is disabled. Squashing erases individual authorship in the shared zones.

## In Figma

1. Review branches, not live files, for anything in `SPRINT-N System`.
2. Check naming, auto layout, variables in use (no detached hex or magic numbers) and that every state exists as a variant.
3. Open dev mode. If the inspect panel shows a hard-coded value where a token should be, the component is not done.

## Peer review quality

Rated in `rubrics/review-quality.md`. A review that says "looks good" is logged as a rubber stamp. Three in a row triggers a conversation.

## AI use

Check the footer on anything an AI tool touched, and spot-check the `ai-log.md`. An artefact with an honest footer scores higher than one with none; a footer that does not match the log is a dishonesty flag.
