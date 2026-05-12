# Week 2: Content Build — Every Section Populated

## Day 9: Skills Section

> Build `<section id="skills">` with heading and skill list matching the reference image layout.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open VS Code with your project | Terminal | `code ~/Desktop/html-cv` | VS Code opens with `html-cv` in sidebar | `code not found` → Open VS Code manually |
| 2 | Click `index.html` in the Explorer sidebar | VS Code — Explorer Panel | — | `index.html` opens in editor tab | File missing → Run `ls` in Terminal to confirm it exists |
| 3 | Use Find to locate the skills section | VS Code — `index.html` | `Cmd+F` (Mac) or `Ctrl+F` (Windows) then type `id="skills"` | `<section id="skills">` tag highlighted in editor | Nothing found → Confirm Day 6 work is saved; the tag must exist |
| 4 | Close the Find bar | VS Code — `index.html` | `Escape` | Find bar closes, cursor remains near the skills section | — |
| 5 | Click on the blank line inside `<section id="skills">` to place cursor there | VS Code — `index.html` | — | Cursor blinks on the empty line between `<section id="skills">` and `</section>` | No blank line → Click at end of `<section id="skills">` tag and press Enter |
| 6 | Type the section heading tag | VS Code — `index.html` | `<h2>Skills</h2>` | `<h2>Skills</h2>` appears on its own line | Autocomplete adds extra tags → Press Escape and retype manually |
| 7 | Press Enter to move to the next line | VS Code — `index.html` | `Enter` | Cursor on new line | — |
| 8 | Type the opening `<p>` tag for the skills list | VS Code — `index.html` | `<p>` | Opening `<p>` tag appears | — |
| 9 | Type your full skills list as comma-separated text | VS Code — `index.html` | See box [SKILLS-LIST] below | Skills text appears on the same line as `<p>` | Skills look different from reference → Reference image shows all skills in a single paragraph block, not a bullet list |
| 10 | Type the closing `</p>` tag immediately after the last skill | VS Code — `index.html` | `</p>` | Closing tag appears at end of skills line | — |
| 11 | Save the file | VS Code — `index.html` | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Unsaved dot disappears from tab | Dot remains → Click File → Save |
| 12 | Verify the skills section looks correct | VS Code — `index.html` | — | See box [DAY9-VERIFY] below and compare line by line | Something wrong → Check that `<h2>` and `<p>` are both inside `<section id="skills">` |
| 13 | Open index.html in browser | Terminal | `open index.html` (Mac) or `start index.html` (Windows) | Page loads showing header content from Day 8 plus Skills section below it | Page blank → Check for an unclosed tag introduced today |
| 14 | Scroll down to confirm the Skills section is visible | Browser | — | "Skills" heading appears followed by skills text in a paragraph | Nothing visible below header → Confirm `<section id="skills">` content was saved |
| 15 | Compare the Skills section against the reference image | Browser + Reference Image | — | Heading "Skills" appears above a single paragraph of comma-separated skills | Layout looks different → Confirm you used `<p>` not `<ul>` — reference image uses a paragraph, not a list |
| 16 | Open DevTools and click the Elements tab | Browser | `F12` (Windows) or `Cmd+Option+I` (Mac) | Elements panel opens | Panel won't open → Right-click page → Inspect |
| 17 | Expand `<main>` then `<section id="skills">` in the Elements panel | Browser — DevTools Elements | — | `<h2>Skills</h2>` and `<p>` tag both nested inside `<section id="skills">` | Tags appear outside section → Fix nesting in VS Code and re-save |
| 18 | Confirm the `<h2>` tag contains exactly "Skills" | Browser — DevTools Elements | — | `<h2>Skills</h2>` visible | Wrong text → Fix in VS Code |
| 19 | Close DevTools | Browser | `F12` or `Cmd+Option+I` | DevTools closes | — |
| 20 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 21 | Commit with a descriptive message | Terminal | `git commit -m "feat: add skills section content"` | Output shows `1 file changed` | Nothing to commit → Confirm file was saved in Step 11 |
| 22 | Push to GitHub | Terminal | `git push origin main` | Output shows `main -> main` | `Authentication failed` → See Day 1 box [GH-AUTH] |
| 23 | Reload GitHub repo, click index.html, confirm skills section visible | Browser — Repo Page | `F5` or `Cmd+R` | `<h2>Skills</h2>` and skills paragraph visible in the file on GitHub | Old content showing → Wait 15 seconds and refresh |

---

### 📋 Box: SKILLS-LIST

Replace the skills below with your actual skills — keep them comma-separated, matching the reference image style:

```text
HTML, CSS, JavaScript, Accessibility, Figma to Design, Responsive Web Design, Technical Writing, Presentation
```

Edit this list to reflect your real skills. Keep the format: each skill separated by a comma and space. No bullet points.

---

### 📋 Box: DAY9-VERIFY

Your `<section id="skills">` block should look exactly like this (with your real skills substituted):

```html
<section id="skills">

  <h2>Skills</h2>
  <p>HTML, CSS, JavaScript, Accessibility, Figma to Design, Responsive Web Design, Technical Writing, Presentation</p>

</section>
```

Two tags inside the section: `<h2>` for the heading and `<p>` for the skills paragraph. No `<ul>`, no `<li>` — the reference image shows a flat comma-separated paragraph layout.
