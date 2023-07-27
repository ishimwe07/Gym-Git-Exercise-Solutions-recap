# Git Exercises

## Bundle 1

### Exercise 1

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap
$ git init
Initialized empty Git repository in C:/Users/hp/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/.git/

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (master)
$ git branch -m master main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git commit -m"Added an index.html file"
[main (root-commit) f66d885] Added an index.html file
 1 file changed, 11 insertions(+)
 create mode 100644 index.html

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git remote add origin https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 383 bytes | 191.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout -b dev
Switched to a new branch 'dev'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (dev)
$ git checkout -b test
Switched to a new branch 'test'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (test)
$ git checkout dev
Switched to branch 'dev'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (dev)
$ git branch --delete test
Deleted branch test (was f66d885).

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (dev)
$ git branch -a
* dev
  main
  remotes/origin/main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (dev)
```

### Exercise 2

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash
Saved working directory and index state WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash
Saved working directory and index state WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash
Saved working directory and index state WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash list
stash@{0}: WIP on main: 2c8b0b2 Added a readMe
stash@{1}: WIP on main: 2c8b0b2 Added a readMe
stash@{2}: WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (967cc7d26e6bf9a0884e92047547c5db50e923a4)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped stash@{0} (7fc0af0e28b59a2ee980397c8facbe3c2f18e4a3)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{0} (7ee3541091e305c7612ab93c019dde6cca9fb065)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash home.html
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'home.html'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash "home.html"
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'home.html'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash
Saved working directory and index state WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash list
stash@{0}: WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash
Saved working directory and index state WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash list
stash@{0}: WIP on main: 2c8b0b2 Added a readMe
stash@{1}: WIP on main: 2c8b0b2 Added a readMe

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{1} (832ca2320d7a29fcbad0a2f4a4a226722abfd48e)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git commit "Added some 3 pages"
error: pathspec 'Added some 3 pages' did not match any file(s) known to git

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git commit -m"Added some 3 pages"
[main 75328d2] Added some 3 pages
 3 files changed, 33 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 team.html

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 627 bytes | 627.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
   2c8b0b2..75328d2  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   teamPage.html

Dropped stash@{0} (dc01930acea552a2bbaa8ea55c1b04841c04c697)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git reset teamPage.html

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        teamPage.html

nothing added to commit but untracked files present (use "git add" to track)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$

```

##Bundle 2

### Exercise 2

```bash
hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout -b  ft/service-redesign
Switched to a new branch 'ft/service-redesign'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git commit -m"modified a file"
[ft/service-redesign 296ff68] modified a file
 1 file changed, 3 insertions(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git push origin  ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 109.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap/pull/new/ft/service-redesign
remote:
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git commit -m"modified a services file"
[main 081c385] modified a services file
 1 file changed, 3 insertions(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 348 bytes | 348.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
   b7285fa..081c385  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git diff

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git diff main ft/service-redesign
diff --git a/services.html b/services.html
index aea62c2..482d322 100644
--- a/services.html
+++ b/services.html
@@ -8,7 +8,7 @@
 <body>
     <h1>Services Page</h1>
     <ul>
-        <li>All Items We Have</li>
+        <li>Item 1</li>
     </ul>
 </body>
 </html>
\ No newline at end of file

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main|MERGING)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main|MERGING)
$ git commit -m"merged changes of services file between two branches"
[main c5265d9] merged changes of services file between two branches

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 394 bytes | 394.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
   081c385..c5265d9  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$
```
