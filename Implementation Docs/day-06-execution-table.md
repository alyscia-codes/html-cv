# Week 1: Foundation — Setup, Structure & Core HTML

## Day 6: Semantic Layout Skeleton

> Add all semantic landmark elements (`<header>`, `<main>`, `<section>`, `<footer>`) with correct IDs and no content yet.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Click on the blank line inside `<body>` to place your cursor there | VS Code — `index.html` | — | Cursor blinks on the empty line between `<body>` and `</body>` | No blank line → Click at end of `<body>` tag and press Enter |
| 4 | Type the opening `<header>` tag with an id | VS Code — `index.html` | `<header id="contact">` | Tag appears on its own line | Autocomplete closes the tag early → Press Escape and retype |
| 5 | Press Enter twice to leave a blank line inside the header | VS Code — `index.html` | `Enter` `Enter` | Two new lines created inside `<header>` | — |
| 6 | Type the closing `</header>` tag | VS Code — `index.html` | `</header>` | Closing tag appears | — |
| 7 | Press Enter twice to add spacing before the next element | VS Code — `index.html` | `Enter` `Enter` | Two blank lines between `</header>` and next line | — |
| 8 | Type the opening `<main>` tag | VS Code — `index.html` | `<main>` | Tag appears on its own line | — |
| 9 | Press Enter twice to leave a blank line inside `<main>` | VS Code — `index.html` | `Enter` `Enter` | Two new lines created inside `<main>` | — |
| 10 | Type the Skills section tag with id | VS Code — `index.html` | `<section id="skills">` | Tag appears inside `<main>` | — |
| 11 | Press Enter twice then type the closing section tag | VS Code — `index.html` | `Enter` `Enter` then `</section>` | Empty `<section id="skills">` block complete | — |
| 12 | Press Enter twice to add spacing | VS Code — `index.html` | `Enter` `Enter` | Blank lines between sections | — |
| 13 | Type the Education section tag with id | VS Code — `index.html` | `<section id="education">` | Tag appears inside `<main>` | — |
| 14 | Press Enter twice then type the closing section tag | VS Code — `index.html` | `Enter` `Enter` then `</section>` | Empty `<section id="education">` block complete | — |
| 15 | Press Enter twice to add spacing | VS Code — `index.html` | `Enter` `Enter` | Blank lines between sections | — |
| 16 | Type the Experience section tag with id | VS Code — `index.html` | `<section id="experience">` | Tag appears inside `<main>` | — |
| 17 | Press Enter twice then type the closing section tag | VS Code — `index.html` | `Enter` `Enter` then `</section>` | Empty `<section id="experience">` block complete | — |
| 18 | Press Enter twice to add spacing | VS Code — `index.html` | `Enter` `Enter` | Blank lines between sections | — |
| 19 | Type the Across the Internet section tag with id | VS Code — `index.html` | `<section id="links">` | Tag appears inside `<main>` | — |
| 20 | Press Enter twice then type the closing section tag | VS Code — `index.html` | `Enter` `Enter` then `</section>` | Empty `<section id="links">` block complete | — |
| 21 | Press Enter twice to add spacing | VS Code — `index.html` | `Enter` `Enter` | Blank lines after last section | — |
| 22 | Type the closing `</main>` tag | VS Code — `index.html` | `</main>` | Closing main tag appears | — |
| 23 | Press Enter twice to add spacing before footer | VS Code — `index.html` | `Enter` `Enter` | Blank lines between `</main>` and footer | — |
| 24 | Type the opening `<footer>` tag with an id | VS Code — `index.html` | `<footer id="footer">` | Tag appears on its own line | — |
| 25 | Press Enter twice then type the closing footer tag | VS Code — `index.html` | `Enter` `Enter` then `</footer>` | Empty `<footer>` block complete | — |
| 26 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 27 | Verify the full `<body>` block looks correct | VS Code — `index.html` | — | See box [DAY6-VERIFY] below and compare | Missing a section → Add it between `<main>` and `</main>` |
| 28 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Blank white page loads — no visible content yet | Page errors → Check for unclosed tags in `<body>` |
| 29 | Open DevTools and click the Elements tab | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | Elements panel shows full HTML tree | Panel won't open → Right-click page → Inspect |
| 30 | Expand the `<body>` element in DevTools | Browser — DevTools Elements | — | `<header>`, `<main>`, 4 `<section>` tags, and `<footer>` all visible and nested correctly | A tag is missing → Return to VS Code and add it |
| 31 | Confirm each section has its correct id attribute | Browser — DevTools Elements | — | ids visible: `contact`, `skills`, `education`, `experience`, `links`, `footer` | Wrong id → Find the tag in VS Code with `Cmd+F` / `Ctrl+F` and correct it |
| 32 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 33 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 34 | Commit with a descriptive message | Terminal | `git commit -m "feat: add semantic HTML layout skeleton to body"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 26 |
| 35 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 36 | Reload GitHub repo, click index.html, confirm body structure visible | Browser — Repo Page | `F5` or `Cmd+R` | All semantic tags visible in the file preview on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: DAY6-VERIFY

Your `<body>` block should look exactly like this:

```html
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
```

All tags empty — no content yet. Content fills in starting Day 8.
