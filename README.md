# AlturaFlow

This isn't the actual codebase. AlturaFlow is a live fintech product and the code is proprietary, so I can't share it here. This is a writeup of what the product does and what I worked on while I was there.

## About the company

AlturaFlow is a fintech startup building tools for retail traders, market scanning, chart analysis, and trade execution in one platform. I worked there for about a year as a backend/full-stack engineer, as part of a small founding team.

## The product

<img width="1881" height="911" alt="image" src="https://github.com/user-attachments/assets/af2ba626-5061-426a-b907-9476028f2108" />

*The scanner surfaces setups across thousands of symbols, with direction, win rate, and suggested entry, stop loss, and take profit levels.*
<br><br>
<img width="1901" height="912" alt="image" src="https://github.com/user-attachments/assets/923b90c9-5e09-464b-a265-a6de79daf7e1" />

*Scanner output feeds directly into a trade setup, with live charting and order placement side by side.*
<br><br>
<img width="1878" height="888" alt="image" src="https://github.com/user-attachments/assets/5281b71e-c066-409a-a513-ce789157433d" />

*Positions and watchlist in one view.*

## What I built

**Market scanner (Python, Flask, PostgreSQL)**

Built a scanner that tracks 12,000 to 13,000 tickers. It pulled data from two separate sources and cross checked them against each other, so discrepancies got caught before they ever reached a user. Data came in batches of around 8,000 records at a time, processed in chunks of 100. It ran in production for close to a year without needing a rewrite.

**Discord bot**

Built and maintained a Discord bot serving around 100 active users. It pushed real time alerts based on what the scanner picked up. Had to deal with the normal headaches of running a live bot too, rate limits, uptime, keeping the alert logic in sync whenever the backend changed.

**Dashboards (React, TypeScript)**

Built parts of the frontend on top of the scanner data, focused on making dense financial data readable at a glance.

As a small team, most of us touched more than one part of the product, so the screenshots above show the platform as a whole rather than being a one to one map of what I personally built.

## Why there's no code or demo here

I don't have the rights to share it and there's no public demo to link to since it's a live product. If you want to know more about how any of it works, happy to go through it in an interview. I know this system well enough to talk through the actual decisions, not just what it does on paper.

## Stack

Python, Flask, PostgreSQL, React, TypeScript, Discord API
