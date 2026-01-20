---
name: update_onto
description: Incorporate refinements from an update.md file into the ontological clarity framework (SKILL.md).
allowed-tools: Read, Edit, Bash(git diff:*), Bash(git status:*), Bash(git add:*), Bash(git commit:*), Bash(git push:*)
---

# Update Ontological Clarity Framework

Incorporates refinements from an update file into the main SKILL.md framework.

## Instructions

1. **Ask for the update file path** if not provided (default: `~/Downloads/update.md`).

2. **Read the update file** to understand what changes are being made.

3. **Read the current SKILL.md** in this repo.

4. **Incorporate the changes** intelligently:
   - If adding new patterns, add to the appropriate section
   - If refining existing content, update in place
   - If adding new sections, place them logically
   - Preserve the framework's structure and voice

5. **Show the diff** for review:
   ```bash
   git diff SKILL.md
   ```

6. **Ask user to confirm** the changes look correct.

7. **Commit and push**:
   ```bash
   git add SKILL.md
   git commit -m "Refinement: [brief description of what was updated]"
   git push origin main
   ```

## Notes

- The update.md should describe what to add/change, not be a complete replacement
- Maintain the existing structure and formatting conventions
- The framework's epistemological stance: clarity is movement, not arrival
