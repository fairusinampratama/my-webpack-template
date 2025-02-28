INITIATE PROJECT

npm init -y

npm install webpack webpack-cli --save-dev

GIT

Create a repository on GitHub and push the project

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main

Deployment

//Make new branch
git branch gh-pages

//Commit and check
git status

//change branch and sync changes to main
git checkout gh-pages && git merge main --no-edit

//deploy
git add dist -f && git commit -m "Deployment commit"
git subtree push --prefix dist origin gh-pages
git checkout main