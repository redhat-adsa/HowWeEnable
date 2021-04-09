# Advanced Git

## Pull Request Reviews

It is a best practice to have at least one other person review all pull requests when code is pushed into a repository. This ensures that we are following [Linus's Law](https://en.wikipedia.org/wiki/Linus%27s_law) which states "given enough eyeballs, all bugs are shallow".

The process to review code is nearly the same with all git services, since we are using github for this training we will show how to do it here.

1. Click the **Pull Request* tab and then from the **Pull Request** page, choose the pull request you would like to review.

   Example:

   ![addimage](images/select_pr.png)

2. Click **Files Changed** in the center (1 in example below), and then **AFTER** you have reviewed all of the files, click **Review Changes** on the right (2 in example below).

   Example:

   ![addimage](images/review_changes.png)

3. If there is something you would like to change, you can add a comment for changes to the individual who submitted the pull request by clicking the plus next to the code you want to change.

   Example:

   ![hovercomment](images/hover-comment-icon.gif)

4. Even better than just commenting, you can also suggest a change so they can easily review the proposed change as it will highlight the code with the desired change by clicking the insert suggestion button.

   Example:

   ![sugestion block](images/suggestion-block.png)

## Rebase

Rebasing is the process of moving or combining a sequence of commits to a new base commit. Rebasing is most used to fix a bug in the main branch and makes sure you have a clean history of changes which can be visualized as the following:

![image](images/rebase.svg)

_Note:_ You should not rebase in public repositories as it will look like some of the history disappear.

The most common use of rebase is if you have gotten behind the upstream main branch in a remote feature branch. Before trying to commit for a PR make sure to `git rebase main --interactive`

## Git Log

`git log` shows the commit history for the repository. This is helpful if you need to revert to previous commits or if you want to take a look at the history to see where a change was made.

1. ```git history```

   Output:

   ```shell
   commit 65c309341aacf50e280383d394c48f0b009547ad
   Author: user <user@user.com>
   Date:   Mon Apr 5 08:11:56 2021 -0500
   ```

2. Lets get the output in a cleaner format that illustrates branches with `git log --oneline --graph`:

   ```shell
   git log --oneline --graph
   |\  
   | * 22a7493 fixed linting in README.md
   | * d12416f added more content and created file structure for more workshops
   | * d47de7b added practice scenarios section as WIP
   |/  
   *   ec09034 Merge pull request #3 from chadhellyea/fleshout
   |\  
   | * 756e040 fixed linting issues
   | * 96ae557 built out skeleton for enablement workshop
   | * b49996a updated readme and started strategy
   |/  
   * cb8413e Update README.md

## Git Reset

If you are working on a branch and you want to reset it to the last commit you can do so with `git reset`.

1. First we will create a file:

   ```shell
   touch reset.txt
   ```

2. Add the file to git with `git commit`

   ```shell
   git add reset.txt
   ```

3. Check status with `git status` and look at the changes to be committed section:

   ```shell
   Changes to be committed:
     (use "git restore --staged <file>..." to unstage)
           new file:   reset.txt
    ```

4. Do a `git reset` to revert back to previous commit, remember this will revert all changes you have made since last commit.

   ```shell
   git reset
   Untracked files:
     (use "git add <file>..." to include in what will be committed)
           reset.txt
    ```

5. Now you can perform a `git pull` to get latest upstream changes.

   ```shell
   git pull
   Updating ac4d849..6098c98
   Fast-forward
   reset.txt        | 10 +++++-----
   ```

## Git Diff

Git diff is a way to see what is changed between two branches. You can target specific files or the entire branch.

1. Let's create a file called `test_diff.txt`, commit it and make a change so we can see the differences:

   ```shell
   echo "this is a git diff test example" > test_diff.txt
   git commit -am 'commiting test_diff'
   git push origin main
   echo "test diff example" > test_diff.txt
   ```

2. Now run a `git diff` on the recently created file:

   ```shell
   git diff test_diff.txt
   ```

   Output:

   ```shell
   diff --git a/test_diff.txt b/test_diff.txt
   --- a/test_diff.txt
   +++ b/test_diff.txt
   @@ -1 +1 @@
   -this is a git diff test example
   +test diff example
   ```

### What does each part of the `git diff` mean?

1. ```diff --git a/test_diff.txt b/test_diff.txt```

   This line shows the files git found differences in.

2. ```shell
   --- a/test_diff.txt
   +++ b/test_diff.txt
   ```

   These lines above show which marker denotes which file ie `-` is for `a/test_diff.txt` and `+` is for `b/test_diff.txt`.

   Example:

   ```shell
   @@ -1 +1 @@
   -this is a git diff test example
   +test diff example
   ```

## Git Stash

`Git stash` saves uncommitted changes for later and reverts to last commit so you can switch branches and work on other things.

1. ```shell
   git stash
   ```

   Output:

   ```shell
   On branch git102
   Your branch is up to date with 'origin/git102'.

   Changes not staged for commit:
     (use "git add <file>..." to update what will be committed)
     (use "git restore <file>..." to discard changes in working directory)
          modified:   workshops/git_101/03-advanced.md
   ```

2. In order to restore your session `git stash apply`

   ```shell
   git stash apply
   ```

   Output:

   ```shell
   On branch git102
   Your branch is up to date with 'origin/git102'.

   Changes not staged for commit:
     (use "git add/rm <file>..." to update what will be committed)
     (use "git restore <file>..." to discard changes in working directory)
           modified:   workshops/git_101/03-advanced.md
   ```

   _Note:_ `git stash` will not store files that have not been added with `git add`.

## Branching Strategies

There are many different strategies for branching code, however the feature branch strategy has become the standard in Open Source. This is also referred to as [GitHub Flow](https://guides.github.com/introduction/flow/).

For in depth information on all strategies, Martin Fowler has a great blog on it [here.](https://martinfowler.com/articles/branching-patterns.html)

---

[Merge Conflicts](04-merge-conflicts.md)
