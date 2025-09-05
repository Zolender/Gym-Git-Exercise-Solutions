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

## Exercise 2

```bash
git switch -c ft/footer
Switched to a new branch 'ft/footer'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"add a footer to the home page"
[ft/footer b192647] add a footer to the home page
 1 file changed, 3 insertions(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m"add more changes to the home page's footer"
[ft/footer b42968e] add more changes to the home page's footer
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
* ft/footer
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin footer
error: src refspec footer does not match any
error: failed to push some refs to 'https://github.com/Zolender/Exercises.git'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 649 bytes | 108.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/footer
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/footer -> ft/footer
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git switch -c ft/squashing
Switched to a new branch 'ft/squashing'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git merge --squash ft/footer
Updating 40cd25a..b42968e
Fast-forward
Squash commit -- not updating HEAD
 home.html | 3 +++
 1 file changed, 3 insertions(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git log --oneline
40cd25a (HEAD -> ft/squashing, origin/main, origin/HEAD, git-copy/main, main) updated the home page
259ec50 update the home page
3b7cbf0 change the main title of the services page
2e7ec72 add new services to the service page
d322785 Merge pull request #1 from Zolender/ft/bundle-2
a9327af (origin/ft/bundle-2, ft/bundle-2) create a services page
0e75b64 (origin/dev, dev) Save the about and home pages
ba19dec Add the basics files index.html and styles.css in the repository
a9f7997 first commit
a468aa8 clean up the repository
cc9b523 Merge branch 'main' of https://github.com/Zolender/Exercises First merge operation.
2400df8 Initial commit
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git add .\home.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit -m "add a footer to the home page"

[ft/squashing 5919388] add a footer to the home page
 1 file changed, 3 insertions(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git commit --amend -m"footer changes squashing"
[ft/squashing af8472d] footer changes squashing
 Date: Sun Aug 31 21:11:29 2025 +0200
 1 file changed, 3 insertions(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git branch 
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
  ft/footer
  ft/home-page-redesign
  ft/service-redesign
* ft/squashing
  ft/team-page
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git push origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 399 bytes | 133.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises/pull/new/ft/squashing
remote:
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/squashing -> ft/squashing
```

### Bundle 5

## Exercise 1
     - Done in Github

## Exercise 2
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git clone https://github.com/TheGymRwanda/git-cafe-exercise.git
To https://github.com/Zolender/Exercises.git
 * [new branch]      ft/squashing -> ft/squashing
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> git clone https://github.com/TheGymRwanda/git-cafe-exercise.git
-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 92 (from 1)
Receiving objects: 100% (107/107), 1.95 MiB | 2.70 MiB/s, done.
Resolving deltas: 100% (5/5), done.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises> cd .\git-cafe-exercise\
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git add .\index.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git commit -m"Updated the title of the index page"
[main 0ced733] Updated the title of the index page
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git push
remote: Permission to TheGymRwanda/git-cafe-exercise.git denied to Zolender.
fatal: unable to access 'https://github.com/TheGymRwanda/git-cafe-exercise.git/': The requested URL returned error: 403
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git switch -c ft/change-title
Switched to a new branch 'ft/change-title'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git log --oneline
0ced733 (HEAD -> ft/change-title, main) Updated the title of the index page
d1d3f9c (origin/main, origin/HEAD) Create README.md
659c868 first commit
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git push origin ft/change-title
remote: Permission to TheGymRwanda/git-cafe-exercise.git denied to Zolender.
fatal: unable to access 'https://github.com/TheGymRwanda/git-cafe-exercise.git/': The requested URL returned error: 403
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git push -u origin main    
remote: Permission to TheGymRwanda/git-cafe-exercise.git denied to Zolender.
fatal: unable to access 'https://github.com/TheGymRwanda/git-cafe-exercise.git/': The requested URL returned error: 403
```

### Bundle 6
## Exercise 1
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git switch -c ft/menu
Switched to a new branch 'ft/menu'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git add .\Menu.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git commit -m"create a new menu page"
[ft/menu b2b9dcb] create a new menu page
 1 file changed, 19 insertions(+)
 create mode 100644 Menu.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git status
On branch ft/menu
nothing to commit, working tree clean
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git push origin ft/menu    
remote: Permission to TheGymRwanda/git-cafe-exercise.git denied to Zolender.
fatal: unable to access 'https://github.com/TheGymRwanda/git-cafe-exercise.git/': The requested URL returned error: 403
```

