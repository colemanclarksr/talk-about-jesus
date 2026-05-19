# Talk About Jesus

A one-page mission site for Life Group. Auto-detects device and routes mobile users to the vertical reels version, desktop users to the standard version.

**Live URL after deployment:** `https://colemanclarksr.github.io/talk-about-jesus`

## What's inside

| File | Purpose |
|------|---------|
| `index.html` | Landing page, auto-redirects based on device |
| `desktop.html` | Standard 16:9 mission video for desktop/laptop |
| `reels.html` | Vertical 9:16 version for mobile, stories, reels |
| `music.m4a` | Brother Joe's full track (4 minutes) |
| `baptism.mp4` | Joe and Coleman's full baptism footage (58 seconds) |
| `README.md` | This file |

## How the experience flows

1. User lands on the page, taps the gold play button
2. Brother Joe's music starts at 40% volume
3. 11 mission scenes play with fade transitions (about 41 seconds)
4. Baptism scene begins. Text fades after 6 seconds. Baptism video plays full 58 seconds clean while music continues
5. Music fades out over 3 seconds, YouTube "Watch Before Friday" video loads and auto-plays
6. Replay button to restart

**Total runtime before YouTube end screen: about 99 seconds**

## Deploy to GitHub Pages (web upload, no terminal)

1. On your new GitHub repo page (talk-about-jesus), click **"uploading an existing file"**
2. Drag all 6 files from the unzipped folder into the upload box
3. Type a commit message like "Initial site"
4. Click green **"Commit changes"** button
5. Go to **Settings > Pages**
6. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**
7. Click **Save**
8. Wait 1-2 minutes
9. Site goes live at: `https://colemanclarksr.github.io/talk-about-jesus`

## Deploy via command line (alternative)

```bash
cd talk-about-jesus
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/colemanclarksr/talk-about-jesus.git
git push -u origin main
```

Then Settings > Pages, same as above.

## Share

Once live, just share the root URL. The landing page handles routing:
- Phones get `reels.html` (vertical)
- Desktops get `desktop.html` (standard)

## Swap content later

- **Change YouTube video:** Edit `YOUTUBE_ID` in both `desktop.html` and `reels.html`
- **Change music:** Replace `music.m4a` (keep same filename)
- **Change baptism video:** Replace `baptism.mp4` (keep same filename, mp4 format)
- **Change mission text:** Edit the `.scene` blocks in both HTML files

## Total payload

- Music: 3.8 MB (full 4 minutes)
- Baptism video: 11 MB (full 58 seconds, compressed from 80 MB)
- HTML + everything else: under 50 KB
- **Total: ~15 MB** — fast load even on cellular
