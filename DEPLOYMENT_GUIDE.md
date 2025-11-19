# Lumina Bridging Website - Deployment Guide

Complete step-by-step instructions to deploy your GitHub Pages website.

## 📋 Prerequisites

- GitHub account (already have one: https://github.com/Lumina-Bridging-Inc)
- Git installed on your computer ([Download Git](https://git-scm.com))
- Basic command line knowledge

## 🚀 Deployment Steps

### Step 1: Create the GitHub Pages Repository

**Important:** The repository name MUST be exactly: `lumina-bridging-inc.github.io`

1. Go to [GitHub](https://github.com) and sign in
2. In the top right, click **+** → **New repository**
3. Fill in the details:
   - **Repository name:** `lumina-bridging-inc.github.io` (MUST be exact)
   - **Description:** "Lumina Bridging Inc. - Healthcare AI Solutions"
   - **Visibility:** Public
   - **Initialize with:** Do NOT add README, .gitignore, or license
4. Click **Create repository**

### Step 2: Prepare Your Local Repository

1. Open Terminal/Command Prompt
2. Navigate to the website folder:
   ```bash
   cd path/to/lumina-bridging-website
   ```

3. Initialize git (if not already done):
   ```bash
   git init
   ```

4. Configure git with your GitHub account:
   ```bash
   git config user.name "Your Name"
   git config user.email "your.email@example.com"
   ```

### Step 3: Add and Commit Files

1. Stage all files:
   ```bash
   git add .
   ```

2. Create your first commit:
   ```bash
   git commit -m "Initial commit: Lumina Bridging website"
   ```

### Step 4: Connect to GitHub

1. Add the GitHub repository as your remote:
   ```bash
   git remote add origin https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io.git
   ```

2. Verify the remote is connected:
   ```bash
   git remote -v
   ```
   Should show:
   ```
   origin  https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io.git (fetch)
   origin  https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io.git (push)
   ```

### Step 5: Push to GitHub

1. Rename branch to main (if using older git):
   ```bash
   git branch -M main
   ```

2. Push your code:
   ```bash
   git push -u origin main
   ```

3. GitHub will prompt for authentication:
   - **Option A:** Enter your GitHub username and password (if 2FA enabled, use Personal Access Token instead)
   - **Option B:** Use GitHub CLI: `gh auth login`

### Step 6: Enable GitHub Pages

1. Go to your repository: https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io
2. Click **Settings** (gear icon)
3. In the left sidebar, click **Pages**
4. Under "Source" section:
   - Select **Deploy from a branch**
   - Choose branch: `main`
   - Choose folder: `/ (root)`
   - Click **Save**
5. GitHub will show your site URL (usually takes 1-2 minutes to build)

### Step 7: Verify Your Site is Live

1. Wait 1-2 minutes for GitHub to build your site
2. Go to: https://lumina-bridging-inc.github.io
3. You should see your website!

## 🖼️ Adding Your Logo

1. Save your logo as `logo.png` or `logo.svg`
2. Place it in the `assets/images/` folder:
   ```
   assets/
   └── images/
       └── logo.png
   ```

3. Update `index.html` logo section (around line 30):
   ```html
   <div class="logo">
       <img src="assets/images/logo.png" alt="Lumina Bridging Logo" class="logo-image">
       <h1>Lumina Bridging</h1>
   </div>
   ```

4. Add CSS to `assets/style.css` (in `.logo` selector):
   ```css
   .logo-image {
       height: 40px;
       width: auto;
       margin-right: 12px;
       vertical-align: middle;
   }
   ```

5. Commit and push:
   ```bash
   git add assets/images/logo.png assets/style.css index.html
   git commit -m "Add company logo to website"
   git push
   ```

## 🔄 Making Updates

To make changes to your website:

1. Edit files locally (HTML, CSS, JavaScript)
2. Test in your browser or local server
3. Commit changes:
   ```bash
   git add .
   git commit -m "Update: [describe what changed]"
   ```
4. Push to GitHub:
   ```bash
   git push
   ```
5. Your site updates automatically (usually within 1-2 minutes)

## ✅ Checklist Before Going Live

- [ ] Repository created and named `lumina-bridging-inc.github.io`
- [ ] All files pushed to GitHub
- [ ] GitHub Pages enabled in repository settings
- [ ] Site accessible at https://lumina-bridging-inc.github.io
- [ ] All links working correctly
- [ ] Tested on mobile devices
- [ ] Logo added and displaying correctly
- [ ] Contact information is accurate
- [ ] Project links point to correct repositories
- [ ] No broken images or assets

## 🆘 Troubleshooting

### Issue: Site not showing up

**Solution:**
1. Verify repository name is exactly: `lumina-bridging-inc.github.io`
2. Check GitHub Pages is enabled in Settings > Pages
3. Wait 2-3 minutes for GitHub to build
4. Go to Actions tab to see build status
5. Try a hard refresh: `Ctrl+Shift+Delete` then refresh page

### Issue: Styles/images not loading

**Solution:**
1. Verify file paths are correct in `index.html`
2. Ensure files are committed and pushed to GitHub
3. Check for typos in file names (case-sensitive)
4. Try clearing browser cache: `Ctrl+Shift+Delete`
5. Check browser console for 404 errors (F12)

### Issue: Build fails in Actions

**Solution:**
1. Check the Actions tab for error messages
2. Ensure all files are UTF-8 encoded
3. Check that file paths use forward slashes `/` not backslashes `\`
4. Verify `_config.yml` has no syntax errors
5. Try removing `_config.yml` temporarily

### Issue: Custom domain not working

**Solution:**
1. Add CNAME file to root of repository with your domain
2. Update DNS records at your domain registrar
3. Wait 24-48 hours for DNS propagation
4. See GitHub docs: [Custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## 📊 Performance Tips

1. **Optimize images:** Compress logos and screenshots
2. **Minify CSS:** Consider minifying `assets/style.css` for production
3. **Lazy loading:** Use `loading="lazy"` on images
4. **Caching:** GitHub Pages automatically handles caching

## 🔐 Security Best Practices

1. **Never commit secrets:** Don't add API keys or passwords
2. **Keep dependencies updated:** If using Jekyll plugins, keep them updated
3. **Use HTTPS:** GitHub Pages enforces HTTPS automatically
4. **Review permissions:** Only give GitHub access to trusted applications

## 📞 Getting Help

### GitHub Pages Issues
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Community Forum](https://github.community)
- [GitHub Status Page](https://www.githubstatus.com)

### Website Design/Development
- [MDN Web Docs](https://developer.mozilla.org)
- [CSS-Tricks](https://css-tricks.com)
- [GitHub Marketplace](https://github.com/marketplace) for GitHub Actions

## 🎯 Next Steps After Deployment

1. **Share your site:**
   - Add link to GitHub organization profile
   - Include in project README files
   - Share on social media

2. **Monitor performance:**
   - Use Google Analytics (optional)
   - Monitor GitHub Actions for build failures
   - Check broken links monthly

3. **Keep content fresh:**
   - Update project links as new projects launch
   - Update solution descriptions
   - Add new team members to contact section

4. **Maintain SEO:**
   - Add meta descriptions
   - Update title tags
   - Ensure proper heading hierarchy

## 📝 Example Git Workflow

```bash
# Check status before committing
git status

# Add specific files
git add index.html assets/style.css

# Or add all changes
git add .

# View what will be committed
git diff --cached

# Commit with descriptive message
git commit -m "Update: Improve mobile responsiveness"

# Push to GitHub
git push origin main

# View commit history
git log --oneline
```

## 🎉 Success!

Your Lumina Bridging website is now live! You can:
- Share the URL: https://lumina-bridging-inc.github.io
- Manage it entirely through GitHub
- Make updates by pushing code
- Track changes through git history

---

**Questions?** Check the [GitHub Pages docs](https://docs.github.com/en/pages) or reach out to your development team.

**Happy deploying! 🚀**
