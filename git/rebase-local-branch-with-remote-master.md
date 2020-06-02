# Rebase local branch with remote master

After committing changes to your branch(RB in the example), checkout master and pull it to get its latest changes from the repo:

```
git checkout master
git pull origin master
```
Then checkout your branch and rebase your changes on master:

```
git checkout RB
git rebase master
```
...or last two commands in one line:

`git rebase master RB`

When trying to push back to origin/RB, you'll probably get an error; if you're the only one working on RB, you can force push:

`git push --force origin RB`
...or as follows if you have git configured appropriately:

`git push -f`

[Source](https://stackoverflow.com/questions/7929369/how-to-rebase-local-branch-with-remote-master)
