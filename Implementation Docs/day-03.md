# Week 1: Foundation — Setup, Structure & Core HTML

## Day 3: Head Section — SEO & Meta Tags

> Add all required SEO `<meta>` tags (charset, viewport, description, keywords, author) to `<head>`.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Click on the blank line 4 (inside `<head>`) to place your cursor there | VS Code — `index.html` | — | Cursor is blinking on line 4 between `<head>` and `</head>` | Line 4 isn't blank → Press Enter after `<head>` to create space |
| 4 | Type the charset meta tag | VS Code — `index.html` | `<meta charset="UTF-8">` | Line 4 shows the charset tag | Autocomplete suggests wrong tag → Press Escape and retype |
| 5 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line inside `<head>` | — |
| 6 | Type the viewport meta tag | VS Code — `index.html` | `<meta name="viewport" content="width=device-width, initial-scale=1.0">` | Viewport tag appears on its own line | Tag wraps oddly → That's fine, it's one line of code |
| 7 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 8 | Type the title tag with your name | VS Code — `index.html` | `<title>Your Name — Junior Frontend Developer</title>` | Title tag appears | Replace `Your Name` with your actual name |
| 9 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 10 | Type the description meta tag | VS Code — `index.html` | See box [META-DESC] below | Description tag appears on its own line | Tag looks broken → Confirm opening and closing quotes match |
| 11 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 12 | Type the keywords meta tag | VS Code — `index.html` | See box [META-KEYWORDS] below | Keywords tag appears on its own line | — |
| 13 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 14 | Type the author meta tag with your name | VS Code — `index.html` | `<meta name="author" content="Your Full Name">` | Author tag appears | Replace `Your Full Name` with your actual name |
| 15 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 16 | Verify the full `<head>` block looks correct | VS Code — `index.html` | — | See box [DAY3-VERIFY] below and compare line by line | Something missing → Add the missing tag between `<head>` and `</head>` |
| 17 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Blank white page loads — browser tab now shows your name as the title | Tab still says "index.html" → Confirm `<title>` tag was saved correctly |
| 18 | Check the browser tab title shows your name | Browser — Tab Bar | — | Tab reads `Your Name — Junior Frontend Developer` | Shows wrong text → Re-check `<title>` tag content in VS Code |
| 19 | Open DevTools | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | DevTools panel opens | — |
| 20 | Click the "Elements" tab in DevTools | Browser — DevTools | — | Elements tab shows your full HTML tree | Tab not visible → Click `>>` to find hidden tabs |
| 21 | Click the `<head>` element in the Elements panel to expand it | Browser — DevTools Elements | — | All 5 meta tags + title tag visible inside `<head>` | Tags missing → Confirm file was saved and page was refreshed |
| 22 | Confirm all 5 tags are present: charset, viewport, title, description, keywords, author | Browser — DevTools Elements | — | 6 tags visible nested inside `<head>` | Missing a tag → Go back to VS Code and add it |
| 23 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 24 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 25 | Commit with a descriptive message | Terminal | `git commit -m "feat: add SEO meta tags to head section"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 15 |
| 26 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 27 | Reload GitHub repo, click index.html, confirm meta tags are visible in the file | Browser — Repo Page | `F5` or `Cmd+R` | Meta tags visible in the file preview on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: META-DESC

```html
<meta name="description" content="CV of Your Name — Junior Frontend Developer specializing in HTML, CSS, JavaScript, and Responsive Web Design.">
```

Replace `Your Name` with your actual name. Keep this under 160 characters — Google truncates anything longer.

---

### 📋 Box: META-KEYWORDS

```html
<meta name="keywords" content="HTML, CSS, JavaScript, Frontend Developer, Responsive Web Design, Figma, Technical Writing">
```

Edit the keywords to match your actual skills listed in your CV.

---

### 📋 Box: DAY3-VERIFY

Your `<head>` block should look exactly like this (with your real name/details substituted):

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Name — Junior Frontend Developer</title>
  <meta name="description" content="CV of Your Name — Junior Frontend Developer specializing in HTML, CSS, JavaScript, and Responsive Web Design.">
  <meta name="keywords" content="HTML, CSS, JavaScript, Frontend Developer, Responsive Web Design, Figma, Technical Writing">
  <meta name="author" content="Your Full Name">
</head>
```

7 lines inside `<head>`. Nothing else yet — OG tags and favicon come on Days 4 and 5.
