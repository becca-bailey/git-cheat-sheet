# Git Cheat Sheet
```
git log
```
Shows you a list of your most recent commits

```
git rebase <branchname>
```
Rebases your branch onto another branch

```
git rebase -i <commit>
```
This will show you a list of commits, starting at the commit id you specified. (Copy this from `git log` or use `head~<number>` to specify the number of commits you want to see. From this list, you can edit, rename, or squash commits together.

```
git push -f origin <branchname>
```
If you have changed the commit history in a rebase, you may need to force push your branch back to Github. This can be dangerous, so if you are working with a team and there is a possibility that someone else may have made changes to the same branch, use `--force-with-lease` instead.

```
git commit --amend
```
This will squash your current changes into your last commit, and give you the opportunity to update your commit message.

```
git commit --amend --no-edit
```
This will squash your current changes into your last commit, preserving the last commit message.

---
If you want to save your changes, but aren’t at a good stopping place, typically we mark these commits with a `WIP`.  Once your tests are passing and you have made all the changes you want to make in this commit, you can go back and fix up this commit with  `git commit --amend` or `git rebase -i`. WIP commits should not be merged to master.
