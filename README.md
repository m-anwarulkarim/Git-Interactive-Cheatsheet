````markdown
# 🌟 Git & GitHub Complete Cheatsheet (Color-coded & Updated)

> এই Cheatsheet-এ Git এবং GitHub-এর প্রয়োজনীয় সব কমান্ড একসাথে সাজানো হয়েছে, logical এবং color-coded view সহ।

---

# 🧭 1) Git Installation & Configuration

```bash
# Check Git Version
git --version

# Configure User Info
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

# View Config
git config --get user.name
git config --get user.email
```
````

---

# 📁 2) Repository Management

```bash
# Initialize Repository
git init

# Clone Repository
git clone <repo-url>

# Check Repo Status
git status
```

---

# 📂 3) File & Staging Operations

```bash
# Add Files
git add .
git add <file>

# Commit Changes
git commit -m "message"

# Remove Files
git rm <file>
git rm --cached <file>
```

---

# 📜 4) View History

```bash
# Full History
git log

# One-line History
git log --oneline

# Graph View
git log --graph --oneline --all
```

---

# 🌿 5) Branch Management

```bash
# List Branches
git branch

# Create Branch
git branch <branchName>

# Switch Branch
git switch <branchName>

# Rename Branch
git branch -m <newName>

# Delete Branch
git branch -d <branchName>    # safe delete
git branch -D <branchName>    # force delete

# Merge Branch
git merge <branchName>
```

---

# 💾 6) Stash (Temporary Save)

```bash
# Save Stash
git stash save "Work in progress"

# Show Stash Details
git stash show -p

# Restore Stash
git stash pop
```

---

# ♻️ 7) Undo / Reset / Restore

```bash
# View HEAD History
git reflog

# Reset to a Commit
git reset --hard <hash>  # WARNING: deletes unstaged changes
```

---

# 🌍 8) GitHub Commands

```bash
# Add Remote
git remote add origin <repo-url>

# Check Remote
git remote -v

# Push Code
git push -u origin main

# Pull Latest Code
git pull origin main

# Fetch (Download Updates Only)
git fetch origin
```

---

# 🔥 9) Git History Rewrite & Force Push

```bash
rm -rf .git
git init
git add .
git commit -m "Initial public release"
git branch -M main
git remote add origin <repo-url>
git push -u --force origin main
```

> **Quick Summary:**
>
> - Deletes old history
> - Creates new initial commit
> - Pushes current code only
>   ⚠️ Warning: Previous commit history will be gone!

---

# 🔁 10) Common Fix Commands

```bash
# Recover Overwritten File
git checkout -- <file>

# Undo Last Commit (keep code)
git reset --soft HEAD~1

# Remove All Local Changes
git reset --hard
```

---

# 📦 11) Git Ignore

```bash
# Create .gitignore
touch .gitignore

# Common Patterns
node_modules/
dist/
.env
```

---

# 📚 12) Summary Table

| Category         | Commands                                |
| ---------------- | --------------------------------------- |
| Install & Config | `git --version`, `git config`           |
| Repo             | `git init`, `git clone`                 |
| Stage & Commit   | `git add`, `git commit`                 |
| History          | `git log`, `git log --oneline`          |
| Branch           | `git branch`, `git switch`, `git merge` |
| Stash            | `git stash`                             |
| Undo             | `git reset`, `git reflog`               |
| GitHub           | `git push`, `git pull`, `git remote`    |

---

**Author:** ANWARUL KARIM
**Updated:** 2025

---

# 🚀 13) GitHub SSH Setup

```bash
# Generate SSH Key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# Start SSH Agent
eval $(ssh-agent -s)

# Add Key to Agent
ssh-add ~/.ssh/id_rsa

# Copy Public Key to Add in GitHub
cat ~/.ssh/id_rsa.pub
```

---

# 🍴 14) GitHub Fork Workflow

```bash
# Fork → Clone
git clone <forked-repo-url>

# Add Upstream Remote
git remote add upstream <original-repo-url>

# Sync Fork
git fetch upstream
git merge upstream/main
```

---

# 🔄 15) Pull Request Workflow

```bash
# Create Feature Branch
git switch -c feature-branch

# Stage & Commit
git add .
git commit -m "Added new feature"

# Push Branch
git push origin feature-branch

# Create Pull Request via GitHub Web UI
```

---

# 🔀 16) Rebase & Cherry-pick

```bash
# Rebase (Clean History)
git rebase main

# Abort Rebase
git rebase --abort

# Cherry-pick Commit
git cherry-pick <commit-hash>
```

---

# ⚔️ 17) Solve Merge Conflicts

```bash
# Conflict markers:

=======


# Fix, then:
git add <file>
git commit
```

---

# 🧭 18) Git Flow (Branch Strategy)

```bash
# Main Branches
main    # production
develop # development

# Supporting Branches
feature/*
release/*
hotfix/*

# Example Workflow
git switch -c feature/login
# work...
git commit -m "login added"
git switch develop
git merge feature/login
```

```


```
