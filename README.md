# Gym-Git-Exercise-Solutions
The gym git basics excericises

## Bundle 1

### Excercise 1

...bash

user@Emelyne1024 MINGW64 ~ (main)
$ mkdir gitexercise

user@Emelyne1024 MINGW64 ~ (main)
$ cd gitexercise

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ cd ..

user@Emelyne1024 MINGW64 ~ (main)
$ cd gitexercise

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git init
Initialized empty Git repository in C:/Users/user/gitexercise/.git/

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ code gitexercise

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ code gitexercise

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ code gitexercise

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ echo >index.html

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ echo >style.css

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ echo >file.txt

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ ls
file.txt  gitexercise  index.html  style.css

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git branch -m main master

user@Emelyne1024 MINGW64 ~/gitexercise (master)
$ git branch -m master main

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git add .
warning: in the working copy of 'file.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'style.css', LF will be replaced by CRLF the next time Git touches it

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file.txt
        new file:   gitexercise
        new file:   index.html
        new file:   style.css


user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git commit -m "Initial commit of 3 files"
[main (root-commit) 8311be9] Initial commit of 3 files
 4 files changed, 3 insertions(+)
 create mode 100644 file.txt
 create mode 100644 gitexercise
 create mode 100644 index.html
 create mode 100644 style.css

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git remote add origin "https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git"

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git remote -v
origin  https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git (push)
user@Emelyne1024 MINGW64 ~/gitexercise (main)
$git pull origin main --rebase
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 903 bytes | 100.00 KiB/s, done.
From https://github.com/Emelyne749/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
Successfully rebased and updated refs/heads/main.

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 366 bytes | 366.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
   115d770..10f7f7e  main -> main
branch 'main' set up to track 'origin/main'.

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ code README.md
user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git branch dev

user@Emelyne1024 MINGW64 ~/gitexercise (main)
$ git checkout dev
M       README.md
Switched to branch 'dev'

user@Emelyne1024 MINGW64 ~/gitexercise (dev)
$ git branch test

user@Emelyne1024 MINGW64 ~/gitexercise (dev)
$ git checkout test
M       README.md
Switched to branch 'test'

user@Emelyne1024 MINGW64 ~/gitexercise (test)
$ git checkout dev
M       README.md
Switched to branch 'dev'

user@Emelyne1024 MINGW64 ~/gitexercise (dev)
$ git branch -d test
Deleted branch test (was 10f7f7e)
...

### Excercise 2

...bash

C:\Users\user\gitexercise [main ≡ +1 ~0 -0 !]> echo "<h1>Home Page</h1>" > home.html
C:\Users\user\gitexercise [main ≡ +2 ~0 -0 !]> git add home.html
C:\Users\user\gitexercise [main ≡ +1 ~0 -0 | +1 ~0 -0 !]> git stash
Saved working directory and index state WIP on main: 8a66fa5 Submitting readme file contsining Bundle1 Excercise 1
C:\Users\user\gitexercise [main ≡]> echo "<h1>Home Page</h1>" > about.html
C:\Users\user\gitexercise [main ≡ +1 ~0 -0 !]> git add about.html
C:\Users\user\gitexercise [main ≡ +1 ~0 -0 ~]> git stash -m "about"
Saved working directory and index state On main: about
C:\Users\user\gitexercise [main ≡]> echo "<h1>Home Page</h1>" > team.html
C:\Users\user\gitexercise [main ≡ +1 ~0 -0 !]> git add team.html   
C:\Users\user\gitexercise [main ≡ +1 ~0 -0 ~]> git stash -m "team" 
Saved working directory and index state On main: team
C:\Users\user\gitexercise [main ≡]> git stash list
stash@{0}: On main: team
stash@{1}: On main: about
stash@{2}: WIP on main: 8a66fa5 Submitting readme file contsining Bundle1 Excercise 1
stash@{3}: WIP on main: 8a66fa5 Submitting readme file contsining Bundle1 Excercise 1
C:\Users\user\gitexercise [main ≡]> git stash pop "stash@{1}"             
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (c2dca7a928adab4dc52bc9ae0c7b9846d8c8b6b9)
:\Users\user\gitexercise [main ≡ +1 ~0 -0 ~]> git stash pop "stash@{2}"
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
        modified:   index.html