## Exercise 2
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git switch -c bug-fix
Switched to a new branch 'bug-fix'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git add .\index-4.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git commit -m"change the index-4 page title from menu to Contact "
[bug-fix 549e784] change the index-4 page title from menu to Contact
 1 file changed, 1 insertion(+), 1 deletion(-)
 git push origin bug-fix
remote: Permission to TheGymRwanda/git-cafe-exercise.git denied to Zolender.
fatal: unable to access 'https://github.com/TheGymRwanda/git-cafe-exercise.git/': The requested URL returned error: 403
```

## Exercise 3
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git add .\index-4.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git commit -m"update the tel number"
[bug-fix 21e63ca] update the tel number
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\git basics\Exercises\git-cafe-exercise> git push origin bug-fix    
remote: Permission to TheGymRwanda/git-cafe-exercise.git denied to Zolender.
fatal: unable to access 'https://github.com/TheGymRwanda/git-cafe-exercise.git/': The requested URL returned error: 403
```







### Git Advanced Exercises: Part 1
## Missing File Fix
```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log
commit 298533a6b63fc71346ba983829bc452353429f46 (HEAD -> main)
Author: Zolender <ndeingare@gmail.com>
Date:   Tue Sep 2 07:47:43 2025 +0200

    chore: Create third file and fourth files

commit 991870dde64648c27a3b2e9be3bf3b0575ca330d
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
298533a (HEAD -> main) chore: Create third file and fourth files
991870d chore: Create another file
227e781 chore: Create initial file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\test4.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit --amend -m "Create thrid and fourth files"

[main 477dcc1] Create thrid and fourth files
 Date: Tue Sep 2 07:47:43 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
477dcc1 (HEAD -> main) Create thrid and fourth files
991870d chore: Create another file
227e781 chore: Create initial file
```


## Editing Commit History
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
477dcc1 (HEAD -> main) Create thrid and fourth files
991870d chore: Create another file
227e781 chore: Create initial file
git rebase -i HEAD~2
[detached HEAD fcf1a5d] chore: Create second file
 Date: Tue Sep 2 07:47:03 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
2342d2b (HEAD -> main) Create thrid and fourth files
fcf1a5d chore: Create second file
227e781 chore: Create initial file
```

## Keeping History Tidy
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rebase -i --root
[detached HEAD cf8886a] Create initial and Second file
 Date: Tue Sep 2 07:45:44 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
f36f6ec (HEAD -> main) Create thrid and fourth files
cf8886a Create initial and Second file
``` 

## Splitting a Commit
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
f36f6ec (HEAD -> main) Create thrid and fourth files
cf8886a Create initial and Second file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git reset HEAD~1
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\test3.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m "Create third file"
[main 3c7db25] Create third file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\test4.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m "Create fourth file"
[main 3481b7c] Create fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
3481b7c (HEAD -> main) Create fourth file
3c7db25 Create third file
cf8886a Create initial and Second file
```

## Advanced Squashing
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
3481b7c (HEAD -> main) Create fourth file
3c7db25 Create third file
cf8886a Create initial and Second file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rebase -i cf8886a
[detached HEAD ad65bde] Create third and fourth files
 Date: Tue Sep 2 10:07:25 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
ad65bde (HEAD -> main) Create third and fourth files
cf8886a Create initial and Second file
```
## Dropping a Commit
```bash
git add .\unwanted.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"Unwanted commit"
[main 16ddb8c] Unwanted commit
 1 file changed, 1 insertion(+)
 create mode 100644 unwanted.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
ad65bde (HEAD -> main) Create third and fourth files
cf8886a Create initial and Second file
```
## Reodering Commits
```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
ad65bde (HEAD -> main) Create third and fourth files
cf8886a Create initial and Second file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rebase -i --root
Successfully rebased and updated refs/heads/main.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
98fa211 (HEAD -> main) Create initial and Second file
9c06514 Create third and fourth files
```

