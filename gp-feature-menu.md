# gp.sahl.ie — the 75 (v2)

The trainee's home on the internet. You come here first: lost, unsure of a diagnosis, or starting a clinic day. Everything is one click, one scroll-and-click, or two clicks away — or one search. Orientation lives here; material stays with its owners. Apple-level calm, FT-level density, the sahl.ie paper-and-forest identity. Owner says yay or nay per line or per group; build order follows his choices.

## 0. The architecture (decided by the owner, 2026-08-23)

* Repo `drsahl/gp` is **private** (done today). Code is no longer public.

* Hosting moves from GitHub Pages to **Cloudflare Pages** (free tier builds from private repos; no build step, output `/`).

* Login is **Cloudflare Access** in front of the site: SSO via **Google and Apple** only (both are built-in Access identity providers; no passwords exist to leak). Users are managed in the Cloudflare Zero Trust dashboard — an email allow-list, one screen, no code. Free tier covers up to 50 users.

* One prerequisite: Cloudflare Access protects hostnames whose DNS runs through Cloudflare, so the sahl.ie zone moves to Cloudflare nameservers. Every existing record is documented (rebuild.md §2.1) and gets recreated first — Zoho MX, SPF, DKIM, zoho-verification, google-site-verification, the four GitHub A records, and the education/www CNAMEs — verified with dig before the Blacknight nameserver flip. Mail and both live sites are untouched by a correct recreation.

* Sequenced so nothing live ever breaks: Cloudflare zone recreated → verify records → flip nameservers → connect Pages to the private repo → Access policy (Google + Apple, email allow-list) → DNS for gp → done.

***

## A. Identity and access (8)

1. SSO sign-in: Google and Apple buttons only. No passwords anywhere in the system.
2. A sign-in page in the identity: paper, crest, one line — "the trainee signs in".
3. User management in Cloudflare Zero Trust: add or remove a doctor by email in one screen.
4. Two tiers: trainee and trainer-admin (the admin sees management rows).
5. Private repo (done). The code is not public.
6. Sessions sane for shared clinic machines: sign-out at day's end, re-auth tomorrow in one tap.
7. Invite flow: paste an email, they have access. Nobody creates an account.
8. Offline grace: once signed in, the timer and calendar keep working through dead clinic wifi.

## B. The front-page law (6)

9. Anything on the site reachable in one click, one scroll-and-click, or two clicks maximum.
10. One persistent search box searching topics, guidelines, calendar entries, and contacts together.
11. Forgiving search: "derm red flags", misspellings, and abbreviations all land.
12. Above the fold always answers "what day is it for me" — next Wednesday needs zero clicks.
13. The updates stream lives on the homepage (group E).
14. First-visit empty states teach by example: three sample searches shown.

## C. The clinic timer (15)

15. Day builder: template (AM surgery / PM surgery / telephone triage / mixed), slot length (10/12/15), patient count. Three taps to a drawn day.
16. Live session view: current slot large, elapsed vs planned, next patient below.
17. "Call next patient" cue at slot end, or early when you finish ahead.
18. "Wrap up" nudge at 80% of the slot — the history-to-examination signal.
19. Phase switcher: hx → exam → plan → clerking/offboarding, each phase timed, building your own rhythm data over weeks.
20. Late-drift meter: minutes behind or ahead, visible, quiet.
21. One-tap +5-minute catch-up buffer; the day re-flows.
22. Breaks, admin, phone-call and home-visit blocks as first-class citizens of the timeline.
23. Inline edit of any slot: lengthen, shorten, rename, reorder, delete.
24. End-of-session summary: on-time rate, overruns, where the day went. Stored locally, exportable.
25. Named personal templates ("Mon AM — 14 × 10min + 2 urgent").
26. Telephone mode: slots that open with "dial" and close with "document".
27. Room display mode: big type, readable from the door.
28. Gentle alerts: visual pulse by default, optional soft chime, never a klaxon.
29. Hand-off line: the day summary formatted to paste into practice notes.

## D. Decision orientation — "come here first" (8)

