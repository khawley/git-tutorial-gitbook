# Collaboration and Contribution Workflow

## Collaboration access

If you have collaboration access (the ability to push directly to the repo), this workflow will work for you.

1) First clone and pull from the remote.

    
    git clone <remote_url> <folder>  
    cd <folder>
    git fetch
    git pull origin master
    

2) Create a new branch for whatever you are fixing or creating.

    
    git branch <feature>
    git checkout <feature>
    

3) Do all of your commits and development on that branch.

4) When you're ready to submit your changes, do a final pull, to make sure you are up-to-date and resolve any merge conflicts.

    
    git pull origin master
    

5) Push your new branch up to the remote.

    
    git push origin <feature>
    

6) Create a pull request for your changes


## Forking Access

If you don't have edit access to a repo, you'll need to fork first, but most of your steps will look very similar.  You'll also have _two_ remotes here, your forked remote repo (`origin`), and the original remote repo (we'll name `source`).

1) Fork the project on GitHub.

2) Clone your forked project.

    
    git clone <remote_url> <folder>  
    cd <folder>
    git fetch
    git pull origin master
    

3) Add the original repo to your remotes list.

    
    git remote add source <source_clone_url>
    

4) Create a new branch for whatever you are fixing or creating.

    
    git branch <feature>
    git checkout <feature>
    

5) Do all of your commits and development on that branch.

6) When you're ready to submit your changes, do a final pull, to make sure you are up-to-date and resolve any merge conflicts.  For this, you'll want to pull from `source` and not `origin`.  This ensures that you are getting the changes from the _original_ project and not your forked project.

    
    git pull source master
    

5) Push your new branch up to _your_ remote.

    
    git push origin <feature>
    

6) Create a pull request from your remote + branch, to the source remote and branch.
