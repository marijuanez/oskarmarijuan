# Deployment Guide

This project is configured to deploy to **Firebase Hosting** using **GitHub Actions**.

## Firebase Configuration
* **Project ID**: `oskarmarijuan-73678`
* **Site ID**: `oskarmarijuan`
* **Production URL**: https://oskarmarijuan.web.app
* **Source Directory**: Root (`.`) - The files you edit in MAMP are the ones deployed.
* **Ignored Files**: PHP files, git configuration, and the old `public` folder are excluded from upload.

## GitHub Actions Setup
The deployment workflow is located in `.github/workflows/firebase-hosting.yml`.

### Required Actions (One-Time Setup)
To enable automatic deployment, you must set the following **Secrets** in your GitHub Repository Settings -> Secrets and variables -> Actions:

1.  **FIREBASE_PROJECT_ID**:
    *   Value: `oskarmarijuan-73678`

2.  **FIREBASE_TOKEN**:
    *   Value: Your Firebase CI token.
    *   *To generate this token*, run `firebase login:ci` in your terminal and copy the result.

### How to Deploy
*   **Automatic**: Every time you push changes to the `main` branch, the site will automatically deploy.
*   **Manual**: You can run `firebase deploy` locally if you have the Firebase CLI installed and logged in.
