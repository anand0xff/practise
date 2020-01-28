# line-by-line explanation:

Developer D:
git checkout -b dev # create branch locally and switch to it
#DT created dev branch locally.

# added content to cmdline.txt
add, commit, then: git push origin dev  # git push <remote> <branch>

Developer A:
$ git pull origin dev   FAILED: 
        error: Your local changes to the following files would be overwritten by merge:
$ git checkout cmdline.txt  # re-fetch the repo's file
$ git pull origin dev  
A & D local are synched.

-------------
#git branch -[rla] helpful
 git branch --list
        * master
$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
$ gs
origin	https://github.com/anand0xff/practise.git (fetch)
origin	https://github.com/anand0xff/practise.git (push)
commit 2f4ed9a9bef163c4e645892ced86265a0e7acb45
Author: Developer D <devd@inst.org>
Date:   Tue Jan 28 10:04:12 2020 -0500

On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
-------------
$ git push origin dev

Developer D:
$ git pull origin dev

Branch dev on the local repo of D is in sync with the remote branch dev.
changed cmdline.txt, pushed to origin/dev

Developer A:
$ git diff dev origin/dev  # doesn't show differences
$ git fetch origin
$ git diff dev origin/dev  # shows differences
$ git merge  # merged the fetched changes to local dev file.

$ git branch --list
$ git checkout dev  # switch to branch dev

Developer A:
$ git checkout -b adev origin/dev  # create branch adev off <<origin>>/dev, switch to it
add stuff to adev; commit; push

<---

$ git checkout -b ddev origin/dev  # create branch ddev off branch <<origin>>/dev locally, switch to it
add stuff to bdev; commit; push


git rm tutorial.txt  # deleting a file locally and remotely...
git commit -m "delete tutorial"
git push