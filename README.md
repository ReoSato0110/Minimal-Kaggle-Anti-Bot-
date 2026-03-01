README.md (Draft)
Kaggle Anti-Bot Protocol (KABP) 🛡️
"Because if your LB is a lottery, it's not data science—it's gambling."
This is a lightweight, entropy-based detection engine designed to expose Sybil Attacks and Lottery Submission patterns on Kaggle leaderboards.

When a "Contributor" with zero history submits the same public notebook with a 4-minute uniform interval, it's not a "classroom assignment." It's a low-effort bot farm exploiting the variance of the private test set. This script catches them.

🧠 The Logic (Why this works)
Human behavior is messy. It has "burstiness" and "idle time."
Bots, however, are victims of their own loops. They tend to follow:

Low Entropy Intervals: Submission timestamps that fit a uniform distribution (K-S Test).

Zero Variance Collusion: Identical scores and metadata across multiple "unique" accounts.

🚀 Quick Start
Bash

pip install pandas numpy scipy
python kabp_detector.py --input leaderboard.csv
🛠 Features (Alpha)
Statistical Uniformity Check: Uses Kolmogorov-Smirnov to detect non-human submission cadences.

Clone Detection: Flags clusters of accounts submitting identical artifacts.

Shame-as-a-Service: Generates a list of suspicious UIDs for manual flagging.

⚠️ Disclaimer
"Verified on my machine (mostly)."
I wrote this in a 15-minute caffeine-fueled sprint. If it throws a KeyError, submit a PR or stop complaining. We're here to catch bots, not to write enterprise-grade boilerplate.
