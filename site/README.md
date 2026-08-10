# ideagent.github.io — Site Source

This folder contains the static site files for **https://ideagent.github.io**.

## 🚀 Deploying (one-time setup)

1. **Create a new public repository** named exactly `ideagent.github.io` in the `ideagent` organization on GitHub.
2. **Copy these files** (`index.html`, `styles.css`, `CNAME` if using a custom domain) into the root of that new repo.
3. Push to the `main` branch.
4. GitHub Pages is enabled automatically for `<org>.github.io` repos — no extra configuration needed.
5. Your site will be live at **https://ideagent.github.io** within a minute or two.

## 🌐 Optional: Custom domain (e.g. ideagent.io)

1. Edit the `CNAME` file so it contains just your domain, e.g. `ideagent.io`.
2. In your DNS provider, add A records pointing your apex domain to GitHub Pages IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
3. In the new repo → Settings → Pages → Custom domain, enter `ideagent.io` and enable "Enforce HTTPS".

## ✏️ Editing the site

- `index.html` — all page content and structure
- `styles.css` — all visual styling (dark theme, responsive layout)
