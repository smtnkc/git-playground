# Git Cheatsheet

## Undo / Delete / Squash operations

**Undo uncommitted add for single file:**

```git reset <file>```

**Undo uncommitted add for all files:**

```git reset```

**Undo the most recent commit, keeping the work you've done:**

```git reset --soft HEAD~1```

**Undo most recent commit, destroying the work you've done:**

```git reset --hard HEAD~1```

**Add more changes to last pushed commit:**

Make the additional changes and run:

```git add . && git commit --amend --no-edit && git push -f origin <branch_name>```

**Squash last 3 pushed commits:**

```
git reset --soft HEAD~3
git add .
git commit -m "new commit message"
git push -f origin <branch_name>
```

**Delete last 3 commits remotely and locally**:

```git push origin +HEAD~3:master``` :arrow_right: Delete remote commits (from master branch)

```git reset --soft HEAD~3``` :arrow_right: Delete local commits, keeping local changes

```git reset --hard HEAD~3``` :arrow_right: Delete local commits, destroying local changes

## Branch operations

**Create new branch**:

```git checkout -b <branch_name>```

**Merge branch to master**:

```git checkout master && git merge <branch_name>```

**Delete branch both locally and remotely:**

```
git push -d origin <branch_name>
git branch -d <branch_name>
```
