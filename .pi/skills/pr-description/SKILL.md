---
name: pr-description
description: Write pull request description. Use this tool whtn create a PR, writing a PR, or when user ask to summarize changes for pull request.
---

When writing a PR description:

1. Run `git diff main...HEAD` to see all changes on this branch
2. Write a description following this format:

## What 
One sentence explaining what this PR does.

## Why 
Brief context on why this change needed

## Changes
- Bullet points of specific changes made
- Group related changes together
- Mention any file deleted or renamed

## Testing
How to verify this works. Include specific commands if relevant.

Keep description concise. Focus on what a reviewer needs to know.
