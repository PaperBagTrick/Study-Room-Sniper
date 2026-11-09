# Elicitation: UTD Office of Information Technology (Q3, Q6)

| Field | Value |
| --- | --- |
| Conducted by | Lee Ballard (elicitation lead) |
| Stakeholder role | UTD OIT (identity / SSO) and campus accessibility staff |
| Channel | Email |
| Sent on | 2026-11-08 |
| Reply received on | Pending |
| Questions | Q3, Q6 (P2 document, section 11) |
| Requirements affected | FR-02, FR-08, QR-04, QR-06, CON-01; assumption A3; ADR-03; risk R3 |

## Message sent

> **Subject:** Student course project: NetID sign-in and accessibility standard
>
> Hello,
>
> I am a UTD student in CS/SE 3354 (Software Engineering). My team is designing a class project called Study Room Sniper, a small web app that emails a student when a McDermott Library study room they want becomes free. We would like it to follow UTD policy, and we have two questions.
>
> 1. **NetID sign-in.** Can a student course project register to use UTD NetID single sign-on? If so, what is the process, and which identity details would the app receive? We only need the NetID and the student's email address, and those are the only personal data we plan to store. Is there a claim that confirms the user is a currently enrolled student? If student projects cannot use NetID SSO, is there an approved alternative you would recommend?
> 2. **Accessibility.** Which accessibility standard does UTD expect a campus-facing web service to meet? We are currently designing to WCAG 2.2 Level AA.
>
> This is a course project with no budget and no commercial purpose. If another office handles these questions, I would be grateful to be pointed to the right contact.
>
> Thank you,
> Lee Ballard
> CS/SE 3354, Team 4, section .003
> Project repository: https://github.com/PaperBagTrick/Study-Room-Sniper

## Reply summary (de-identified)

_Pending. When a reply arrives, summarize it here in your own words. Do not paste the raw reply or include names or contact details._

| Question | Answer in brief | Effect on requirements / design |
| --- | --- | --- |
| Q3 | Pending | Confirms CON-01, A3 and ADR-03, or triggers a change request to CON-01 (email-verified accounts) |
| Q6 | Pending | Confirms or changes the standard in QR-04 |

## Follow-up

- [ ] Update section 11 status for Q3 and Q6
- [ ] Update ADR-03 evidence (section 7.1) with the OIT answer
- [ ] If NetID SSO is refused, ask Alexander to raise the CON-01 change request (risk R3)
