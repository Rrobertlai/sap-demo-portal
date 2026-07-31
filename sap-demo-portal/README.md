# SAP DEMO Portal

A single-page interactive demo aggregation site for SAP Analytics Cloud, SAP Business Data Cloud + Databricks, AI & Joule, and SAP Demo Environments.

**Live URL** → `https://<your-github-username>.github.io/sap-demo-portal/`

---

## Features

- **Tab navigation** — filter by SAC / BDC+Databricks / AI & Joule / Demo Env / Datasphere
- **SAC sub-filters** — Finance, Procurement, Sales, Other
- **Real-time search** — filter by title, Chinese name, or tags (`Ctrl+K` shortcut)
- **Clickable cards** — click any card to open the demo in a new tab
- **45 demo resources** across 6 categories

---

## Quick Deploy to GitHub Pages

### Step 1 — Create a new GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `sap-demo-portal`
3. Set to **Public**
4. Click **Create repository**

### Step 2 — Upload files

Drag and drop all files from this ZIP (keeping the folder structure) into the new repo, **or** use the commands below:

```bash
git init
git add .
git commit -m "Initial commit: SAP DEMO Portal"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/sap-demo-portal.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Save

The site will be live at:
```
https://<YOUR_USERNAME>.github.io/sap-demo-portal/
```

> Deployment typically completes within 1–2 minutes after the first push.

---

## Adding Your Own SAC Reports

Open `index.html` and find the `DEMOS` array. Add a new entry following this pattern:

```javascript
{
  id: 46,
  title: "財務分析報表",
  zh: "財務報表",
  desc: "您的報表描述",
  url: "https://your-sac-tenant.jp10.sapanalytics.cloud/...",
  cat: "sac",          // sac | bdc | ai | demo-env | datasphere
  sub: "finance",      // finance | procurement | sales | other
  icon: "💰",
  badge: "Finance",
  badgeCls: "",        // "" (blue) | g (green) | o (amber) | p (purple) | r (red)
  region: "jp10",
  tags: ["Finance", "SAC", "Custom"]
},
```

---

## License

Internal SAP use only.
