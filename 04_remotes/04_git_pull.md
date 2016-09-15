# git pull

`git pull` is a combination of `git fetch` and `git merge`.  It will grab the remote changes and merge them into your branch for you.

Its a good habit to `git pull` if you haven't in a while.  Its an especially good habit to pull `master` into a whatever feature branch you are working in, so that you're always up-to-date.

Since we want to keep our `demo` branch in sync with `master`, we could run a fetch and merge, like these commands: 

```
$ git fetch
$ git merge origin master
```

Or we could use `git pull` as a combined command, adding the remote and branch name to the command.

```
git pull origin master
```
