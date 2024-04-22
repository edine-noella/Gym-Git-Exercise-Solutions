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

## Bundle 3

### Exercise 1

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ touch team.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git commit -m "added the team page"
[ft/team-page 76a811c] added the team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 429 bytes | 429.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/team-page
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/team-page -> ft/team-page

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git log
commit 76a811c6b82cf59857af43a5a0327b788efe6316 (HEAD -> ft/team-page, origin/ft/team-page)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 15:49:27 2024 +0200

    added the team page

commit de131fda8de2b24732ff6742820068524a9d17cf (origin/main, main, ft/contact-page)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 15:24:16 2024 +0200

    added changes to our conflicts

commit 78b8f5a5a52349fee46a42444a517e830477624f
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 15:18:32 2024 +0200

    added Objects of list to our services

commit 2e4beb04108f652a2ea9326c48ca697f3c760d9b
Merge: e8a65d0 7891da4
Author: tuyishimehono <tuhonori1@gmail.com>
Date:   Mon Apr 22 14:59:51 2024 +0200

    Merge pull request #3 from edine-noella/ft/bundle-2

    Added our services

commit 7891da44f24fc94bf2bc1d37eed5f44022acedfd (origin/ft/bundle-2, ft/bundle-2)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 14:21:16 2024 +0200

    new branch

commit 757662f0e6f73be9a8939cc5fe1e6ed06b6f3ef4
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 13:42:22 2024 +0200

    added our services

commit e8a65d07c7f3b42451652dc0f4f9ec79da8ec331
Merge: 3276ce4 b4c6cae
Author: Mugisha Edine Noella <edinenoella@gmail.com>
Date:   Mon Apr 22 12:47:29 2024 +0200

    Merge pull request #1 from edine-noella/dev

    Dev

commit b4c6cae11c443faf935d2d4725e36ced08daaf1c (origin/dev, dev)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 12:40:34 2024 +0200

    home and about pages

commit e3f0917a5254b5dad1dac4204666fa1acacbf3b0
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 12:35:01 2024 +0200

    restored eveything

:
commit 76a811c6b82cf59857af43a5a0327b788efe6316 (HEAD -> ft/team-page, origin/ft/team-page)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 15:49:27 2024 +0200

    added the team page

commit de131fda8de2b24732ff6742820068524a9d17cf (origin/main, main, ft/contact-page)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 15:24:16 2024 +0200

    added changes to our conflicts

commit 78b8f5a5a52349fee46a42444a517e830477624f
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 15:18:32 2024 +0200

    added Objects of list to our services

commit 2e4beb04108f652a2ea9326c48ca697f3c760d9b
Merge: e8a65d0 7891da4
Author: tuyishimehono <tuhonori1@gmail.com>
Date:   Mon Apr 22 14:59:51 2024 +0200

    Merge pull request #3 from edine-noella/ft/bundle-2

    Added our services

commit 7891da44f24fc94bf2bc1d37eed5f44022acedfd (origin/ft/bundle-2, ft/bundle-2)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 14:21:16 2024 +0200

    new branch

commit 757662f0e6f73be9a8939cc5fe1e6ed06b6f3ef4
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 13:42:22 2024 +0200

    added our services

commit e8a65d07c7f3b42451652dc0f4f9ec79da8ec331
Merge: 3276ce4 b4c6cae
Author: Mugisha Edine Noella <edinenoella@gmail.com>
Date:   Mon Apr 22 12:47:29 2024 +0200

    Merge pull request #1 from edine-noella/dev

    Dev

commit b4c6cae11c443faf935d2d4725e36ced08daaf1c (origin/dev, dev)
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 12:40:34 2024 +0200

    home and about pages

commit e3f0917a5254b5dad1dac4204666fa1acacbf3b0
Author: edine-noella <edinenoella@gmail.com>
Date:   Mon Apr 22 12:35:01 2024 +0200

    restored eveything


Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git cherry-pick 76a811c6b82cf59857af43a5a0327b788efe6316
[ft/contact-page 498c21f] added the team page
 Date: Mon Apr 22 15:49:27 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git commit -m "contact page branch cherry pick the team page branch"
