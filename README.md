### 📁 Repo Name: `github-cli-cheatsheet`

### 📄 `README.md` (Full content below)

````markdown
# 🧾 GitHub CLI Cheatsheet

This repository is a command-line reference for working with **GitHub** using `git` and `gh` (GitHub CLI).

---

## 🔧 Git Setup

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
````

---

## 📁 Repository Operations

### Clone a repo

```bash
git clone https://github.com/user/repo.git
```

### Create a new repo (local + remote)

```bash
mkdir my-repo && cd my-repo
git init
gh repo create my-repo --public --source=. --remote=origin --push
```

---

## 🌿 Branching

### Create and switch to a branch

```bash
git checkout -b feature-branch
```

### Push branch to GitHub

```bash
git push -u origin feature-branch
```

---

## 🔄 Syncing

### Pull latest changes

```bash
git pull origin main
```

### Rebase current branch

```bash
git pull --rebase origin main
```

---

## ✅ Staging & Committing

```bash
git add .
git commit -m "Your commit message"
git push
```

---

## 🔍 Status & Log

```bash
git status
git log --oneline --graph --all
```

---

## 🔁 Undo

```bash
git reset HEAD~1       # Undo last commit, keep changes
git checkout .         # Discard all unstaged changes
git clean -fd          # Remove untracked files/folders
```

---

## 🔀 Merging & Rebasing

```bash
git merge feature-branch
git rebase main
```

---

## 🚀 Pull Requests (via `gh`)

```bash
gh pr create --base main --head feature-branch --title "PR title" --body "PR description"
gh pr view --web
gh pr checkout 123
```

---

## 🧪 GitHub Actions

```bash
gh workflow list
gh run list
gh run watch <run-id>
```

---

## 🔒 SSH Setup

```bash
ssh-keygen -t ed25519 -C "you@example.com"
cat ~/.ssh/id_ed25519.pub
```

Add the key to GitHub → Settings → SSH and GPG keys

---

## 🕒 Cron Example for Repo Backup (Linux/macOS)

```bash
crontab -e
```

Add line to pull daily:

```cron
0 2 * * * cd /path/to/repo && git pull >> ~/git-sync.log 2>&1
```

---

## 📦 Submodules

```bash
git submodule add https://github.com/user/lib.git lib
git submodule update --init --recursive
```

---

## 📤 GitHub Release (via `gh`)

```bash
gh release create v1.0.0 ./build.zip --title "Release v1.0.0" --notes "First stable release"
```

---

## 📚 Resources

* [GitHub CLI Docs](https://cli.github.com/manual/)
* [Git Handbook](https://guides.github.com/introduction/git-handbook/)

---

### ✍️ Author: \[Jamaurice Holt]

```

