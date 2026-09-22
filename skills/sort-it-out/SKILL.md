---
name: sort-it-out
description: "Hand the whole errand to Foundaree when the user wants someone found AND asked, not a list to choose from: \"sort out an electrician for Saturday\", \"get me a home nurse this week\", \"find a plumber and book them\", \"just handle it\". Foundaree searches, ranks, asks the best one to three people and reports who was asked; later it says who accepted. Use when the user wants it done, not browsed."
argument-hint: "[the need, place and time, e.g. \"an electrician in Kochi on Saturday morning\"]"
---

# Sort it out on Foundaree

Some people want a shortlist. Others want it handled. This skill is for the second kind: the user says what they need, where and when, and Foundaree does the finding, the ranking and the asking itself. You never pick a person; you carry the errand and report back.

Use the `foundaree` connector's `find_and_ask` and `check_errand` tools.

## Steps

1. **Collect what is missing**, asking only for what you do not have:
   - what they need, in a sentence ("an electrician for a fan and two sockets");
   - the city, and the area if it matters;
   - when, in plain words ("Saturday morning");
   - their **own** name and phone number, with country code.
2. **Read it back and get a yes.** Say that Foundaree will ask up to two people (or however many they want, up to three), that each gets their name and number, and that whoever can take it will call them. Send nothing without a clear yes.
3. **Run it** with `find_and_ask`. Two people is the usual choice: a fallback without pestering.
4. **Report exactly what it says.** Who was asked (with profile links), who was skipped and why, and whether the search had to widen to find enough people. If nobody could be asked, say so plainly and offer the `find-people` skill instead.
5. **Keep the `errandId`.** When the user later asks "did anyone get back to me?", call `check_errand` and tell them who accepted, who declined, and who has not answered.

## Rules

- Only the user's own name and number, given by them in this conversation. Never guess or reuse a number.
- Do not run the same errand twice for the same need. Foundaree will refuse to ask the same person again while a request is open, and the report will say so.
- If Foundaree says the number's allowance for the day is spent, tell the user and stop. Do not try with another number.
- **Nothing is confirmed until someone calls.** Say that every time.
- When the user names one specific person, use the `book-someone` skill instead: that is a single request, not an errand.
