# 🌐 GitHub Pages Deployment Guide

> *A complete guide to hosting your static websites for free directly from a GitHub repository.*

GitHub Pages is one of the most powerful features for front-end developers, students, and open-source contributors. It allows you to host a website securely via HTTPS without paying anything.

---

## 🚀 1. What is GitHub Pages?

**GitHub Pages** is a static site hosting service. It takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process (like Jekyll, Hugo, React, etc.), and publishes them online.

- **URL Structure (User/Organization):** `https://<username>.github.io`
- **URL Structure (Project Site):** `https://<username>.github.io/<repository-name>`
- **Custom Domains:** It fully supports custom domains (e.g., `www.yourportfolio.com`).

---

## 🏗️ 2. Deploying a Static HTML/CSS/JS Site

If your project consists only of plain HTML, CSS, and JS files, deploying it is incredibly fast.

### The Source Branch Method
1. Create a repository on GitHub (e.g., `my-portfolio`).
2. Push your `index.html` and assets to the `main` branch.
3. In your repository on GitHub, navigate to **Settings** > **Pages** (on the left sidebar).
4. Under **Build and deployment**, select **Source** as *Deploy from a branch*.
5. Select the `main` branch, and the `/` (root) directory.
6. Click **Save**.
7. Wait ~1 minute, and your site will be live at the generated URL shown at the top of the Pages settings.

---

## ⚡ 3. Deploying a Modern App (React, Vue, Next.js)

When you are using frameworks, you cannot just host the raw code. The code must be *built* before it can be hosted as static files. This is where **GitHub Actions** shines.

### Deploying via GitHub Actions (The Modern Way)

Since 2022, GitHub has provided first-class support for deploying Pages using Actions, bypassing the old `gh-pages` branch method entirely.

1. Go to **Settings** > **Pages** in your repository.
2. Under **Build and deployment**, change the source to **GitHub Actions**.
3. Under **Configure the build and deployment workflow**, GitHub will automatically suggest a starter workflow based on your repository.
    - E.g., if it detects React/Node, it will suggest a Node workflow.
    - If it detects a Next.js static export, it will suggest the Next.js workflow.
4. Click **Configure**, review the generated `.yml` file, and commit it to your repository.
5. Watch the **Actions** tab on your repository while GitHub builds and deploys your application.

---

## 🛠️ 4. Setting Up a Custom Domain

Adding a custom domain makes your portfolio or project look 10x more professional.

### Steps
1. Purchase a domain from your registrar of choice (Namecheap, GoDaddy, Google Domains, etc.).
   *(If you are a student, remember you get one free from the Student Developer Pack!)*
2. In your GitHub Repo's **Settings** > **Pages**, scroll down to **Custom domain**.
3. Type your domain (e.g., `portfolio.com`) and click **Save**.
   - *This will automatically create a `CNAME` file in the root of your source branch.*
4. Log into your Domain Registrar's DNS settings.
5. Create an **A Record** pointing your bare domain (e.g., `portfolio.com`) to these GitHub IPs:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
6. Create a **CNAME Record** for `www` pointing to `<your-username>.github.io`.
7. Wait for DNS propagation (can take several hours) and ensure the "Enforce HTTPS" box is checked in your GitHub settings.

---

## 🚫 5. Limitations of GitHub Pages

While amazing, keep in mind what GitHub Pages **cannot** do:

- **No Server-Side Code:** You cannot host PHP, Python, Java, or Express.js backends here. Pages only serves static files.
- **Size Limits:** Sites have a soft limit of 1 GB and a bandwidth limit of 100 GB per month.
- **Commercial Use:** It is intended to showcase open-source projects, portfolios, or documentation, not to run a commercial e-commerce business. Use Vercel, Netlify, or AWS for that.

> **Pro Tip:** Need a backend for your GitHub Pages site? Use serverless functions elsewhere (e.g., Supabase, Firebase, or Vercel Functions) and make API calls from your static Pages site!
