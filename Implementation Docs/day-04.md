# Week 1: Foundation — Setup, Structure & Core HTML

## Day 4: Head Section — Open Graph Tags

> Add all Open Graph `<meta>` tags (og:title, og:description, og:image, og:url, og:type) to `<head>`.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Click at the end of the `<meta name="author">` line to place cursor there | VS Code — `index.html` | — | Cursor blinks at end of author line | Can't find it → Use `Ctrl+F` / `Cmd+F` and search `author` |
| 4 | Press Enter to create a new line below author | VS Code — `index.html` | `Enter` | Blank line created below author tag | — |
| 5 | Type a comment to label the OG tag section | VS Code — `index.html` | `<!-- Open Graph Tags -->` | Comment appears as a section label | — |
| 6 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 7 | Type the og:title tag | VS Code — `index.html` | `<meta property="og:title" content="Your Name — Junior Frontend Developer">` | og:title tag appears | Replace `Your Name` with your actual name |
| 8 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 9 | Type the og:description tag | VS Code — `index.html` | See box [OG-DESC] below | og:description tag appears | Quotes look broken → Confirm no smart/curly quotes — use straight quotes only |
| 10 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 11 | Type the og:type tag | VS Code — `index.html` | `<meta property="og:type" content="website">` | og:type tag appears | — |
| 12 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 13 | Type the og:url tag with a placeholder URL for now | VS Code — `index.html` | See box [OG-URL] below | og:url tag appears with placeholder | This will be updated on Day 22 when GitHub Pages is live |
| 14 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 15 | Type the og:image tag with a placeholder | VS Code — `index.html` | See box [OG-IMAGE] below | og:image tag appears | This will be updated when you have a real image URL |
| 16 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 17 | Verify the OG block looks correct | VS Code — `index.html` | — | See box [DAY4-VERIFY] and compare line by line | Something wrong → Fix mismatched quotes or missing `property=` attribute |
| 18 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Blank white page loads with your name in the tab title | Page errors → Check `<head>` for unclosed tags |
| 19 | Open DevTools | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | DevTools panel opens | — |
| 20 | Click the "Elements" tab | Browser — DevTools | — | Full HTML tree visible | — |
| 21 | Expand the `<head>` element | Browser — DevTools Elements | — | All tags visible including new OG tags | Tags missing → Confirm file saved and refresh page with `Cmd+R` / `F5` |
| 22 | Confirm all 5 OG tags present: og:title, og:description, og:type, og:url, og:image | Browser — DevTools Elements | — | 5 OG `<meta>` tags visible inside `<head>` | Missing tags → Return to VS Code and add them |
| 23 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 24 | Navigate to the LinkedIn Post Inspector to test OG tags | Browser | `https://www.linkedin.com/post-inspector/` | LinkedIn Post Inspector page loads | Won't load → Log into LinkedIn first |
| 25 | Type your placeholder URL into the Inspect field | Browser — LinkedIn Post Inspector | `https://yourusername.github.io/html-cv` | URL accepted in the field | Field rejects input → Ensure URL starts with `https://` |
| 26 | Click the "Inspect" button | Browser — LinkedIn Post Inspector | — | Preview shows — note it will be incomplete since page isn't live yet | Error: can't fetch URL → Expected at this stage, site isn't deployed yet |
| 27 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 28 | Commit with a descriptive message | Terminal | `git commit -m "feat: add Open Graph meta tags to head section"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 16 |
| 29 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 30 | Reload GitHub repo, click index.html, confirm OG tags visible in file | Browser — Repo Page | `F5` or `Cmd+R` | OG meta tags visible in the raw file on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: OG-DESC

```html
<meta property="og:description" content="Junior Frontend Developer skilled in HTML, CSS, JavaScript, and Responsive Web Design. View my CV and career history.">

```html
Keep under 200 characters. This is what appears as the preview blurb when someone shares your CV link on LinkedIn or Slack.

---

### 📋 Box: OG-URL

```html
<meta property="og:url" content="https://yourusername.github.io/html-cv">
```

Replace `yourusername` with your actual GitHub username. This URL won't be live until Day 22 — that's fine, add it now so you don't forget.

---

### 📋 Box: OG-IMAGE

```html
<meta property="og:image" content="https://yourusername.github.io/html-cv/preview.png">
```

This image doesn't exist yet — you'll add a real screenshot on Day 22 when the site is live. For now this is a placeholder so the tag structure is correct.

---

### 📋 Box: DAY4-VERIFY

Your full `<head>` block should now look like this:

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Name — Junior Frontend Developer</title>
  <meta name="description" content="CV of Your Name — Junior Frontend Developer specializing in HTML, CSS, JavaScript, and Responsive Web Design.">
  <meta name="keywords" content="HTML, CSS, JavaScript, Frontend Developer, Responsive Web Design, Figma, Technical Writing">
  <meta name="author" content="Your Full Name">
  <!-- Open Graph Tags -->
  <meta property="og:title" content="Your Name — Junior Frontend Developer">
  <meta property="og:description" content="Junior Frontend Developer skilled in HTML, CSS, JavaScript, and Responsive Web Design. View my CV and career history.">
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://yourusername.github.io/html-cv">
  <meta property="og:image" content="https://yourusername.github.io/html-cv/preview.png">
</head>
```

13 lines inside `<head>`. Favicon comes tomorrow on Day 5.
