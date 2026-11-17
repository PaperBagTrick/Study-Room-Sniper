# Elicitation: McDermott Library reservations staff (Q1, Q2, Q4)

| Field | Value |
| --- | --- |
| Conducted by | Lee Baillard (elicitation lead) |
| Stakeholder role | McDermott Library reservations / systems staff |
| Channel | Email |
| Sent on | 2026-11-08 |
| Reply received on | 2026-11-11 |
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

Reply from library reservations staff, received 2026-11-11. Summarized in our own words; the raw reply and the sender's name are not stored in the repository.

The library declined to support or approve the project. LibCal does have an API, but the library cannot grant access narrow enough for this app: any access that returns the availability data the app needs would also expose confidential information about existing bookings, which the library treats as a privacy and security risk.

| Question | Answer in brief | Effect on requirements / design |
| --- | --- | --- |
| Q1 | LibCal has an API, but the library will not grant access to it, because the access needed would also expose confidential booking data. | The API route is closed. A1 cannot be met through a supported channel. R1 is realized for the API route; ADR-02 evidence must record this. |
| Q2 | The library did not approve the project, so automated reading and alerting students are not approved. No request rate was offered. | A2 does not hold. R2 is realized. Following the R2 mitigation (pause reading if the library objects) and A1's fallback, the team should not read live library availability and should demonstrate against recorded sample data or the stub library system. Change request needed for FR-03, FR-04 and FR-05 (section 0.2). |
| Q4 | Not answered, because the library declined the project as a whole. | Keep the interim definition: "bookable" means free (section 1.3). |

The reply also supports CON-02 and QR-06: the library's concern is the privacy of booking data, which the design already avoids by never holding credentials or booking data.

## Follow-up

- [ ] Update section 11: Q1 and Q2 answered (declined), Q4 unanswered (interim assumption kept)
- [ ] Tell Arshan Khimani: R1 and R2 realized; spike S-01 should use recorded or replayed data, not live reads
- [ ] Ask Alexander Eng to raise a change request in section 0.2 to move FR-03 to FR-05 onto recorded sample data or the stub
- [ ] Update risk statuses for R1 and R2 in section 10.3 (with Isaam Memon)
