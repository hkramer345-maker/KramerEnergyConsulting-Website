# Branding & Logo

Your original uploaded logo is now used directly on the site:
- Source file: `images/logo.svg`
- The image includes its own dark background and is intentionally shown as-is.

## Use HTML/CSS to display your image (without moving files)
If your image already exists in your project, just point the HTML `src` to that file path.
Do **not** move or create image files for this step.

```html
<section class="logo-section">
  <img src="images/my-picture.png" alt="Kramer Consulting logo" class="center-logo">
</section>
```

```css
.logo-section {
  display: flex;
  justify-content: center;
  padding: 24px 16px;
}

.center-logo {
  width: min(320px, 78vw);
  height: auto;
  display: block;
  border-radius: 14px;
}
```

Replace only the `src` value with your real file path (example: `images/my-picture.png`).

## If you want to swap to a new logo later
1. Replace `images/logo.svg` with your new file.
2. Keep the same filename, or update the `img src` in:
   - `index.html`
   - `about.html`
   - `contact.html`
   - `publications.html`

## Theme colors
The site colors are controlled in `style.css` variables at the top and are currently tuned to match the uploaded logo's greens and dark background.

## Save this website to your GitHub account (step-by-step)

If you want the **quickest possible path**, follow this exact checklist in order.

### Super simple checklist (Windows-friendly)
1. **Install Git first** (this fixes `git is not recognized`):
   - Go to: https://git-scm.com/download/win
   - Install with default options.
2. Open **Git Bash** (not PowerShell).
3. Run these exact commands:

```bash
git clone https://github.com/hkramer345-maker/KramerEnergyConsulting-Website.git
cd KramerEnergyConsulting-Website
git checkout -b work
git push -u origin work:main
```

4. Refresh GitHub and confirm the newest commits/files appear.

### If you already have the project on your computer
Use this only if you already have a local project folder with your newest work:

```bash
cd "C:/path/to/your/project/folder"
git remote set-url origin https://github.com/hkramer345-maker/KramerEnergyConsulting-Website.git
git push -u origin work:main
```

### If you see `nothing to commit` and old commits like `1c5011b Delete logo.png`
That means your local folder is synced to the **old remote history**, not the updated files from this coding workspace.

Do this:
1. In your local repo folder, confirm the top commit:

```bash
git log --oneline -n 1
```

2. If it still shows `1c5011b Delete logo.png`, add the new files/edits you received from this chat into that same folder.
3. Then run:

```bash
git add .
git commit -m "Add latest website updates from Codex session"
git push origin main
```

If Git says `nothing to commit`, no new files were copied into the repo yet.

### Why your screenshot failed
- `cd /workspace/...` failed because that path exists in this cloud coding environment, not on your Windows PC.
- `||` failed because PowerShell handles that differently.
- `git` was not found because Git is not installed (or not in PATH).

### If Git asks for login
- Username: your GitHub username (`hkramer345-maker`)
- Password box: use a **GitHub Personal Access Token (PAT)**, not your normal password.

### Save future changes
Each time you edit the site later:

```bash
git add .
git commit -m "Describe what you changed"
git push
```
