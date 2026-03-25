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

# Repair an archive
Check the git archive:
```
git fsck
git fsck --full
```

To try and salvage existing commits:
```
git gc --prune=now --aggressive
```
or
```
git repack -a -d
```

Re-initialize the archive (prior commits will be lost)
```
rm -rf .git
git init
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:KK7JJI/Ruby_Sorting.git
git push -u origin main
```

To force a push to GitHub:
```
git push -u origin main --force
```
