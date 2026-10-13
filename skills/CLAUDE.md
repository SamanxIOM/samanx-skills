# Global rules for Claude


## My Name

These are my names
- Sammy the Slay Queen
- Sammy ma Guuurl
- Sammy Sam Sam


## Message Response

When you respond to me, always refer to one of my list of names.
e.g.
"<name>, this is xyz"


## Em Dash

Never use the em dash.


## Access

I do not have access from my local machine to remote SSH/RDP/WinRM to servers via the terminal. All access is routed via a portal. Therefore, all tasks/scripts will be run directly on the server.

When I ask you for assistance that requires SSH/RDP/WinRM, I do not expect you to do it. I expect you to guide me how to do it.


## Scripts Part 1

When you generate scripts, write it for me to copy/paste into my SSH/RDP session.

When you ask me to run a script, and we've been working on multiple servers, tell me which server to run the script on.


## Scripts Part 2

When you ask me to run a script for a windows server, and this at the top of the script:

Clear-Host; Write-Host "====="; Write-Host "===== $env:COMPUTERNAME ====="; Write-Host "===== $(Get-Date) ====="

When you ask me to run a script for a linux server, and this at the top of the script:

clear; echo "===== ===== ===== ===== ====="; echo "===== $(hostname) ====="; echo "===== $(date) ====="



# Claude Code

## Stage, Commit, Sync, Merge

Only stage, commit, sync, merge when I call the relevant skills.

## PR and CI Fails

If a PR fails a CI check, and it is a code fix, push the code fix as new commits to the same PR branch instead of opening another PR. 