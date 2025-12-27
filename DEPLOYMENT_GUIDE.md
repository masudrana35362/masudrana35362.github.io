# 🚀 GitHub Pages Deployment Guide

Complete step-by-step guide to deploy your portfolio to GitHub Pages and make it live at `https://masudrana35362.github.io`

## 📋 Prerequisites

- GitHub account (create at github.com if you don't have one)
- Git installed on your computer
- Your portfolio files ready (✅ Already done!)

---

## 🎯 Deployment Steps

### Step 1: Create GitHub Repository

1. **Go to GitHub**: Open [github.com](https://github.com) and sign in
2. **Create New Repository**:
   - Click the `+` icon in the top-right corner
   - Select **"New repository"**
   - **Repository name**: `masudrana35362.github.io` (IMPORTANT: use your exact username)
   - **Description**: "My professional portfolio website"
   - **Visibility**: Public (required for free GitHub Pages)
   - **DO NOT** check "Add a README file"
   - **DO NOT** add .gitignore or license
   - Click **"Create repository"**

### Step 2: Initialize Git in Your Project

Open terminal in your portfolio directory and run:

```bash
cd /home/masudrana/projects/practice/portfolio

# Initialize git repository
git init

# Add all files to staging
git add .

# Create first commit
git commit -m "Initial portfolio commit"
```

### Step 3: Connect to GitHub Repository

```bash
# Add GitHub repository as remote (replace with your actual repo URL)
git remote add origin https://github.com/masudrana35362/masudrana35362.github.io.git

# Rename branch to main (GitHub's default)
git branch -M main

# Push to GitHub
git push -u origin main
```

**Note**: You'll be prompted for GitHub credentials. Use your:
- **Username**: masudrana35362
- **Password**: Use a Personal Access Token (not your GitHub password)

#### How to Create Personal Access Token:

1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Name: "Portfolio Deployment"
4. Expiration: Choose as needed (e.g., 90 days)
5. Select scope: Check **"repo"** (full control of private repositories)
6. Click "Generate token"
7. **COPY THE TOKEN** (you won't see it again!)
8. Use this token as your password when git asks

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/masudrana35362/masudrana35362.github.io`
2. Click **"Settings"** tab
3. Scroll down to **"Pages"** in the left sidebar
4. Under **"Source"**:
   - Branch: Select `main`
   - Folder: Select `/ (root)`
   - Click **"Save"**

### Step 5: Wait for Deployment

- GitHub will automatically build and deploy your site
- Wait 1-2 minutes
- You'll see a green message: "Your site is published at https://masudrana35362.github.io"

### Step 6: Visit Your Live Portfolio! 🎉

Open your browser and go to:
```
https://masudrana35362.github.io
```

---

## 🔄 Making Updates After Initial Deployment

Whenever you make changes to your portfolio:

```bash
# 1. Add changed files
git add .

# 2. Commit with a descriptive message
git commit -m "Updated project section"

# 3. Push to GitHub
git push origin main
```

GitHub Pages will automatically rebuild and deploy in 1-2 minutes!

---

## 🛠️ Quick Commands Reference

### Check Git status
```bash
git status
```

### Add specific files
```bash
git add filename.html
```

### View commit history
```bash
git log --oneline
```

### Undo uncommitted changes
```bash
git checkout -- filename.html
```

---

## ⚠️ Common Issues & Solutions

### Issue 1: "Repository already exists"
**Solution**: The repository name must be exactly `yourusername.github.io`. If it exists, either:
- Delete the existing repository and create a new one
- Or use a project repository (URL will be `username.github.io/portfolio`)

### Issue 2: "Permission denied (publickey)"
**Solution**: Use HTTPS URL instead of SSH, or set up SSH keys:
```bash
git remote set-url origin https://github.com/masudrana35362/masudrana35362.github.io.git
```

### Issue 3: "Site not loading / 404 error"
**Solutions**:
- Wait 2-3 minutes for first deployment
- Check that repository name is exactly `masudrana35362.github.io`
- Verify GitHub Pages is enabled in Settings → Pages
- Make sure `index.html` is in the root directory (not in a subfolder)

### Issue 4: "Images not loading"
**Solution**: All image paths must be relative:
- ✅ Correct: `assets/images/profile.png`
- ❌ Wrong: `/assets/images/profile.png` or absolute paths

### Issue 5: "CSS/JavaScript not working"
**Solution**: Check file paths in index.html:
- ✅ Correct: `<link rel="stylesheet" href="styles.css">`
- ❌ Wrong: `<link rel="stylesheet" href="/styles.css">`

---

## 📱 Test Your Portfolio

After deployment, test these features:

- ✅ All sections load correctly
- ✅ Navigation links work
- ✅ Smooth scrolling functions
- ✅ Typing effect in hero section
- ✅ Project filters work
- ✅ Skill bars animate on scroll
- ✅ Contact form opens Gmail
- ✅ Download Resume button works
- ✅ All images load
- ✅ Mobile responsive design
- ✅ Social media links work

---

## 🎨 Optional: Custom Domain

Want to use your own domain (e.g., `masudrana.com`)?

1. Buy a domain from any registrar (Namecheap, GoDaddy, etc.)
2. In your repository, create a file named `CNAME` (no extension)
3. Add your domain: `masudrana.com`
4. Commit and push
5. In your domain registrar, add these DNS records:
   ```
   Type: A
   Host: @
   Value: 185.199.108.153
   
   Type: A
   Host: @
   Value: 185.199.109.153
   
   Type: A
   Host: @
   Value: 185.199.110.153
   
   Type: A
   Host: @
   Value: 185.199.111.153
   
   Type: CNAME
   Host: www
   Value: masudrana35362.github.io
   ```
6. Wait 24-48 hours for DNS propagation

---

## 📊 Monitor Your Site

### GitHub Repository Insights
- Go to repository → Insights → Traffic to see:
  - Views
  - Unique visitors
  - Referrers

### Google Analytics (Optional)
Add to your `index.html` before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

---

## ✅ Final Checklist

Before going live, verify:

- [ ] All personal information is correct
- [ ] Email addresses work
- [ ] Phone number is correct
- [ ] GitHub/LinkedIn URLs are accurate
- [ ] All project links work
- [ ] Resume PDF downloads correctly
- [ ] No placeholder text remaining
- [ ] All images load
- [ ] Mobile view looks good
- [ ] Forms work correctly

---

## 🎉 Congratulations!

Your portfolio is now live! Share it on:
- LinkedIn profile
- Resume
- Job applications
- Email signature
- Social media

**Your live URL**: `https://masudrana35362.github.io`

---

## 📞 Need Help?

If you run into issues:
1. Check the Common Issues section above
2. Review GitHub Pages documentation: https://pages.github.com
3. Check repository Actions tab for build errors
4. Verify all files are committed and pushed

**Remember**: Every time you make changes, just run:
```bash
git add .
git commit -m "Your update description"
git push origin main
```

And your site will automatically update in 1-2 minutes! 🚀
