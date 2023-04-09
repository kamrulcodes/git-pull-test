# git-pull-test
Git test - Checking git pull effects on local files  

`$ git init`  
Initialized empty Git repository in /home/kamrul/Projects/git-pull-test/.git/  

`$ git remote add origin git@github.com:kamrulcodes/git-pull-test.git`  

`$ touch 'A file to stage.txt' 'A file not to stage.txt'`  

`$ git add 'A file to stage.txt'`  

`$ git commit -m 'Initial Commit.'`  
[main (root-commit) 8f89afb] Initial Commit.  
 1 file changed, 0 insertions(+), 0 deletions(-)  
 create mode 100644 A file to stage.txt  

`$ git push`  
fatal: The current branch main has no upstream branch.  
To push the current branch and set the remote as upstream, use  

    `git push --set-upstream origin main`  

`$ git push --set-upstream origin main`  
To github.com:kamrulcodes/git-pull-test.git  
 ! [rejected]        main -> main (fetch first)  
error: failed to push some refs to 'github.com:kamrulcodes/git-pull-test.git'  
hint: Updates were rejected because the remote contains work that you do  
hint: not have locally. This is usually caused by another repository pushing  
hint: to the same ref. You may want to first integrate the remote changes  
hint: (e.g., 'git pull ...') before pushing again.  
hint: See the 'Note about fast-forwards' in 'git push --help' for details.  

**There is a read me file there. I should not have created that file in github to keep the test simple. Let's delete the readme file and the innitial commit from github.com and try again - to keep things simple.**

**Oops! There is no way to delete commit from github.com.**

**Note:** I am keeping this test result here for later understanding and going to create another git test [git-pull-test-1](https://github.com/kamrulcodes/git-pull-test-1.git).  

`$ git pull`  
remote: Enumerating objects: 6, done.  
remote: Counting objects: 100% (6/6), done.  
remote: Compressing objects: 100% (4/4), done.  
remote: Total 6 (delta 1), reused 0 (delta 0), pack-reused 0  
Unpacking objects: 100% (6/6), 1.91 KiB | 392.00 KiB/s, done.  
From github.com:kamrulcodes/git-pull-test  
 * [new branch]      main       -> origin/main  
There is no tracking information for the current branch. 👈️  
Please specify which branch you want to merge with. 👈️  
See git-pull(1) for details.  

    git pull <remote> <branch>  

If you wish to set tracking information for this branch you can do so with:  

    git branch --set-upstream-to=origin/<branch> main  

`$ git branch --set-upstream-to=origin/main`  
Branch 'main' set up to track remote branch 'main' from 'origin'.  


` $ git pull origin main --rebase`
From github.com:kamrulcodes/git-pull-test  
 * branch            main       -> FETCH_HEAD  
Successfully rebased and updated refs/heads/main.  

`$ git log`

`$ git push origin main`  
Enumerating objects: 4, done.  
Counting objects: 100% (4/4), done.  
Delta compression using up to 8 threads  
Compressing objects: 100% (2/2), done.  
Writing objects: 100% (3/3), 297 bytes | 297.00 KiB/s, done.  
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0  
To github.com:kamrulcodes/git-pull-test.git  
   436cf2b..fbcbe02  main -> main  

