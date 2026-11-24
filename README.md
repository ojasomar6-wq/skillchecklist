# SkillCheck

A browser-based skill assessment platform featuring timed multiple-choice tests across **HTML**, **CSS**, and **C Programming** (Easy, Moderate, and Hard levels), built with vanilla HTML, CSS, and JavaScript.

## Repository Structure

```text
skillcheck-repo/
├── .github/
│   └── workflows/
│       └── deploy.yml      # Automated GitHub Pages deployment workflow
├── .gitignore              # Standard editor & OS ignore rules
├── .nojekyll               # Prevents Jekyll processing on GitHub Pages
├── index.html              # Root entry point (redirects to login.html)
├── login.html              # User login page
├── signup.html             # User registration page (place your signup file here)
├── main.html               # Main dashboard (place your dashboard file here)
├── htmleasy.html           # HTML - Easy Test (25 MCQs, 10 min)
├── htmlmoderate.html       # HTML - Moderate Test (25 MCQs, 10 min)
├── htmlhard.html           # HTML - Hard Test (25 MCQs, 10 min)
├── csseasy.html            # CSS - Easy Test (25 MCQs, 10 min)
├── cssmoderate.html        # CSS - Moderate Test (25 MCQs, 10 min)
├── csshard.html            # CSS - Hard Test (25 MCQs, 10 min)
├── ceasy.html              # C Language - Easy Test (25 MCQs, 10 min)
├── cmoderate.html          # C Language - Moderate Test (25 MCQs, 10 min)
├── chard.html              # C Language - Hard Test (25 MCQs, 10 min)
└── README.md               # Project documentation & deployment guide
```

## Features

- **Authentication Flow:** Client-side user session management via `localStorage` (`skillCheckUsers`, `skillCheckCurrentUser`).
- **Timed Assessments:** 10-minute countdown timer with automatic submission on timeout.
- **Randomized Questions & Options:** Shuffles question order and option order on every attempt while preserving accurate grading.
- **Instant Answer Review:** Displays score percentage, attempted/unanswered counts, color-coded answer highlights, and detailed explanations.
- **Persistent Test History:** Logs scores, skill, difficulty level, and timestamp in `localStorage` (`skillCheckTestHistory`).

## Quick Start & GitHub Pages Deployment

1. **Add Remaining Pages:** Copy `signup.html` and `main.html` into this root folder so navigation links from `login.html` and the test pages resolve cleanly.
2. **Initialize & Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: SkillCheck web application"
   git branch -M main
   git remote add origin https://github.com/<your-username>/skillcheck.git
   git push -u origin main
   ```
3. **Enable GitHub Pages:**
   - Go to **Settings** -> **Pages** in your GitHub repository.
   - Under **Build and deployment** -> **Source**, choose **GitHub Actions** (uses `.github/workflows/deploy.yml`) or **Deploy from a branch** (`main` / `/ (root)`).
   - Your site will be live at `https://<your-username>.github.io/skillcheck/`.
