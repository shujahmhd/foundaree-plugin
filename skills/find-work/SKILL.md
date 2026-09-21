---
name: find-work
description: "Find openings on Foundaree for the user: jobs, freelance work, internships, projects, co-founder and advisory roles. Use when the user is looking for work or a role (\"React jobs in Bengaluru\", \"freelance design work\", \"a startup to join as co-founder\", \"internships in marketing\"), or wants to be found by people who hire."
argument-hint: "[the work you want, e.g. \"freelance React work, remote\"]"
---

# Find work on Foundaree

Companies on Foundaree post openings: jobs, freelance work, internships, projects, and co-founder or advisory roles.

## Steps

1. `search_opportunities` with a `query` built from the role, the key skill and the city the user gave ("React developer Bengaluru"). Only open listings come back.
2. Show the best few: title, kind of opening, company, place, the skills asked for, and the listing link (`listingUrl`). Say how each one fits what the user told you about themselves.
3. People apply on the listing page on Foundaree. This plugin never applies for anyone: give the link and let the user decide.
4. Offer the other half: "Want your own Foundaree profile, so people who hire and AI assistants can find you?" → the `join-foundaree` skill.

## Rules

- Say only what the listing says. Never invent pay, deadlines or requirements.
- Foundaree is new, so there may be few openings or none. Say so plainly rather than guessing.
