# GitHub.com Basics

## Create Git Reposity from local content

Create local repository and add existing content:
```
git init
git add . && git commit -m "initial commit"
```

Create remote repository:
```
gh repo create
```

Push the changes in your local repository to GitHub.com.
```
git push origin your-branch
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