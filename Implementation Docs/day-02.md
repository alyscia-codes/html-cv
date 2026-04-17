# Week 1: Foundation — Setup, Structure & Core HTML

## Day 2: HTML Boilerplate

> Build the base `index.html` with DOCTYPE, `<html>`, `<head>`, and `<body>` tags — nothing else.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code if not already open | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` project in sidebar | `code not found` → Open VS Code manually from Applications/Start Menu |
| 2 | Click `index.html` in the Explorer sidebar to open it | VS Code — Explorer Panel | — | `index.html` opens in the editor tab | File not in sidebar → Run `ls` in Terminal to confirm file exists |
| 3 | Select all existing content in the file | VS Code — `index.html` | `Ctrl+A` (Windows) or `Cmd+A` (Mac) | All text highlighted | Nothing highlights → Click inside the editor first |
| 4 | Delete all selected content | VS Code — `index.html` | `Backspace` or `Delete` | File is completely empty | Content remains → Repeat Steps 3–4 |
| 5 | Type the DOCTYPE declaration on line 1 | VS Code — `index.html` | `<!DOCTYPE html>` | Line 1 shows `<!DOCTYPE html>` | Autocomplete interferes → Press Escape then retype |
| 6 | Press Enter to move to line 2 | VS Code — `index.html` | `Enter` | Cursor moves to line 2 | — |
| 7 | Type the opening `<html>` tag with language attribute | VS Code — `index.html` | `<html lang="en">` | Line 2 shows `<html lang="en">` | VS Code autocompletes wrong tag → Press Escape and retype manually |
| 8 | Press Enter to move to line 3 | VS Code — `index.html` | `Enter` | Cursor on line 3 | — |
| 9 | Type the opening `<head>` tag | VS Code — `index.html` | `<head>` | Line 3 shows `<head>` | — |
| 10 | Press Enter to create an empty line 4 (placeholder for head content) | VS Code — `index.html` | `Enter` | Blank line 4 created | — |
| 11 | Type the closing `</head>` tag on line 5 | VS Code — `index.html` | `</head>` | Line 5 shows `</head>` | — |
| 12 | Press Enter to move to line 6 | VS Code — `index.html` | `Enter` | Cursor on line 6 | — |
| 13 | Type the opening `<body>` tag | VS Code — `index.html` | `<body>` | Line 6 shows `<body>` | — |
| 14 | Press Enter to create an empty line 7 (placeholder for body content) | VS Code — `index.html` | `Enter` | Blank line 7 created | — |
| 15 | Type the closing `</body>` tag on line 8 | VS Code — `index.html` | `</body>` | Line 8 shows `</body>` | — |
| 16 | Press Enter to move to line 9 | VS Code — `index.html` | `Enter` | Cursor on line 9 | — |
| 17 | Type the closing `</html>` tag | VS Code — `index.html` | `</html>` | Line 9 shows `</html>` | — |
| 18 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Tab no longer shows a dot (unsaved indicator disappears) | Dot remains → Try File → Save from menu |
| 19 | Verify the complete file looks correct | VS Code — `index.html` | — | See box [DAY2-VERIFY] below for expected final output | Structure looks wrong → See box [DAY2-VERIFY] and compare line by line |
| 20 | Open index.html in a browser to confirm it loads blank | Browser | See box [OPEN-BROWSER] below | A blank white page loads with no errors | Error page loads → Check file path is correct |
| 21 | Open browser DevTools to check for HTML errors | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | DevTools panel opens | Panel doesn't open → Right-click page → Inspect |
| 22 | Click the "Console" tab in DevTools | Browser — DevTools | — | Console tab is active and showing | Tab not visible → Click the `>>` arrow to find hidden tabs |
| 23 | Confirm no red errors appear in the Console | Browser — DevTools Console | — | Console is empty or shows no red error messages | Red errors visible → Compare your file to box [DAY2-VERIFY] and fix mismatches |
| 24 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 25 | Commit with a descriptive message | Terminal | `git commit -m "feat: add HTML boilerplate structure"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 18 |
| 26 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 27 | Reload your GitHub repo page and click index.html to verify content | Browser — Repo Page | `F5` or `Cmd+R` | File shows your boilerplate HTML when clicked | Old content showing → Wait 15 seconds and refresh again |

---

### 📋 Box: DAY2-VERIFY

Your completed `index.html` should look exactly like this:

```html
<!DOCTYPE html>
<html lang="en">
<head>

</head>
<body>

</body>
</html>
```

9 lines total. Nothing else. No content, no meta tags yet — those come on Day 3.

---

### 📋 Box: OPEN-BROWSER

To open index.html directly in your browser:

- **Mac:** In Terminal, run `open index.html`
- **Windows:** In Terminal, run `start index.html`
- **Alternative (any OS):** In VS Code, right-click `index.html` in the Explorer panel → "Open with Live Server" (requires Live Server extension) or "Reveal in Finder/Explorer" then double-click the file
