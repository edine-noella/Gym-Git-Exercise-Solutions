# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1
$ git init
Initialized empty Git repository in C:/Users/ghzno/Documents/the Gym/Git-practice-project1/.git/

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (master)
$ git branch -M main

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git commit -m "first commit"
[main (root-commit) 3276ce4] first commit
 2 files changed, 13 insertions(+)
 create mode 100644 index.html
 create mode 100644 main.js

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git remote add origin https://github.com/edine-noella/Git-practice-project1.git

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 503 bytes | 251.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout -b dev
Switched to a new branch 'dev'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git checkout -b test
Switched to a new branch 'test'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (test)
$ git checkout dev
Switched to branch 'dev'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git branch -d test
Deleted branch test (was 3276ce4).

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git branch
* dev
  main
```

### Exercise 2

```bash

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ touch home.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash
Saved working directory and index state WIP on dev: e3f0917 restored eveything

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ touch about.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash
Saved working directory and index state WIP on dev: e3f0917 restored eveything

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ touch team.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash
Saved working directory and index state WIP on dev: e3f0917 restored eveything

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash list
stash@{0}: WIP on dev: e3f0917 restored eveything
stash@{1}: WIP on dev: e3f0917 restored eveything
stash@{2}: WIP on dev: e3f0917 restored eveything

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped refs/stash@{1} (31a6144c47927082bbcf6427552a550303c183b3)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git add about.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (942c27116b05670335b79d051a465144be7d6f39)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git branch
* dev
  main

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git commit -m "home and about pages"
[dev b4c6cae] home and about pages
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git push --set-upstream origin dev
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (11/11), 1.31 KiB | 448.00 KiB/s, done.
Total 11 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/dev
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash list
stash@{0}: WIP on dev: e3f0917 restored eveything

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git stash pop 0
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (c54690a736c7f92013a0be6c12feee808d1a4602)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git reset --hard
HEAD is now at b4c6cae home and about pages

```