# 2006.phonofestivalen.no

Recreation of 2006 version of Phonofestivalen using Internet Archive assets.

## GitHub Pages (subdomain)

Published at **https://2006.phonofestivalen.no** when DNS and GitHub Pages are configured.

### 1. Repository visibility

On the **srib-dev** org **Free** plan, GitHub Pages only works for **public** repositories. Either:

- Make this repo public: **Settings → General → Danger zone → Change visibility**, or  
- Use a paid plan that includes Pages for private repos.

### 2. Enable Pages

After the repo is public:

1. **Settings → Pages**
2. **Source:** Deploy from a branch  
3. **Branch:** `main` / **/(root)**  
4. **Custom domain:** `2006.phonofestivalen.no` (matches the `CNAME` file in the repo root)  
5. Save, wait for DNS check, then enable **Enforce HTTPS**

Until the custom domain is live, the site is also at  
`https://srib-dev.github.io/2006.phonofestivalen.no/` (project URL).

### 3. DNS (phonofestivalen.no)

At your DNS host, add:

| Type  | Name  | Value              |
|-------|-------|--------------------|
| CNAME | `2006` | `srib-dev.github.io` |

Use only the hostname `srib-dev.github.io` (no `https://`, no path). Propagation can take up to 24–48 hours.

### 4. Push changes

Commit and push `index.html`, `CNAME`, and `.nojekyll` so the site root and custom domain file are on `main`.
