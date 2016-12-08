# Github command using

To add new files to the repository or add changed files to staged area:

```github
 $ git add <files>
```

To commit them:

```github
$ git commit -m "description"
```

To commit unstaged but changed files:

```github
$ git commit -a
```
To push to a repository (say origin):

```github
$ git push origin
```
To push only one of your branches (say master):

```github
$ git push origin master
```

To fetch the contents of another repository (say origin):

```github
$ git fetch origin
```

To fetch only one of the branches (say master):

```github
$ git fetch origin master
```

To merge a branch with the current branch (say other_branch):

```github
$ git merge other_branch
```

Note that origin/master is the name of the branch you fetched in the previous step from origin. Therefore, updating your master branch from origin is done by:

```github
$ git fetch origin master
$ git merge origin/master
```

