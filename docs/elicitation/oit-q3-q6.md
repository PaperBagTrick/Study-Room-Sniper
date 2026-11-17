# Elicitation: UTD Office of Information Technology (Q3, Q6)

| Field | Value |
| --- | --- |
| Conducted by | Lee Ballard (elicitation lead) |
| Stakeholder role | UTD OIT (identity / SSO) and campus accessibility staff |
| Channel | Email |
| Sent on | 2026-11-08 |
| Reply received on | 2026-11-11 |
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

Reply from UTD OIT, received 2026-11-11. Summarized in our own words; the raw reply and the sender's name are not stored in the repository.

| Question | Answer in brief | Effect on requirements / design |
| --- | --- | --- |
| Q3 | Students cannot request NetID single sign-on. A UTD faculty or staff member must submit the request (OIT knowledge base article "Request Single Sign-On for Application or Service"). If the professor sponsors the project, they can submit it and state that the app needs only NetID and UTD email. If that route is not available, OIT suggests discussing other sign-in options with the professor. | A3 holds only with a faculty sponsor. CON-01 and ADR-03 now depend on the instructor sponsoring the request. If the instructor will not, a change request to CON-01 is needed (email-verified accounts, as described in A3 and R3). ADR-03 evidence must record this answer. |
| Q6 | OIT pointed to UTD's digital accessibility policy and guidelines on the Web Resources Center "Web Accessibility" page, which reference WCAG 2.1. | QR-04 already targets WCAG 2.2 Level AA, which includes every WCAG 2.1 Level AA success criterion, so meeting QR-04 also meets UTD's 2.1 guideline. No change to QR-04 is required; its source can cite the UTD policy alongside [R5]. |

## Follow-up

- [ ] Update section 11: Q3 answered (faculty sponsor required), Q6 answered (UTD guidelines reference WCAG 2.1; QR-04 at 2.2 AA covers it)
- [ ] Update ADR-03 evidence (section 7.1) with the OIT answer
- [ ] Ask the instructor whether they will sponsor the NetID SSO request
- [ ] If the instructor will not sponsor it, ask Alexander Eng to raise the CON-01 change request (risk R3)
