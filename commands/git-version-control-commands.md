# Git Version Control

> **Section:** 24  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `git init` | Initialize a Git repository. | Added |  |
| `git clone URL` | Clone a repository. | Added |  |
| `git status` | Show working-tree and staging status. | Added |  |
| `git add FILE` | Stage changes. | Added |  |
| `git add -p` | Interactively stage selected hunks. | Added |  |
| `git commit -m "MESSAGE"` | Commit staged changes. | Added |  |
| `git log --oneline --graph --decorate --all` | Show compact decorated history graph. | Added |  |
| `git diff` | Show unstaged changes. | Added |  |
| `git diff --staged` | Show staged changes. | Added |  |
| `git branch` | List local branches. | Added |  |
| `git switch BRANCH` | Switch branches. | Added |  |
| `git switch -c NEW_BRANCH` | Create and switch to a branch. | Added |  |
| `git merge BRANCH` | Merge a branch into the current branch. | Added |  |
| `git rebase BASE` | Replay commits on a new base. | Added |  |
| `git fetch --all --prune` | Fetch all remotes and remove stale remote-tracking refs. | Added |  |
| `git pull --rebase` | Fetch and replay local commits on top of the remote branch. | Added |  |
| `git push -u origin BRANCH` | Push a branch and set its upstream. | Added |  |
| `git remote -v` | List remotes and URLs. | Added |  |
| `git stash push -m "MESSAGE"` | Temporarily save uncommitted changes. | Added |  |
| `git stash list` | List stashes. | Added |  |
| `git stash pop` | Apply and remove the latest stash. | Added |  |
| `git restore FILE` | Restore working-tree content from the index/HEAD. | Added |  |
| `git restore --staged FILE` | Unstage a file without discarding working-tree changes. | Added |  |
| `git revert COMMIT` | Create a new commit that reverses a prior commit. | Added |  |
| `git reset --soft HEAD~1` | Move HEAD back one commit while keeping changes staged. | Added |  |
| `git cherry-pick COMMIT` | Apply a specific commit onto the current branch. | Added |  |
| `git tag -a VERSION -m "MESSAGE"` | Create an annotated tag. | Added |  |
| `git reflog` | Show local reference movement history; useful for recovery. | Added |  |
| `git bisect start` | Start binary search for a regression. | Added |  |
| `git clean -nfd` | Preview removal of untracked files/directories. | Added |  |
| `git clean -fd` | Remove untracked files/directories. | Added | Destructive; run the -n preview first. |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
