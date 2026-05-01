# Week 2: Content Build — Every Section Populated

## Day 8: Header / Contact Block

> Add name, title, address, phone, and email to `<header>` using semantic tags (`<h1>`, `<address>`, `<p>`).

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor tab | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Click on the blank line inside `<header id="contact">` to place cursor there | VS Code — `index.html` | — | Cursor blinks on the empty line between `<header id="contact">` and `</header>` | Can't find it → Use `Cmd+F` / `Ctrl+F` and search `id="contact"` |
| 4 | Type the horizontal rule divider line | VS Code — `index.html` | `<hr>` | `<hr>` tag appears on its own line | — |
| 5 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 6 | Type your full name inside an `<h1>` tag | VS Code — `index.html` | `<h1>Your Full Name</h1>` | h1 tag appears with your name | Replace `Your Full Name` with your actual name |
| 7 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 8 | Type your job title inside a `<p>` tag | VS Code — `index.html` | `<p>Junior Frontend Developer</p>` | p tag appears with job title | Adjust title to match your actual role if different |
| 9 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 10 | Type the opening `<address>` tag | VS Code — `index.html` | `<address>` | Opening address tag appears | — |
| 11 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line inside `<address>` | — |
| 12 | Type your street address inside a `<p>` tag | VS Code — `index.html` | `<p>123 Your Street</p>` | Street address appears | Replace with your real street address |
| 13 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 14 | Type your city, state, and zip inside a `<p>` tag | VS Code — `index.html` | `<p>Your City, ST 12345</p>` | City/state/zip appears | Replace with your real city, state abbreviation, and zip code |
| 15 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 16 | Type your phone number inside a `<p>` tag | VS Code — `index.html` | `<p>(123) 456-7890</p>` | Phone number appears | Replace with your real phone number |
| 17 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 18 | Type your email as a clickable `<a>` link inside a `<p>` tag | VS Code — `index.html` | `<p><a href="mailto:you@example.com">you@example.com</a></p>` | Email link appears | Replace both instances of `you@example.com` with your real email |
| 19 | Type the closing `</address>` tag | VS Code — `index.html` | `</address>` | Closing address tag appears | — |
| 20 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 21 | Verify the `<header>` block looks correct | VS Code — `index.html` | — | See box [DAY8-VERIFY] below and compare line by line | Something missing → Add the missing tag inside `<header>` |
| 22 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Page loads showing your name, title, and contact details | Page blank → Check for unclosed tags inside `<header>` |
| 23 | Confirm the page matches the reference image header section | Browser | — | Name visible as large heading, job title below, address block beneath that | Layout looks wrong → Check tag nesting in box [DAY8-VERIFY] |
| 24 | Click the email address on the page | Browser | — | Your email client opens with a new email pre-addressed to you | Nothing happens → Check `href="mailto:you@example.com"` is correct |
| 25 | Open DevTools and expand `<header>` in the Elements tab | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | `<hr>`, `<h1>`, `<p>`, `<address>` all nested correctly inside `<header>` | Tags out of order → Fix nesting in VS Code and re-save |
| 26 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 27 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 28 | Commit with a descriptive message | Terminal | `git commit -m "feat: add contact block to header section"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 20 |
| 29 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 30 | Reload GitHub repo, click index.html, confirm header content is visible | Browser — Repo Page | `F5` or `Cmd+R` | Your name, title, and address visible in the file on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: DAY8-VERIFY

Your `<header>` block should look exactly like this (with your real details substituted):

```html
<header id="contact">

  <hr>
  <h1>Your Full Name</h1>
  <p>Junior Frontend Developer</p>
  <address>
    <p>123 Your Street</p>
    <p>Your City, ST 12345</p>
    <p>(123) 456-7890</p>
    <p><a href="mailto:you@example.com">you@example.com</a></p>
  </address>

</header>
```

`<address>` is the correct semantic tag for contact information — not a `<div>`. The `<hr>` matches the horizontal rule visible at the top of the reference image.
