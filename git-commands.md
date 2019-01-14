# Git-Commands

Tutorials:

http://rogerdudler.github.io/git-guide/

https://www.atlassian.com/git/tutorials/undoing-changes/git-revert

https://education.github.com/git-cheat-sheet-education.pdf


Pushing to Repo and Adding a Remote Origin

<pre>
git add * - for all files to add to stage
git commit -m “commit message” - to add files to heads 
git remote add origin ssh://johnmark@192.168.11.111/git/ilcdwebsite.git  - adding a remote repo to your local repo (master and other branches). Later you can now use origin to push commit to your remote repo
git push -u origin master - pushing commits to repo in master branch, -u will provide username and password

git checkout ‘branch name’ - is to change your location to your different branches in local
</pre>
Note: master is the development branch, and Branches is for versioning
<pre>
git push origin 

Creating branch to remote repo
git checkout -b “branch name”
git push origin “branch name”
</pre>
<pre>
Deleting unwanted files/folder
git rm -r “file/folder”
git commit -m “message”
git push origin “branch name”  - since we already added a remote origin, we can just use origin instead a “ssh:// chu chu” as our remote.
</pre>
<pre>
git checkout master
git pull - to update state to the latest remote master state
git merge develop - to bring changes to local master from your develop branch git
git push origin master - push current head to remote master branch
</pre>

Update your branch when the original branch from official repository has been updated
<pre>
git fetch [name_of_your_remote]
Then you need to apply to merge changes, if your branch is derivated from develop you need to do 
git merge [name_of_your_remote]/develop
Delete a branch on your local filesystem
git branch -d [name_of_your_new_branch]
Force Delete
git branch -D [name_of_your_new_branch]
Delete the branch on github
git push origin :[name_of_your_new_branch]
</pre>


Note: Before you take a push to the remote repository, you must update your local branch using the remote master branch. So that you can proceed to changes and push your commits master branch/branches.

