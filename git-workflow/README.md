# Git workflow

The basic guidelines for working on a small team project. The philosphy is to create a branch for every feature, and each team member is responsible for handling merges to master. This assumes you have cloned or setup the repo.

### Starting new feature:
**IMPORTANT:** Stay up to date before creating a new branch:
```
git checkout master
git pull
```

Create new feature branch from master:
```
git checkout -b feature-name
```

### Working on feature:
Do work on feature, make commits per usual. You can then create the remote branch:
```
git push -u origin feature-name
```
This creates a branch on your remote repository called **feature-name**. Additional commits can simply be pushed with with `git push`.

[Work on a pre-exising remote branch](#work-on-a-pre-existing-remote-branch)

### Finishing feature:
When you are ready to merge your feature into master, first make sure all your changes have been committed and pushed. If you are using [GitHub](https://github.com), you can first try a pull request:
* Go to the webpage of your remote repository branch
* Click the green button "new pull request"
* Adjust the info as needed, then click "create pull request"
* If all goes well you can click the "merge" button

If successful, you can make your local repository up-to-date with the new feature in master:
```
git checkout master
git pull
```

And [delete the feature branch](delete the feature branch).

If not succesful or you do not have GitHub, you can do it manually:
```
git checkout master
git pull
git checkout feature-name
git rebase master
```

If conflicts exists you must resolve them, then:
```
git add -A
git rebase --continue
```

Switch back to master, merge in feature, then push to remote:
```
git checkout master
git merge feature-name
git push origin master
```

And [delete the feature branch](delete the feature branch).

### Delete the feature branch
This will delete a feature branch both locally and then on the remote repository.
``` 
git branch -d feature-name
git push origin --delete feature-name
```

### Work on a pre-existing remote branch:
```
git fetch
git checkout --track origin/feature-name -b feature-name
```

### Resources for learning git
[http://www.git-tower.com/learn/git/ebook/command-line/introduction](http://www.git-tower.com/learn/git/ebook/command-line/introduction)
[https://www.atlassian.com/git/tutorials/](https://www.atlassian.com/git/tutorials/)