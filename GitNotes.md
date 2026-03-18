# Starting a new branch
To see all current branches:
```
git branch
```

To start a new branch in the current project:
```
git checkout -b refactor
```

This creates the branch and checks it out at the same time.

# Merge a branch
To merge a branch:
```
git checkout main
git pull
git merge refactor
```

Finally to delete the branch:
```
git branch -d refactor
```

