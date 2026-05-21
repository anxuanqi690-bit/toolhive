# ToolHive Deployment Guide

This guide covers how to deploy ToolHive to Vercel.

## Prerequisites

- Node.js 18+ installed
- A Vercel account (free at vercel.com)

## Option 1: Deploy via Vercel CLI (Recommended)

### Step 1: Install Vercel CLI

```bash
npm install -g vercel
```

### Step 2: Login to Vercel

```bash
vercel login
```

Follow the prompts to authenticate with your Vercel account.

### Step 3: Deploy

Navigate to the `toolhive` directory and run:

```bash
cd toolhive
vercel --yes
```

The `--yes` flag accepts all default options automatically.

### Step 4: Configure for Production (Optional)

After testing with preview deployment, promote to production:

```bash
vercel --prod
```

## Option 2: Deploy via GitHub

### Step 1: Push to GitHub

Create a new repository on GitHub and push your code:

```bash
cd toolhive
git init
git add .
git commit -m "Initial commit: ToolHive MVP"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/toolhive.git
git push -u origin main
```

### Step 2: Import to Vercel

1. Go to [vercel.com/new](https://vercel.com/new)
2. Click "Import Git Repository"
3. Select your GitHub repository
4. Vercel will auto-detect it's a static site
5. Click "Deploy"

## Option 3: Drag and Drop

### Step 1: Zip the Project

```bash
cd toolhive
zip -r toolhive.zip .
```

### Step 2: Deploy

1. Go to [vercel.com/new](https://vercel.com/new)
2. Click "Import Third-Party Git Repository" (or scroll down)
3. Select "Deploy via Static File" (or drag the zip file to Vercel dashboard)

## Configuration

The `vercel.json` file is already configured for this static site:

```json
{
  "version": 2,
  "buildCommand": null,
  "installCommand": null,
  "framework": null,
  "outputDirectory": ".",
  "rewrites": [
    { "source": "/(.*)", "destination": "/index.html" }
  ]
}
```

The rewrites configuration ensures all routes serve `index.html`, enabling client-side routing.

## Custom Domain (Optional)

### Step 1: Add Domain

1. Go to your project settings on Vercel
2. Navigate to "Domains"
3. Enter your custom domain (e.g., `toolhive.dev`)
4. Click "Add"

### Step 2: Configure DNS

Vercel will provide DNS records to add:

```
Type: A     Name: @     Value: 76.76.21.21
Type: CNAME Name: www   Value: cname.vercel-dns.com
```

### Step 3: Verify

Wait a few minutes for DNS propagation, then verify your domain works.

## Post-Deployment Checklist

- [ ] Test all tools in the deployed version
- [ ] Verify meta tags and SEO in browser dev tools
- [ ] Test responsive design on mobile devices
- [ ] Check Open Graph preview with [Facebook Debugger](https://developers.facebook.com/tools/debug/)
- [ ] Set up Google AdSense (if applicable)
- [ ] Submit sitemap to Google Search Console

## Troubleshooting

### "Command not found: vercel"

Reinstall the CLI:
```bash
npm install -g vercel
```

### Build fails

This is a static site - no build step is needed. Check that `vercel.json` has `null` for buildCommand.

### 404 errors on tool pages

Ensure the `rewrites` configuration in `vercel.json` is correct. All routes should fallback to `index.html`.

## Getting Help

- [Vercel Documentation](https://vercel.com/docs)
- [Vercel Support](https://vercel.com/support)
- [Create an Issue](https://github.com/your-repo/issues)

## Environment Variables (Not needed for static sites)

Since ToolHive is a pure static site, no environment variables are required.
