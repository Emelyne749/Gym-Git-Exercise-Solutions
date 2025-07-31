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

