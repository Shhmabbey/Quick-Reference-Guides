git feature branch workflow
feature/new-feture used as example branch name

git checkout main
git fetch origin
git reset --hard origin/main

The above lines switch the repo to the main branch, fetch all remote branches and reset the repo's local copy of main to match the latest version from origin.
(WARNING: be sure that you don't have any uncommitted changes you want to keep before issuing the following command): git reset --hard origin/main

git checkout -b feature/new-feture

This checks out a branch called feature/new-feature based on main (locally), and the -b flag tells Git to create the branch if it doesn’t already exist.

git status
git add
git commit -m "Add commit message"
git push -u origin feature/new-feture

The -u flag adds it as a remote tracking branch

Create a pull request on Github
Merge the  pull request (feature) into the stable projecton Github

git checkout main
git pull
git push



Other Notable Git Commands and Tips
 git pull = git fetch + git merge
 git pull origin feature/new-feture
    - If you do a git pull with a remote branch name, it will fetch the remote branch and then merge it into your current local branch




How To Rename a Local and Remote Git Branch
1.  Switch to branch you want to rename:
    git checkout <old_name>
2. Rename the local branch:
    git branch -m <new_name>
3. Push the <new_name> local branch and reset the upstream branch:
    git push origin -u <new_name>
4. Delete the <old_name> remote branch:
    git push origin --delete <old_name>

NOTE: Renaming a local Git Branch is a matter of running a single command. However, you can’t directly rename a remote branch; you need to push the renamed local branch and delete the branch with the old name.
