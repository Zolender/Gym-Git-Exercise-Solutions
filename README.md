### Bundle 1

## Exercise 1
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git init
Reinitialized existing Git repository in C:/Users/Eben/OneDrive - MSFT/Desktop/The Gym curriculum/Git learning/git basics/Exercises/.git/
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
* main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch -m main master
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
* master
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch -m master main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"first commit"
[main a9f7997] first commit
 2 files changed, 12 insertions(+)
 create mode 100644 index.html
 create mode 100644 styles.css
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 467 bytes | 93.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Zolender/Exercises.git
   a468aa8..a9f7997  main -> main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c dev
Switched to a new branch 'dev'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
* dev
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c test
Switched to a new branch 'test'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch dev
Switched to branch 'dev'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch -d test
Deleted branch test (was a9f7997).
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
* dev
  main
```

## Exercise 2

```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash 
Saved working directory and index state WIP on dev: ba19dec Add the basics files index.html and styles.css in the repository
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\about.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash 
Saved working directory and index state WIP on dev: ba19dec Add the basics files index.html and styles.css in the repository
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash
Saved working directory and index state WIP on dev: ba19dec Add the basics files index.html and styles.css in the repository
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash list
stash@{0}: WIP on dev: ba19dec Add the basics files index.html and styles.css in the repository
stash@{1}: WIP on dev: ba19dec Add the basics files index.html and styles.css in the repository
stash@{2}: WIP on dev: ba19dec Add the basics files index.html and styles.css in the repository
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash pop "stash@{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (33ca98ec5ee98108c94b9a4c73500c9f7ff8979e)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash pop "stash@{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (6298019209a19a80df6b8fffcaaa69e18f986c1f)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\about.html .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"Save the about and home pages"
[dev 0e75b64] Save the about and home pages
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin dev
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 970 bytes | 121.00 KiB/s, done.
Total 8 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/dev
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      dev -> dev
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (d12c7aa43587ca51783308510ef0766b504dff1c)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git reset --hard
HEAD is now at 0e75b64 Save the about and home pages
```

### Bundle 2

## Exercise 1
```bash
     git switch -c ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\services.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"create a services page"
[ft/bundle-2 a9327af] create a services page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 451 bytes | 112.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/bundle-2
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```
## Exercise 2
```bash PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git pull origin main
From https://github.com/Zolender/Exercises
 * branch            main       -> FETCH_HEAD
Updating a9f7997..d322785
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 11 +++++++++++
 3 files changed, 33 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\services.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"modify the services page"
[ft/service-redesign f4cff1e] modify the services page
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 327 bytes | 163.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/service-redesign
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\services.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"add new services to the service page
>> "
[main 2e7ec72] add new services to the service page
 1 file changed, 5 insertions(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 358.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Zolender/Exercises.git
   d322785..2e7ec72  main -> main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\services.html                      
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"change the main title of the services page"
[main 3b7cbf0] change the main title of the services page
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin main                         
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 359 bytes | 359.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Zolender/Exercises.git
   2e7ec72..3b7cbf0  main -> main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
  dev
  ft/bundle-2
* ft/service-redesign
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git diff main ft/service-redesign
diff --git a/services.html b/services.html
index 7247d25..ed773cc 100644
--- a/services.html
+++ b/services.html
@@ -6,11 +6,6 @@
     <title>Document</title>
 </head>
 <body>
-    <h1>Hello Dear Customer. Here is a list of the services we provide</h1>
-    <ol>
-        <li>Cooking</li>
-        <li>Laundry</li>
-        <li>Massage</li>
-    </ol>
+    <h1>Hey dearest. Here are the services our company offer</h1>
 </body>
 </html>
\ No newline at end of file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"merge the changes from main to this branch"
On branch ft/service-redesign
nothing to commit, working tree clean
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"merge the changes from main to this branch"
On branch ft/service-redesign
nothing to commit, working tree clean
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push
Everything up-to-date
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/service-redesign 
Switched to branch 'ft/service-redesign'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 237 bytes | 237.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Zolender/Exercises.git
   f4cff1e..e8c2953  ft/service-redesign -> ft/service-redesign
```

### Bundle 3
## Exercise 1

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"create a team page"
[ft/team-page 581ae69] create a team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 439 bytes | 146.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/team-page
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/team-page -> ft/team-page
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log --oneline
581ae69 (HEAD -> ft/team-page, origin/ft/team-page) create a team page
3b7cbf0 (origin/main, origin/HEAD, main, ft/contact-page) change the main title of the services page
2e7ec72 add new services to the service page
d322785 Merge pull request #1 from Zolender/ft/bundle-2
a9327af (origin/ft/bundle-2, ft/bundle-2) create a services page
0e75b64 (origin/dev, dev) Save the about and home pages
ba19dec Add the basics files index.html and styles.css in the repository
a9f7997 first commit
a468aa8 clean up the repository
cc9b523 Merge branch 'main' of https://github.com/Zolender/Exercises First merge operation.
2400df8 Initial commit
54f02eb Initializing the repository adding two files(simple website), renaming the branch to master
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git cherry-pick 581ae69                      
[ft/contact-page 4ce43e2] create a team page
 Date: Sun Aug 31 07:35:16 2025 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"add new changes to the team page"
[ft/contact-page b6d2b4a] add new changes to the team page
 1 file changed, 6 insertions(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 728 bytes | 728.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/contact-page
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
  dev
  ft/bundle-2
* ft/contact-page
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c ft/faq-page
Switched to a new branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\faq.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"create a frequently asked questions page"
[ft/faq-page ca37faa] create a frequently asked questions page
 1 file changed, 15 insertions(+)
 create mode 100644 faq.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 526 bytes | 526.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/faq-page
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log ft/team-page
commit 581ae692e9e6da60fce733092f57b363e2e14a15 (origin/ft/team-page, ft/team-page)
Author: Zolender <ndeingare@gmail.com>
Date:   Sun Aug 31 07:35:16 2025 +0200

    create a team page

commit 3b7cbf0b6d973d86f0cca8871343522b90e3683e (origin/main, origin/HEAD, main)
Author: Zolender <ndeingare@gmail.com>
Date:   Sun Aug 31 07:10:17 2025 +0200

    change the main title of the services page

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
  dev
  ft/bundle-2
  ft/contact-page
* ft/faq-page
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert 581ae692e9e6da60fce733092f57b363e2e14a15
CONFLICT (modify/delete): team.html deleted in parent of 581ae69 (create a team page) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 581ae69... create a team page
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
team.html: needs merge
error: you need to resolve your current index first
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert --abort
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page
Switched to branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"update the team page"
[ft/team-page a3aed40] update the team page
 1 file changed, 6 insertions(+), 2 deletions(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page
Switched to branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log ft/team-page
commit a3aed406eb22df04012c28a7458bbb21a8e9849c (ft/team-page)
Author: Zolender <ndeingare@gmail.com>
Date:   Sun Aug 31 07:59:00 2025 +0200

    update the team page

commit 581ae692e9e6da60fce733092f57b363e2e14a15 (origin/ft/team-page)
Author: Zolender <ndeingare@gmail.com>
Date:   Sun Aug 31 07:35:16 2025 +0200

    create a team page

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
  dev
  ft/bundle-2
  ft/contact-page
* ft/faq-page
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert 581ae692e9e6da60fce733092f57b363e2e14a15
CONFLICT (modify/delete): team.html deleted in parent of 581ae69 (create a team page) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 581ae69... create a team page
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert --abort
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"update the team page"
[ft/faq-page 636d844] update the team page
 1 file changed, 1 insertion(+), 2 deletions(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert 581ae692e9e6da60fce733092f57b363e2e14a15
CONFLICT (modify/delete): team.html deleted in parent of 581ae69 (create a team page) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 581ae69... create a team page
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert --abort
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page                     
Switched to branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Already on 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page 
Switched to branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page 
error: Your local changes to the following files would be overwritten by checkout:
        team.html
Please commit your changes or stash them before you switch branches.
Aborting
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
M       team.html
Already on 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\team.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"update the team page"
[ft/team-page 6b07c2d] update the team page
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page 
Switched to branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log ft/team-page 
commit 6b07c2d94f6e9946bdab668d29549929c760dc8b (ft/team-page)
Author: Zolender <ndeingare@gmail.com>
Date:   Sun Aug 31 08:06:44 2025 +0200

    update the team page

commit a3aed406eb22df04012c28a7458bbb21a8e9849c
Author: Zolender <ndeingare@gmail.com>
Date:   Sun Aug 31 07:59:00 2025 +0200

    update the team page

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log --oneline
636d844 (HEAD -> ft/faq-page) update the team page
ca37faa (origin/ft/faq-page) create a frequently asked questions page
b6d2b4a (origin/ft/contact-page, ft/contact-page) add new changes to the team page
4ce43e2 create a team page
3b7cbf0 (origin/main, origin/HEAD, main) change the main title of the services page
2e7ec72 add new services to the service page
d322785 Merge pull request #1 from Zolender/ft/bundle-2
a9327af (origin/ft/bundle-2, ft/bundle-2) create a services page
0e75b64 (origin/dev, dev) Save the about and home pages
ba19dec Add the basics files index.html and styles.css in the repository
a9f7997 first commit
a468aa8 clean up the repository
cc9b523 Merge branch 'main' of https://github.com/Zolender/Exercises First merge operation.
2400df8 Initial commit
54f02eb Initializing the repository adding two files(simple website), renaming the branch to master
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log --oneline
6b07c2d (HEAD -> ft/team-page) update the team page
a3aed40 update the team page
581ae69 (origin/ft/team-page) create a team page
3b7cbf0 (origin/main, origin/HEAD, main) change the main title of the services page
2e7ec72 add new services to the service page
d322785 Merge pull request #1 from Zolender/ft/bundle-2
a9327af (origin/ft/bundle-2, ft/bundle-2) create a services page
0e75b64 (origin/dev, dev) Save the about and home pages
ba19dec Add the basics files index.html and styles.css in the repository
a9f7997 first commit
a468aa8 clean up the repository
cc9b523 Merge branch 'main' of https://github.com/Zolender/Exercises First merge operation.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/faq-page 
Switched to branch 'ft/faq-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert 581ae69
CONFLICT (modify/delete): team.html deleted in parent of 581ae69 (create a team page) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 581ae69... create a team page
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert 6b07c2d
error: Reverting is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: revert failed
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert --abort
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git revert 6b07c2d
[ft/faq-page 14a6785] Revert "update the team page"
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/faq-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 617 bytes | 205.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/Zolender/Exercises.git
   ca37faa..14a6785  ft/faq-page -> ft/faq-page
```

## Exercise 2
```bash
 git branch
  dev
  ft/bundle-2
  ft/contact-page
* ft/faq-page
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"update the home page
>> "
[main 259ec50] update the home page
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 370 bytes | 370.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Zolender/Exercises.git
   3b7cbf0..259ec50  main -> main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"update the home page"
[ft/home-page-redesign 58ca20f] update the home page
 1 file changed, 1 insertion(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/home-page-redesign
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 4 threads
Compressing objects: 100% (18/18), done.
Writing objects: 100% (18/18), 2.00 KiB | 93.00 KiB/s, done.
Total 18 (delta 10), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (10/10), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/home-page-redesign
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
```

### Bundle 4

## Exercise 1

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git remote add git-copy https://github.com/Zolender/Exercise2.git
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git remote -v
git-copy        https://github.com/Zolender/Exercise2.git (fetch)
git-copy        https://github.com/Zolender/Exercise2.git (push)
origin  https://github.com/Zolender/Exercises.git (fetch)
origin  https://github.com/Zolender/Exercises.git (push)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"updated the home page"
[main 40cd25a] updated the home page
 1 file changed, 1 insertion(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 373 bytes | 373.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Zolender/Exercises.git
   259ec50..40cd25a  main -> main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push git-copy main
Enumerating objects: 36, done.
Counting objects: 100% (36/36), done.
Delta compression using up to 4 threads
Compressing objects: 100% (32/32), done.
Writing objects: 100% (36/36), 5.75 KiB | 190.00 KiB/s, done.
Total 36 (delta 11), reused 9 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (11/11), done.
To https://github.com/Zolender/Exercise2.git
 * [new branch]      main -> main
```