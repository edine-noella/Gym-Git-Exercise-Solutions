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

## Bundle 2

### Exercise 1

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/bundle-2)
$ touch services.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/bundle-2)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/bundle-2)
$ git commit -m "added our services"
[ft/bundle-2 757662f] added our services
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 438 bytes | 438.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/bundle-2
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

```

### Exercise 2

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git pull
remote: Enumerating objects: 2, done.
remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 1.74 KiB | 296.00 KiB/s, done.
From https://github.com/edine-noella/Git-practice-project1
   3276ce4..2e4beb0  main       -> origin/main
Updating 3276ce4..2e4beb0
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 12 ++++++++++++
 3 files changed, 34 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git commit -m "added a list of services"
[ft/service-redesign 666d88f] added a list of services
 1 file changed, 8 insertions(+), 1 deletion(-)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 345 bytes | 345.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/service-redesign
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git commit -m "added Objects of list to our services"
[main 78b8f5a] added Objects of list to our services
 1 file changed, 4 insertions(+)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 343 bytes | 343.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/edine-noella/Git-practice-project1.git
   2e4beb0..78b8f5a  main -> main

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git diff

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git branch
  dev
  ft/bundle-2
* ft/service-redesign
  main

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git diff

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git diff main
diff --git a/services.html b/services.html
index e792658..d371bf9 100644
--- a/services.html
+++ b/services.html
@@ -7,28 +7,13 @@
 </head>
 <body>
     <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
-    <h1>Services Page</h1>
-    <h1>Forgot to add reviewers</h1>
+
+    <ul>
+        <li>Service 1</li>
+        <li>Service 2</li>
+        <li>Service 3</li>
+        <li>Service 4</li>
+    </ul>
+
 </body>
 </html>
\ No newline at end of file

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign|MERGING)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign|MERGING)
$ git commit -m "resolved merge conflicts"
[ft/service-redesign aa01bfa] resolved merge conflicts

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 366 bytes | 366.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/edine-noella/Git-practice-project1.git
   666d88f..aa01bfa  ft/service-redesign -> ft/service-redesign

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/service-redesign)
$

```