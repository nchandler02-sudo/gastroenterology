# Gut Check GI 🩺

A gamified GI (Gastroenterology) education platform for medical residents and students. Built as a lightweight, single-page web app with no framework dependencies.

## What's Inside

- **20 GI Topics** — each with 5 clinical sections (Panic Card, Overview, ICU Triggers, Orders, CDI Documentation)
- **40 ABIM-Style Questions** — 2 per topic with detailed rationales
- **80 Flash Cards** — 4 per topic for rapid recall
- **Pre-Test & Post-Test** — 20-question assessments with per-topic score breakdown
- **Gamification** — XP, levels, streaks, badges, coins, and topic completion tracking
- **Dark/Light Theme** — toggle in sidebar
- **Mobile Responsive** — works on phone, tablet, and desktop
- **LocalStorage Persistence** — progress saves automatically in your browser

## Quick Start

### Option 1: Local Development

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/gut-check-gi.git
cd gut-check-gi

# Serve with any static server:
npx serve .
# or
python3 -m http.server 8000
```

Then open `http://localhost:3000` (or `:8000`).

> ⚠️ **Important**: You must use a local server. Opening `index.html` directly as `file://` will fail because `data.json` is loaded via `fetch()`, which requires HTTP.

### Option 2: GitHub Pages (Free Hosting)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to **main branch**, root directory
4. Your app will be live at `https://YOUR_USERNAME.github.io/gut-check-gi/`

### Option 3: Netlify / Vercel

Just drag the folder into [Netlify Drop](https://app.netlify.com/drop) or connect the repo to Vercel. Zero config needed.

## File Structure

```
gut-check-gi/
├── index.html    ← App code (35KB) — all HTML, CSS, JS in one file
├── data.json     ← Topic content, quizzes, assessments (270KB)
└── README.md     ← This file
```

## How It Works

### Learning Flow
1. **Onboarding** — Enter name and PGY level
2. **Pre-Test** — 20 ABIM-style questions (optional, can skip)
3. **Study Topics** — Open topics, read sections, answer quizzes, flip flash cards
4. **Post-Test Unlocks** — Complete 16 of 20 topics to unlock the post-test
5. **Compare Scores** — See pre vs. post improvement

### Topic Completion (3 of 4 criteria)
- ✅ Opened the topic
- ✅ Viewed 3+ sections
- ✅ Answered all ABIM quiz questions
- ✅ Flipped all flash cards

### XP & Levels
| Action | Base XP |
|--------|---------|
| Open a new topic | 10 |
| View a section | 5 |
| Correct quiz answer | 25 |
| Incorrect quiz answer | 5 |
| Flip a flash card | 5 |
| Complete pre-test | 100 |
| Complete post-test | 250 |

**Streak multiplier**: 3+ days = 1.5×, 5+ days = 2×, 7+ days = 2.5×

### 15 Badges
Streak milestones, question counts, topic progress, assessment completion, and score improvement.

## Topics Covered

1. Upper GI Bleeding
2. Lower GI Bleeding
3. Acute Pancreatitis
4. Acute Hepatitis
5. Acute Liver Failure
6. Cirrhosis & Portal Hypertension
7. Hepatic Encephalopathy
8. Spontaneous Bacterial Peritonitis
9. Inflammatory Bowel Disease
10. C. difficile Infection
11. Peptic Ulcer Disease
12. GERD & Esophageal Disorders
13. Celiac Disease
14. Acute Diarrhea
15. Chronic Diarrhea
16. Hepatitis B & C
17. Mesenteric Ischemia
18. Biliary Disease
19. Colorectal Cancer Screening
20. Nutrition & Enteral Feeding

## Tech Stack

- Vanilla HTML/CSS/JS (no React, no build step)
- Google Fonts (DM Sans + Playfair Display)
- LocalStorage for persistence
- `fetch()` for loading `data.json`

## License

Educational use. Clinical content is guideline-sourced and intended as a study aid, not a substitute for clinical judgment.
