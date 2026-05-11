# GIT WORKFLOW - QUICK REFERENCE

---

# 1. INITIAL GIT SETUP *(One-Time Configuration)*

| Command | Description |
|---|---|
| `git config --global user.email "you@example.com"` | Set your Git email globally |
| `git config --global user.name "Your Name"` | Set your Git username globally |

---

# 2. SETUP *(Fresh Local Project)*

| Command | Description |
|---|---|
| `git init` | Initialize a new local Git repository |

---

# 3. REMOTE ORIGIN & BRANCH SETUP

| Command | Description |
|---|---|
| `git remote add origin <URL>` | Link local repo to remote repository |
| `git remote -v` | Verify remote origin URL is set correctly |
| `git branch -a` | List all branches (local + remote) `*` = current branch |
| `git branch <branch-name>` | Create a new branch only *(without switching)* |
| `git switch -c <branch-name>` | Create and switch to a new branch |
| `git switch <branch-name>` | Switch to mentioned branch (recommended) |

---

# 4. WORKING WITH FILES

| Command | Description |
|---|---|
| `git status` | Show current changes and file states |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show staged changes ready for commit |

---

# 5. STAGING & COMMIT 🔁 *(Repeat for every change)*

| Command | Description |
|---|---|
| `git add .` | Stage all modified/new files |
| `git commit -m "your commit message"` | Commit staged changes with a message |
| `git log` | Verify commit history after each commit |

---

# 6. SYNC WITH REMOTE & PR FLOW

| Command | Description |
|---|---|
| `git pull origin <branch-name>` | Fetch + merge latest changes *(before push in teams)* |
| `git push -u origin <branch-name>` | Push branch and set upstream tracking |

> GitHub → New Pull Request → Assign Approver → Review → Approve → Merge into main

---

# 7. UNDO / FIX MISTAKES

| Command | Description |
|---|---|
| `git restore <file>` | Discard local *(unstaged)* changes in a file |
| `git restore --staged <file>` | Unstage a file *(keep changes in working directory)* |
| `git reset --soft HEAD~1` | Undo last commit but keep changes staged |
| `git reset --hard HEAD~1` | Undo last commit and discard all changes |

---

# 8. DELETE BRANCHES

## Method 1: Delete Branch from GitHub UI

1. Navigate to the main page of your repository on GitHub.
2. Click the **Branches** link *(usually shows the number of branches)* above the file list.
3. Find the branch you want to remove.
4. Click the **Trash can icon** next to the branch name to delete it.

---

## Method 2: Delete Using Git Commands

| Command | Description |
|---|---|
| `git push origin --delete <branch_name>` | Delete the remote branch from GitHub |
| `git branch -d <branch_name>` | Delete the local branch |

---

# 9. SCENARIO 2: REPO ALREADY EXISTS *(Clone/Pull)*

| Command | Description |
|---|---|
| `git clone <URL>` | Clone full remote repository *(first time)* |
| `git pull origin <branch-name>` | Pull latest changes *(already cloned)* |