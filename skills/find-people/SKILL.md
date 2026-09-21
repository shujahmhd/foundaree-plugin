---
name: find-people
description: "Find real people on Foundaree, a free public directory: someone to hire (a developer, designer, accountant, doctor, tutor), a local service (electrician, plumber, driver, cleaner, home nurse), or a co-founder or teammate with given skills. Use when the user asks to find, recommend, shortlist or compare people for work, by job, city or area, skills, or who is free now."
argument-hint: "[who you need, e.g. \"a React developer in Bengaluru who is free now\"]"
---

# Find people on Foundaree

Foundaree is a free public directory of real people, in two groups: hands-on local work (trades, repairs, driving, care) and office or professional work (software, design, health, business). Everyone listed made, or claimed, their own profile.

Use the `foundaree` connector's tools.

## Which tool

- **The user names a job and a place** ("an electrician in Kochi", "a dentist in Pune"): `search_people` with `query` for the job, plus `location` (city), `area` (neighbourhood) and `availability: "available"` when they need someone now.
- **The user describes a need by skills** ("a co-founder who knows React and sales"): `match_people` with `skills`. It ranks people by how many of the skills they have; someone with 3 of 5 still shows, below someone with 5.
- **The user picks someone**: `get_person` with the username, for the full profile: skills, experience, projects, proof, and phone, WhatsApp or email when the person made them public.

If a search finds nobody, widen it once (drop the area, then the availability) and say that you did. Foundaree is new, so some cities have few people: say so plainly rather than padding the answer.

## How to answer

- Lead with the 3 to 5 best fits, one or two lines each: name, what they do, where, whether they are free, and why they fit what the user asked for.
- Always give each person's profile link (`https://foundaree.com/person/<username>`).
- Say only what the profile says. Never invent skills, prices, reviews or availability.
- What the badges mean: **Verified** (they proved a phone, GitHub or Google account), **Proof: N of 3** (proven GitHub facts, a website that links back), **Founding member** (one of the first 150 members; among equal matches they are listed first), **Foundaree founder / team** (Foundaree's own people).
- Contact details come only from `get_person`, and only when the person made them public. Never guess a number.

## Next steps to offer

- "Want me to ask them for a booking?" → the `book-someone` skill.
- "Want your own profile so people and AI assistants can find you?" → the `join-foundaree` skill.
- A company or team rather than one person → the `find-companies` skill. Work for the user → the `find-work` skill.
