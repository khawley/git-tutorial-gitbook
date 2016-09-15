# Terms {#terms}

- **repository (repo)** - is a parent folder that is using version control
- **untracked file(s)** - a file that git is not tracking changes for
- **tracked file(s)** - a file that git is tracking any changes for
- **staging area** - storage area for what will go into your next commit
- **stage/unstage** - to add or remove something from the staging area
- **commit** - a timestamped set of changes with an explanatory message
- **diff** - a set of changes between one state and another, like the last commit and your current directory (`git diff`) or between one commit and another (`git show <hash>`)
- **log** - the historical list of commits
- **commit hash** - the unique identifier created with each commit
- **HEAD** - the alias and pointer to the most recent commit's hash on this branch
- **master** - the default first branch of a repo
- **branch** - a separate direction for commits, independent of your main branch, but with the ability to be added into your main branch later.
- **merge** - combining the changes of one branch into another
- **merge conflict** - the result when a merge doesn't resolve flawlessly.  This usually happens when both branches edited the same line with different text.  Git asks the user to pick which is the correct text.
- **remote** - an external location of your repo that can be used for backup and collaboration
- **origin** - the default first remote location of a repo
- **fork** - a cloned remote copy, created from the original owner's repo.  Best used when you do not have edit/push privileges on the original repo.
- **pull request/merge request** - a request created on the remote website (like GitHub) asking that changes you have made to your branch be merged into the main branch of the project.


#  Commands {#command_summary}
- `git config` - used for adding/changing git configurations, such as your name or email that is used on commits
- `git init` - command to add git tracking to your directory
- `git status` - show the status of any untracked, unstaged, and staged in the repository.  Also displays the current branch name.
- `git add <file_or_path> [...]` - add file(s) to the staging area in preparation for committing
- `git commit -m "<commit_msg">`
- `git diff` - shows the changes in your working directory compared to your most recent commit
- `git log` - shows your commit history
    * `git log --decorate` - shows your commit history, including pointers like `HEAD`, branches, and remote brances
- `git show <hash>` - shows the diff of a specific commit, the changes that saved in that commit
- `git reset`
    * `git reset HEAD <file_or_path> [...]` - removes file(s) from the staging area, but keeps the changes in your working directory.
    * `git reset <hash>` - rollback your history to the specified commit.  Removes all commits that came after it, bur preserves the changes in your working directory.
- `git checkout`
    * `git checkout <hash>` - jump to a point in your history, but does not _alter_ your history.  This is a 'detached HEAD' state
    * `git checkout -- <file>` - clear the changes of a tracked file from your working directory
    * `git checkout <branch>` - change to that branch and able to make changes to that branch's history
- `git branch` - list all branches, with `*` designating the current branch
    * `git branch <new_branch>` - create a new branch using your current branch as a starting point
    * `git branch -m <old_name> <new_name>` - rename a branch
    * `git branch -d <branch_to_delete>` - delete a branch that you are not currently in
- `git merge <branch>` - add the commits of specified branch into your current one
- `git remote` - shows a list of your remote location aliases.  The default is `origin`
    * `git remote -v` - shows the list of your remote location aliases and their clone urls
    * `git remote add <remote_alias> <remote_url>` - adds a remote location to your repo
- `git clone <remote_url> <new_local_folder>` - copies a project from the remote_url to the specified local folder
- `git fetch` - grabs all remote branches and changes, but does not merge them in
- `git pull <remote> <remote_branch>` - does a fetch of changes, then merges them into your current branch
- `git push <remote> <branch>` - pushes changes from your current branch to the remote
- `git mv <old_file> <new_file>` - both renames/moves the file and tells git to link the history of the old file to the new
- `git rm <file>` - both deletes the file and tells git to stop tracking it.
