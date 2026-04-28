# Week 1: Foundation — Setup, Structure & Core HTML

## Day 7: Week 1 Audit

> Validate HTML via W3C validator, fix all errors, commit clean checkpoint.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Open index.html in the editor | VS Code — Explorer Panel | — | `index.html` opens in editor tab | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Visually scan the entire file top to bottom | VS Code — `index.html` | — | No obvious unclosed tags or typos visible | Something looks wrong → Compare against box [DAY7-FULL-VERIFY] below |
| 4 | Navigate to the W3C HTML Validator | Browser | `https://validator.w3.org` | W3C Validator homepage loads | Won't load → Try again in 30 seconds, site occasionally slow |
| 5 | Click the "Validate by Direct Input" tab | Browser — W3C Validator | — | A large text area appears for pasting HTML | Tab not visible → Look along the top of the validator page |
| 6 | Select all content in index.html | VS Code — `index.html` | `Ctrl+A` (Windows) or `Cmd+A` (Mac) | All file content highlighted | Nothing highlights → Click inside the editor first |
| 7 | Copy the selected content | VS Code — `index.html` | `Ctrl+C` (Windows) or `Cmd+C` (Mac) | Content copied to clipboard | — |
| 8 | Click inside the W3C text area and paste your code | Browser — W3C Validator | `Ctrl+V` (Windows) or `Cmd+V` (Mac) | Your full HTML appears in the text area | Nothing pasted → Try right-click → Paste |
| 9 | Click the "Check" button | Browser — W3C Validator | — | Validation results load below the form | Page doesn't respond → Wait 10 seconds, validator can be slow |
| 10 | Read the results summary at the top | Browser — W3C Validator Results | — | Green banner: "Document checking completed. No errors or warnings to show." | Red/yellow banner showing errors → Proceed to Step 11 |
| 11 | Read the first error message listed | Browser — W3C Validator Results | — | Error description shows line number and tag name | Multiple errors → Fix one at a time starting from the top — fixing early errors often clears later ones |
| 12 | Note the line number shown in the error | Browser — W3C Validator Results | — | Line number visible next to the error (e.g. "Line 4, Column 3") | No line number → Read the error description carefully for the tag name |
| 13 | Navigate to that line number in VS Code | VS Code — `index.html` | `Ctrl+G` (Windows) or `Cmd+G` (Mac) then type the line number | Cursor jumps to the flagged line | Shortcut doesn't work → Scroll manually or use `Ctrl+F` to search for the tag |
| 14 | Fix the error on that line | VS Code — `index.html` | See box [COMMON-ERRORS] below for fixes | Error resolved in code | Unsure how to fix → Copy the full error message and reference box [COMMON-ERRORS] |
| 15 | Save the file after each fix | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears | — |
| 16 | Re-paste the updated code into W3C and re-run Check | Browser — W3C Validator | Repeat Steps 6–9 | Updated results load | — |
| 17 | Repeat Steps 11–16 until green banner appears | Browser — W3C Validator | — | "No errors or warnings to show" green banner | Stuck on same error → See box [COMMON-ERRORS] for that specific fix |
| 18 | Take a screenshot of the green W3C result | Browser | `Cmd+Shift+4` (Mac) or `Win+Shift+S` (Windows) | Screenshot saved to Desktop | — |
| 19 | Run a second check — paste code into the Nu Html Checker | Browser | `https://validator.w3.org/nu/` | Nu Html Checker loads | Won't load → Skip this step, W3C pass is sufficient |
| 20 | Paste your HTML and click "Check" | Browser — Nu Html Checker | Repeat Steps 6–9 | Results load | — |
| 21 | Confirm no errors or warnings appear | Browser — Nu Html Checker Results | — | "The document validates according to the specified schema(s)" message | Warnings appear → See box [COMMON-ERRORS] and fix each one |
| 22 | Open index.html in browser for a final visual check | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Blank white page loads with favicon and correct tab title | Page errors → Check for any remaining unclosed tags |
| 23 | Confirm favicon still appears in tab | Browser — Tab Bar | — | Your initials icon visible in the tab | Missing → Hard refresh with `Cmd+Shift+R` / `Ctrl+Shift+R` |
| 24 | Confirm tab title shows your name | Browser — Tab Bar | — | Tab reads `Your Name — Junior Frontend Developer` | Wrong title → Check `<title>` tag in VS Code |
| 25 | Open DevTools Elements tab and do a final structure check | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | Full HTML tree visible | — |
| 26 | Confirm `<head>` contains all 13 expected lines | Browser — DevTools Elements | — | charset, viewport, title, description, keywords, author, 5 OG tags, favicon link all present | Missing tag → Add it in VS Code, save, re-validate |
| 27 | Confirm `<body>` contains header, main, 4 sections, footer — all with correct ids | Browser — DevTools Elements | — | All 6 landmark elements present with correct ids | Wrong id → Fix in VS Code with `Cmd+F` / `Ctrl+F` search |
| 28 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 29 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 30 | Commit with a descriptive message | Terminal | `git commit -m "chore: week 1 audit — validated HTML, fixed all errors"` | Output shows `1 file changed` | Nothing to commit → File was already clean, skip to Step 31 |
| 31 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 32 | Reload GitHub repo and confirm latest commit message is visible | Browser — Repo Page | `F5` or `Cmd+R` | Latest commit shows `chore: week 1 audit — validated HTML, fixed all errors` | Old commit showing → Wait 15 seconds and refresh |

---

### 📋 Box: COMMON-ERRORS

Most common W3C errors at this stage and how to fix them:

**"Element head is missing a required instance of child element title"**
→ Your `<title>` tag is missing or outside `<head>`. Add `<title>Your Name — Junior Frontend Developer</title>` inside `<head>`.

**"Attribute property not allowed on element meta at this point"**
→ This is a false positive for OG tags. W3C doesn't recognise `property=` — it's valid, ignore this specific warning.

**"End tag seen without matching open tag"**
→ You have a closing tag (e.g. `</section>`) with no matching opening tag. Count your opening and closing tags for that element — they must be equal.

**"Stray end tag"**
→ Same as above — a closing tag with nothing to close. Delete the extra closing tag.

**"No space between attributes"**
→ Two attributes are merged together (e.g. `charset="UTF-8"name="viewport"`). Add a space between them.

**"Bad value for attribute href"**
→ Your favicon `href` has a typo or wrong filename. Check `href="favicon.ico"` matches the exact filename in your folder.

---

### 📋 Box: DAY7-FULL-VERIFY

Your complete `index.html` at end of Week 1 should look like this:

```html
<!DOCTYPE html>
<html lang="en">
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
  <!-- Favicon -->
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>

  <header id="contact">

  </header>

  <main>

    <section id="skills">

    </section>

    <section id="education">

    </section>

    <section id="experience">

    </section>

    <section id="links">

    </section>

  </main>

  <footer id="footer">

  </footer>

</body>
</html>
```

If your file matches this (with your real name substituted), Week 1 is complete. ✅
