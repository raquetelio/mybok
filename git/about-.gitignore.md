# About .gitignore

## How do I make Git forget about a file that was tracked, but is now in .gitignore?

_Source: https://stackoverflow.com/questions/1274057/how-can-i-make-git-forget-about-a-file-that-was-tracked-but-is-now-in-gitign_

Step 1: Commit all your changes. Before proceeding, make sure all your changes are committed, including your . gitignore file.
Step 2: Remove everything from the repository. To clear your repository, use: 
```
git rm -r --cached .
```
- rm is the remove command
- -r will allow recursive removal
- –cached will only remove files from the index. Your files will still be there.

The rm command can be unforgiving. If you wish to try what it does beforehand, add the -n or --dry-run flag to test things out.

Step 3: Readd everything. 
```
git add .
```
Step 4: Commit. 
```
git commit -m ".gitignore fix"
```


## git status is showing "Changes not staged for commit" for files listed in .gitignore?

_Source: https://stackoverflow.com/questions/28101020/git-status-is-showing-changes-not-staged-for-commit-for-files-listed-in-gitig_

The .gitignore file doesn't mean what you think it means. [1]
In particular, once you have made a file "known" to git, in that it's in the index, adding that file's name to .gitignore has no effect. Git already tracks the file, and it will continue to track it.
In essence, the .gitignore file is not actually a list of files to ignore. Instead, when git comes across a case of an "untracked" file and is about to report it to you, the .gitignore contents are a list of names it should suppress.
For the .gitignore file itself you probably just want to git add the changes and commit them, since as a general rule, anyone cloning your repository probably wants to ignore the same set of untracked files, so .gitignore should be tracked and version-controlled.
For the XML file, however, it may be "generated content" that you don't want version-controlled, but you still want to keep it in the work-tree. This is a bit of a problem, because git is already tracking it and will insist on continuing to version-control the file.
What you can do at this point is remove it from git's index, but not from the work-tree:

```
git rm --cached <file_or_folder>
```


[1] (More seriously, everyone makes this mistake. Probably gitignore was the wrong name, and something like git-screen-away-untracked might have been better, if klunkier. However, listing a file in .gitignore has other side effects as well: specifically, it permits Git to clobber such files in some cases.)