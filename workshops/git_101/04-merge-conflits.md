# Merge Conflicts

Merge conflicts happen when you or someone else edits the same file and tries to push into a remote branch. This is common when multiple people are working on the code base. A good way to make sure this does not happen is to `git pull origin main` often if you know others may be working on the same files.

`Note:` Main could be called master if it is an older repository.

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
           new file:   reset
    ```

4. Do a `git reset` to revert back to previous commit, remember this will revert all changes you have made since last commit.
