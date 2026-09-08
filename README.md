# islamulhaque.com — site source

Static site: `index.html`, `research.html`, `teaching.html`, `cv.html`, `style.css`.
No build step. Edit the HTML, commit, and GitHub Pages redeploys in about a minute.

## Deploy on GitHub Pages (one-time, ~10 minutes)
1. Create a public GitHub repository named `islamulhaque.com` (any name works).
2. Upload every file in this folder to the repository root (drag-and-drop on github.com works).
3. Repository → Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
4. Under "Custom domain" enter `islamulhaque.com` and save (the `CNAME` file already matches). Tick "Enforce HTTPS" once it becomes available (can take up to an hour).

## Point the domain (Namecheap)
Domain List → Manage → Advanced DNS. Remove the existing Google Sites records, then add:

| Type  | Host | Value                 |
|-------|------|-----------------------|
| A     | @    | 185.199.108.153       |
| A     | @    | 185.199.109.153       |
| A     | @    | 185.199.110.153       |
| A     | @    | 185.199.111.153       |
| CNAME | www  | `<github-username>.github.io.` |

DNS changes propagate within an hour, usually minutes. The `www` host currently points at Google Sites (ghs.googlehosted.com) and the bare domain at Namecheap URL forwarding; delete both before adding the records above. Keep the Google Site saved as a backup until the new site is live.
