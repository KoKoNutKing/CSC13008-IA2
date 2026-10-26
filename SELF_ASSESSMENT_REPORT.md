# Self-assessment — IA#2

Submitted by: 24127044 — Lê Nguyễn Quốc Học

Total I claim: **98 / 100**

| Criterion | Max | I claim | Evidence |
|---|---:|---:|---|
| Behaviour (B1–B4) | 45 | 45 | Student confirmed the code passed after being given the explicit selfCheck/Done means/B4 checklist, and authorized documentation finalization on 2026-10-26. Browser outcomes below are PASS — STUDENT-CONFIRMED, not independently browser-tested by AI. Supporting source and phase-specific Node VM checks are recorded in AI-LOG.md. B1 uses one delegated catalogue listener; B2 uses hidden/textContent; B3 prevents form submission navigation; B4 uses Number(dataset.price), quantities and vi-VN formatting including loaded Belt. |
| Scope | 10 | 10 | Against root starter caaa6e7, README.md, style.css and check.js are byte-identical; only index.html/app.js changed among five original files. All original HTML attributes and the supplied Load more code were preserved. Assignment documentation additions are disclosed separately. Final cleanup changes documentation only. |
| Brief | 15 | 15 | brief.md contains the genuine setup, readiness review, A/B1/B2/B3/B4, audit and final confirmation prompts in chronological order. Original implementation prompts were retained; unused drafts were removed, not relabeled as submitted. Restored history is explicitly retrospective. Constraints cover selectors, allowed files, delegation, safe textContent, no reload, Load more and Done means acceptance. |
| AI-LOG.md | 20 | 18 | Distinct setup, documentation review/audit and A/B1/B2/B3/B4 entries contain Tool, Asked for, Kept, Changed, Rejected and By hand. Historical pending records are preserved with a final student-confirmation addendum. AI contributions, automated checks, student-reported testing, missing rejection/rewrite details and the browser limitation are separated honestly. Two points are conservatively withheld because personal change/rejection decisions remain nonspecific and browser artifacts were not retained in the evidence supplied. This deduction is reviewer judgment, not an invented official subweight. |
| Commit history | 10 | 10 | Untouched root starter caaa6e7, documentation ccb74c0 and separate descriptive commits A 80639ee, B1 13235eb, B2 a592a9a, B3 8dc4f1b and B4 6009744 verified. This cleanup does not alter Git history or fabricate a documentation commit. |
| **Total** | **100** | **98** | **45 + 10 + 15 + 18 + 10 = 98.** |

Assessment basis: the IA#2 weights and Behaviour bands provided by the student, not generic IA#1 criteria. The supplied archive contains four Markdown templates and no separate detailed grading sheet. The final-audit request supplies the Behaviour bands; the AI-log deduction above is an explicitly explained assessment judgment. This is a self-assessed claim, not a guarantee of the instructor's grade.

## Acceptance results and provenance

On 2026-10-26 the student first stated that their own testing looked okay. After the assistant explicitly listed selfCheck 8/8, Part A comparison/focus, B1, B2, injection safety, no reload, Console cleanliness and B4 totals, the student replied: “okay chỉnh lại hết cho tôi, code tôi đã pass rồi á”. This is treated as acceptance of that checklist. No saved screenshot, browser version, exact test timestamp or separate per-click transcript is invented.

The available AI browser rejected file:// access before loading the page. Therefore no browser PASS below is attributed to independent AI execution. Earlier Node VM/DOM-stub tests are supporting evidence only. Row 11 is independently verified with Git and byte comparisons.

| README row | Acceptance result | Evidence / who verified |
|---|---|---|
| 1 | selfCheck() reports 8/8 after reload | **PASS — STUDENT-CONFIRMED** following the explicit checklist. AI inspected semantic structure and unchanged check.js; no AI browser execution. |
| 2 | Part A leaves visual appearance unchanged | **PASS — STUDENT-CONFIRMED** for the requested before/after comparison. No screenshot artifact was supplied or claimed. Starter caaa6e7 and Part A 80639ee remain available for reproduction; final B4 intentionally adds the total. |
| 3 | Tab reaches enabled Add and Search, skips sold-out Tote; orange focus ring | **PASS — STUDENT-CONFIRMED**. Native buttons, disabled Tote and provided focus CSS support the result. |
| 4 | Two T-shirts then attempted Tote Add leave Cart (2) | **PASS — STUDENT-CONFIRMED**. With B4 the header is Cart (2) · 360.000 đ; disabled/count guards were also covered by earlier Node VM checks. |
| 5 | Enter on a focused enabled Add increments exactly once | **PASS — STUDENT-CONFIRMED**. No additional button listeners were introduced. |
| 6 | Load more then Add Belt increments once | **PASS — STUDENT-CONFIRMED**. Earlier Node VM execution also exercised the unchanged loadMore() and Belt Add. |
| 7 | scarf and SCARF show one card and Showing 1 of 12 products after loading; clear restores all 12 and empties status | **PASS — STUDENT-CONFIRMED**. Earlier stubs covered case/trim matching, clear/whitespace reset, and denominators 8/12. |
| 8 | HTML-like query produces no image/alert and exactly the literal no-match message | **PASS — STUDENT-CONFIRMED**. Source status writes use textContent only; earlier stubs checked raw text and no innerHTML write. |
| 9 | cap + Enter preserves URL/cart and does not reload | **PASS — STUDENT-CONFIRMED**. searchInput.form listener calls preventDefault() before applyFilter(); earlier stubs verified ordering/state. |
| 10 | Console has no red JavaScript errors | **PASS — STUDENT-CONFIRMED**. AI additionally ran node --check app.js; this syntax check is not presented as browser Console evidence. |
| 11 | Only index.html/app.js differ among original starter files | **VERIFIED — AI Git/byte comparison** against caaa6e7. README.md/style.css/check.js are unchanged. Added documentation is listed separately. |

