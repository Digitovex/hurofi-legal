# hurofi-legal

Public GitHub Pages host for Hurofi store-listing legal documents.

**Contents only:** `index.html`, `privacy.html`, `terms.html` (verbatim from `hurofi-app/docs/legal/*-FINAL.md`).

## Deploy (Digitovex org — manual steps)

`gh` as `alaaalsarayrah` cannot create repos under `Digitovex`. An org owner must:

1. Open https://github.com/organizations/Digitovex/settings/member_privileges — ensure members can create repositories, **or**
2. GitHub → **Digitovex** → **New repository** → name `hurofi-legal` → **Public** → Create (empty, no README).

Then from this folder:

```powershell
cd D:\hurofi-legal
git branch -M main
git remote add origin https://github.com/Digitovex/hurofi-legal.git
git commit -m "chore: initial privacy and terms pages for GitHub Pages"
git push -u origin main
```

Enable Pages: **Settings → Pages → Build from branch → `main` / root → Save**.

Verify:

- https://digitovex.github.io/hurofi-legal/privacy.html
- https://digitovex.github.io/hurofi-legal/terms.html

`hurofi-app` `src/constants/legal.js` already points to these URLs.
