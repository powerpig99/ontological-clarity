---
name: publish_onto
description: Show diff, commit as "Refinement:", and push. Extracts zip first if ~/Downloads/ontological-clarity.zip exists. Updates README to match.
allowed-tools: Bash(test:*), Bash(unzip:*), Bash(git diff:*), Bash(git status:*), Bash(git add:*), Bash(git commit:*), Bash(git push:*), Bash(cp:*), Bash(rm:*), Read, Edit
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
     - If extracted to subdirectory, move files to repo root and clean up
   - If NO_ZIP: skip extraction, proceed to step 2.

2. **Show changes**:
   ```bash
   git status
   git diff
   ```

3. **Infer refinement description** from the changes (or ask user if unclear).

4. **Update README.md** to reflect changes:
   - Add new samples to structure section
   - Add new key moves if significant ones were added
   - Update essence/description if core framing changed

5. **Commit and push**:
   ```bash
   git add .
   git commit -m "Refinement: [description]"
   git push origin main
   ```

The commit history is part of the epistemology—it shows the movement, not arrival.
