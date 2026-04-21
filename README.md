# Git Identity Management & Workflow

This repository is configured to use a specific SSH alias to separate **Personal/University** work from **Work/Office** projects. Follow this guide to ensure your commits and remotes are mapped correctly.

---

## 🚀 Cloning the Repository

When cloning a **Personal** or **University** project, use the `github-personal` hostname:

```bash
git clone git@github-personal:OWNER/REPO.git
For work-related projects, you would use git clone git@github-work:OWNER/REPO.git.
```
Real Example 
```bash
git clone git@github-work:skmjcdev/browngro-dev.git
```

## 🛠️ Repository Configuration
Immediately after cloning, navigate into the project folder and set your local identity. This ensures your commits are linked to your personal email.
Bash

# 1. Enter the directory
```bash
cd browngro-dev
```

# 2. Set personal identity
```bash
git config user.name "nihilhesara"
git config user.email "nihilhesa@gmail.com"
```

# 3. Verification check
```bash
git config user.name
git config user.email
git remote -v
Verification Goal:
* Name: nihilhesara
* Email: nihilhesa@gmail.com
* Remote: Should contain github-personal
```

## 🔄 Daily Workflow
Once the identity is set, use your standard Git commands as usual:
```bash
git pull
git add .
git commit -m "your message"
git push
```

## 🛡️ Quick Safety Check
Before pushing to a new repository, run this quick check to prevent identity leaks:
```bash
git remote -v
git config user.email
```
If Remote Shows...	Use Identity...
github-personal	Personal (nihilhesara)
github-work	Work (Office Email)

## 💡 Memory Trick
* github-personal = Your personal, university, and side projects.
* github-work = Your office and company work.
The only command that changes is the clone command or when fixing a remote. Everything else remains the same.