## Cherry-picking Commits
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git switch -c ft/branch
Switched to a new branch 'ft/branch'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\test5.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m "Implemented test 5"
[ft/branch 5c8076c] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
5c8076c (HEAD -> ft/branch) Implemented test 5
98fa211 (main) Create initial and Second file
9c06514 Create third and fourth files
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch
* ft/branch
  main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git cherry-pick 5c8076c
[main 4bfcd4a] Implemented test 5
 Date: Tue Sep 2 10:27:28 2025 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
4bfcd4a (HEAD -> main) Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
```

## Visualizing Commit History
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --graph
* commit 4bfcd4a2ee0b67b630364564468a1ee7d058ba15 (HEAD -> main)
| Author: Zolender <ndeingare@gmail.com>
| Date:   Tue Sep 2 10:27:28 2025 +0200
|
|     Implemented test 5
|
* commit 98fa211818ec4511e2d9baab5b58ed70a3251a33
:...skipping...
* commit 4bfcd4a2ee0b67b630364564468a1ee7d058ba15 (HEAD -> main)
| Author: Zolender <ndeingare@gmail.com>
| Date:   Tue Sep 2 10:27:28 2025 +0200
| 
|     Implemented test 5
| 
* commit 98fa211818ec4511e2d9baab5b58ed70a3251a33
| Author: Zolender <ndeingare@gmail.com>
| Date:   Tue Sep 2 07:45:44 2025 +0200
| 
|     Create initial and Second file
| 
* commit 9c0651430113d463d54a8722b56e8320533266b3
  Author: Zolender <ndeingare@gmail.com>
  Date:   Tue Sep 2 10:07:25 2025 +0200
  
      Create third and fourth files

```

