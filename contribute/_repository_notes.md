# About this repository

This GitHub repo is a git subtree of a larger, private, internal GitLab repository. The code in both locations can be kept in sync with one another.

Here is some information about how Git Subtree works:
- `git subtree` docs: https://github.com/apenwarr/git-subtree/blob/master/git-subtree.txt
- Walkthrough I used: https://makingsoftware.wordpress.com/2013/02/16/using-git-subtrees-for-repository-separation/

## Sync instructions

First, add this GitHub repository as a remote:
```
git remote add gh https://github.com/upenn-libraries/Accessibility.git
```

To pull code from the GitHub master branch and push to GitLab's master branch, do this:
```
git subtree pull --prefix=Accessibility --squash gh master
git push origin master
```

To pull code from GitLab and push it to the GitHub master branch, do this:
```
git pull
git subtree push --prefix=Accessibility --squash gh master
```
