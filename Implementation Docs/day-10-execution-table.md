# Week 2: Content Build — Every Section Populated

## Day 10: Education Section

> Build `<section id="education">` with school, degree, dates, and description using `<h3>`, `<p>`, `<time>`.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor tab | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Use Find to locate the education section | VS Code — `index.html` | `Cmd+F` (Mac) or `Ctrl+F` (Windows) then type `id="education"` | `<section id="education">` tag highlighted in editor | Nothing found → Confirm Day 6 skeleton is saved; the tag must exist |
| 4 | Close the Find bar | VS Code — `index.html` | `Escape` | Find bar closes, cursor remains near the education section | — |
| 5 | Click on the blank line inside `<section id="education">` to place cursor there | VS Code — `index.html` | — | Cursor blinks on the empty line between `<section id="education">` and `</section>` | No blank line → Click at end of `<section id="education">` tag and press Enter |
| 6 | Type the section heading tag | VS Code — `index.html` | `<h2>Education</h2>` | `<h2>Education</h2>` appears on its own line | Autocomplete closes early → Press Escape and retype manually |
| 7 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 8 | Type the school name and degree inside an `<h3>` tag | VS Code — `index.html` | See box [EDU-H3] below | `<h3>` tag appears with school name, location, and degree | Replace placeholder with your real school and degree |
| 9 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 10 | Type the date range using a `<p>` tag with two `<time>` elements | VS Code — `index.html` | See box [EDU-DATES] below | Date range appears on its own line using semantic `<time>` tags | Dates look wrong → Confirm both `datetime` attribute values use `YYYY-MM` format |
| 11 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 12 | Type the education description inside a `<p>` tag | VS Code — `index.html` | `<p>List of exciting things you did at university</p>` | Description paragraph appears on its own line | Replace placeholder text with your real description |
| 13 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 14 | Verify the education section looks correct | VS Code — `index.html` | — | See box [DAY10-VERIFY] below and compare line by line | Something wrong → Check that `<h3>`, date `<p>`, and description `<p>` are all inside `<section id="education">` |
| 15 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Page loads showing header, skills, and now education section | Page blank → Check for an unclosed tag introduced today |
| 16 | Scroll down to confirm the Education section is visible | Browser | — | "Education" heading appears, followed by school/degree as a subheading, then dates, then description | Nothing visible → Confirm file was saved in Step 13 |
| 17 | Compare the Education section against the reference image | Browser + Reference Image | — | School name and degree on one line in a subheading, date range below it, description text below that | Layout looks different → Check you used `<h3>` for the school line, not `<h2>` |
| 18 | Open DevTools and click the Elements tab | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | Elements panel opens | Panel won't open → Right-click page → Inspect |
| 19 | Expand `<main>` then `<section id="education">` in the Elements panel | Browser — DevTools Elements | — | `<h2>`, `<h3>`, two `<p>` tags all nested correctly inside `<section id="education">` | Tags appear outside section → Fix nesting in VS Code and re-save |
| 20 | Confirm the `<time>` elements are nested inside the date `<p>` tag | Browser — DevTools Elements | — | Two `<time>` elements visible inside the date paragraph | `<time>` tags missing → Return to VS Code and add them per box [EDU-DATES] |
| 21 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 22 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 23 | Commit with a descriptive message | Terminal | `git commit -m "feat: add education section content"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 13 |
| 24 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 25 | Reload GitHub repo, click index.html, confirm education section visible | Browser — Repo Page | `F5` or `Cmd+R` | `<h2>Education</h2>`, `<h3>` school line, and date paragraph visible in the file on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: EDU-H3

```html
<h3>School Name, Location - Degree</h3>
```

Replace with your real details. Match the reference image format exactly — school name, comma, city, dash, then degree name all on one line inside the `<h3>`.

Example: `<h3>Florida State University, Tallahassee - B.S. Computer Science</h3>`

---

### 📋 Box: EDU-DATES

```html
<p><time datetime="YYYY-MM">Month 20xx</time> to <time datetime="YYYY-MM">Month 20xx</time></p>
```

Replace both `YYYY-MM` values with your actual start and end year-month (e.g. `2019-09`).
Replace both `Month 20xx` display values with human-readable dates (e.g. `September 2019`).

Full example:

```html
<p><time datetime="2019-09">September 2019</time> to <time datetime="2023-05">May 2023</time></p>
```

If you're currently enrolled and have no end date, use:

```html
<p><time datetime="2024-01">January 2024</time> to Present</p>
```

---

### 📋 Box: DAY10-VERIFY

Your `<section id="education">` block should look exactly like this (with your real details substituted):

```html
<section id="education">

  <h2>Education</h2>
  <h3>School Name, Location - Degree</h3>
  <p><time datetime="2019-09">September 2019</time> to <time datetime="2023-05">May 2023</time></p>
  <p>List of exciting things you did at university</p>

</section>
```

Four tags inside the section: `<h2>` section heading, `<h3>` school/degree line, `<p>` with `<time>` elements for dates, `<p>` for description. This matches the reference image layout exactly.
