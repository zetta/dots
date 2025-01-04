# Daily Dots: Keep Your GitHub Contribution Graph Green

Let’s face it: the tech world can be ridiculous. You might be out there building scalable systems, debugging production issues at 3 a.m., or writing clean, modular code that would make Uncle Bob proud. But if your GitHub contribution graph doesn’t look like a meadow in spring, some recruiter might think you’re slacking.

**Enter Daily Dots**—a no-nonsense tool to keep your contribution graph active because, sadly, appearances matter. Whether you're grinding on private repos, busy with work, or just taking a well-deserved break, this project has your back.

---

## Why This Project Exists

**Green squares ≠ skill**, but many recruiters act like they do. They love an active graph, and a sparse one might hurt your chances before you even get to the interview. Is it fair? Nope. Is it reality? Unfortunately, yes.

Daily Dots automates small, random contributions to your repo. It ensures your graph stays vibrant, varied, and human-looking. You’re not faking skill—you’re making sure people see the work ethic you’ve always had.

---

## How It Works

This GitHub Action runs daily (or manually, if you’re feeling proactive) to:
1. Generate a random number of commits (up to your defined max).
2. Push those commits via pull requests, which are automatically merged.
3. Keep your graph fresh and varied—because recruiters like “activity,” not patterns.

---

## Quick Setup Guide

Getting this running is easier than explaining pointers to a junior dev. Here’s how:

### Step 1: Fork the Repo

Click the **Fork** button at the top right of this repo. Now it’s yours.

### Step 2: Update the `config` File

Edit the `config` file in your fork. Here’s what it looks like:

```plaintext
user_name=your-github-username
user_email=your-github-email
max_commits=5
```

- `user_name`: Your GitHub username. Keep it simple.
- `user_email`: Use your GitHub-provided no-reply email (format: ID+USERNAME@users.noreply.github.com).
- `max_commits`: Maximum number of commits per day. Keep it reasonable—randomness is key.

### Step 3: Add a GitHub Token
To let the workflow make commits and create PRs, you need a Personal Access Token (PAT):

1. Go to Settings → Developer Settings → Personal Access Tokens → Generate New Token.
2. Select permissions for:
    - repo (write access).
    - workflow (for triggering actions).
3. Generate the token and copy it immediately (you won’t see it again).
4. Add the token to your forked repo:
    - Go to Settings → Secrets and Variables → Actions → New Repository Secret.
    - Name it GH_TOKEN and paste the token.

### Step 4: Enable and Run the Workflow
1. Go to Actions in your forked repo.
2. Enable workflows if prompted.
3. Sit back and let the cron job do its thing daily—or run it manually if you’re impatient.

## Why This Matters
Here’s the hard truth: an inactive GitHub profile can cost you opportunities. Whether it’s fair or not, some recruiters and hiring managers equate activity with skill.

But life happens. Maybe your work is on private repos. Maybe you’ve been swamped with real-world coding. Maybe you’ve just been taking a breather. Daily Dots keeps your profile alive and well, making sure you’re judged for your skills—not your graph.

## Final Thoughts
This isn’t cheating. This is leveling the playing field in a game that cares too much about appearances. So fork this repo, set it up, and let Daily Dots handle the tedious work of staying “active” while you focus on actual coding.

Remember, you’re not defined by your contribution graph. But hey, it doesn’t hurt to keep it green.

Stay green, stay sane. 🚀
