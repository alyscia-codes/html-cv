# Week 2: Content Build — Every Section Populated

## Day 11: Experience — Job 1

> Add first work experience entry with company, location, title, dates, bullet achievements, and skills line.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor tab | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Use Find to locate the experience section | VS Code — `index.html` | `Cmd+F` (Mac) or `Ctrl+F` (Windows) then type `id="experience"` | `<section id="experience">` tag highlighted in editor | Nothing found → Confirm Day 6 skeleton is saved; the tag must exist |
| 4 | Close the Find bar | VS Code — `index.html` | `Escape` | Find bar closes, cursor remains near the experience section | — |
| 5 | Click on the blank line inside `<section id="experience">` to place cursor there | VS Code — `index.html` | — | Cursor blinks on the empty line between `<section id="experience">` and `</section>` | No blank line → Click at end of `<section id="experience">` tag and press Enter |
| 6 | Type the section heading tag | VS Code — `index.html` | `<h2>Experience</h2>` | `<h2>Experience</h2>` appears on its own line | Autocomplete closes early → Press Escape and retype manually |
| 7 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 8 | Type the company name, location, and job title inside an `<h3>` tag | VS Code — `index.html` | See box [EXP1-H3] below | `<h3>` tag appears with company, location, and title | Replace placeholder with your real company and job title |
| 9 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 10 | Type the date range using a `<p>` tag with two `<time>` elements | VS Code — `index.html` | See box [EXP1-DATES] below | Date range appears on its own line using semantic `<time>` tags | Dates look wrong → Confirm both `datetime` attributes use `YYYY-MM` format |
| 11 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 12 | Type the opening `<ul>` tag for the achievements list | VS Code — `index.html` | `<ul>` | Opening `<ul>` tag appears | — |
| 13 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line inside `<ul>` | — |
| 14 | Type the first achievement inside an `<li>` tag | VS Code — `index.html` | `<li>List of achievements</li>` | First `<li>` tag appears | Replace placeholder with your real achievement |
| 15 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 16 | Type the second achievement inside an `<li>` tag | VS Code — `index.html` | `<li>List of achievements</li>` | Second `<li>` tag appears | Replace placeholder with your real achievement |
| 17 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 18 | Type the third achievement inside an `<li>` tag | VS Code — `index.html` | `<li>List of achievements</li>` | Third `<li>` tag appears | Add more `<li>` lines if you have additional achievements — same pattern |
| 19 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 20 | Type the closing `</ul>` tag | VS Code — `index.html` | `</ul>` | Closing `</ul>` tag appears | — |
| 21 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 22 | Type the skills line inside a `<p>` tag | VS Code — `index.html` | See box [EXP1-SKILLS] below | Skills paragraph appears below the achievements list | Replace placeholder with skills you used or gained at this job |
| 23 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 24 | Verify the experience section looks correct | VS Code — `index.html` | — | See box [DAY11-VERIFY] below and compare line by line | Something wrong → Check that all tags are nested inside `<section id="experience">` |
| 25 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Page loads showing header, skills, education, and now experience section | Page blank → Check for an unclosed `<ul>` or `<li>` introduced today |
| 26 | Scroll down to confirm the Experience section is visible | Browser | — | "Experience" heading, company subheading, dates, bulleted achievements, and skills line all visible | Nothing visible → Confirm file was saved in Step 23 |
| 27 | Compare the Experience entry against the reference image | Browser + Reference Image | — | Company/location/title on one `<h3>` line, date range below, bullet list of achievements, skills line at bottom | Bullets not showing → Confirm you used `<ul>` and `<li>`, not `<p>` tags |
| 28 | Open DevTools and click the Elements tab | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | Elements panel opens | Panel won't open → Right-click page → Inspect |
| 29 | Expand `<section id="experience">` in the Elements panel | Browser — DevTools Elements | — | `<h2>`, `<h3>`, date `<p>`, `<ul>` with three `<li>` children, and skills `<p>` all nested correctly | `<li>` tags appear outside `<ul>` → Fix nesting in VS Code and re-save |
| 30 | Confirm `<time>` elements are nested inside the date `<p>` | Browser — DevTools Elements | — | Two `<time>` elements visible inside the date paragraph | `<time>` tags missing → Return to VS Code and add them per box [EXP1-DATES] |
| 31 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 32 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 33 | Commit with a descriptive message | Terminal | `git commit -m "feat: add first work experience entry"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 23 |
| 34 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 35 | Reload GitHub repo, click index.html, confirm experience content is visible | Browser — Repo Page | `F5` or `Cmd+R` | `<h2>Experience</h2>`, `<h3>` company line, `<ul>` and `<li>` tags visible in the file on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: EXP1-H3

```html
<h3>Company Name, Location - Job Title</h3>
```

Replace with your real details. Match the reference image format exactly — company name, comma, city, dash, then job title all on one line inside the `<h3>`.

Example: `<h3>Acme Corp, Tampa - Junior Frontend Developer</h3>`

---

### 📋 Box: EXP1-DATES

```html
<p><time datetime="YYYY-MM">Month 20xx</time> to <time datetime="YYYY-MM">Month 20xx</time></p>
```

Replace both `YYYY-MM` values with your actual start and end year-month (e.g. `2022-03`).
Replace both `Month 20xx` display values with human-readable dates (e.g. `March 2022`).

Full example:

```html
<p><time datetime="2022-03">March 2022</time> to <time datetime="2024-01">January 2024</time></p>
```

If this is your current role, use:

```html
<p><time datetime="2022-03">March 2022</time> to Present</p>
```

---

### 📋 Box: EXP1-SKILLS

```html
<p>Skills: List of skills used or gained at this company</p>
```

Replace the placeholder with a comma-separated list of skills relevant to this role.

Example: `<p>Skills: HTML, CSS, JavaScript, Git, Figma, Cross-browser Testing</p>`

---

### 📋 Box: DAY11-VERIFY

Your `<section id="experience">` block should look exactly like this after Day 11 (with your real details substituted):

```html
<section id="experience">

  <h2>Experience</h2>
  <h3>Company Name, Location - Job Title</h3>
  <p><time datetime="2022-03">March 2022</time> to <time datetime="2024-01">January 2024</time></p>
  <ul>
    <li>List of achievements</li>
    <li>List of achievements</li>
    <li>List of achievements</li>
  </ul>
  <p>Skills: List of skills used or gained at this company</p>

</section>
```

Day 12 adds Job 2 inside the same `<section id="experience">` — do not close or duplicate the section tag today.
