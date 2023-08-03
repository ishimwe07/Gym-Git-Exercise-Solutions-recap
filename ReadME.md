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

## Bundle 3 
### Exercise 2

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git commit -m"Added a parag on home page."
[main 2a3f50d] Added a parag on home page.
 1 file changed, 1 insertion(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 335 bytes | 335.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
   5f0a9c3..2a3f50d  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git log
commit 2a3f50d3ebee066999408f99937442c7d3a6a5ec (HEAD -> main, origin/main)
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Mon Jul 31 11:05:59 2023 +0200

    Added a parag on home page.

commit 5f0a9c381e6f9067aee0e689535f89fbccb3ed24
Merge: 1f48b74 3adc771
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Mon Jul 31 10:58:12 2023 +0200

    Merge branch 'main' of https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap

commit 1f48b74010052154fc485b18e42b261391588353
Author: Ishimwe <ishimwgabby@gmail.com>
Date:   Mon Jul 31 10:57:37 2023 +0200

    Added a paragraph on home page.

commit 3adc771e160f534ed67c3d04e19b8b4ddc393c06
Author: ISHIMWE Gabby <81089765+ishimwe07@users.noreply.github.com>
Date:   Fri Jul 28 11:38:29 2023 +0200

    Update ReadME.md

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git rebase 2a3f50d3ebee066999408f99937442c7d3a6a5ec
Successfully rebased and updated refs/heads/ft/home-page-redesign.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
nothing to commit, working tree clean

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git commit -m"Added new content on the page"
[ft/home-page-redesign f0b9381] Added new content on the page
 1 file changed, 1 insertion(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.47 KiB | 754.00 KiB/s, done.
Total 14 (delta 8), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (8/8), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap/pull/new/ft/home-page-redesign
remote:
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$

```

## Bundle 4

### Exercise 1

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git remote add git-copy https://github.com/ishimwe07/gym-git-exercise-solutions-recap-new.git

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git commit -m"Duplicated some paragaraphs on the home page."
[main 1c13f0d] Duplicated some paragaraphs on the home page.
 1 file changed, 6 insertions(+)


hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push
Enumerating objects: 9, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 613 bytes | 204.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
   0a908d9..51b19c4  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git push git-copy main
Enumerating objects: 55, done.
Counting objects: 100% (55/55), done.
Delta compression using up to 4 threads
Compressing objects: 100% (54/54), done.
Writing objects: 100% (55/55), 10.24 KiB | 499.00 KiB/s, done.
Total 55 (delta 29), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (29/29), done.
To https://github.com/ishimwe07/gym-git-exercise-solutions-recap-new.git
 * [new branch]      main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$

```

## Bundle 4

### Exercise 2

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/footer)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/footer)
$ git commit -m"Added a list on the team page"
[ft/footer 9497aa8] Added a list on the team page
 1 file changed, 4 insertions(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/footer)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/footer)
$ git commit -m"Updated a list of teams on the team page"
[ft/footer 7be6bad] Updated a list of teams on the team page
 1 file changed, 6 insertions(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/footer)
$ git push origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 754 bytes | 377.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap/pull/new/ft/footer
remote:
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
 * [new branch]      ft/footer -> ft/footer


hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$ git merge --squash ft/footer)
bash: syntax error near unexpected token `)'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$ git merge --squash ft/footer
Updating 51b19c4..7be6bad
Fast-forward
Squash commit -- not updating HEAD
 team.html | 10 ++++++++++
 1 file changed, 10 insertions(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$ git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   team.html


hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$ git commit -m"footer changes squashing"
[ft/squashing 0dfddd3] footer changes squashing
 1 file changed, 10 insertions(+)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$ git push origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 501 bytes | 250.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap/pull/new/ft/squashing
remote:
To https://github.com/ishimwe07/Gym-Git-Exercise-Solutions-recap.git
 * [new branch]      ft/squashing -> ft/squashing

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$
```
## Bundle 5

