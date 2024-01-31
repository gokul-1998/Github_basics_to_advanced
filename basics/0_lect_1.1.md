# This document will compile the knowledge from the video above and other sources

- `git reset` is used to unstage files
- `git reset --hard` is used to unstage files and discard changes
- `git reset --hard HEAD~1` is used to unstage files, discard changes and go back to the previous commit
- `git reset --hard HEAD~2` is used to unstage files, discard changes and go back to the previous commit before the previous commit`
- `git reset --hard <commit_id>` is used to unstage files, discard changes and go back to the commit with the specified commit id (the commit id can be found using `git log`), e.g. `git reset --hard 1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s0t1u2v3w4x5y6z` (the commit id is a 40 character string)

- `git reset --hard HEAD~<number_of_commits>` is used to unstage files, discard changes and go back to the commit with the specified commit id (the commit id can be found using `git log`), e.g. `git reset --hard HEAD~3` (go back 3 commits)
- `git reset --hard origin/<branch_name>` is used to unstage files, discard changes and go back to the last commit on the remote repository

- `git reset --hard origin/master` is used to unstage files, discard changes and go back to the last commit on the remote repository

## Conventional commits
- https://www.conventionalcommits.org/en/v1.0.0/
    - this tells you how to write commit messages
    - e.g. `git commit -m "feat: add summation function"` 
        - `feat`: feature, 
        - `fix`: bug fix, 
        - `docs`: documentation, 
        - `style`: formatting, 
        - `refactor`: code refactoring, 
        - `test`: when adding missing tests
        - `chore`: when updating build tasks 

- There are several merging Techniques
    - `git merge <branch_name>` is used to merge the specified branch into the current branch
    - `git merge --abort` is used to abort a merge
    - `git merge --continue` is used to continue a merge after resolving conflicts
    - `git merge --no-ff <branch_name>` is used to merge the specified branch into the current branch without fast-forwarding
        - this creates a new commit even if the merge could be done with a fast-forward
        - this is useful if you want to keep track of the fact that you merged the branch
        - fast-forwarding is when the branch you are merging into has not changed since the branch you are merging from was created
        
- `git diff` is used to show the difference between the current state of the repository and the last commit

- `git branch` is used to show the current branch
- `git branch <branch_name>` is used to create a new branch
- `git branch -d <branch_name>` is used to delete a branch
- `git branch -D <branch_name>` is used to delete a branch even if it has not been merged
- `git branch -m <branch_name>` is used to rename a branch
- `git branch -a` is used to show all branches
- `git branch -r` is used to show all remote branches

-  `git checkout <branch_name>` is used to switch to the specified branch
- `git checkout -b <branch_name>` is used to create a new branch and switch to it
- `git checkout -b <branch_name> <commit_id>` is used to create a new branch from the specified commit and switch to it
- `git checkout -b <branch_name> <branch_name>` is used to create a new branch from the specified branch and switch to it
- `git checkout -b <branch_name> origin/<branch_name>` is used to create a new branch from the specified remote branch and switch to it
- `git checkout -b <branch_name> origin/master` is used to create a new branch from the master branch on the remote repository and switch to it

- 