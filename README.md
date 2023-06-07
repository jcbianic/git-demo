# git-demo
A Git Repo to demonstrate Git functionnalities
SHOULD NOT BE HERE
### Preparing your commit

- Choose which Files to Stage
- Choose which Lines to Stage
- Concise descriptive and specific message (you can add details in the description)
- [Optional] Amend you last commit if you need to (and avoid duplicates)

### Clean up the Mess behind you

Mistakes are common. Git is here to help you clean up the mess.

You might need to:

- Ignore a commit (erase it from history) ⇒ drop or reset
- Move one or several commits to another branch ⇒ cherry-pick or reset
- Change the whole history (change order, rename, squash…) ⇒ interactive rebase
```bash# Soft Resetgit reset HEAD~1 --soft # modification go back to staginggit reset HEAD~1 --hard # modifications are discarded and not committed modification git reset HEAD~1 # modification# Cherry-Pickinggit cherry-pick 3a9cb3agit cherry-pick 927b562# Interactive Rebasegit rebase -i HEAD~5 # will allow you to drop, squash, rename, reorder commits, through text.```Squashing is useful to have a more concise commit history (some commits’ content do belongs together).Renaming is also a good way to tell a proper story after all the work has been done.Reordering can help tell a better story by reordering the commits, but where I find it useful is when you need to move a commit to the latest position (typically to amend it).