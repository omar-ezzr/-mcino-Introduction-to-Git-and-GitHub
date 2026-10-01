# Final Project Submission Guide

Replace `YOUR_GITHUB_USERNAME` below with your real GitHub username.

Expected fork:

```text
https://github.com/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub
```

## Part 1 — URLs to submit

### Task 1 — README.md

```text
https://github.com/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub/blob/main/README.md
```

### Task 2 — LICENSE

```text
https://github.com/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub/blob/main/LICENSE
```

### Task 3 — CODE_OF_CONDUCT.md

```text
https://github.com/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub/blob/main/CODE_OF_CONDUCT.md
```

### Task 4 — CONTRIBUTING.md

```text
https://github.com/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub/blob/main/CONTRIBUTING.md
```

### Task 5 — simple-interest.sh

```text
https://github.com/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub/blob/main/simple-interest.sh
```

---

# Part 2 — Required real terminal outputs

The files below cannot contain invented data. Run the commands against your
real GitHub repository and paste the resulting contents into Coursera.

## Task 6 — forked-repo

Run:

```bash
curl https://api.github.com/repos/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub | tee forked-repo
```

Verify the output contains:

```text
"fork": true
```

and references:

```text
ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub
```

## Task 7 — merge_branches

The grader expects output containing:

```bash
git checkout main
git merge bug-fix-typo
```

and merge output showing that one file changed.

You can capture the commands and output with:

```bash
{
  echo '$ git checkout main'
  git checkout main

  echo '$ git merge bug-fix-typo'
  git merge bug-fix-typo
} 2>&1 | tee merge_branches
```

Do this only when the branch is ready to merge.

## Task 8 — bug-fix-revert

Replace `PULL_REQUEST_NUMBER` with the actual PR number.

If the pull request is in the IBM repository:

```bash
curl https://api.github.com/repos/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub/pulls/PULL_REQUEST_NUMBER | tee bug-fix-revert
```

If the lab asks you to inspect a PR in your own fork, use:

```bash
curl https://api.github.com/repos/YOUR_GITHUB_USERNAME/mcino-Introduction-to-Git-and-GitHub/pulls/PULL_REQUEST_NUMBER | tee bug-fix-revert
```

Verify the output shows the pull request and that the `head` repository
belongs to your fork.

## Task 9 — github-branches

Run:

```bash
git branch -avv | tee github-branches
```

This should display branch names and their current status.

---

# Initial Git Setup

After copying these files into your fork:

```bash
chmod +x simple-interest.sh

git add README.md LICENSE CODE_OF_CONDUCT.md CONTRIBUTING.md simple-interest.sh
git commit -m "Complete Git and GitHub final project files"
git push origin main
```

Before submission:

```bash
git status
git remote -v
git branch -avv
```
