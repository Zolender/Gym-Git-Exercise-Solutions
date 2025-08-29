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