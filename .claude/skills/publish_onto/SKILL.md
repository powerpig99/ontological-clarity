---
name: publish_onto
description: Show diff, commit as "Refinement:", and push. Extracts zip first if ~/Downloads/ontological-clarity.zip exists.
allowed-tools: Bash(test:*), Bash(unzip:*), Bash(git diff:*), Bash(git status:*), Bash(git add:*), Bash(git commit:*), Bash(git push:*)
---

# Publish Ontological Clarity Updates

## Instructions

1. **Check if zip exists**:
   ```bash
   test -f ~/Downloads/ontological-clarity.zip && echo "ZIP_EXISTS" || echo "NO_ZIP"
   ```
   - If ZIP_EXISTS: extract it (overwrite existing files):
     ```bash
     unzip -o ~/Downloads/ontological-clarity.zip -d /Users/jingliang/Documents/trae_projects/ontological-clarity
     ```
   - If NO_ZIP: skip extraction, proceed to step 2.

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
