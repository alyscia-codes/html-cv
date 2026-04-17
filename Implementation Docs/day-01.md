# Week 1: Foundation — Setup, Structure & Core HTML

## Day 1: Environment Setup

> Create GitHub account (if needed), set up repo, configure Git locally, and push first commit.

| Step # | What To Do | Where | Input | Expected Result | Troubleshooting |
| -------- | ------------ | ------- | ------- | ----------------- | ----------------- |
| 1 | Open GitHub in browser | Browser | `https://github.com` | GitHub homepage loads | Doesn't load → Check internet connection |
| 2 | Check top-right corner — if profile avatar visible, skip to Step 9 | Browser | — | Avatar = already have account | Not sure → Click "Sign In" and attempt login |
| 3 | Click "Sign up" to start account creation | Browser | — | Sign-up form loads | Button missing → Navigate to `https://github.com/signup` |
| 4 | Type your email address in the email field | Browser — Sign Up Form | Your real email | Field turns green | Invalid format → Use `name@domain.com` |
| 5 | Type a strong password (12+ chars, mixed case + numbers) | Browser — Sign Up Form | A strong password | Strength indicator turns green | Too weak → Add numbers and symbols |
| 6 | Type a professional username | Browser — Sign Up Form | e.g. `janedoe` | Green checkmark appears | Taken → Append a number or middle initial |
| 7 | Complete the CAPTCHA puzzle | Browser — Sign Up Form | — | CAPTCHA passes, Continue activates | Keeps failing → Refresh and use keyboard CAPTCHA option |
| 8 | Open email inbox and click the GitHub verification link | Email Inbox | — | GitHub dashboard loads | Email not received → Check spam, click Resend on GitHub |
| 9 | Open Terminal (Mac/Linux) or Git Bash (Windows) | Terminal | — | Blank terminal prompt appears | Can't find it → Search "Terminal" in Spotlight (Mac) or Start Menu (Windows) |
| 10 | Check if Git is already installed | Terminal | `git --version` | Shows `git version 2.x.x` — skip to Step 16 | `command not found` → Continue to Step 11 |
| 11 | Navigate to the Git download page | Browser | `https://git-scm.com/downloads` | Git download page loads | Won't load → Search "git download" in Google |
| 12 | Click the download button matching your OS | Browser — Git Downloads | — | Installer downloads to Downloads folder | Wrong OS → Manually click your OS tab |
| 13 | Double-click the downloaded installer to open it | File Manager | — | Installation wizard opens | Permission denied → Right-click → Run as administrator (Windows) or use `sudo` (Mac) |
| 14 | Click "Next" through all screens keeping defaults, then "Install" | Installer | — | "Installation complete" screen appears | Stuck → Wait 60 seconds, files are unpacking |
| 15 | Close Terminal, reopen it, confirm Git installed | Terminal | `git --version` | Shows `git version 2.x.x` | Still not found → Restart computer and retry |
| 16 | Set your global Git display name | Terminal | See box [GIT-NAME] below | No output = success | `unknown flag` → Check for typos in command |
| 17 | Verify Git name saved correctly | Terminal | `git config --global user.name` | Your full name prints back | Nothing printed → Repeat Step 16 |
| 18 | Set your global Git email (must match GitHub email exactly) | Terminal | See box [GIT-EMAIL] below | No output = success | Error → Ensure email matches your GitHub account |
| 19 | Verify Git email saved correctly | Terminal | `git config --global user.email` | Your email prints back | Wrong email → Re-run Step 18 with correct address |
| 20 | Navigate to your GitHub dashboard | Browser | `https://github.com` | Dashboard loads | Redirected to login → Log in first |
| 21 | Click the "+" icon top-right, then "New repository" | Browser — GitHub Dashboard | — | New repository form loads | Can't find "+" → Navigate to `https://github.com/new` |
| 22 | Type the repository name | Browser — New Repo Form | `html-cv` | Name field shows `html-cv` with green checkmark | Name taken → Use `html-cv-project` |
| 23 | Click the "Public" radio button | Browser — New Repo Form | — | "Public" option selected | Already selected → No action needed |
| 24 | Check the "Add a README file" checkbox | Browser — New Repo Form | — | Checkbox shows a checkmark | Missing → Scroll down in form |
| 25 | Click the green "Create repository" button | Browser — New Repo Form | — | Repo page loads at `github.com/yourusername/html-cv` | Greyed out → Ensure repo name field is filled |
| 26 | Click the green "Code" button on the repo page | Browser — Repo Page | — | Dropdown opens showing clone URL | Not visible → Confirm you are on the repo main page |
| 27 | Click the copy icon next to the HTTPS URL | Browser — Code Dropdown | — | URL copied to clipboard (ends in `.git`) | No icon → Manually select and copy the URL text |
| 28 | Navigate to your Desktop folder in Terminal | Terminal | `cd ~/Desktop` | Prompt shows `~/Desktop` | No Desktop folder → Use `cd ~` for home directory |
| 29 | Clone the repository to your Desktop | Terminal | See box [CLONE-CMD] below | Folder `html-cv` created on Desktop | `Permission denied` → Confirm repo is set to Public |
| 30 | Navigate into the cloned folder | Terminal | `cd html-cv` | Prompt changes to show `html-cv` | Folder not found → Run `ls` to confirm clone succeeded |
| 31 | Open the folder in VS Code | Terminal | `code .` | VS Code opens with `html-cv` in the sidebar | `code: command not found` → See box [VSCODE-PATH] below |
| 32 | Create a new file in VS Code | VS Code | `Ctrl+N` (Windows) or `Cmd+N` (Mac) | Blank untitled file opens | Nothing happens → Click File → New File |
| 33 | Save the file as index.html | VS Code | `Ctrl+S` (Windows) or `Cmd+S` (Mac) | Save dialog opens | Dialog doesn't open → Click File → Save As |
| 34 | Type the filename and confirm | VS Code — Save Dialog | `index.html` | Tab now shows `index.html` | Wrong extension → Rename in the Explorer panel |
| 35 | Type a placeholder comment into index.html | VS Code — `index.html` | `<!-- Day 1: HTML CV Project -->` | Comment appears in file | Typing in wrong file → Check filename in tab header |
| 36 | Stage all changes | Terminal | `git add .` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 37 | Commit with a descriptive message | Terminal | `git commit -m "feat: initial commit — add index.html placeholder"` | Output shows `1 file changed` | `Author identity unknown` → Complete Steps 16–19 first |
| 38 | Push to GitHub | Terminal | `git push origin main` | Output shows `Branch 'main' set up to track remote` | `Authentication failed` → See box [GH-AUTH] below |
| 39 | Reload your repo page and confirm index.html appears | Browser — Repo Page | `F5` or `Cmd+R` | `index.html` visible in repo file list | Not showing → Wait 10 seconds and refresh again |

---

### 📋 Box: GIT-NAME

```bash
git config --global user.name "Your Full Name"
```

---

### 📋 Box: GIT-EMAIL

```bash
git config --global user.email "you@example.com"
```

Use the same email you signed up to GitHub with.

---

### 📋 Box: CLONE-CMD

```bash
git clone https://github.com/YOURUSERNAME/html-cv.git
```

Replace `YOURUSERNAME` with your GitHub username exactly as shown on your profile.

---

### 📋 Box: VSCODE-PATH

VS Code's `code` command isn't on your PATH. Fix:

1. Open VS Code manually from Applications or Start Menu
2. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)
3. Type: `Shell Command: Install 'code' command in PATH`
4. Click the result
5. Close and reopen Terminal, then retry `code .`

---

### 📋 Box: GH-AUTH

GitHub no longer accepts passwords in Terminal. Use a Personal Access Token:

1. Go to `https://github.com/settings/tokens`
2. Click "Generate new token (classic)"
3. Set expiration: 90 days — check the `repo` scope checkbox
4. Click "Generate token" — copy it immediately (shown only once)
5. Re-run `git push origin main` — when prompted for password, paste the token

---
---

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