30. Red-flag click-throughs, starting with derm: three to five questions to "settle, watch, or escalate". Trees orient; the last step links out to the source.
31. The same tree grammar for chest pain, headache, feverish child, back pain, dizziness — the GP classics, added in that order.
32. "What am I missing?" second-check lists per presentation.
33. Safety-netting phrasing bank: the exact sentence to hand the patient, one tap to copy.
34. When-to-refer thresholds per presentation, quoted from the linked guideline with its date.
35. Every tree ends in references (CKS / NICE / DermNet), never in our own medical prose.
36. Trees carry a version and a date. Trust is visible.
37. A "wrong tree?" escape on every step — back to search in one tap.

## E. Staying current — the stream (6)

38. A dated what's-new stream on the homepage: guideline updates and site additions in one feed.
39. Sources watched: NICE, CKS, HSE, ICGP, antibioticprescribing.ie.
40. Every stream item is one line, one link, one date. We never summarise medicine.
41. The site's own changelog flows into the same stream (new tree, calendar change).
42. "New since your last visit" marker, per user, stored locally.
43. Annual calendar diff: the new scheme PDF is re-parsed and diffed against calendar.json; changes proposed for one-click accept.

## F. The calendar (8)

44. Next-up cockpit — the coming Wednesday computed live. ✅ built
45. The radar — weighted weeks with days left. ✅ built
46. The year register with filters and dimmed past weeks. ✅ built
47. PM rhythm and leads. ✅ built
48. calendar.json as the editable single source of truth. ✅ built
49. Rotation timeline: current post, changeover dates, PR-prep weeks.
50. "Read for Wednesday": each topic links straight into the atlas.
51. ePortfolio Sunday-evening nudge with the ICGP link.

## G. The reference atlas (10)

52. The dispatcher: one box routing a query into CKS, NICE, antibioticprescribing.ie, and DermNet searches.
53. Guideline shelf: NICE, SIGN, HSE, ICGP, RCPI — ruled rows, one line each.
54. Calculator set: MDCalc pre-filtered (eGFR, CHA₂DS₂-VASc, HAS-BLED, Wells, CURB-65, QRISK3) plus emed.ie.
55. BNF row for doses and interactions.
56. DermNet NZ — the rash atlas.
57. ECG: ecglibrary.com and LITFL ECG library.
58. Radiopaedia and Radiology Assistant.
59. LITFL for emergency and critical care.
60. GPnotebook for fast differentials.
61. Mental health prescribing: choiceandmedication.org in plain language.

## H. Admin and money (5)

62. Who-to-contact register: scheme office, UL, PCRO — ruled rows; the owner supplies addresses.
63. Renewal countdowns: IMC registration, indemnity, Garda vetting, ATLS/ACLS expiry.
64. Pay and PCRS panel: payslips, PCRS, Revenue in one place.
65. Study-leave pointer: the form and the rules, one row.
66. Audit pipeline tracker and a CBD/mini-CEX counter per rotation.

## I. Craft and comfort (9)

67. The rotating wordmark: the name stays — `sahl.ie` — while the "gp" prefix cycles through funny-professional trainee truths, one per visit or on a slow fade. Starter rotation for the owner's yay/nay: *general practice · genuinely puzzled · growing physician · gentle pacing · guardedly optimistic · good prognosis · gran's pills, explained · gatekeeping, kindly*.
68. The background ghost is gone (removed today, by order).
69. Lamp-off mode: the paper dims for night reading; the choice is remembered.
70. Print: the clinic day sheet and the Wednesday sheet come out as clean A4.
71. Keyboard control: space advances the timer, arrows edit slots, no mouse mid-clinic.
72. Home-screen installable (PWA): full-screen, crest icon, opens like a native app.
73. Privacy: no analytics, no trackers; beyond Cloudflare's access log, nothing clinical leaves the device.
74. Focus type scales: the timer is big and calm; the atlas is dense and FT-like. Each view maximised for its job, desktop and mobile.
75. The colophon row: "built by a trainee, for trainees" — one line in the footer, dated.

***

*Reply with yays and nays — per line, per group, or "A, C, D, G all in; trim the rest". The architecture in §0 proceeds on your word; the Cloudflare dashboard steps are one screen each and I will walk them with you.*