Exact row 8 message:

~~~text
No products match "<img src=x onerror=alert(1)>"
~~~

B4 results, **PASS — STUDENT-CONFIRMED** following the explicit checklist:

- Three T-shirts: Cart (3) · 540.000 đ.
- Load more, then Belt once: Cart (4) · 680.000 đ.
- Sold-out Tote: no change to count or total.

Earlier Node VM checks additionally covered an empty cart total of 0 đ, repeated Belt quantities and prices of filtered-out cards. These extra cases are not represented as separately reported student browser observations.

## Scope and commit evidence

Original-source comparison: git diff --name-status caaa6e7 HEAD -- README.md index.html app.js style.css check.js lists only app.js and index.html. Direct byte comparisons verified the protected files, and the given moreProducts/loadMore/listener section matches the starter. Original/current HTML attribute comparison verified every original attribute value. Added documentation: AGENTS.md, brief.md, AI-LOG.md and SELF_ASSESSMENT_REPORT.md. No dependency or build-tool files were introduced.

| Protected file | Byte-identical to starter | SHA-256 |
|---|---|---|
| README.md | Yes | fbb95f5882f2b379a60184cb3cd9544899ee382817890c7b8ba131bb57d50fbb |
| style.css | Yes | ee8f0df27b5c29c7f4405d7fd6fc4b36b0a55e2f0cfcff949dc5ff396edf45db |
| check.js | Yes | f859b1ddbb4ac08f5c21073dca3588b078c56d1becd318443772afa2bb8fd6dd |

| Stage | Actual commit | Message |
|---|---|---|
| Root starter, five original files | caaa6e7 | starter |
| Documentation setup | ccb74c0 | docs: initialize AI workflow |
| Part A | 80639ee | feat: complete Part A semantic HTML |
| B1 | 13235eb | B1: delegated add-to-cart |
| B2 | a592a9a | B2: case-insensitive live search |
| B3 | 8dc4f1b | B3: prevent search form reload |
| B4 | 6009744 | B4: calculate cart total |

The starter is a root commit containing the five expected files, original div markup and TODOs. No external original-source archive was supplied for independent comparison. Earlier AI-log statements that AI made no commit were accurate at those task times; the later verified commits now exist. Final documentation corrections are not falsely represented as committed.

## What I did not manage

No functional failure was reported in the student's final passing confirmation. Evidence retention is less complete than the implementation: no screenshots, browser version or per-step browser transcript were supplied, and the AI could not independently rerun the page because its browser blocks file://. Some documentation review/audit entries had to be restored retrospectively from the conversation and are labeled accordingly. The student did not report specific personal rewrites or rejected proposals; the log records that limitation without inventing human coding, failures or rejections. These documentation limitations explain the conservative AI-log score.

## What I would do differently

I would retain a baseline screenshot before Part A and save a short result for each Done means row immediately after testing each phase. I would record specific Kept/Changed/Rejected/By hand decisions at the same time, rather than restoring missing documentation during the final audit. I would keep the separate A/B1/B2/B3/B4 commit structure already used here. This reflection does not claim that unreported code changes or rejections occurred.

## Submission checklist

- [x] Student identity confirmed: 24127044 — Lê Nguyễn Quốc Học.
- [x] Student confirmed the requested browser acceptance checklist and B4 passed; provenance is stated explicitly.
- [x] Protected starter files and actual separate phase commits independently verified.
- [x] Genuine missing review/audit prompts restored with retrospective labels; unused drafts removed from submission copy.
- [x] AI-log updated with final acceptance/testing confirmation; no specific student coding or rejection invented.
- [x] Numerical claim totals 98 and uses the five IA#2 weights.
- [ ] Review and commit the final documentation changes separately; this report does not claim that commit already exists.
- [ ] Package as **24127044_98.zip**, including the complete hidden .git directory, five source files, brief.md, AI-LOG.md and this report.
- [ ] Exclude the AGENTS.md working-copy file if unnecessary under hand-in scope, without rewriting historical Git commits.
- [ ] Test extraction and verify git log, file completeness and index.html before handing in.

No ZIP was created by this documentation update.
