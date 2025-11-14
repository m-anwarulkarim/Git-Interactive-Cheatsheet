# 🌟 Git & GitHub Complete Cheatsheet (Grouped & Updated)

এই ডকুমেন্টে Git এবং GitHub-এর **সব প্রয়োজনীয় ও প্রচলিত কমান্ডগুলোকে গ্রুপ করে সাজানো হয়েছে**, যাতে যেকোনো সময় খুব সহজে দেখা জায় ।

---

# 🧭 1) Git Installation & Configuration

### ✔️ Check Git Installation
```
git --version
```

### ✔️ Configure User Info (Required)
```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

### ✔️ View Config
```
git config --get user.name
git config --get user.email
```

---

# 📁 2) Repository Management

### ✔️ Initialize Repo
```
git init
```

### ✔️ Clone Repository
```
git clone <repo-url>
```

### ✔️ Check Repo Status
```
git status
```

---

# 📂 3) File & Staging Operations

### ✔️ Add Files
```
git add .
git add <file>
```

### ✔️ Commit Changes
```
git commit -m "message"
```

### ✔️ Remove Files
```
git rm <file>
git rm --cached <file>
```

---

# 📜 4) View History

### ✔️ Full History
```
git log
```

### ✔️ One-line History
```
git log --oneline
```

### ✔️ Graph View
```
git log --graph --oneline --all
```

---

# 🌿 5) Branch Management (Most Used)

### ✔️ List Branches
```
git branch
```

### ✔️ Create Branch
```
git branch <branchName>
```

### ✔️ Switch Branch
```
git switch <branchName>
```

### ✔️ Rename Branch
```
git branch -m <newName>
```

### ✔️ Delete Branch
```
git branch -d <branchName>    # safe delete
git branch -D <branchName>    # force delete
```

### ✔️ Merge Branch
```
git merge <branchName>
```

---

# 💾 6) Stash (Temporary Save)

### ✔️ Save Stash
```
git stash save "Work in progress"
```

### ✔️ Show Stash Details
```
git stash show -p
```

### ✔️ Restore Stash
```
git stash pop
```

---

# ♻️ 7) Undo / Reset / Restore

### ✔️ Reflog (HEAD History)
```
git reflog
```

### ✔️ Reset to a Commit
```
git reset --hard <hash>
```

⚠️ সতর্কতা: `--hard` unstaged changes মুছে দেয়।

---

# 🌍 8) GitHub Commands (Most Important)

### ✔️ Add Remote Origin
```
git remote add origin <repo-url>
```

### ✔️ Check Remote
```
git remote -v
```

### ✔️ Push Code
```
git push -u origin main
```

### ✔️ Pull Latest Code
```
git pull origin main
```

### ✔️ Fetch (Only Download Updates)
```
git fetch origin
```

---

# 🔁 9) Common Fix Commands

### ✔️ Fix: Overwritten File Recovery
```
git checkout -- <file>
```

### ✔️ Fix: Undo Last Commit (Keep Code)
```
git reset --soft HEAD~1
```

### ✔️ Fix: Remove All Local Changes
```
git reset --hard
```

---

# 📦 10) Git Ignore

### ✔️ Create `.gitignore`
```
touch .gitignore
```

### ✔️ Common Patterns
```
node_modules/
dist/
.env
```

---

# 📚 11) Summary Table

| Category | Commands |
|----------|-----------|
| Install & Config | `git --version`, `git config` |
| Repo | `git init`, `git clone` |
| Stage & Commit | `git add`, `git commit` |
| History | `git log`, `git log --oneline` |
| Branch | `git branch`, `git switch`, `git merge` |
| Stash | `git stash` |
| Undo | `git reset`, `git reflog` |
| GitHub | `git push`, `git pull`, `git remote` |

---

**Author:** ANWARUL KARIM
**Updated:** 2025


---

# 🚀 12) GitHub SSH Setup

### ✔️ Generate SSH Key
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### ✔️ Start SSH Agent
```
eval $(ssh-agent -s)
```

### ✔️ Add Key to Agent
```
ssh-add ~/.ssh/id_rsa
```

### ✔️ Copy Public Key (Add to GitHub)
```
cat ~/.ssh/id_rsa.pub
```

---

# 🍴 13) GitHub Fork Workflow

### ✔️ Fork → Clone
```
git clone <forked-repo-url>
```

### ✔️ Add Upstream Remote
```
git remote add upstream <original-repo-url>
```

### ✔️ Sync Fork
```
git fetch upstream
git merge upstream/main
```

---

# 🔄 14) Pull Request (PR) Workflow

### ✔️ Create a New Branch
```
git switch -c feature-branch
```

### ✔️ Stage & Commit
```
git add .
git commit -m "Added new feature"
```

### ✔️ Push Branch
```
git push origin feature-branch
```

### ✔️ Create Pull Request
GitHub → Compare & Pull Request → Submit.

---

# 🔀 15) Rebase & Cherry-pick

### ✔️ Rebase (Clean History)
```
git rebase main
```

### ✔️ Abort Rebase
```
git rebase --abort
```

### ✔️ Cherry-pick (Pick Specific Commit)
```
git cherry-pick <commit-hash>
```

---

# ⚔️ 16) Solve Merge Conflicts

### ✔️ When conflict occurs
Git will show conflict markers like:
```
<<<<<<< HEAD
=======
>>>>>>> branch
```

### ✔️ Fix File → Then Run
```
git add <file>
git commit
```

---

# 🧭 17) Git Flow (Branch Strategy)

### ✔️ Main Branches
- `main` → production
- `develop` → development

### ✔️ Supporting Branches
- `feature/*`
- `release/*`
- `hotfix/*`

### ✔️ Example
```
git switch -c feature/login
# work...
git commit -m "login added"
git switch develop
git merge feature/login
```