### Exerise 1
```bash
All clear, pages are being displayed.
```

### Exersise 2
```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (ft/squashing)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git clone https://github.com/ishimwe07/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 93
Receiving objects: 100% (107/107), 1.95 MiB | 202.00 KiB/s, done.
Resolving deltas: 100% (5/5), done.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ git cd git-cafe-exercise
git: 'cd' is not a git command. See 'git --help'.

The most similar command is
        add

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap (main)
$ cd git-cafe-exercise

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git commit -m"Changed Welcome to our place to Welcome to our restaurant in index.html"
[main 4665ce3] Changed Welcome to our place to Welcome to our restaurant in index.html
 1 file changed, 1 insertion(+), 1 deletion(-)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 352 bytes | 352.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishimwe07/git-cafe-exercise.git
   d1d3f9c..4665ce3  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$

```

## Bundle 6

### Exercise 1

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git checkout -b ft-bundle-6-Exer-1
Switched to a new branch 'ft-bundle-6-Exer-1'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git status
On branch ft-bundle-6-Exer-1
nothing to commit, working tree clean

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git status
On branch ft-bundle-6-Exer-1
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        menu.html

nothing added to commit but untracked files present (use "git add" to track)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git add .
g
hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git commit -m"added a menu page"
[ft-bundle-6-Exer-1 dd02ad6] added a menu page
 1 file changed, 14 insertions(+)
 create mode 100644 menu.html

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git push
fatal: The current branch ft-bundle-6-Exer-1 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft-bundle-6-Exer-1

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git remote -v
origin  https://github.com/ishimwe07/git-cafe-exercise.git (fetch)
origin  https://github.com/ishimwe07/git-cafe-exercise.git (push)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git push origin ft-bundle-6-Exer-1
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 455 bytes | 227.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft-bundle-6-Exer-1' on GitHub by visiting:
remote:      https://github.com/ishimwe07/git-cafe-exercise/pull/new/ft-bundle-6-Exer-1
remote:
To https://github.com/ishimwe07/git-cafe-exercise.git
 * [new branch]      ft-bundle-6-Exer-1 -> ft-bundle-6-Exer-1

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$
```
## Bundle 6

### Exercise 2
```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (ft-bundle-6-Exer-1)
$ git checkout -b bug-fix-branch
Switched to a new branch 'bug-fix-branch'

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (bug-fix-branch)
$ git status
On branch bug-fix-branch
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    index-4.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Contact.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (bug-fix-branch)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (bug-fix-branch)
$ git commit -m"Changed the title of the index-4.html file to “Contact”"
[bug-fix-branch 1156c47] Changed the title of the index-4.html file to “Contact”
 1 file changed, 203 insertions(+), 203 deletions(-)
 rename index-4.html => Contact.html (97%)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (bug-fix-branch)
$ git push origin bug-fix-branch
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 2.52 KiB | 2.52 MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'bug-fix-branch' on GitHub by visiting:
remote:      https://github.com/ishimwe07/git-cafe-exercise/pull/new/bug-fix-branch
remote:
To https://github.com/ishimwe07/git-cafe-exercise.git
 * [new branch]      bug-fix-branch -> bug-fix-branch

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-rec
```

## Bundle 6

### Exercise 3

```bash

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (bug-fix-branch)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index-4.html

no changes added to commit (use "git add" and/or "git commit -a")

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git add .

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git commit -m"Changed the telephone on the index-4.html page from +1 800 603 6035 to +1 800 659 6035"
[main 598978b] Changed the telephone on the index-4.html page from +1 800 603 6035 to +1 800 659 6035
 1 file changed, 1 insertion(+), 1 deletion(-)

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 337 bytes | 337.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishimwe07/git-cafe-exercise.git
   4665ce3..598978b  main -> main

hp@DESKTOP-IQUI18G MINGW64 ~/Desktop/The Gym/Exercises/Gym-Git-Exercise-Solutions-recap/git-cafe-exercise (main)
$
```
