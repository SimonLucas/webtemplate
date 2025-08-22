# GitHub Pages Starter (Jekyll)

A minimal Jekyll site with a single template and a top navigation bar, ideal for lightweight company sites.

## How to use

1. **Create a new GitHub repo** (public or private).
2. Download and unzip this starter, then commit/push the files to your repo's default branch (usually `main`).

3. **Enable GitHub Pages**
   - Go to **Settings → Pages**.
   - **Source:** “Deploy from a branch”
   - **Branch:** `main` and select `/ (root)`.
   - Click **Save**.

4. **Set your custom domain (optional but recommended)**
   - In **Settings → Pages → Custom domain**, enter your domain, e.g. `www.example.com`.
   - GitHub will create a `CNAME` file automatically (this starter already includes one with `www.example.com` — edit if needed).
   - Tick **Enforce HTTPS** once the certificate is ready.

5. **DNS records (simplest setup)**
   - **For `www` (recommended canonical):** create a CNAME record
     - **Host/Name:** `www`
     - **Value/Target:** `USERNAME.github.io`
   - **For the root domain (`example.com`):** create A records pointing to GitHub Pages:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153

   In GitHub Pages, set the custom domain to the **`www`** version (e.g., `www.example.com`). With the A records in place, GitHub will redirect the root domain to `www`.

6. **Edit navigation**
   - Open `_config.yml` and edit the `nav:` list to add/remove pages.
   - Create new pages as Markdown files with YAML front matter:

     ```md
     ---
     layout: default
     title: New Page
     permalink: /new-page
     ---

     Page content in Markdown.
     ```

## Local preview (optional)
If you want to run the site locally, install Jekyll:

```bash
gem install bundler jekyll   # Requires Ruby
jekyll serve
```

Then open http://127.0.0.1:4000

---

**Tip:** Keep it simple. You don't need any build workflows — GitHub will build Jekyll for you.
