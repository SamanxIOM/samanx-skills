---
name: pitstop
description: Tidy every repo in the folder back to a clean, synced main branch
---

# Prelim Step

- Name the Claude chat to be the name of the folder, plus the word "pitstop". e.g. "folder-pitstop"
- Review the current folder.
	- If the current folder is one repo, review the one repo
	- If the current folder is not a repo, but, the immediate sub folders are, review the multiple repos.
- Silently skip any folder that is not a git repo. 
- If no repos are found, say so and stop.
- Do a scan/check of all the local branches.
- Do a scan/check of all the remote branches.


# Step 1 - Local - Back to Main

- Go through each repo
- Any repos not on main, switch to main and sync from GitHub remote.
- Any uncommitted code, discard it.

- Create a table called "Local - Back to Main":
  - Repo name
  - What the branch was on before
  - What changes have happened on main since the sync. i.e. deployed xyz. Make it brief.
  - The name of the person who did the change.
  

# Step 2 - Local - Cleanup on Aisle 5

- Go through each repo
- Check what local branches there are.
- Any that have a local branch, but have been merged into main on GitHub remote, delete them from my local machine.
- Any that have a local branch, but have NOT been merged into main on GitHub remote, leave them alone.

- Create a table called "Local - Cleanup on Aisle 5":
  - Repo name
  - Local branch
  - If it was deleted or skipped
  - If it was skipped, explain why
  

# Step 3 - Remote - Branch Overview

- Go through each repo
- Check what remote branches are open by the current user of this machine. Ignore branches by other users.
- Any that have a remote branch, open by the current user of this machine, but have been merged into main on GitHub remote, delete the GitHub remote branch.
- Any that have a remote branch, open by the current user of this machine, but have not been merged into main, leave them alone.

- Create a table called "Remote - Branch Overview"
  - Repo name
  - The remote branch name
  - Last authored by name
  - Last authored by date
  - How many commits far behind main it is
  - If it was deleted or skipped
  - If it was skipped, explain why