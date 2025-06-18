# Gym-Git-Exercise-Solutions
## Bundle_1
   - Renaming the git branch from master to main:
       * git branch -m  master main
   - Staging the files:
       * git add index.html
       * git add style.css
   - Commit message part:
       * git commit -m"Initializing the repository adding two files(simple website), renaming the branch to master"
   - Linking the local repository to the GitHub repository:
       * git remote add origin https://github.com/Zolender/Exercises.git
   - Pushing my changes to GitHub:
       * git pull origin main --allow-unrelated-histories
       * git push origin main
   - Creating a new branch "dev" from main
        * git branch dev
   - Creating a new branch "test" from "dev"
        * git checkout dev
        * git branch test
        * git checkout test
   - Deleting the "test" branch
        * git checkout dev
        * git branch -d test
   - Stashing the new changes to the repository
        * git add home.html
        * git stash -m "Stashing the home.html file"
        * git add about.html
        * git stash -m "Stashing the about.html file"
        * git add team.html
        * git stash -m "Stashing the team.html file"
   - Stash popping the most recent changes
        * git stash pop
   - Using index, stash popping the old stashed file(before I added new ones)
        * git stash list
        * git stash pop 0
         
