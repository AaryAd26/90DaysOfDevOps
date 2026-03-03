# Day 25 – Git Reset vs Revert & Branching Strategies

---

## Git Reset – Practical Understanding

First, create three commits in your repository:

Commit A → Commit B → Commit C

Now let’s understand how different reset modes behave.

---

### git reset --soft

When you run:

git reset --soft HEAD~1

Git moves the HEAD pointer one commit back.

What happens:
- The latest commit is removed from history.
- All the changes from that commit remain staged.
- Your working directory is not affected.

Use case:
When you want to modify the last commit (for example, change the commit message or add more changes before recommitting).

---

### git reset --mixed (default mode)

When you run:

git reset --mixed HEAD~1

What happens:
- The latest commit is removed from history.
- Changes remain in your working directory.
- Changes are unstaged (you must run git add again).

Use case:
When you want to rework or edit the changes before committing again.

---

### git reset --hard

When you run:

git reset --hard HEAD~1

What happens:
- The latest commit is removed from history.
- All changes from that commit are permanently deleted.
- Working directory is reset to match the previous commit.

Important:
This is destructive because it deletes changes completely.

Use case:
When you want to completely discard commits and changes.

---

### Difference Between Soft, Mixed, and Hard

Soft → Removes commit but keeps changes staged.  
Mixed → Removes commit and keeps changes unstaged.  
Hard → Removes commit and deletes changes permanently.

---

### Should You Use Reset on Pushed Commits?

No.

If commits are already pushed and shared, using reset rewrites history.  
This can create conflicts and confusion for other team members.

Reset should mainly be used on local, unshared commits.

---

## Git Revert – Safe Undo Method

Create three commits again:

Commit X → Commit Y → Commit Z

Now revert the middle commit:

git revert <commit-hash-of-Y>

What happens:
- Git creates a new commit.
- This new commit reverses the changes made by commit Y.
- Commit Y still remains in history.

Key point:
Revert does not delete history. It adds a corrective commit.

---

### Reset vs Revert – Core Difference

git reset:
- Rewrites history.
- Removes commits.
- Can delete changes.
- Not safe for shared branches.

git revert:
- Keeps history intact.
- Adds a new commit to undo changes.
- Safe for shared and production branches.

Simple explanation:
Reset erases history.
Revert fixes history.

---

## Branching Strategies

### GitFlow

GitFlow uses structured long-term branches:

- master → Production-ready code.
- develop → Active development branch.
- feature branches → Created from develop for new features.
- release branches → Created from develop when preparing a release.
- hotfix branches → Created from master for urgent production fixes.

Workflow:
Features merge into develop → release branch → master  
Hotfix merges into master and develop.

Best for:
- Large teams
- Enterprise environments
- Scheduled releases

Pros:
- Very organized
- Clear separation of development stages

Cons:
- Complex
- Slower workflow
- Heavy process

---

### GitHub Flow

GitHub Flow is simple:

- main → Always production-ready.
- Feature branches → Created from main, reviewed via pull request, then merged back.

Workflow:
Create branch → Make changes → Open PR → Review → Merge to main

Best for:
- Continuous deployment
- Small to medium teams

Pros:
- Simple
- Fast
- Lightweight

Cons:
- Can become messy without discipline
- No structured release cycle

---

### Trunk-Based Development

In this strategy:

- main (trunk) is the central branch.
- Developers commit directly or use very short-lived branches.
- Code is merged frequently.

Best for:
- Startups
- Fast-moving teams
- Continuous integration environments

Pros:
- Very simple
- Encourages small frequent commits
- Faster development

Cons:
- Risky without proper CI/CD
- Unstable code can affect everyone quickly

---

![WhatsApp Image 2026-03-03 at 8 31 36 PM](https://github.com/user-attachments/assets/f0008805-5974-4e92-857c-e99c1efb2711)

---
