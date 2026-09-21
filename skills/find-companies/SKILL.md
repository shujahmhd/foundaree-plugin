---
name: find-companies
description: "Find companies, studios, agencies, clinics and other organizations on Foundaree, and what they are hiring for. Use when the user asks for a company or team rather than one person (\"a design studio in Kochi\", \"a clinic near me\", \"startups working on farming\"), or asks what a company on Foundaree is hiring for."
argument-hint: "[what kind of company, e.g. \"design studio in Kochi\"]"
---

# Find companies on Foundaree

Companies and organizations have public pages on Foundaree, next to the people who run them.

## Steps

1. `search_organizations` with a `query` that says the kind of company and, when known, the city ("design studio Kochi").
2. Show the best few: name, what they do, where, their website if they list one, and their Foundaree page link (`pageUrl`).
3. If the user wants to know what a company is hiring for, or wants work there: `search_opportunities` with the company's name or the role.
4. To reach a company, share its page. To reach a person at it, use the `find-people` skill, then `book-someone` if the user asks for a booking.

## Rules

- Say only what the page says. Never invent what a company does, its size or its prices.
- Foundaree is new, so there may be few companies or none for a city. Say so plainly rather than guessing, and offer to look for individual people instead (`find-people`).
