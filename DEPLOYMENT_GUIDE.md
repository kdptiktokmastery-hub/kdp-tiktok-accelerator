# GitHub Pages Deployment Guide

This guide will walk you through deploying your KDP TikTok Profit Accelerator website to GitHub Pages with your custom domain `kdptiktok.com`.

## Prerequisites

- A GitHub account (create one at https://github.com if you don't have one)
- Git installed on your computer
- The project files from this repository

## Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in to your account
2. Click the **+** icon in the top right corner and select **New repository**
3. Name your repository: `kdp-tiktok-accelerator`
4. Add a description (optional): "KDP TikTok Profit Accelerator - Resource hub for Amazon KDP authors"
5. Choose **Public** (required for free GitHub Pages)
6. Click **Create repository**

## Step 2: Initialize Git and Push Your Code

Open your terminal/command prompt and navigate to your project folder:

```bash
cd /path/to/kdp-tiktok-github
```

Initialize Git and push your code:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: KDP TikTok Profit Accelerator website"

# Add remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/kdp-tiktok-accelerator.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (gear icon in the top right)
3. In the left sidebar, click **Pages**
4. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
   - This will automatically use the workflow file we've provided

The site will start building automatically. You should see a workflow running under the **Actions** tab.

## Step 4: Configure Your Custom Domain

### Option A: Using CNAME (Recommended)

1. Go back to your repository settings
2. Click **Pages** in the left sidebar
3. Under "Custom domain", enter: `kdptiktok.com`
4. Click **Save**
5. GitHub will automatically create a `CNAME` file in your repository

### Option B: Update Your Domain's DNS Settings

You'll need to update your domain registrar's DNS settings. Contact your domain provider (GoDaddy, Namecheap, etc.) and add:

**For CNAME record:**
- Name: `www`
- Value: `YOUR_USERNAME.github.io`

**For A records (if CNAME not available):**
Add these IP addresses:
- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

## Step 5: Verify Deployment

1. Go to your repository's **Actions** tab
2. You should see a workflow named "Deploy to GitHub Pages"
3. Wait for it to complete (green checkmark means success)
4. Visit your domain: `https://kdptiktok.com`

If you see a 404 error, wait a few minutes for DNS to propagate.

## Troubleshooting

### Site not showing up

- **Wait for DNS propagation**: This can take up to 24 hours
- **Check GitHub Actions**: Go to Actions tab and verify the deployment workflow succeeded
- **Clear browser cache**: Try accessing the site in an incognito/private window

### CNAME file keeps getting deleted

- Make sure GitHub Pages is set to "GitHub Actions" as the source
- The workflow file should automatically recreate the CNAME file

### Build failed

- Check the Actions tab for error messages
- Make sure all files are committed and pushed to GitHub
- Verify `package.json` dependencies are correct

## Making Updates

After your initial deployment, any time you want to update your site:

1. Make changes to your local files
2. Commit and push to GitHub:

```bash
git add .
git commit -m "Update: describe your changes"
git push
```

3. GitHub Actions will automatically build and deploy your changes
4. Your site will be updated within a few minutes

## Updating Content

### Change Trending Niches

Edit `src/components/TrendDashboard.tsx`:

```typescript
const niches = [
  { genre: "Your Genre", growth: "+XXX%", potential: X.X, status: "Hot" },
  // ... more niches
];
```

### Change Script Templates

Edit `src/components/ScriptGenerator.tsx`:

```typescript
const hookTemplates = [
  "Your template with {genre}, {title}, {audience}, {emotion}",
  // ... more templates
];
```

### Change Resources/Tools

Edit `src/components/Resources.tsx`:

```typescript
const resources = [
  {
    name: "Tool Name",
    desc: "Tool description",
    category: "Category",
  },
  // ... more resources
];
```

### Update Contact Information

Edit `src/components/Footer.tsx` to update:
- Email address
- Website URL
- Social media links

## Performance Tips

- The site is already optimized with Vite
- CSS is minified and bundled
- JavaScript is code-split for faster loading
- Images are lazy-loaded

## Security

- Your site is served over HTTPS automatically
- GitHub Pages handles SSL certificates
- No backend or database needed (static site)

## Support

For GitHub Pages documentation, visit: https://docs.github.com/en/pages

For issues with this project, check the README.md or contact: kdptiktokmastery@gmail.com

## Next Steps

1. Customize the content to match your brand
2. Add your own testimonials
3. Update the resources with affiliate links
4. Monitor analytics (add Google Analytics if desired)
5. Promote your site on social media
