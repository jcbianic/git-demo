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

Rebasing your branches has two main benefits :

- Resolving conflicts at the right moment and in the correct order: the commits you are about to merge come after commits that are already part of the master. ⇒ a little bit of an overkill in our case because we don’t have a lot of conflicts yet.
- Making the CI/CD status of your PR more reliable. (that is the real reason)
    
    Your branch might pass the CI/CD when outdated but then fail when merged into the master because your fresh commits introduce a bug with the newest code version (like broken import due to moving files around or renaming objects). 
    
    By rebasing on the latest HEAD of the master, the HEAD of your branch has the exact same state as will the master once it is merged. Thus the result of the CI/CD is more reliable when your branch is rebased just before merging.
    
