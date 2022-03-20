# Git Workshop

 ### Links and resources:
 * [Playground](https://learngitbranching.js.org)
 * [Git Documentation](https://git-scm.com/about)
 * [GitHub guide](https://github.com/git-guides) or [BitBucket guide](https://www.atlassian.com/git/tutorials/setting-up-a-repository)

 ### Steps

1. Prerequisites
You should have git and a terminal (CLI).
On Windows, use the git bash cli that comes with git for Windows.
On macOS or Linux, the built-in one should be fine.
Verify that git is installed:
```
git version
```

2. Init and config
Create a directory, initialise a local git repository and configure git (check if e-mail is configured, otherwise, configure it).
```
git init
git config --list
git config --global user.name "Your name"
git config --global user.email "Your email"
```

3. Help
Use documentation and git community.
```
git help
git help show
git help add
```

4. Add changes
Create text files, add content.
```
git status
git add <file>
```

You can also use . to add all changes at once.
```
git add .
```
[Staging](https://git-scm.com/about/staging-area)

5. Commit changes
Commit your changes.
```
git commit -m "my first commit"
git log
git show
```
Make a change.
```
git diff
```

[Commit](https://github.com/git-guides/git-commit)

6. Branches
Create a branch, create a new file, commit the change.
Change back to previous branch, verify that the new file is not there.
Compare the git log on the branches.
```
git branch new-branch
git checkout new-branch
```

You can also use -b to create and checkout to a new branch with one command.
```
git checkout -b new-branch
```

Git log A DOG.
To get a visual representation of the commits and branches you have, use A DOG command.

```
git log --all --decorate --oneline --graph
```

7. HEAD
A head is simply a reference to a commit object. Each head has a name (branch name, tag name, etc). A repository can contain any number of heads. At any given time, one head is selected as the “current head”. This head is aliased to HEAD, always in capitals.

Note this difference: a “head” (lowercase) refers to any one of the named heads in the repository; “HEAD” (uppercase) refers exclusively to the currently active head. This distinction is used frequently in Git documentation.

Use git log and find your HEAD in the current state.
Use git checkout to move switch to another branch.

8. Cherry-picking
Commit a change to the wrong branch.
Switch to the correct branch and cherry-pick the commit to where it should belong.

```
git cherry-pick <commit hash>
```
[Cherry-pick](https://www.atlassian.com/git/tutorials/cherry-pick)

9. Reset changes
Add faulty commit. Reset it.

```
git reset HEAD^
```

You can reset HEAD using relative references or specify a commit.

```
git reset HEAD^
git reset HEAD~2
git reset <commit hash>
```

10. Amend changes
Make a change and stage it.
You can use amend to add this change to the previous commit.

```
git commit --amend
```

11. Stashing
Make a change and hide it.

```
git stash
git stash pop
```

12. Merging
Merge branches to the main branch.

```
git merge new-branch
```
[Merge](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)
