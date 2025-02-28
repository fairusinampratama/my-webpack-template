# Webpack Project Deployment Guide

## 1️⃣ Initialize Project
Run the following commands to set up your Webpack project:
```sh
npm init -y
npm install webpack webpack-cli --save-dev
```

## 2️⃣ Set Up Git Repository

### **Create a Repository on GitHub**
1. Go to [GitHub](https://github.com) and create a new repository (e.g., `my-webpack-template`).
2. Copy the repository URL.

### **Initialize Git and Push to GitHub**
Run these commands in your project folder:
```sh
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```
*(Replace `<your-repo-url>` with your actual GitHub repository URL.)*

## 3️⃣ Deployment to GitHub Pages

### **Create a Deployment Branch**
```sh
git branch gh-pages
```

### **Ensure Everything is Committed**
```sh
git status
```
Make sure there are no uncommitted changes.

### **Switch to `gh-pages` and Merge `main`**
```sh
git checkout gh-pages && git merge main --no-edit
```

### **Build the Project**
```sh
npx webpack
```

### **Deploy to GitHub Pages**
```sh
git add dist -f && git commit -m "Deployment commit"
git subtree push --prefix dist origin gh-pages
git checkout main
```

## 4️⃣ Set GitHub Pages Source
1. Go to your **GitHub repository**.
2. Open **Settings** → **Pages**.
3. Under **Source**, select `gh-pages`.
4. Save changes.

## 🎉 Your Project is Live!
Your project will be available at:
```
https://<your-github-username>.github.io/<your-repo-name>/
```

