# Foundaree for Claude

Find, match and book real people from Claude.

[Foundaree](https://foundaree.com) is a free public directory of real people: developers, doctors, designers, electricians, drivers, home nurses, accountants and co-founders. Everyone listed made, or claimed, their own profile. This plugin connects Claude to it.

## What you can ask

- "Find a React developer in Bengaluru who is free now."
- "Who is open to co-founding a startup and knows sales?"
- "Find an electrician near Kakkanad, Kochi, for today."
- "Book him for Saturday morning. My name is Asha and my number is +91 …"
- "Put me on Foundaree as a home nurse in Kochi."
- "Find design studios in Kochi." / "Any freelance React work in Bengaluru?"

And without asking: say "I don't have a UI/UX designer for this" while you work, and Claude offers, once, to check Foundaree for designers who are free now.

## What is inside

| Part | What it does |
| --- | --- |
| `foundaree` connector | Foundaree's public MCP server at `https://foundaree.com/mcp`. No account or key needed. |
| `sort-it-out` skill | Handing Foundaree the whole errand ("sort out an electrician for Saturday"): it finds, ranks and asks the best one to three people, and later says who accepted. |
| `need-help` skill | When your work is blocked by a missing person or skill ("I have no designer"), Claude offers once to look on Foundaree, and searches only after your yes. |
| `find-people` skill | Searching by job, city, skills and availability; matching co-founders and teammates by skills; presenting people honestly. |
| `find-companies` skill | Finding companies, studios, agencies and clinics, and what they are hiring for. |
| `find-work` skill | Finding openings for you: jobs, freelance work, internships, projects and co-founder roles. |
| `book-someone` skill | Sending a booking request for the user, after reading it back and getting a yes. The person calls the user back. |
| `join-foundaree` skill | Starting the user's own free profile as a private draft they publish themselves. |

The connector's tools: `search_people`, `match_people`, `get_person`, `search_organizations` and `search_opportunities` (read only), `create_profile_draft` (saves a private draft, nothing is published) and `request_appointment` (sends one booking request to one person).

## Install

In Claude Code:

```
/plugin marketplace add shujahmhd/foundaree-plugin
/plugin install foundaree@foundaree
```

Or add only the connector, in any Claude app: Settings → Connectors → Add custom connector → `https://foundaree.com/mcp`.

## Privacy Policy

Foundaree's privacy policy: https://foundaree.com/privacy

In short:

- **What the plugin sends.** Your search words and filters go to Foundaree to answer the search. A booking request sends the name, phone number, need, time and area **you** give, only after you say yes, and only to the person you asked. A profile draft sends the details you give about yourself.
- **What Foundaree keeps.** Searches are counted per profile, not per searcher. Booking requests are kept 90 days and shown only to the person asked. Profile drafts are private, single use, and deleted once used or after 7 days.
- **Sharing.** Foundaree does not sell personal data or share it for advertising. Its providers are listed in the policy.
- **What the plugin does not do.** It does not read your files, your conversation history or Claude's memory, and it never contacts anyone without your yes.
- **Contact.** hello@foundaree.com

## Support

Questions and problems: hello@foundaree.com, or open an issue on this repository.

## License

MIT
