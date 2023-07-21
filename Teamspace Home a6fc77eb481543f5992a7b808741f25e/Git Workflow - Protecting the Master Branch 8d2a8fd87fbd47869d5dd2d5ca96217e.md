# Git Workflow - Protecting the Master Branch

Owner: ravagedshell
Tags: Guide, Software Developement
Created time: July 19, 2023 12:20 AM

# Table of Contents

# Process

**When working on new features, additions, hotfixes, or bugs, work should be done in a separate branch and then later merged into the main branch. This is to protect the continuity of the code and avoid changes that may interfere with work that other developers are working on. This prevents breaking features, introducing new bugs, and overwriting others work.**

Step 1: **Fetch all current changes and create a branch specific to the sprint, feature, hotfix, or bug you are working on**

****

```bash
git pull
**git checkout -b “branchname”**
```

Step 2: **Complete the work you are working on**

Step 3: **Push the changes to the upstream branch**

```bash
**git add <files>
git commit -m “A commit message”
git push origin “branchname”**
```

Step 4: **Merge the changes from your branch into the master or main branch only when completed and validated to not cause issues with the existing codebase.**

```bash
git checkout master
git fetch origin
git merge “branchname”
git push
```

**In the future, we will move to using pull requests where merges to the master codebase are reviewed for potential errors, new bugs, etc., before being committed to the main codebase. This will require some additional training and hence has been pushed off till a larger project is in the works.**

# Version Control

| Version | Date | Author | Changes |
| --- | --- | --- | --- |
| 1.0 | July 15, 2023 | ravagedshell | Document Origination |
| 1.1 | July 18, 2023 | ravagedshell | New format for Notion, Updated Screenshots |