Dropped stash@{2} (63f417793a1932819ded6359392bb27aa84bdcc9)
C:\Users\user\gitexercise [main ≡ +2 ~1 -0 | +0 ~1 -0 !]> git add .
C:\Users\user\gitexercise [main ≡ +2 ~1 -0 | +0 ~1 -0 !]> git add .
C:\Users\user\gitexercise [main ≡ +2 ~1 -3 ~]> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   about.html
        deleted:    file.txt
        new file:   home.html
        deleted:    index.html
        deleted:    style.css

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

C:\Users\user\gitexercise [main ≡ +2 ~1 -3 | +0 ~1 -0 !]> git add .
C:\Users\user\gitexercise [main ≡ +2 ~1 -3 ~]> git commit -m "Commiting excercise 2 current change"
[main a4c5889] Commiting excercise 2 current change
 6 files changed, 48 insertions(+), 4 deletions(-)
 create mode 100644 about.html
 delete mode 100644 file.txt
 create mode 100644 home.html
 delete mode 100644 index.html
 delete mode 100644 style.css
C:\Users\user\gitexercise [main ↑1]> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.29 KiB | 1.29 MiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
   8a66fa5..a4c5889  main -> main
C:\Users\user\gitexercise [main ≡]> git  stash list
stash@{0}: On main: team
stash@{1}: WIP on main: 8a66fa5 Submitting readme file contsining Bundle1 Excercise 1
C:\Users\user\gitexercise [main ≡]> git stash pop "stash@{0}"
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (1e54a8e182534727a9374cc5275b7a528a6d5188)
C:\Users\user\gitexercise [main ≡ +1 ~0 -0 ~]> git reset --hard
HEAD is now at a4c5889 Commiting excercise 2 current change

...

## Bundle 2
### Excercise 1

...bash
C:\Users\user\gitexercise [main ≡]> git branch ft/bundle-2
C:\Users\user\gitexercise [main ≡ +0 ~1 -0 !]> git checkout ft/bundle-2
M       README.md
Switched to branch 'ft/bundle-2'
C:\Users\user\gitexercise [ft/bundle-2 +0 ~1 -0 !]> git merge main
Already up to date.
C:\Users\user\gitexercise [ft/bundle-2 +0 ~1 -0 !]> echo "<h1>service Page</h1>" > services.html 
C:\Users\user\gitexercise [ft/bundle-2 +1 ~1 -0 !]> git add services.html
C:\Users\user\gitexercise [ft/bundle-2 +1 ~0 -0 | +0 ~1 -0 !]> git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   services.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

C:\Users\user\gitexercise [ft/bundle-2 +1 ~0 -0 | +0 ~1 -0 !]> git commit -m "adding a new services page"
[ft/bundle-2 65afa0e] adding a new services page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 services.html
C:\Users\user\gitexercise [ft/bundle-2 +0 ~1 -0 !]> git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 513 bytes | 36.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Emelyne749/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

 ...

 ### Excercise 2

...bash

// I accidentally deleted my history, of the previous activities.

C:\Users\user\gitexercise [main|MERGING ≡ +0 ~0 -0 !2 | +1 ~0 -1 !1 !]> git difftool main ft/service-redesign

Viewing (1/2): 'README.md'
Launch 'vscode' [Y/n]? y

Viewing (2/2): 'services.html'
Launch 'vscode' [Y/n]? y
C:\Users\user\gitexercise [main ≡]> git add services.html 
C:\Users\user\gitexercise [main ≡]> git commit -m "services updated to resolve conflict"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
C:\Users\user\gitexercise [main ≡]> git push
Everything up-to-date
C:\Users\user\gitexercise [main ≡]> git merge ft/service-redesign       

...

## Bundle 3
### Excercise 1

...bash