On branch ft/contact-page
nothing to commit, working tree clean

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 434 bytes | 434.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/contact-page
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/contact-page -> ft/contact-page

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git checkout ft/faq-page
error: pathspec 'ft/faq-page' did not match any file(s) known to git

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ touch faq.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git commit -m 'Added the FAQ page'
[ft/faq-page 9c9c6c7] Added the FAQ page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 431 bytes | 431.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/faq-page
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/faq-page -> ft/faq-page

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git revert 76a811c6b82cf59857af43a5a0327b788efe6316
[ft/faq-page 33bc7ca] Revert "added the team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git commit -m "reverted the added the team page commit"
On branch ft/faq-page
nothing to commit, working tree clean

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 270 bytes | 270.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/edine-noella/Git-practice-project1.git
   9c9c6c7..33bc7ca  ft/faq-page -> ft/faq-page

```

### Exercise 2

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git commit -m " bundle3 exericeses2 chaning main branch"
[main bfeb393]  bundle3 exericeses2 chaning main branch
 2 files changed, 1 insertion(+), 11 deletions(-)
 delete mode 100644 index.html

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 409 bytes | 409.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/edine-noella/Git-practice-project1.git
   de131fd..bfeb393  main -> main

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/home-page-redesign)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/home-page-redesign)
$ git commit -m "rebase main branch"
On branch ft/home-page-redesign
nothing to commit, working tree clean

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 924 bytes | 924.00 KiB/s, done.
Total 8 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/home-page-redesign
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

```

## Bundle 4

### Exercise 1

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git remote add git-copy https://github.com/edine-noella/Git-practice-project-2.git

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git remote -v
git-copy        https://github.com/edine-noella/Git-practice-project-2.git (fetch)
git-copy        https://github.com/edine-noella/Git-practice-project-2.git (push)
origin  https://github.com/edine-noella/Git-practice-project1.git (fetch)
origin  https://github.com/edine-noella/Git-practice-project1.git (push)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git commit -m "adde changes to the home page"
[main 34337bd] adde changes to the home page
 1 file changed, 4 insertions(+), 2 deletions(-)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 390 bytes | 390.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/edine-noella/Git-practice-project1.git
   bfeb393..34337bd  main -> main

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git push origin main
Everything up-to-date

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git push git-copy main
Enumerating objects: 35, done.
Counting objects: 100% (35/35), done.
Delta compression using up to 4 threads
Compressing objects: 100% (35/35), done.
Writing objects: 100% (35/35), 5.04 KiB | 860.00 KiB/s, done.
Total 35 (delta 17), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (17/17), done.
To https://github.com/edine-noella/Git-practice-project-2.git
 * [new branch]      main -> main

```

### Exercise 2

```bash
Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/footer)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/footer)
$ git commit -m "added address to home page"
[ft/footer b6b17c7] added address to home page
 1 file changed, 1 insertion(+)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/footer)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/footer)
$ git commit -m " added our phone number"
[ft/footer cd0d546]  added our phone number
 1 file changed, 1 insertion(+)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/footer)
$ git push origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 606 bytes | 606.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/footer
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/footer -> ft/footer

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/squashing)
$ git merge --squash ft/footer
Updating 34337bd..cd0d546
Fast-forward
Squash commit -- not updating HEAD
 home.html | 2 ++
 1 file changed, 2 insertions(+)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/squashing)
$ git add .

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/squashing)
$ git commit -m "footer changes squashing"
[ft/squashing 19f9868] footer changes squashing
 1 file changed, 2 insertions(+)

Edine@DESKTOP-DTASPUT MINGW64 ~/Documents/the Gym/Git-practice-project1 (ft/squashing)
$ git push origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 350 bytes | 350.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/edine-noella/Git-practice-project1/pull/new/ft/squashing
remote:
To https://github.com/edine-noella/Git-practice-project1.git
 * [new branch]      ft/squashing -> ft/squashing

```