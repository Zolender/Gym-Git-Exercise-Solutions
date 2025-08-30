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