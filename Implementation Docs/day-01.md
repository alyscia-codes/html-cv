# Week 1: Foundation — Setup, Structure & Core HTML

## Day 1: Environment Setup

> Create GitHub account (if needed), set up repo, configure Git locally, and push first commit.

| Step # | Step Letter | Step Action | Location | Action | Subject | Input | Expected Result | Troubleshooting |
| -------- | ------------- | ------------- | ---------- | -------- | --------- | ------- | ----------------- | ----------------- |
| 1 - GitHub Account Setup | A - Check for existing account | a. Open GitHub in browser | Browser | Open | Address bar | `"https://github.com"` | GitHub homepage loads | Doesn't load → Check internet connection |
| 1 - GitHub Account Setup | A - Check for existing account | b. Confirm if you are already logged in | Browser | Read | Top-right corner of page | *(no input — look for profile icon)* | Profile avatar visible = already have account; skip to Step 2 | Not sure → Click "Sign In" and attempt login |
| 1 - GitHub Account Setup | B - Create new account (skip if account exists) | a. Click Sign Up | Browser | Click | "Sign up" button (top-right) | *(no input)* | Sign-up form loads | Button missing → Navigate directly to `"https://github.com/signup"` |
| 1 - GitHub Account Setup | B - Create new account | b. Enter your email address | Browser | Type | Email field | Your real email address | Email accepted, field turns green | Invalid email → Use format `name@domain.com` |
| 1 - GitHub Account Setup | B - Create new account | c. Create a password | Browser | Type | Password field | A strong password (12+ chars, mixed case) | Password strength indicator shows green | Too weak → Add numbers and symbols |
| 1 - GitHub Account Setup | B - Create new account | d. Choose a username | Browser | Type | Username field | A professional username (e.g., `"firstnamelastname"`) | Username available checkmark appears | Taken → Append a number or middle initial |
| 1 - GitHub Account Setup | B - Create new account | e. Complete CAPTCHA and verify email | Browser | Click | "Verify" button, then email inbox | *(follow on-screen steps)* | GitHub dashboard loads after verification | Email not received → Check spam folder, click Resend |
| 2 - Install Git Locally | A - Check if Git is already installed | a. Open Terminal (Mac/Linux) or Git Bash (Windows) | Terminal | Open | Terminal app | *(no input)* | Blank terminal prompt appears | Can't find Terminal → Search "Terminal" in Spotlight (Mac) or Start Menu (Windows) |
| 2 - Install Git Locally | A - Check if Git is already installed | b. Check Git version | Terminal | Run | Terminal prompt | `"git --version"` | Output shows `git version 2.x.x` — skip to Step 3 | Command not found → Proceed to Step 2B to install |
| 2 - Install Git Locally | B - Install Git (skip if already installed) | a. Navigate to Git download page | Browser | Navigate | Address bar | `"https://git-scm.com/downloads"` | Git download page loads with OS options | Page won't load → Search "git download" in Google |
| 2 - Install Git Locally | B - Install Git | b. Download installer for your OS | Browser | Click | Download button matching your OS (Mac / Windows / Linux) | *(no input)* | Installer file downloads to Downloads folder | Wrong OS detected → Manually click your OS tab |
| 2 - Install Git Locally | B - Install Git | c. Run the installer | File Manager | Open | Downloaded installer file | *(double-click the file)* | Installation wizard opens | Permission denied → Right-click → "Run as administrator" (Windows) or `"sudo"` prefix (Mac) |
| 2 - Install Git Locally | B - Install Git | d. Accept all defaults and complete install | Installer | Click | "Next" through all screens, then "Install" | *(no input — keep all defaults)* | "Git has been installed" screen appears | Stuck on screen → Wait 60 seconds, installer is unpacking |
| 2 - Install Git Locally | B - Install Git | e. Confirm install succeeded | Terminal | Run | Terminal prompt (reopen it first) | `"git --version"` | Output shows `git version 2.x.x` | Still not found → Restart computer and retry |
| 3 - Configure Git Identity | A - Set your name | a. Set global Git username | Terminal | Run | Terminal prompt | `"git config --global user.name "Your Full Name""` | No output = success | Error: unknown flag → Check for typos, use exact command |
| 3 - Configure Git Identity | A - Set your name | b. Verify name was saved | Terminal | Run | Terminal prompt | `"git config --global user.name"` | Your full name prints back | Nothing printed → Repeat Step 3A-a |
| 3 - Configure Git Identity | B - Set your email | a. Set global Git email (must match GitHub email) | Terminal | Run | Terminal prompt | `"git config --global user.email "you@example.com""` | No output = success | Error → Ensure email matches your GitHub account exactly |
| 3 - Configure Git Identity | B - Set your email | b. Verify email was saved | Terminal | Run | Terminal prompt | `"git config --global user.email"` | Your email prints back | Wrong email → Re-run Step 3B-a with correct email |
| 4 - Create GitHub Repository | A - Open New Repo form | a. Navigate to GitHub dashboard | Browser | Navigate | Address bar | `"https://github.com"` | Your GitHub dashboard loads | Redirected to login → Log in first |
| 4 - Create GitHub Repository | A - Open New Repo form | b. Click the New repository button | Browser | Click | "+" icon (top-right) → "New repository" | *(no input)* | New repository creation form loads | Can't find "+" → Navigate directly to `"https://github.com/new"` |
| 4 - Create GitHub Repository | B - Fill in repo details | a. Type repository name | Browser | Type | "Repository name" field | `"html-cv"` | Name field shows `html-cv` with green checkmark | Name taken → Use `"html-cv-project"` or add your username suffix |
| 4 - Create GitHub Repository | B - Fill in repo details | b. Set visibility to Public | Browser | Click | "Public" radio button | *(no input)* | "Public" option is selected (filled dot) | Already selected → No action needed |
| 4 - Create GitHub Repository | B - Fill in repo details | c. Check "Add a README file" | Browser | Click | "Add a README file" checkbox | *(no input)* | Checkbox shows checkmark | Checkbox missing → Scroll down in form |
| 4 - Create GitHub Repository | C - Create the repo | a. Click Create repository | Browser | Click | "Create repository" button (green, bottom of form) | *(no input)* | Repo page loads at `github.com/yourusername/html-cv` | Button greyed out → Ensure repo name field is filled |
| 5 - Clone Repo to Local Machine | A - Copy the repo URL | a. Click the green Code button on repo page | Browser | Click | Green "Code" button | *(no input)* | Dropdown opens showing clone URL | Button not visible → Ensure you are on the repo main page |
| 5 - Clone Repo to Local Machine | A - Copy the repo URL | b. Copy the HTTPS URL | Browser | Click | Copy icon next to HTTPS URL | *(no input)* | URL copied to clipboard (ends in `.git`) | No copy icon → Manually select and copy the URL text |
| 5 - Clone Repo to Local Machine | B - Clone via Terminal | a. Navigate to where you want the project folder | Terminal | Run | Terminal prompt | `"cd ~/Desktop"` | Prompt now shows `~/Desktop` | No Desktop folder → Use `"cd ~"` to go to home directory |
| 5 - Clone Repo to Local Machine | B - Clone via Terminal | b. Clone the repository | Terminal | Run | Terminal prompt | See box [CLONE-CMD] below | Folder `html-cv` created on Desktop | `Permission denied` → Check that repo is Public |
| 5 - Clone Repo to Local Machine | C - Open in VS Code | a. Navigate into the cloned folder | Terminal | Run | Terminal prompt | `"cd html-cv"` | Prompt changes to show `html-cv` | Folder not found → Run `"ls"` to confirm clone succeeded |
| 5 - Clone Repo to Local Machine | C - Open in VS Code | b. Open folder in VS Code | Terminal | Run | Terminal prompt | `"code ."` | VS Code opens with `html-cv` folder in sidebar | `code: command not found` → See box [VSCODE-PATH] below |
| 6 - Create index.html & Push First Commit | A - Create the file | a. Create a new file in VS Code | VS Code | Press | Keyboard | `"Ctrl+N"` (Windows) or `"Cmd+N"` (Mac) | Untitled blank file opens | Nothing happens → Click File → New File from menu |
| 6 - Create index.html & Push First Commit | A - Create the file | b. Save the file as index.html | VS Code | Press | Keyboard | `"Ctrl+S"` (Windows) or `"Cmd+S"` (Mac) | Save dialog opens | Dialog doesn't open → Click File → Save As |
| 6 - Create index.html & Push First Commit | A - Create the file | c. Type the filename | VS Code Save Dialog | Type | Filename field | `"index.html"` | File saved, tab now shows `index.html` | File saves with wrong extension → Rename in Explorer panel |
| 6 - Create index.html & Push First Commit | B - Add placeholder content | a. Type one line into index.html | VS Code `index.html` | Type | Empty editor | `"<!-- Day 1: HTML CV Project -->"` | Comment appears in file | Typing in wrong file → Check filename in tab |
| 6 - Create index.html & Push First Commit | C - Stage, commit, push | a. Stage all changes | Terminal | Run | Terminal prompt | `"git add ."` | No output = success | `not a git repository` → Confirm you are inside `html-cv` folder |
| 6 - Create index.html & Push First Commit | C - Stage, commit, push | b. Commit with message | Terminal | Run | Terminal prompt | `"git commit -m "feat: initial commit — add index.html placeholder""` | Output shows `1 file changed` | `Author identity unknown` → Complete Step 3 (Git config) first |
| 6 - Create index.html & Push First Commit | C - Stage, commit, push | c. Push to GitHub | Terminal | Run | Terminal prompt | `"git push origin main"` | Output shows `Branch 'main' set up to track remote` | `Authentication failed` → See box [GH-AUTH] below |
| 6 - Create index.html & Push First Commit | D - Verify on GitHub | a. Reload your repo page in browser | Browser | Press | Keyboard | `"F5"` or `"Cmd+R"` | `index.html` now appears in repo file list | File not showing → Wait 10 seconds and refresh again |

---

### 📋 Box: CLONE-CMD

```text
git clone https://github.com/YOURUSERNAME/html-cv.git
```

Replace `YOURUSERNAME` with your actual GitHub username exactly as it appears on your profile.

---

### 📋 Box: VSCODE-PATH

VS Code's `code` command isn't on your PATH. Fix it:

1. Open VS Code manually (find it in Applications or Start Menu)
2. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)
3. Type `"Shell Command: Install 'code' command in PATH"`
4. Click it
5. Close and reopen Terminal, then retry `code .`

---

### 📋 Box: GH-AUTH

GitHub no longer accepts passwords via Terminal. Use a Personal Access Token:

1. Go to `https://github.com/settings/tokens`
2. Click "Generate new token (classic)"
3. Set expiration to 90 days, check the `repo` scope checkbox
4. Click "Generate token" — copy it immediately (shown only once)
5. Re-run `git push origin main` — when asked for password, paste the token instead
