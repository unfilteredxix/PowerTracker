# Kanyn's Power Tracker

**A gamified behavior tracking app built by someone with zero programming background—just Claude and curiosity.**

## Live Demo

**[Try it here](https://kpt-manage-accordion.netlify.app)** — See the app in action. Log in with any four-digit PIN(1234 default) to explore both kid and parent modes.

---

## What Is This?

A behavior tracking app for a child that uses Dragon Ball Z gamification to make positive habits engaging. The kid logs daily progress across categories like "Listening," "School Effort," and "Health." A parent reviews and finalizes the scores. Points accumulate toward ranks (Base Form → Super Saiyan → Ultra Instinct), coins can be spent on rewards, and achievements unlock as milestones are hit.

It's built to actually work—deployed live, syncing across devices, and actively used.

---

## Why I Built It

I needed a tool that was fair, motivating, and didn't feel punitive. Early versions had harsh penalties that made even good days feel discouraging. Through iteration, I calibrated the point economy so it rewards progress without crushing motivation. The parent review workflow needed to be transparent—parents couldn't see the kid's original scores while entering their own feedback, so I added side-by-side display. Every feature exists because it solved a real problem.

---

## The Stack

- **Frontend**: Vanilla JavaScript (single HTML file), Tailwind-style custom CSS, Chart.js
- **Backend**: Netlify Functions (serverless)
- **Storage**: localStorage (client-side persistence)
- **Hosting**: Netlify
- **No build step** — one HTML file, easy to deploy and easy to reason about

I learned by building. No degree, no bootcamp — just reading docs, asking Claude, and iterating until things worked.

---

## Key Features

- ✅ **Dual Login Modes** — Kid self-reports, parent verifies and adjusts
- ✅ **Power Level System** — DBZ-themed rank progression with visual Ki Aura power bars
- ✅ **Coin Economy** — Earn coins for good days, spend them in the Capsule Corp shop
- ✅ **Streak Bonuses** — Bigger Senzu Bean rewards at 3, 7, and 30-day milestones
- ✅ **Dragon Ball Collection** — Unlockable progression tied to consistent tracking
- ✅ **Weekly History** — Day-by-day breakdown with a week picker
- ✅ **Food & Macro Logging** — USDA FoodData Central integration with offline caching
- ✅ **Bonus Behaviors** — Optional healthy-choice actions (exercise, water over soda) that award coins separately from core scoring
- ✅ **Customizable Categories** — Manage tab lets you adjust tracking areas in-app

---

## The Product Thinking

### Problem: Penalties Felt Harsh
Early versions deducted so many points for tardiness and demerits that even a solid day could end negative. That kills motivation fast.

**Solution:** Rebalanced the math — absences now score zero instead of going negative, tardiness dropped to -5, demerits to -10. A perfect day is achievable, and a rough day isn't devastating.

### Problem: Parent Couldn't See the Kid's Scores While Reviewing
Parents were adjusting their own ratings blind, with no visibility into what the kid had originally logged.

**Solution:** Added a side-by-side display showing both child and parent scores during review. Simple, transparent, and it builds trust in the process.

### Problem: Generic Point System Felt Arbitrary
How many coins should a good day earn? What makes a streak bonus feel fair rather than random?

**Solution:** Grounded the economy in real math, tested against realistic daily score ranges (max 30 pts/day across 6 categories) so streak thresholds and rewards feel earned, not handed out.

### Problem: New Feature Requests Kept Threatening to Complicate Core Scoring
Requests like "give points for exercise" or "reward drinking water instead of soda" could have bloated the main scoring logic.

**Solution:** Built a separate "Bonus Behaviors" track — optional checkboxes that award coins independently, keeping the core daily score clean while still letting the system grow.

---

## How to Use

### For Kids
1. Log in with the shared PIN
2. Rate yourself 0–5 stars on each category
3. Submit for parent review

### For Parents
1. Log in with your PIN
2. Review the kid's scores and add your own (weighted 2x in the final score)
3. Record attendance and any demerits
4. Finalize — points calculate, coins award, streaks and history update

### To Run Locally
```bash
npm install
netlify dev
```
Then open http://localhost:8888

---

## Deployment

Deployed to Netlify as a static single-page app with Netlify Functions for any server-side needs. Push to the connected branch or deploy directly via `netlify deploy --prod` from the CLI.

---

## What I Learned

- **Point economy math matters.** Unfair penalties break motivation — always test against realistic day ranges before shipping.
- **Simplicity wins.** A single well-organized HTML file has been easier to maintain and reason about than I expected.
- **Listen to users.** The bonus behaviors feature, category tweaks, and attendance rules all came directly from real feedback.
- **Ship early, iterate constantly.** This app has gone through 17+ versions while in active daily use. Real usage teaches you things planning never will.

---

## Next Steps

- Monitoring the point economy as more data accumulates
- Potential new tracking categories based on ongoing feedback
- Deeper analytics for long-term trend tracking

---

## About Me

I'm not a programmer. I have no formal CS education — just a few recent Anthropic certifications and a lot of curiosity. This app is what happens when a parent wants to build something meaningful for their kid and has the right tools to make it happen.

---

**Built with zero formal training. Just Claude, curiosity, and a lot of iteration.**