C:\Users\user\Desktop\gitexercise [main ≡]> git branch ft/team-page  
C:\Users\user\Desktop\gitexercise [main ≡]> git checkout ft/team-page
Switched to branch 'ft/team-page'
C:\Users\user\Desktop\gitexercise [ft/team-page]> git add team.html
C:\Users\user\Desktop\gitexercise [ft/team-page +1 ~0 -0 ~]> git commit -u origin ft/team-page
error: pathspec 'origin' did not match any file(s) known to git
error: pathspec 'ft/team-page' did not match any file(s) known to git
C:\Users\user\Desktop\gitexercise [ft/team-page +1 ~0 -0 ~]> git commit -m "Created a new page called team.html"
[ft/team-page 8d2851d] Created a new page called team.html
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
C:\Users\user\Desktop\gitexercise [ft/team-page]> git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

C:\Users\user\Desktop\gitexercise [ft/team-page]> git push -u origin ft/team-page  
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 451 bytes | 451.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Emelyne749/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
C:\Users\user\Desktop\gitexercise [ft/team-page ≡]> git checkout main        
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
C:\Users\user\Desktop\gitexercise [main ≡]> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
C:\Users\user\Desktop\gitexercise [ft/contact-page]> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
C:\Users\user\Desktop\gitexercise [ft/team-page ≡]> git log
commit 8d2851d0031f9764a2ab5f374b4c6801143815b1 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Emelyne1024 <emelyneishimwe749@gmail.com>
Date:   Mon Aug 4 08:22:27 2025 +0200

    Created a new page called team.html

commit 47be825ceb54aacdeb101e7fc031273ca545ff06 (origin/main, origin/HEAD, main, ft/contact-page)
Author: Emelyne1024 <emelyneishimwe749@gmail.com>
Date:   Thu Jul 31 13:58:03 2025 +0200

     Updated readme file with bundle 2 excercise 2

commit 9ba0d66221d761617a704d9ed2fb90c30421c3c5
Merge: 6f3930d db93993
Author: Emelyne1024 <emelyneishimwe749@gmail.com>
Date:   Thu Jul 31 13:27:06 2025 +0200

C:\Users\user\Desktop\gitexercise [ft/team-page ≡]> git checkout ft/contact-page   
Switched to branch 'ft/contact-page'
C:\Users\user\Desktop\gitexercise [ft/contact-page]> git cherry-pick 8d2851d0031f9764a2ab5f374b4c6801143815b1
[ft/contact-page afecadf] Created a new page called team.html
 Date: Mon Aug 4 08:22:27 2025 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
C:\Users\user\Desktop\gitexercise [ft/contact-page]> git add contact.html
C:\Users\user\Desktop\gitexercise [ft/contact-page +1 ~0 -0 ~]> git commit -m "added a new page called contact"
[ft/contact-page 3e97bee] added a new page called contact
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html
C:\Users\user\Desktop\gitexercise [ft/contact-page]> git push -u origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 731 bytes | 243.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Emelyne749/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
C:\Users\user\Desktop\gitexercise [ft/contact-page ≡]> git checkout ft/faq-page    
error: pathspec 'ft/faq-page' did not match any file(s) known to git
C:\Users\user\Desktop\gitexercise [ft/contact-page ≡]> git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
C:\Users\user\Desktop\gitexercise [ft/faq-page]> git add faq.html
C:\Users\user\Desktop\gitexercise [ft/faq-page +1 ~0 -0 ~]> git commit -m "added a new page called faq.html"
[ft/faq-page 36698cc] added a new page called faq.html
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
C:\Users\user\Desktop\gitexercise [ft/faq-page]> git push -u origin ft/faq-page    
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 450 bytes | 450.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Emelyne749/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
C:\Users\user\Desktop\gitexercise [ft/faq-page ≡]> git revert 8d2851d0031f9764a2ab5f374b4c6801143815b1
[ft/faq-page 0e88926] Revert "Created a new page called team.html"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html
C:\Users\user\Desktop\gitexercise [ft/faq-page ↑1]> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 292 bytes | 292.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Emelyne749/Gym-Git-Exercise-Solutions.git
   36698cc..0e88926  ft/faq-page -> ft/faq-page
C:\Users\user\Desktop\gitexercise [ft/faq-page ≡]> git checkout main           
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

...
