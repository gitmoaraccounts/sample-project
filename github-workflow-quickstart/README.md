# GitHub Workflow Quickstart  
*A guide to help new engineers contribute using GitHub with confidence*

---

## 📖 Overview

This guide provides step-by-step instructions for working with Git and GitHub in a collaborative engineering environment. It’s designed for onboarding new developers, engineers, or technical team members who are new to version control workflows.

By the end of this guide, you’ll be able to:
- Clone a repository and create a new branch
- Commit your changes following best practices
- Submit a pull request (PR) for review
- Collaborate through code reviews and finalize merges

---

## 🧰 Prerequisites

Before you begin, make sure you have the following installed:

| Tool            | Purpose                          | Link                             |
|-----------------|----------------------------------|----------------------------------|
| Git             | Version control                  | [Install Git](https://git-scm.com/) |
| GitHub account  | Repository hosting               | [github.com](https://github.com) |
| GitHub CLI *(optional)* | Command-line shortcuts for GitHub | [GitHub CLI](https://cli.github.com/) |
| VS Code *(optional)*    | Code editing with Git tools      | [Visual Studio Code](https://code.visualstudio.com/) |

---

## 🌱 Cloning a Repo and Creating a Branch

Next, peruse GitHub and decide which repository you'd like to contribute to or edit. Often, you'll see tags on repositories that say "Good first issue." Some examples are on the pandas repository: https://github.com/pandas-dev/pandas/contribute

Pick one of those and then follow the below commands:

```bash
# Clone the repository
git clone https://github.com/your-org/project-name.git
cd project-name

# Create a new branch for your changes
git checkout -b your-feature-branch

# Use clear, descriptive branch names:
# Examples: fix/login-bug, feature/add-user-form, docs/update-readme
```

---
## ✍️ Writing Clear Commit Messages

Good commit messages explain why the change was made. Stick to a format like this:

```bash
git commit -m "Fix typo in authentication error message"
```
✅ __Do:__
- Keep messages short and meaningful
- Use imperative mood: "Add feature", "Fix bug", "Update docs"

🚫 __Don't:__
- Write vague messages like "Update stuff" or "Changes"
- Write overly long messages like "Add feature module to improve readability, functionality, and performance, ultimately reducing the computing time from function A to function B."

Note there is some debate on writing commits in imperative mood, which is a tense used for actions and commands. In my own repos here, you'll see I sometimes use it and sometimes not. I think as long as you're concise and clear, you'll be ok.

---
## 🔁 Opening a Pull Request (PR)

After pushing your branch to GitHub:

```bash
git push origin your-feature-branch
```
Go to the repository on GitHub and click “Compare & pull request.”

In your PR:
- Include a summary of the changes
- Reference related issues (if applicable)
- Tag reviewers

>Tip: Use a pull request template to keep your PRs consistent (see `/examples/pull_request_template.md`)

---
## 🔀 Merging and Cleaning Up

Once your PR is approved:
- Choose “Squash and merge” (or your team’s preferred option)
- Delete the feature branch from GitHub
- Pull the latest main branch locally:

```bash
git checkout main
git pull origin main
```
---
## 📝 Additional Resources
- [GitHub Docs](https://docs.github.com/en)
- [Git CLI Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Pro Git Book (Free)](https://git-scm.com/book/en/v2)

---
## 🧠 Why This Guide Exists

This project demonstrates documentation structure, Git workflow clarity, and Markdown formatting best practices. It's designed as part of a technical writing portfolio to highlight instructional writing and enablement content for engineering teams.