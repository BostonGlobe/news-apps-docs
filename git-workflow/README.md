# Git workflow

The basic guidelines for working on a small team project. The philosphy is to create a branch for every feature, and each team member is responsible to handle merges to master.

### Starting new feature:
Stay up to date before creating new branch
``` git
git checkout master
git pull
```

Create new feature branch from master
``` git
git checkout -b feature-name
```

### Working on feature:
Do work on feature, make commits as usual. If you don’t finish the feature or it needs to be shared for someone else to contribute to, then create the remote branch
``` git
git push -u origin feature-name
```
Then push as usual.

### Finishing feature:
Get latest master, switch to feature, and fold in master code
``` git
git checkout master
git pull
git checkout feature-name
git rebase master
```

Resolve conflicts if present, then:
``` git
git add -A
git rebase --continue
```

Switch back to master, merge in feature, then push to remote
``` git
git checkout master
git merge feature-name
git push origin master
```

Delete local feature branch and remote (if exists)
``` git 
git branch -d feature-name
git push --delete feature-name
```

### Work on another remote branch:
``` git
git fetch
git checkout --track origin/feature-name -b feature-name
```