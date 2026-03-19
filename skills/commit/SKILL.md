---
name: git-commit
description: Guide for committing changes following Conventional Commits specification. Use this when asked to commit code changes.
---

## Commit Message Format

Follow Conventional Commits with Jira integration:

```
<type>[(scope)]: [JIRA-123] <Description>

[optional body]
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`, `ci`

**Common Scopes:** `notifications`, `alarms`, `rules`, `devices`, `organizations`, `api`, `django`, `data`, `tests`

**Requirements:**
- Use imperative mood ("Add feature" not "Added feature")
- Capitalize first letter after Jira key
- No period at end of description
- Keep description under 50 characters when possible

## Workflow

### 1. Validate Branch
```bash
git rev-parse --abbrev-ref HEAD
```

**CRITICAL:** STOP if on `master`, or `main`. Never commit directly to protected branches.

- Extract Jira key from branch name (e.g., `feature/ABC-456` → `ABC-456`)
- Expected patterns: `feature/JIRA-XXX`, `bugfix/JIRA-XXX`, `hotfix/JIRA-XXX`

### 2. Check Status
```bash
git status --porcelain
```

**Decision tree:**
- Staged + unstaged changes → Ask which to commit
- No staged changes → Stage all tracked files
- Only staged → Proceed

### 3. Run Quality Checks

**Python files:**
```bash
ruff check
```
STOP if issues found. Do not auto-fix. Let user decide.

**C# files:**
Optionally suggest `dotnet format` (don't block)

### 4. Analyze Changes
```bash
git diff --cached --stat
git diff --cached
```

**Determine:**
- Commit type (infer from changed files)
- Scope (infer from directory structure)
- Description (summarize changes)
- Whether to split into multiple commits

**Automatic inference rules:**
- New files → `feat`
- Test files → `test`
- Doc files → `docs`
- Directory name → scope (e.g., `notifications/` → `notifications`)

### 5. Handle Multiple Changes

If unrelated changes detected, ask user to split commits:
```bash
git add <specific files>
git commit -m "message"
```

Process each group separately through this workflow.

### 6. Generate Message

**Automate whenever possible:**
1. Extract Jira key from branch
2. Infer type from files
3. Infer scope from paths
4. Generate description from diff

**Ask user ONLY if:**
- Type unclear
- Jira key missing (for feat/fix/refactor)
- Multiple scopes possible
- Description ambiguous

### 7. Confirm & Commit

Show generated message. Get confirmation. Execute:
```bash
git commit -m "type(scope): [JIRA-XXX] Description"
```

For multi-line:
```bash
git commit -m "type(scope): [JIRA-XXX] Description" -m "Body text here"
```

### 8. Push

```bash
git push
# or if first push:
git push -u origin <branch>
```

Confirm success and inform of next steps.

## Error Messages

**Protected branch:**
```
❌ Cannot commit to 'develop'. Create feature branch:
   git checkout -b feature/JIRA-XXX
```

**Ruff failures:**
```
⚠️  Code quality issues found:
   [list issues]
   
Fix before committing: ruff check --fix
```

**Unstaged changes:**
```
⚠️  Unstaged changes will not be committed.
Commit only staged changes? (y/n)
```

## Examples

**Single change:**
```
✓ Branch: feature/ABC-456
✓ Ruff: No issues
✓ Changes: 3 files in notifications/

Commit: feat(notifications): [ABC-456] Add SMS retry logic

Confirm? (y/n)
```

**Multiple changes:**
```
Changes detected in 2 areas:
1. notifications/ (5 files) - SMS feature
2. alarms/ (3 files) - View updates

Split into separate commits? (y/n)
```

**With issues:**
```
⚠️  Ruff found 2 issues:
- notifications/sms.py:45 F401 unused import
- models.py:102 E501 line too long

Fix with: ruff check --fix
```

