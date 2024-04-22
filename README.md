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
$ touch main.js

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ touch subMain.js

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ ls
main.js  subMain.js

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ ls
index.html  main.js

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        main.js

nothing added to commit but untracked files present (use "git add" to track)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git commit -m "first commit"
[main (root-commit) 3276ce4] first commit
 2 files changed, 13 insertions(+)
 create mode 100644 index.html
 create mode 100644 main.js

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git status
On branch main
nothing to commit, working tree clean

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