# My Jekyll Site

A simple text-based site built with Jekyll, ready to host free on GitHub Pages.

## Structure

```
.
├── _config.yml     # Site settings (title, description, theme)
├── index.md        # Homepage content
├── about.md        # Example second page (appears at /about/)
├── _posts/         # Optional: dated blog-style posts go here
├── Gemfile         # Ruby dependencies (matches GitHub Pages' build environment)
└── .gitignore
```

## Adding content

- Edit `index.md` for your homepage text.
- Edit or duplicate `about.md` to add more pages. Each page needs a "front matter" block at the top:
  ```
  ---
  layout: page
  title: Page Title
  permalink: /your-url-path/
  ---
  ```
- To add a blog-style post, create a file in `_posts/` named like `2026-09-01-my-post-title.md` with:
  ```
  ---
  layout: post
  title: "My Post Title"
  ---
  Your text here.
  ```

## Running locally (optional, requires Ruby)

```bash
bundle install
bundle exec jekyll serve
```

Then visit http://localhost:4000

## Publishing to GitHub Pages (free)

1. Create a new repository on GitHub (e.g. `my-site`) and push this folder's contents to it.
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment", set Source to **Deploy from a branch**, branch to **main** (or your default branch), folder to **/ (root)**. Save.
4. GitHub will build and publish automatically. Your site will be live at:
   - `https://YOUR_USERNAME.github.io/REPO_NAME/`
5. Once you know that URL, update `_config.yml`:
   ```yaml
   baseurl: "/REPO_NAME"
   url: "https://YOUR_USERNAME.github.io"
   ```
   Commit and push — GitHub Pages rebuilds automatically on every push to the branch you configured.

No server, no Node, no extra hosting needed — this is fully static and free.
