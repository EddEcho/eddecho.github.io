# justedd.com — Personal landing page

Personal portfolio of **Edson Zegarra**, Cloud Support Engineer.

- **Live (GitHub Pages):** https://eddecho.github.io
- **Custom domain (pending purchase):** https://justedd.com

Plain HTML + CSS, no build step, no dependencies. Every push to `main` deploys automatically via GitHub Pages.

## Connecting the domain justedd.com

Once the domain is purchased, do this:

### 1. DNS records (at the registrar)

| Type  | Host | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | eddecho.github.io      |

### 2. Tell GitHub Pages about the domain

Either in the UI (**Settings → Pages → Custom domain → `justedd.com`**, then check **Enforce HTTPS** once available), or via CLI:

```bash
gh api repos/EddEcho/eddecho.github.io/pages -X PUT -f cname=justedd.com
```

HTTPS can take up to an hour after DNS propagates.

## Editing

Everything lives in `index.html` (content + styles inline). Edit, commit, push — done.
