# Starbucks Offer Optimization – Capstone Project

This project analyzes a simulated dataset from Starbucks to understand how users respond to different promotional offers inside the app. By exploring offer types, user demographics, delivery channels, and behavior over time, we uncover actionable strategies for maximizing user engagement and conversions.

Blogpost is here: https://medium.com/p/f7bca6020562/edit

---

## Dataset Overview

The project is based on 3 primary files:

- `profile.json` — 17,000 user profiles with age, gender, income, and membership date
- `portfolio.json` — 10 promotional offers with metadata (type, difficulty, reward, channel, duration)
- `transcript.json` — 306,000+ user events including offer received/viewed/completed and transactions

---

## Data Cleaning

- Removed invalid/missing demographics (age=118, null income/gender)
- Normalized nested JSON fields (`value`, `channels`)
- Unified event log by merging all 3 files
- Manually exploded multi-channel delivery data
- Calculated derived fields like offer response delays and influenced/organic transaction flags

---

## Analysis Goals

1. **Evaluate offer effectiveness** (view and completion rate)
2. **Analyze behavior by demographics** (age, income, gender)
3. **Compare performance across channels** (email, mobile, web, social)
4. **Understand timing patterns** (how quickly users act)
5. **Separate organic purchases vs offer-influenced**

---

## Key Findings

- **Discounts** outperform BOGO offers in completion rate
- Older and higher-income users are more responsive
- **Social** has the highest view rate; **Web** has the highest completion rate
- Most offers are viewed within 12 hours and completed within 1–2 days
- **Organic purchases are rare** (~0.01%)

---

## 🛠Tech Stack

- Python (Pandas, NumPy, Seaborn, Matplotlib)
- Jupyter Notebook
- JSON processing and time series event engineering

---

## Final Insight

> The Starbucks app is highly dependent on promotional offers. By targeting the right offer type (discount), using the right channel (social/web), and following up at the right time (within 48 hours), marketers can significantly increase user engagement and conversions.
