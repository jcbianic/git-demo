# Git Demo

SHOULD NOT BE HERE
SHOULD NOT BE HERE


### Branch Manipulation

### Creation and Tracking

Note: *I like to do these operations with the command-line but you could do it in Fork.*

```bash
# Creating a Branch and Variation

## Creating a new branch locally
git checkout -b feature/app_structure

## Start Tracking a branch that exists on remote
git fetch [origin]
git checkout feature/branch_that_exists_on_remote

# Naming Conventions
git checkout -b feature/name_of_the_feature
git checkout -b hotfix/name_of_bug
git checkout -b misc/for_any_other_thing

# Renaming
git branch -m feature/new_name # will rename the current branch
# If the branch exists remotely, you should delete it (Proceed with caution here !!)
git push --delete feature/old_name
# and push the new branch
git push  feature/new_name
```

### Rebasing
