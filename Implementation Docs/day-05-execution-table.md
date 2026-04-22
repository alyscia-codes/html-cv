# Week 1: Foundation — Setup, Structure & Core HTML

## Day 5: Favicon

> Create or source a favicon, link it in `<head>`, verify it appears in browser tab.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Navigate to a free favicon generator | Browser | `https://favicon.io` | Favicon.io homepage loads | Won't load → Try `https://realfavicongenerator.net` instead |
| 3 | Click "Favicon Generator" — Text option | Browser — Favicon.io | — | Text-based favicon creator opens | Don't see Text option → Look for tabs along the top of the page |
| 4 | Type your initials into the Text field | Browser — Favicon.io Text Generator | Your initials (e.g. `AJ`) | Initials appear in the live preview | Preview doesn't update → Click outside the field after typing |
| 5 | Choose a Background color that suits your personal brand | Browser — Favicon.io | Click any color swatch | Selected color fills the favicon background in preview | — |
| 6 | Choose a Font from the dropdown | Browser — Favicon.io | Click the Font dropdown → select any font | Font updates in the preview | — |
| 7 | Click the "Download" button | Browser — Favicon.io | — | A `.zip` file downloads to your Downloads folder | Nothing downloads → Check browser download bar at bottom of screen |
| 8 | Open your Downloads folder | File Manager | — | Downloads folder opens | — |
| 9 | Double-click the downloaded `.zip` file to extract it | File Manager | — | Folder extracted containing multiple favicon files | Can't extract → Right-click → Extract All (Windows) or double-click (Mac) |
| 10 | Open the extracted folder and locate `favicon.ico` | File Manager | — | `favicon.ico` file visible in the extracted folder | No `.ico` file → Use `favicon-32x32.png` instead — same steps apply |
| 11 | Copy `favicon.ico` | File Manager | `Ctrl+C` (Windows) or `Cmd+C` (Mac) | File copied to clipboard | — |
| 12 | Navigate to your `html-cv` project folder on the Desktop | File Manager | — | `html-cv` folder contents visible | Can't find it → Look on Desktop or check `~/Desktop/html-cv` in Terminal |
| 13 | Paste `favicon.ico` into the root of the `html-cv` folder | File Manager | `Ctrl+V` (Windows) or `Cmd+V` (Mac) | `favicon.ico` now sits alongside `index.html` in the folder | Paste disabled → Try drag-and-drop from Downloads to the html-cv folder |
| 14 | Confirm `favicon.ico` is visible in VS Code sidebar | VS Code — Explorer Panel | — | `favicon.ico` appears in the file list next to `index.html` | Not showing → Click the Refresh icon in the Explorer panel or restart VS Code |
| 15 | Click `index.html` to open it in the editor | VS Code — Explorer Panel | — | `index.html` opens in editor tab | — |
| 16 | Click at the end of the `og:image` meta tag line to place cursor there | VS Code — `index.html` | — | Cursor blinks at end of the og:image line | Can't find it → Use `Cmd+F` / `Ctrl+F` and search `og:image` |
| 17 | Press Enter to create a new line | VS Code — `index.html` | `Enter` | Blank line created below og:image | — |
| 18 | Type a comment to label the favicon section | VS Code — `index.html` | `<!-- Favicon -->` | Comment appears as a section label | — |
| 19 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 20 | Type the favicon link tag | VS Code — `index.html` | `<link rel="icon" type="image/x-icon" href="favicon.ico">` | Favicon link tag appears on its own line | Autocomplete changes the tag → Press Escape and retype manually |
| 21 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 22 | Verify the bottom of your `<head>` block looks correct | VS Code — `index.html` | — | See box [DAY5-VERIFY] below and compare | Something wrong → Check `href="favicon.ico"` matches the exact filename in your folder |
| 23 | Open index.html in the browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Blank white page loads | Page errors → Check for unclosed tags in `<head>` |
| 24 | Look at the browser tab | Browser — Tab Bar | — | A small icon (your initials) appears in the tab next to the page title | No icon showing → See box [FAVICON-TROUBLESHOOT] below |
| 25 | Hard-refresh the browser to force favicon reload | Browser | `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows) | Tab icon updates if it was cached | Still no icon → See box [FAVICON-TROUBLESHOOT] below |
| 26 | Stage all changes including the new favicon file | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 27 | Commit with a descriptive message | Terminal | `git commit -m "feat: add favicon to project and link in head"` | Output shows `2 files changed` (index.html + favicon.ico) | Shows `1 file changed` → favicon.ico wasn't staged — run `git status` to check |
| 28 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 29 | Reload your GitHub repo page and confirm both files appear | Browser — Repo Page | `F5` or `Cmd+R` | Both `index.html` and `favicon.ico` visible in file list | favicon.ico missing → Confirm it was inside the `html-cv` folder, not just Downloads |

---

### 📋 Box: DAY5-VERIFY

The bottom of your `<head>` block should now include the favicon line:

```html
  <meta property="og:url" content="https://yourusername.github.io/html-cv">
  <meta property="og:image" content="https://yourusername.github.io/html-cv/preview.png">
  <!-- Favicon -->
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>

```text
`favicon.ico` must be in the same folder as `index.html` for this path to work.

---

### 📋 Box: FAVICON-TROUBLESHOOT

Favicon not appearing in the tab? Work through these in order:

1. **Check the file is in the right place** — open Terminal and run `ls ~/Desktop/html-cv` — you should see both `index.html` and `favicon.ico` listed
2. **Check the filename matches exactly** — the `href` in your tag must be `favicon.ico` not `Favicon.ico` or `favicon.png` — filenames are case-sensitive
3. **Hard refresh** — `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows) clears the browser's favicon cache
4. **Try a different browser** — Chrome caches favicons aggressively; try Firefox to confirm the file works
5. **If using a `.png` instead of `.ico`** — change the link tag to: `<link rel="icon" type="image/png" href="favicon-32x32.png">`
