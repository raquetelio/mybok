# GitHub.com Basics

## Create Git Reposity from local content

Create local repository and add existing content:
```
git init
git add . && git commit -m "initial commit"
```

Set principal branch to main:
```
git branch -M main
```

Create remote repository:
```
gh repo create
```
    Output:
    ```
    ~/projects/mybok> gh repo create
    ? What would you like to do? Push an existing local repository to GitHub
    ? Path to local repository .
    ? Repository name mybok
    ? Description My BoK (Body of Knowledge)
    ? Visibility Public
    ✓ Created repository raquetelio/mybok on GitHub
    ? Add a remote? Yes
    ? What should the new remote be called? origin
    ✓ Added remote git@github.com:raquetelio/mybok.git
    ? Would you like to push commits from the current branch to "origin"? Yes
    ✓ Pushed commits to git@github.com:raquetelio/mybok.git```

**NB: Make sure visibility is private when applicable.**
## Push changes in local to GitHub.com
```
git push origin your-branch
```

## Git status
```
git status
```

## Branches
Create a new branch:
```
git checkout -b branchname
```

Check current branch:
```
git branch --show-current
```