## Understanding Reflogs
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git reflog
4bfcd4a (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
98fa211 HEAD@{1}: checkout: moving from ft/branch to main
5c8076c (ft/branch) HEAD@{2}: commit: Implemented test 5
98fa211 HEAD@{3}: checkout: moving from main to ft/branch
98fa211 HEAD@{4}: rebase (finish): returning to refs/heads/main
98fa211 HEAD@{5}: rebase (pick): Create initial and Second file
9c06514 HEAD@{6}: rebase (pick): Create third and fourth files
:...skipping...
4bfcd4a (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
98fa211 HEAD@{1}: checkout: moving from ft/branch to main
5c8076c (ft/branch) HEAD@{2}: commit: Implemented test 5
98fa211 HEAD@{3}: checkout: moving from main to ft/branch
98fa211 HEAD@{4}: rebase (finish): returning to refs/heads/main
98fa211 HEAD@{5}: rebase (pick): Create initial and Second file
9c06514 HEAD@{6}: rebase (pick): Create third and fourth files
5e65bd8 HEAD@{7}: rebase (start): checkout 5e65bd80924ca797c7315a8a59ecee894af9d843
ad65bde HEAD@{8}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{9}: rebase: fast-forward
cf8886a HEAD@{10}: rebase: fast-forward
254629c HEAD@{11}: rebase (start): checkout 254629c77b51c568e8fa4164c06d1e5c71e9fd1e
ad65bde HEAD@{12}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{13}: rebase (start): checkout HEAD~1
16ddb8c HEAD@{14}: commit: Unwanted commit
ad65bde HEAD@{15}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{16}: rebase (squash): Create third and fourth files
3c7db25 HEAD@{17}: rebase (start): checkout cf8886a
3481b7c HEAD@{18}: commit: Create fourth file
3c7db25 HEAD@{19}: commit: Create third file
cf8886a HEAD@{20}: reset: moving to HEAD~1
f36f6ec HEAD@{21}: rebase (finish): returning to refs/heads/main
f36f6ec HEAD@{22}: rebase (pick): Create thrid and fourth files
cf8886a HEAD@{23}: rebase (squash): Create initial and Second file
227e781 HEAD@{24}: rebase: fast-forward
e0d6f5f HEAD@{25}: rebase (start): checkout e0d6f5f2ba5e3f539b8e13fdc9dc109fc953434c
2342d2b HEAD@{26}: rebase (abort): returning to refs/heads/main
2342d2b HEAD@{27}: rebase (abort): returning to refs/heads/main
2342d2b HEAD@{28}: rebase (finish): returning to refs/heads/main
2342d2b HEAD@{29}: rebase (start): checkout HEAD~2
2342d2b HEAD@{30}: rebase (finish): returning to refs/heads/main
2342d2b HEAD@{31}: rebase (pick): Create thrid and fourth files
fcf1a5d HEAD@{32}: rebase (reword): chore: Create second file
991870d HEAD@{33}: rebase: fast-forward
227e781 HEAD@{34}: rebase (start): checkout HEAD~2
e1f23ed HEAD@{35}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{36}: rebase (start): checkout HEAD
e1f23ed HEAD@{37}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{38}: rebase (start): checkout HEAD~1
e1f23ed HEAD@{39}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{40}: rebase (reword): Create thrid and fourth files
477dcc1 HEAD@{41}: rebase: fast-forward
991870d HEAD@{42}: rebase (start): checkout HEAD~1
477dcc1 HEAD@{43}: commit (amend): Create thrid and fourth files
298533a HEAD@{44}: commit: chore: Create third file and fourth files
991870d HEAD@{45}: commit: chore: Create another file
227e781 HEAD@{46}: commit (amend): chore: Create initial file
9ad0fa5 HEAD@{47}: commit (initial): chore: create initial file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git reflog --oneline
4bfcd4a (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
98fa211 HEAD@{1}: checkout: moving from ft/branch to main
5c8076c (ft/branch) HEAD@{2}: commit: Implemented test 5
98fa211 HEAD@{3}: checkout: moving from main to ft/branch
98fa211 HEAD@{4}: rebase (finish): returning to refs/heads/main
98fa211 HEAD@{5}: rebase (pick): Create initial and Second file
9c06514 HEAD@{6}: rebase (pick): Create third and fourth files
5e65bd8 HEAD@{7}: rebase (start): checkout 5e65bd80924ca797c7315a8a59ecee894af9d843
ad65bde HEAD@{8}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{9}: rebase: fast-forward
cf8886a HEAD@{10}: rebase: fast-forward
254629c HEAD@{11}: rebase (start): checkout 254629c77b51c568e8fa4164c06d1e5c71e9fd1e
ad65bde HEAD@{12}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{13}: rebase (start): checkout HEAD~1
16ddb8c HEAD@{14}: commit: Unwanted commit
ad65bde HEAD@{15}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{16}: rebase (squash): Create third and fourth files
3c7db25 HEAD@{17}: rebase (start): checkout cf8886a
3481b7c HEAD@{18}: commit: Create fourth file
3c7db25 HEAD@{19}: commit: Create third file
cf8886a HEAD@{20}: reset: moving to HEAD~1
f36f6ec HEAD@{21}: rebase (finish): returning to refs/heads/main
f36f6ec HEAD@{22}: rebase (pick): Create thrid and fourth files
cf8886a HEAD@{23}: rebase (squash): Create initial and Second file
227e781 HEAD@{24}: rebase: fast-forward
e0d6f5f HEAD@{25}: rebase (start): checkout e0d6f5f2ba5e3f539b8e13fdc9dc109fc953434c
2342d2b HEAD@{26}: rebase (abort): returning to refs/heads/main
2342d2b HEAD@{27}: rebase (abort): returning to refs/heads/main
2342d2b HEAD@{28}: rebase (finish): returning to refs/heads/main
2342d2b HEAD@{29}: rebase (start): checkout HEAD~2
2342d2b HEAD@{30}: rebase (finish): returning to refs/heads/main
2342d2b HEAD@{31}: rebase (pick): Create thrid and fourth files
fcf1a5d HEAD@{32}: rebase (reword): chore: Create second file
991870d HEAD@{33}: rebase: fast-forward
227e781 HEAD@{34}: rebase (start): checkout HEAD~2
e1f23ed HEAD@{35}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{36}: rebase (start): checkout HEAD
e1f23ed HEAD@{37}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{38}: rebase (start): checkout HEAD~1
e1f23ed HEAD@{39}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{40}: rebase (reword): Create thrid and fourth files
477dcc1 HEAD@{41}: rebase: fast-forward
991870d HEAD@{42}: rebase (start): checkout HEAD~1
477dcc1 HEAD@{43}: commit (amend): Create thrid and fourth files
298533a HEAD@{44}: commit: chore: Create third file and fourth files
991870d HEAD@{45}: commit: chore: Create another file
227e781 HEAD@{46}: commit (amend): chore: Create initial file
9ad0fa5 HEAD@{47}: commit (initial): chore: create initial file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git reflog show ft/branch
5c8076c (ft/branch) ft/branch@{0}: commit: Implemented test 5
98fa211 ft/branch@{1}: branch: Created from HEAD
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git reflog --all
4bfcd4a (HEAD -> main) refs/heads/main@{0}: cherry-pick: Implemented test 5
4bfcd4a (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
98fa211 HEAD@{1}: checkout: moving from ft/branch to main
5c8076c (ft/branch) refs/heads/ft/branch@{0}: commit: Implemented test 5
5c8076c (ft/branch) HEAD@{2}: commit: Implemented test 5
98fa211 refs/heads/ft/branch@{1}: branch: Created from HEAD
98fa211 HEAD@{3}: checkout: moving from main to ft/branch
98fa211 refs/heads/main@{1}: rebase (finish): refs/heads/main onto 5e65bd80924ca797c7315a8a59ecee894af9d843
98fa211 HEAD@{4}: rebase (finish): returning to refs/heads/main
98fa211 HEAD@{5}: rebase (pick): Create initial and Second file
9c06514 HEAD@{6}: rebase (pick): Create third and fourth files
5e65bd8 HEAD@{7}: rebase (start): checkout 5e65bd80924ca797c7315a8a59ecee894af9d843
ad65bde HEAD@{8}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{9}: rebase: fast-forward
cf8886a HEAD@{10}: rebase: fast-forward
254629c HEAD@{11}: rebase (start): checkout 254629c77b51c568e8fa4164c06d1e5c71e9fd1e
ad65bde refs/heads/main@{2}: rebase (finish): refs/heads/main onto ad65bdee7118fcd35416ad05411e4fb81c341201
ad65bde HEAD@{12}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{13}: rebase (start): checkout HEAD~1
16ddb8c refs/heads/main@{3}: commit: Unwanted commit
16ddb8c HEAD@{14}: commit: Unwanted commit
ad65bde refs/heads/main@{4}: rebase (finish): refs/heads/main onto cf8886a8652e7d02524f78a6505419c53bb2c9d3
ad65bde HEAD@{15}: rebase (finish): returning to refs/heads/main
ad65bde HEAD@{16}: rebase (squash): Create third and fourth files
3c7db25 HEAD@{17}: rebase (start): checkout cf8886a
3481b7c refs/heads/main@{5}: commit: Create fourth file
3481b7c HEAD@{18}: commit: Create fourth file
3c7db25 refs/heads/main@{6}: commit: Create third file
3c7db25 HEAD@{19}: commit: Create third file
cf8886a refs/heads/main@{7}: reset: moving to HEAD~1
cf8886a HEAD@{20}: reset: moving to HEAD~1
f36f6ec refs/heads/main@{8}: rebase (finish): refs/heads/main onto e0d6f5f2ba5e3f539b8e13fdc9dc109fc953434c
f36f6ec HEAD@{21}: rebase (finish): returning to refs/heads/main
f36f6ec HEAD@{22}: rebase (pick): Create thrid and fourth files
cf8886a HEAD@{23}: rebase (squash): Create initial and Second file
227e781 HEAD@{24}: rebase: fast-forward
e0d6f5f HEAD@{25}: rebase (start): checkout e0d6f5f2ba5e3f539b8e13fdc9dc109fc953434c
2342d2b HEAD@{26}: rebase (abort): returning to refs/heads/main
2342d2b HEAD@{27}: rebase (abort): returning to refs/heads/main
2342d2b HEAD@{28}: rebase (finish): returning to refs/heads/main
2342d2b HEAD@{29}: rebase (start): checkout HEAD~2
2342d2b refs/heads/main@{9}: rebase (finish): refs/heads/main onto 227e7812564237393fc6d1574aaf9e0da9f6acd7
2342d2b HEAD@{30}: rebase (finish): returning to refs/heads/main
2342d2b HEAD@{31}: rebase (pick): Create thrid and fourth files
fcf1a5d HEAD@{32}: rebase (reword): chore: Create second file
991870d HEAD@{33}: rebase: fast-forward
227e781 HEAD@{34}: rebase (start): checkout HEAD~2
e1f23ed HEAD@{35}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{36}: rebase (start): checkout HEAD
e1f23ed HEAD@{37}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{38}: rebase (start): checkout HEAD~1
e1f23ed refs/heads/main@{10}: rebase (finish): refs/heads/main onto 991870dde64648c27a3b2e9be3bf3b0575ca330d
e1f23ed HEAD@{39}: rebase (finish): returning to refs/heads/main
e1f23ed HEAD@{40}: rebase (reword): Create thrid and fourth files
477dcc1 HEAD@{41}: rebase: fast-forward
991870d HEAD@{42}: rebase (start): checkout HEAD~1
477dcc1 refs/heads/main@{11}: commit (amend): Create thrid and fourth files
477dcc1 HEAD@{43}: commit (amend): Create thrid and fourth files
298533a refs/heads/main@{12}: commit: chore: Create third file and fourth files
298533a HEAD@{44}: commit: chore: Create third file and fourth files
991870d refs/heads/main@{13}: commit: chore: Create another file
991870d HEAD@{45}: commit: chore: Create another file
227e781 refs/heads/main@{14}: commit (amend): chore: Create initial file
227e781 HEAD@{46}: commit (amend): chore: Create initial file
9ad0fa5 refs/heads/main@{15}: commit (initial): chore: create initial file
9ad0fa5 HEAD@{47}: commit (initial): chore: create initial file
```


### Git Advanced Exercises: Part 2

## Feature Branch Creation

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch
  ft/branch
* main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git switch -c ft/new-feature
Switched to a new branch 'ft/new-feature'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch
  ft/branch
* ft/new-feature
  main
```

## Working on The Feature Branch

```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\feature.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m "Implemented core functionality for new feature"
[ft/new-feature 0814319] Implemented core functionality for new feature
1 file changed, 1 insertion(+)
create mode 100644 feature.txt
```

## Switching Back and Making More Changes

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git switch main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch
  ft/branch
  ft/new-feature
* main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\readme.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m "Update project readme"
[main 3202969] Update project readme
 1 file changed, 4 insertions(+)
 create mode 100644 readme.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
3202969 (HEAD -> main) Update project readme
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
```
## Branch Deletion

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/new-feature
Merge made by the 'ort' strategy.
 feature.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch -d ft/new-feature
Deleted branch ft/new-feature (was 0814319).
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch
  ft/branch
* main
```

## Creating a Branch from a Commit
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
50d7625 (HEAD -> main) Merge branch 'ft/new-feature'
3202969 Update project readme
0814319 Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout -b ft/new-branch-from-commit 0814319
Switched to a new branch 'ft/new-branch-from-commit'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log ft/new-branch-from-commit 
commit 08143191b11553a997d2239b56663a0b93b1bbb8 (HEAD -> ft/new-branch-from-commit)
Author: Zolender <ndeingare@gmail.com>
Date:   Wed Sep 3 09:35:56 2025 +0200

    Implemented core functionality for new feature

commit 4bfcd4a2ee0b67b630364564468a1ee7d058ba15
Author: Zolender <ndeingare@gmail.com>
Date:   Tue Sep 2 10:27:28 2025 +0200

    Implemented test 5

commit 98fa211818ec4511e2d9baab5b58ed70a3251a33
Author: Zolender <ndeingare@gmail.com>
Date:   Tue Sep 2 07:45:44 2025 +0200

    Create initial and Second file

commit 9c0651430113d463d54a8722b56e8320533266b3
Author: Zolender <ndeingare@gmail.com>
Date:   Tue Sep 2 10:07:25 2025 +0200

    Create third and fourth files
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log ft/new-branch-from-commit --oneline
0814319 (HEAD -> ft/new-branch-from-commit) Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\newFeature.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"Implement another important feature    
>> "
[ft/new-branch-from-commit d015897] Implement another important feature
 1 file changed, 2 insertions(+)
 create mode 100644 newFeature.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
d015897 (HEAD -> ft/new-branch-from-commit) Implement another important feature
0814319 Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
```

## Branch Merging
```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\feature.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"Update feature file"
[ft/new-branch-from-commit 130520e] Update feature file
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/new-branch-from-commit
Merge made by the 'ort' strategy.
 feature.txt    | 3 ++-
 newFeature.txt | 2 ++
 2 files changed, 4 insertions(+), 1 deletion(-)
 create mode 100644 newFeature.txt
```

## Branch Rebasing
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout ft/new-branch-from-commit
Switched to branch 'ft/new-branch-from-commit'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rebase main
Successfully rebased and updated refs/heads/ft/new-branch-from-commit.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
e05e826 (HEAD -> ft/new-branch-from-commit, main) Merge branch 'ft/new-branch-from-commit'
130520e Update feature file
d015897 Implement another important feature
50d7625 Merge branch 'ft/new-feature'
3202969 Update project readme
0814319 Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
```

## Renaming Branches
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch -m ft/new-branch-from-commit ft/improved-branch-name
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch
  ft/branch
* ft/improved-branch-name
  main
```

## Checking Out Detached HEAD

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
e05e826 (HEAD -> ft/improved-branch-name, main) Merge branch 'ft/new-branch-from-commit'
130520e Update feature file
d015897 Implement another important feature
50d7625 Merge branch 'ft/new-feature'
3202969 Update project readme
0814319 Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout 50d7625
Note: switching to '50d7625'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 50d7625 Merge branch 'ft/new-feature'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
50d7625 (HEAD) Merge branch 'ft/new-feature'
3202969 Update project readme
0814319 Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout e05e826
Previous HEAD position was 50d7625 Merge branch 'ft/new-feature'
HEAD is now at e05e826 Merge branch 'ft/new-branch-from-commit'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git log --oneline
e05e826 (HEAD, main, ft/improved-branch-name) Merge branch 'ft/new-branch-from-commit'
130520e Update feature file
d015897 Implement another important feature
50d7625 Merge branch 'ft/new-feature'
3202969 Update project readme
0814319 Implemented core functionality for new feature
4bfcd4a Implemented test 5
98fa211 Create initial and Second file
9c06514 Create third and fourth files
```


### Git Advanced Exercises Part 3: Advanced Workflows

## Stashing changes
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\feature3.txt .\feature4.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   feature3.txt
        new file:   feature4.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git stash
Saved working directory and index state WIP on main: e05e826 Merge branch 'ft/new-branch-from-commit'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git stash list
stash@{0}: WIP on main: e05e826 Merge branch 'ft/new-branch-from-commit'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git branch    
  ft/branch
  ft/improved-branch-name
* main
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git switch ft/branch
Switched to branch 'ft/branch'
```

## Retriving Stashed Changes

```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git switch main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git stash pop
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   feature3.txt
        new file:   feature4.txt

Dropped refs/stash@{0} (b7cf0e8196258d8ff3133039f3731d9ec4a9e75d)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"feat: add new features to the project" 

[main 4b95eca] feat: add new features to the project
 2 files changed, 4 insertions(+)
 create mode 100644 feature3.txt
 create mode 100644 feature4.txt
```

## Branch Merging Conflicts

```bash 
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\index.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"Update index page"
[main e31b754] Update index page
 1 file changed, 7 insertions(+)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git switch ft/modify-page
Switched to branch 'ft/modify-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\index.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"Update the main header and added some text"
[ft/modify-page 095af45] Update the main header and added some text
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/modify-page
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/modify-page
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/modify-page
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/modify-page
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git merge ft/modify-page
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

## Resolving merge conflicts with merge tool
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git config --global merge.tool vscode
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git config --global mergetool.vscode.cmd 'code --wait$MERGED'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\about.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"create an about us page for the project"
[main 74cbbad] create an about us page for the project
 1 file changed, 24 insertions(+)
 create mode 100644 about.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout ft/modify-page
Switched to branch 'ft/modify-page'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rebase main  
Successfully rebased and updated refs/heads/ft/modify-page.
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\about.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"update the about us page"
[ft/modify-page 5f89202] update the about us page
 1 file changed, 5 insertions(+), 5 deletions(-)
 PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git push origin ft/modify-page 
Enumerating objects: 63, done.
Counting objects: 100% (63/63), done.
Delta compression using up to 4 threads
Compressing objects: 100% (62/62), done.
Writing objects: 100% (63/63), 6.54 KiB | 145.00 KiB/s, done.
Total 63 (delta 30), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (30/30), done.
To https://github.com/Zolender/Exercises-Git_Advanced.git
 * [new branch]      ft/modify-page -> ft/modify-page

```


## Ignoring files/Directories

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Already on 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git rm --cached .\feature.txt
rm 'feature.txt'
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    feature.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\.gitignore
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore
        deleted:    feature.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        feature.txt
        test/

PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\.gitignore
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"update the git ignore file"
[main 2f09a34] update the git ignore file
 2 files changed, 3 insertions(+), 2 deletions(-)
 create mode 100644 .gitignore
 delete mode 100644 feature.txt
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean
```

## Working with Tags 

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git tag v1.0
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\test\
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git add .\.gitignore            
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git commit -m"remove the test directory from the git ignore file"
[main 1f1017a] remove the test directory from the git ignore file
 2 files changed, 1 deletion(-)
 create mode 100644 test/testfile.html
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git tag v2.0
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git tag --list
v1.0
v2.0
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout v1.0
Note: switching to 'v1.0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 2f09a34 update the git ignore file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout v2.0
Previous HEAD position was 2f09a34 update the git ignore file
HEAD is now at 1f1017a remove the test directory from the git ignore file
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git tag -d v2.0
Deleted tag 'v2.0' (was 1f1017a)
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git tag --list
v1.0
```

## Pushing to remote repository

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git push 
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (7/7), 667 bytes | 133.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'main' on GitHub by visiting:
remote:      https://github.com/Zolender/Exercises-Git_Advanced/pull/new/main
remote: 
To https://github.com/Zolender/Exercises-Git_Advanced.git
 * [new branch]      main -> main
```

## Pulling from remote repository
```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1.05 KiB | 31.00 KiB/s, done.
From https://github.com/Zolender/Exercises-Git_Advanced
   1b4e27f..42d1850  main       -> origin/main
Updating 1f1017a..42d1850
Fast-forward
 index.html | 4 ++--
 readme.txt | 4 +++-
 2 files changed, 5 insertions(+), 3 deletions(-)
```

OR

```bash
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git fetch
PS C:\Users\Eben\OneDrive - MSFT\Desktop\The Gym curriculum\Git learning\Git Advanced> git  merge
Updating 42d1850..d45ba1c
Fast-forward
 readme.txt | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
```