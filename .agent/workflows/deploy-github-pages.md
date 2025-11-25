---
description: Deploy portfolio to GitHub Pages
---

# Deploy Your Portfolio to GitHub Pages

This workflow will guide you through deploying your portfolio website to GitHub Pages, making it accessible at `https://yourusername.github.io/repository-name/`.

## Prerequisites
- A GitHub account
- Git installed on your computer
- Your portfolio files ready to deploy

## Step 1: Initialize Git Repository (if not already done)

Navigate to your portfolio directory and initialize a git repository:

```bash
cd "c:\Users\Mega Providers\Downloads\Abdul Rafay Portfolio"
git init
```

## Step 2: Create a .gitignore File

Create a `.gitignore` file to exclude unnecessary files:

```bash
echo ".agent/" > .gitignore
echo ".DS_Store" >> .gitignore
echo "Thumbs.db" >> .gitignore
```

## Step 3: Stage and Commit Your Files

Add all your portfolio files to git:

```bash
git add .
git commit -m "Initial commit: Add portfolio files"
```

## Step 4: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `portfolio` or `yourusername.github.io`)
   - **Note**: If you name it `yourusername.github.io`, it will be accessible at `https://yourusername.github.io/`
   - Otherwise, it will be at `https://yourusername.github.io/repository-name/`
5. **Do NOT** initialize with README, .gitignore, or license (we already have files)
6. Click "Create repository"

## Step 5: Connect Local Repository to GitHub

Copy the commands from GitHub (they'll look like this) and run them:

```bash
git remote add origin https://github.com/yourusername/your-repo-name.git
git branch -M main
git push -u origin main
```

**Replace** `yourusername` and `your-repo-name` with your actual GitHub username and repository name.

## Step 6: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" in the left sidebar (under "Code and automation")
4. Under "Source", select "Deploy from a branch"
5. Under "Branch", select `main` and `/ (root)` folder
6. Click "Save"

## Step 7: Wait for Deployment

- GitHub Pages will build and deploy your site (usually takes 1-3 minutes)
- You'll see a message at the top with your site URL: `Your site is live at https://yourusername.github.io/repository-name/`
- Click the URL to view your deployed portfolio!

## Step 8: Update Your Portfolio (Future Changes)

Whenever you make changes to your portfolio:

```bash
git add .
git commit -m "Description of your changes"
git push
```

GitHub Pages will automatically rebuild and deploy your updated site within a few minutes.

## Troubleshooting

### Issue: CSS/JS not loading
- Check that your file paths in `index.html` are relative (e.g., `./style.css` not `/style.css`)
- If your repo is NOT named `yourusername.github.io`, you may need to update paths

### Issue: Images not showing
- Verify image paths are relative (e.g., `./images/photo.jpg`)
- Ensure all image files are committed to the repository

### Issue: 404 Error
- Wait a few minutes after enabling GitHub Pages
- Check that you selected the correct branch and folder
- Verify your repository is public (GitHub Pages free tier requires public repos)

## Custom Domain (Optional)

If you want to use a custom domain (e.g., `www.yourname.com`):

1. In repository Settings → Pages → Custom domain
2. Enter your domain name
3. Configure DNS settings with your domain provider
4. Add a CNAME file to your repository with your domain name

## Success!

Your portfolio is now live and accessible to anyone on the internet! 🎉

Share your portfolio URL:
- On your resume
- On LinkedIn
- With potential employers
- On social media
