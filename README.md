## 🚀 HUGO DEPLOYMENT WORKFLOW (GITHUB PAGES)

This summary outlines the steps required whenever you want to update the live site.

### 1. Make and Test Changes Locally 🛠️

1.  **Edit:** Make your changes to content (e.g., Markdown files) or templates (in `layouts/`).
2.  **Verify:** Run the local server to check the changes before committing:
    ```bash
    hugo server
    ```
    (Check: http://localhost:1313/)

### 2. Commit Changes to Git 💾

Once changes are verified and ready to go live:

1.  **Stage Files:** Add all modified files:
    ```bash
    > git add .
    ```
2.  **Commit Changes:** Save the files with a descriptive message:
    ```bash
    > git commit -m "Brief description of the change I made"
    ```

### 3. Push to GitHub and Deploy 🌐

Pushing your commit triggers the automated deployment process.

1.  **Push to main:** Send the changes to your GitHub repository:
    ```bash
   > git push
    ```

**What Happens Next:**
* The **GitHub Action** (defined in `.github/workflows/github-pages.yml`) runs automatically.
* It executes `hugo --minify` to build the static site.
* It pushes the finished site to the **`gh-pages`** branch.
* Your live site at `https://therizinosaurus-cheloniformis.github.io/Absence/` updates within a few minutes.