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

The git init command creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository. Most other Git commands are not available outside of an initialized repository, so this is usually the first command you'll run in a new project.

```
git init
git config --list
git config --global user.name "Your name"
git config --global user.email "Your email"
```

[Init](https://github.com/git-guides/git-init)

3. Help

Use documentation and git community.
If you are having trouble remembering commands or options for commands, you can use Git help.
```
git help
git help show
git help add
```

4. Add changes

Create text files, add content.

When in doubt, run git status. This is always a good idea. The git status command only outputs information, it won't modify commits or changes in your local repository.


```
git status
git add <file>
```

You can also use . to add all changes at once.
```
git add .
```

[Status](https://github.com/git-guides/git-status)
[Add](https://github.com/git-guides/git-add)
[Staging](https://git-scm.com/about/staging-area)

5. Commit changes

Commit your changes.

git commit creates a commit, which is like a snapshot of your repository. These commits are snapshots of your entire repository at specific times. You should make new commits often, based around logical units of change.

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

Instead of copying files from directory to directory, Git stores a branch as a reference to a commit. In this sense, a branch represents the tip of a series of commits—it's not a container for commits.

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

[Branches](https://www.atlassian.com/git/tutorials/using-branches)

7. HEAD

Use git log and find your HEAD in the current state.
Use git checkout to move switch to another branch.

A head is simply a reference to a commit object. Each head has a name (branch name, tag name, etc). A repository can contain any number of heads. At any given time, one head is selected as the “current head”. This head is aliased to HEAD, always in capitals.

Note this difference: a “head” (lowercase) refers to any one of the named heads in the repository; “HEAD” (uppercase) refers exclusively to the currently active head. This distinction is used frequently in Git documentation.

8. Cherry-picking

Commit a change to the wrong branch.
Switch to the correct branch and cherry-pick the commit to where it should belong.

git cherry-pick is a powerful command that enables arbitrary Git commits to be picked by reference and appended to the current working HEAD.

```
git cherry-pick <commit hash>
```

[Cherry-pick](https://www.atlassian.com/git/tutorials/cherry-pick)

9. Reset changes

Add faulty commit. Reset it.

The git reset command is a complex and versatile tool for undoing changes.

```
git reset HEAD^
```

You can reset HEAD using relative references or specify a commit.

```
git reset HEAD^
git reset HEAD~2
git reset <commit hash>
```

[Reset](https://www.atlassian.com/git/tutorials/undoing-changes/git-reset)

10. Amend changes

Make a change and stage it.
You can use amend to add this change to the previous commit.

The git commit --amend command is a convenient way to modify the most recent commit. It lets you combine staged changes with the previous commit instead of creating an entirely new commit.

```
git commit --amend
```

[Commit --amend](https://www.atlassian.com/git/tutorials/rewriting-history)

11. Stashing

Make a change and hide it.

```
git stash
git stash pop
```

git stash temporarily shelves (or stashes) changes you've made to your working copy so you can work on something else, and then come back and re-apply them later on. Stashing is handy if you need to quickly switch context and work on something else, but you're mid-way through a code change and aren't quite ready to commit.

[Stash](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)

12. Merging

Merge branches to the main branch.

```
git merge new-branch
```

[Merge](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)

13. gitignore*

A gitignore file specifies intentionally untracked files that Git should ignore.
Files already tracked by Git are not affected.

Create .gitignore file and add files you don't want to track with git.

[gitgnore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

14. rebase*

Rebasing is the process of moving or combining a sequence of commits to a new base commit.

```
git rebase <branch name>
git rebase -i HEAD~2
```

[Rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)
Check [Playground](https://learngitbranching.js.org) lesson level move2.

### Homework

1. Play around with Git by yourself. It is a powerful tool and is a must for every engineer.
There are plenty of features and in many cases there are multiple ways to solve the same problem.
Git is not scary! Be brave, use Git!
2. Do lessons from the [Playground](https://learngitbranching.js.org)
3. Create account in GitHub
4. Push the projects you've done or you are working on to GitHub repositories!
