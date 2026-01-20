---
name: publish_onto
description: Extract ontological-clarity.zip from Downloads, show diff, commit as "Refinement:", and push.
allowed-tools: Bash(unzip:*), Bash(git diff:*), Bash(git status:*), Bash(git add:*), Bash(git commit:*), Bash(git push:*)
---

# Publish Ontological Clarity Updates

## Instructions

1. **Extract the zip** (overwrite existing files):
   ```bash
   unzip -o ~/Downloads/ontological-clarity.zip -d /Users/jingliang/Documents/trae_projects/ontological-clarity
   ```

2. **Show changes**:
   ```bash
   git status
   git diff
   ```

3. **Ask user** what this refinement addresses (brief description).

4. **Commit and push**:
   ```bash
   git add .
   git commit -m "Refinement: [user's description]"
   git push origin main
   ```

The commit history is part of the epistemology—it shows the movement, not arrival.
