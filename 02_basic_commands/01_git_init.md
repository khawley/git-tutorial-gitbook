# git init

Currently, our lone file is not being version controlled.  If we change it or delete it, its gone.  Let's change that.

In order to change our `git_tutorial` folder into a git **repository \(repo\)** we need to use `git init`.

```
$ git init
```

![git init](./images/git-init-cmd.png)

If you do an `ls -la`, you'll see that a new directory has been added `.git`.

```
$ ls -la
```

![ls after git init](./images/git-init-result.png)

