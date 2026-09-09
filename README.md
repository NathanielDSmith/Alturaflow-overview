AlturaFlow

This isn't the actual codebase. AlturaFlow is a live fintech product and the code is proprietary, so I can't share it here. This is just a writeup of what I actually built while I was there.

About the company

AlturaFlow is a fintech startup building tools for retail traders. I worked there for about a year as a backend/full-stack engineer, building most of the core data infrastructure from scratch.

What I built

Market scanner (Python, Flask, PostgreSQL)

Built a scanner that tracks 12,000 to 13,000 tickers. It pulled data from two separate sources and cross checked them against each other, so discrepancies got caught before they ever reached a user. Data came in batches of around 8,000 records at a time, processed in chunks of 100. It ran in production for close to a year without needing a rewrite.

Discord bot

Built and maintained a Discord bot serving around 100 active users. It pushed real time alerts based on what the scanner picked up. Had to deal with the normal headaches of running a live bot too, rate limits, uptime, keeping the alert logic in sync whenever the backend changed.

Dashboards (React, TypeScript)

Built the frontend on top of the scanner data. The main goal was making a lot of dense financial data actually readable at a glance instead of overwhelming.

Why there's no code or demo here

I don't have the rights to share it and there's no public demo to link to since it's a live product. If you want to know more about how any of it works, happy to go through it in an interview. I know this system well enough to talk through the actual decisions, not just what it does on paper.

Stack

Python, Flask, PostgreSQL, React, TypeScript, Discord API
