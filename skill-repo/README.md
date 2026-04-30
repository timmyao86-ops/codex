# Skill Repository

This repository stores reusable Codex skills.

## Included skills

- `frontend-slides`: migrated from `frontend-slides/skills/frontend-slides`.

## Structure

```text
skill-repo/
  skills/
    <skill-name>/
      SKILL.md
      agents/
      scripts/        (optional)
      references/     (optional)
      assets/         (optional)
```

## Local access

Open and browse locally from this workspace path:

- `/workspace/codex/skill-repo`

## Publish to GitHub (to get a public URL)

```bash
cd /workspace/codex/skill-repo
git init
git add .
git commit -m "init skill repository"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```

After push, your repository URL will be:

- `https://github.com/<your-org-or-user>/<your-repo>`
