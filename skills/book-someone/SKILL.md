---
name: book-someone
description: "Send a booking request to a person on Foundaree for the user: \"book this plumber for Saturday morning\", \"ask this dentist for an appointment\", \"get this designer to call me\". Use only when the user asks to book or contact a specific person found on Foundaree. The person sees the request and calls the user back."
argument-hint: "[who and when, e.g. \"book ravi-kumar for Saturday morning\"]"
---

# Book someone on Foundaree

A booking request is a short note to one person: what the user needs, when, and the user's own name and phone number. The person sees it on Foundaree and by email, and calls the user back if they can take the work. No account is needed.

## Steps

1. **Know who.** You need the person's username, from `search_people`, `match_people` or a profile link. Check with `get_person` that the profile says `bookable: true`; if not, share their profile link and public contact details instead.
2. **Collect what is missing**, asking only for what you do not have:
   - what they need, in a sentence or two;
   - when they would like it, in plain words ("Saturday morning");
   - their area, if the work happens at their place (optional);
   - their **own** name and phone number, with country code.
3. **Read it back and get a yes.** Show exactly what will be sent and to whom, and that their number goes only to that person. Send nothing without a clear yes.
4. **Send it** with `request_appointment`.
5. **Say what happens next:** the person calls them back if they can take it. **Nothing is confirmed until they call.**

## Rules

- Only the user's own name and number, given by them in this conversation. Never guess a number, reuse one from elsewhere, or send a request for someone who has not asked.
- One request per person at a time. If Foundaree says the number already has an open request, or that the day's limit is reached, tell the user in plain words and do not retry.
- Never book several people for the same job at once unless the user asks for that.
