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

##Bundle 3

### Exercise 1

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        teams.html

nothing added to commit but untracked files present (use "git add" to track)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git commit -m"Added Teams file"
[ft/team-page d686204] Added Teams file
 1 file changed, 11 insertions(+)
 create mode 100644 teams.html

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git push origin
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 447 bytes | 447.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap/pull/new/ft/team-page
remote:
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
 * [new branch]      ft/team-page -> ft/team-page

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git checkot main
git: 'checkot' is not a git command. See 'git --help'.

The most similar command is
        checkout

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git chechout -b ft/contact-page
git: 'chechout' is not a git command. See 'git --help'.

The most similar command is
        checkout

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/team-page)
$ git log
commit d686204388606447b87f80ba315001f3e38217e1 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Fri Jul 28 11:04:07 2023 +0200

    Added Teams file

commit c5265d9eef70733dba709f4cd2ed78c28a916742 (origin/main, main, ft/contact-page)
Merge: 081c385 296ff68
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Thu Jul 27 11:26:54 2023 +0200

    merged changes of services file between two branches

commit 081c385218fbd18c278a4c79ab07d7966464d906
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Thu Jul 27 11:16:42 2023 +0200

    modified a services file

commit 296ff68abc79779dd7a4bad9b35cc26a6a58a033 (origin/ft/service-redesign, ft/service-redesign)
:...skipping...
commit d686204388606447b87f80ba315001f3e38217e1 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Fri Jul 28 11:04:07 2023 +0200

    Added Teams file

commit c5265d9eef70733dba709f4cd2ed78c28a916742 (origin/main, main, ft/contact-page)
Merge: 081c385 296ff68
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Thu Jul 27 11:26:54 2023 +0200

    merged changes of services file between two branches

commit 081c385218fbd18c278a4c79ab07d7966464d906
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Thu Jul 27 11:16:42 2023 +0200

    modified a services file

commit 296ff68abc79779dd7a4bad9b35cc26a6a58a033 (origin/ft/service-redesign, ft/service-redesign)
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Thu Jul 27 11:10:53 2023 +0200

    modified a file

commit b7285fa8cee929149ef151be22753c79bfb17099
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Thu Jul 27 11:06:52 2023 +0200

```
```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/faq-page)
$ git log
commit af113f00194278d9dcdaf3d3140f80d33d1d1629 (HEAD -> ft/faq-page)
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Fri Jul 28 11:32:41 2023 +0200

    Revert "Added Teams file"

    This reverts commit d686204388606447b87f80ba315001f3e38217e1.

commit 948aa96755628261d84d94af59a368aecf892160 (origin/ft/faq-page)
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Fri Jul 28 11:30:41 2023 +0200

    Added faq file.
```
```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/faq-page)
$ git push origin ft/faq-page)
bash: syntax error near unexpected token `)'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 272 bytes | 272.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
   948aa96..af113f0  ft/faq-page -> ft/faq-page

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/faq-page)
$
```
