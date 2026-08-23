# gp.sahl.ie — the feature menu (yay / nay per line or per group)

Owner picks. Nothing below group C is built until approved. Design bar: Apple-level polish, FT-level information density, sahl.ie paper-and-forest identity, desktop and mobile as first-class citizens. Privacy default: no accounts, no tracking, everything stored in the browser.

---

## A. The clinic timer (your headline ask — "set my clinic for the day in a few clicks")

1. **Day builder** — pick a template (AM surgery / PM surgery / telephone triage / mixed), choose slot length (10 / 12 / 15 min) and patient count; the day is drawn in three taps.
2. **Live session view** — the current slot large on screen, elapsed vs planned, next patient named below.
3. **"Call next patient" cue** — fires at slot end, or early if you finish ahead.
4. **"Wrap up" nudge** — at 80% of the slot, a quiet signal: move from history to examination.
5. **Phase switcher** — one tap moves the consultation through hx → exam → plan → clerking/offboarding; each phase is timed so you learn your own rhythm over weeks.
6. **Late-drift meter** — minutes behind (or ahead of) schedule, always visible, never shouting.
7. **Catch-up insertion** — one tap inserts a +5 min buffer without rebuilding the day.
8. **Breaks and admin blocks** — tea, paperwork, phone calls, home visits as first-class blocks in the same timeline.
9. **Inline editing** — tap any slot to lengthen, shorten, rename, reorder, delete. The day re-flows instantly.
10. **End-of-session summary** — on-time rate, overruns, where the day actually went. Kept locally, exportable.
11. **Saved templates** — your real clinic shapes saved by name ("Mon AM — 14 × 10min + 2 urgent").
12. **Telephone mode** — slots that start with "dial" and end with "document", for triage mornings.
13. **Room display mode** — a big-type, glance-from-the-door layout for the clinic monitor.
14. **Gentle alerts** — visual pulse by default; optional soft chime; never a klaxon. Apple-approved calm.
15. **Offline-first** — works with the clinic wifi down. Everything in localStorage, survives a browser restart.

## B. The reference atlas ("GP trainee Google + UpToDate — by reference, not material")

16. **Search dispatcher** — one box: type "cellulitis" and get direct links into CKS, NICE, antibioticprescribing.ie, and DermNet searches. We link to the sources; we never host the medicine.
17. **Guideline shelf** — NICE, SIGN, HSE, ICGP, RCPI: one ruled row each, one-line descriptions.
18. **CKS deep links** — NICE Clinical Knowledge Summaries, the trainee's actual UpToDate-equivalent.
19. **Calculator set** — MDCalc pre-filtered: eGFR, CHA₂DS₂-VASc, HAS-BLED, Wells, CURB-65, QRISK3, plus emed.ie.
20. **Antibioticprescribing.ie quick panel** — the HSE formulary one tap away.
21. **BNF row** — bnf.nice.org.uk for doses and interactions.
22. **DermNet NZ** — the dermatology atlas, for the Friday-afternoon rash.
23. **ECG library** — ecglibrary.com and LITFL ECG, with ECG Wave-Maven as backup.
24. **Radiopaedia + Radiology Assistant** — imaging appearances and protocols.
25. **LITFL** — emergency and critical care reference.
26. **GPnotebook** — quick differential refreshes.
27. **Mental health prescribing** — choiceandmedication.org (HEE) for psych meds in plain language.
28. **Pregnancy and drugs** — UKTIS/bumps for safety questions.
29. **Travel medicine** — fitfortravel / NaTHNaC for the "I'm going to Thailand next week" consult.
30. **"Read for Wednesday" links** — each topic in the year register gets a one-tap reading link into the atlas, so day-release prep is one click from the calendar.

## C. The calendar (already built — included for the count)

31. **Next-up cockpit** — the coming Wednesday computed live: topic, lead, onsite/blended, countdown. ✅ built
32. **The radar** — residential, SJT/CPST, primary reviews, conference, CPC, RCPAC, semester turns, days left. ✅ built
33. **The year register** — all 54 Wednesdays, filters, past weeks dimmed. ✅ built
34. **PM rhythm + leads** — the afternoon shape and who leads what. ✅ built
35. **calendar.json as public data** — one file to edit when the scheme moves a date. ✅ built
36. **Rotation timeline** — current post and changeover dates (from the training calendar PDF), with PR-prep weeks flagged.
37. **ePortfolio prompt** — a Sunday-evening "log your week" nudge with the ICGP ePortfolio link.
38. **Audit pipeline tracker** — idea → data → analysis → presentation, with audit-week radar entries linked.
39. **Trainer-meeting checklist** — a printable agenda skeleton for trainer reviews.
40. **CBD / mini-CEX counter** — tally assessments per rotation, target vs done.

## D. Admin and money

41. **Who-to-contact register** — scheme office, UL, PCRO: name, email, phone (you supply the addresses; we rule the rows).
42. **Renewal reminders** — IMC registration, indemnity, Garda vetting, ATLS/ACLS expiry: dates in, countdowns out.
43. **Pay and PCRS panel** — payslips, PCRS, Revenue links in one place.
44. **Study-leave pointer** — the form and the rules, one row.

## E. Craft and comfort

45. **Lamp-off mode** — the paper dims to a night variant for reading in bed. One toggle, remembered.
46. **Print the day** — the clinic plan and the Wednesday sheet print as clean A4.
47. **Keyboard control** — space advances the timer, arrows move slots, no mouse needed mid-clinic.
48. **Home-screen app** — installable (PWA), opens full-screen like a native app, custom crest icon.
49. **Zero-account privacy** — no logins, no cloud, no analytics. Your clinic never leaves the device.
50. **Focus typography** — the timer view gets a larger, calmer type scale; the reference view gets the dense FT register. Each view maximized for its job, desktop and mobile.
51. **Hand-off mode** — end-of-day summary formatted for pasting into the practice notes or WhatsApp to a colleague.

## F. Later, if you want them

52. **Countdown to MICGP exams** — once you name the exam date, it joins the radar permanently.
53. **Shared scheme calendar** — one calendar.json per scheme, so trainees elsewhere fork the page.
54. **Widget** — next Wednesday on the phone home screen.
55. **The annual diff** — a yearly pass that re-parses the new PDF and diffs it against calendar.json automatically.

---

*Reply with yays and nays — per line, per group, or "all of A and C, none of F". I build in that order.*
