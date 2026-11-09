# Elicitation: McDermott Library reservations staff (Q1, Q2, Q4)

| Field | Value |
| --- | --- |
| Conducted by | Lee Baillard (elicitation lead) |
| Stakeholder role | McDermott Library reservations / systems staff |
| Channel | Email |
| Sent on | 2026-11-8 |
| Reply received on | Pending |
| Questions | Q1, Q2, Q4 (P2 document, section 11) |
| Requirements affected | FR-03, FR-04, QR-05, CON-02; assumptions A1, A2, A6; ADR-02; risks R1, R2 |

## Message sent

> **Subject:** Student course project: question about reading study room availability
>
> Hello,
>
> I am a UTD student in CS/SE 3354 (Software Engineering). My team is designing a class project called Study Room Sniper. It would send a student an email when a McDermott group study room that fits their needs becomes free, with a link to the library's booking page. The student would still book the room themselves on LibCal. Our tool would never create, change or cancel a reservation, and it would never ask for anyone's library login.
>
> Before we build anything, we want to make sure this is acceptable to the library. Could you help with these questions?
>
> 1. Is there a supported way for a program to read study room availability (for example a feed, an API, or the public LibCal availability pages) without signing in? If so, which one would you prefer we use, and on what terms?
> 2. Would the library be comfortable with a read-only service checking availability automatically, at no more than 20 requests per minute in total (about one check per room every two minutes, during opening hours only)? Is there a lower rate, or a back-off rule, you would like us to follow? We would stop immediately if asked.
> 3. Is it acceptable for an unofficial student service to tell students when a room opens up?
> 4. When a slot shows as free, can any enrolled student book it, or do individual limits (the 7-day window, the 4-hour maximum, one active reservation per 24 hours) mean it may not be bookable for a particular student? Is room capacity reliably shown on the availability pages?
>
> This is a course project with no budget and no commercial purpose. If someone else at the library is the right contact, I would be grateful to be pointed to them.
>
> Thank you for your time,
> Lee Baillard
> CS/SE 3354, Team 4, section .003
> Project repository: https://github.com/PaperBagTrick/Study-Room-Sniper

## Reply summary (de-identified)

_Pending. When a reply arrives, summarize it here in your own words. Do not paste the raw reply or include names or contact details._

| Question | Answer in brief | Effect on requirements / design |
| --- | --- | --- |
| Q1 | Pending | Confirms or changes A1, FR-03, ADR-02 |
| Q2 | Pending | Confirms or changes A2, QR-05; closes or escalates R2 |
| Q4 | Pending | Fixes the meaning of "bookable" (section 1.3); FR-04, A6 |

## Follow-up

- [ ] Update section 11 status for Q1 (with Arshan), Q2 and Q4
- [ ] If the library sets a lower rate or refuses, raise a change request in section 0.2 (Alexander)
