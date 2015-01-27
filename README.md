# Exercises for various topics

## Git exercises

Thanks for @szhajdu!

### Exercise 1

1. Create a local Git repository.
2. Create a README file.
3. The README you created should appear as an untracked file.
4. Add the new file to the staging area.
5. Commit the contents of the staging area.
6. Create a src directory and add a couple of files to it.
7. Add the directory, not the individual files. See how both files have been staged. Commit them.
8. Make a change to one of the files. Check the different on the details of the change.
9. Next, add the changed file.
10. Make a couple more commits, at least one of which should add an extra file.
11. Delete a file.
12. Look at the status. Compare it to the status, after this, commit the deletion.
13. Now rename a file, for example, rename README to README.txt. How does the status look? Will you get the right outcome if you were to commit at this point? (Answer: almost certainly not, so don’t.)

### Exercise 2

1. Create a new branch and switch to it.
2. Make a couple of commits in the branch – perhaps adding a new file and/or editing existing ones.
3. Checkout the master branch again. Merge your branch in to it. Look for information about it having been a fast-forward merge. Look at git log, and see that there is no merge commit.
4. Switch back to your branch. Make a couple more commits.
5. Switch back to master. Make a commit there, which should edit a different file from the ones you touched in your branch – to be sure there is no conflict.
6. Now merge your branch again. (Aside: you don’t need to do anything to inform Git that you only want to merge things added since your previous merge.)
7. Once again, checkout your branch. Make a couple of commits.
8. Return to your master branch. Make a commit there that changes the exact same line, or lines, as commits in your branch did.
9. Now try to merge your branch. You should get a conflict.
10. Open the file(s) that is in conflict. Search for the conflict marker. Edit the file to remove the conflict markers and resolve the conflict.
11. Now try to commit. Notice that Git will not allow you to do this when you still have potentially unresolved conflicts.
12. Add the files that you have resolved conflicts in to the staging area. Then commit the merge commit.
13. Create a situation where one branch has changed a file, but the other branch has deleted it. What happens when you try to merge? How will you resolve it?
14. Delete everything but your .git directory, then do a checkout, to prove to yourself that this really will restore all of you current working copy.

### Exercise 3

1. Create a public repository using their Bitbucket/GitHub account.
2. You should then follow the instructions from Bitbucket/GitHub to add a remote, and then push their repository.
3. You should now make a local commit, then push it.
4. Now create a README.txt file on Bitbucket/GitHub and commit it.
5. You should now make a commit locally, and race to push it. To keep things simple, be sure to edit different files. What happens to the runner-up?
6. The runner-up should now pull.
7. Now edit the README.txt and commit it on Bitbucket/GitHub.
8. Now edit the same line in the README.txt and commit it locally (without pull). Race to push.
9. When the runner-up does a pull, they should get a merge conflict.
10. Look at the file in conflict, and resolve it.
11. Add to stage the fix, and then use commit to make the merge commit. Notice how this procedure is exactly the one you got used to when resolving conflicts in branches.

### Exercise 4
1. Create a branch. Make a commit.
2. Now switch back to your master branch. Make a (non-conflicting) commit there also.
3. Now switch back to your branch.
4. Use the rebase command in your branch.
5. Make one more commit in your branch.
6. Return to master. Merge your branch. Notice how, thanks to the rebase, this is a fastforward merge.
7. Push a commit to the central repository.
8. Make a commit locally yourself also. Note that you should not have pulled their commit at this point.
9. Try to push, and watch it fail.
10. Now, pull but using the --rebase flag.
11. Notice that your commit is the latest one, even though temporally the other member of your team made their commit afterwards. Why is this?
