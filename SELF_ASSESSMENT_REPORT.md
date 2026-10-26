# Self-assessment — IA#2

Submitted by: [Student ID] — [Full name]

Total I claim: **[TBD] / 100**

> Draft only. Replace all `[TBD]` cells with an evidence-based numerical score before submission. The total must equal the sum of the five "I claim" values and the number in `<StudentID>_<total>.zip`. Do not claim tests not run.

| Criterion | Max | I claim | Evidence |
|---|---:|---:|---|
| Behaviour (B1–B4) | 45 | [TBD] | [Done means rows 1–10 actually verified; explain missing rows, if any.] |
| Scope | 10 | [TBD] | [`git diff <starter-commit> -- index.html app.js style.css check.js README.md`; confirm only the permitted original source files changed.] |
| Brief | 15 | [TBD] | [`brief.md` — quote/identify actual prompts and key constraints.] |
| AI-LOG.md | 20 | [TBD] | [`AI-LOG.md` — identify entries for each assisted part and concrete Changed/Rejected decisions.] |
| Commit history | 10 | [TBD] | [`git log --oneline` — identify starter and Part A/B1/B2/B3/B4 commit hashes.] |

## What I did not manage

[Write one honest paragraph about the criteria, tests, or edge cases you did not finish. If all checks passed, describe remaining limitations only if any exist.]

## What I would do differently

[Write one short, specific reflection on implementation, verification, briefing, or AI collaboration.]

## Final submission verification

- [ ] All 11 *Done means* rows in `README.md` reviewed in a browser; failures documented above.
- [ ] `style.css` and `check.js` unchanged; source diff limited to `index.html` and `app.js`.
- [ ] Each claimed score has a concrete file, test/row, or commit as evidence.
- [ ] Git history includes the untouched-starter commit **first** and part-specific commits.
- [ ] `brief.md` contains the **prompts actually sent**, in chronological order (remove any unused drafts).
- [ ] `AI-LOG.md` is truthful, with entries made as tasks were done.
- [ ] The total matches the ZIP filename and `.git` is included.

## Current status and verification ledger

Documentation setup only. Part A and B1–B4 were not implemented during this task. All claimed scores remain pending. The verified local baseline is caaa6e7e17759b3769cc6c29f70c396ff893995c (starter), with a clean working tree before documentation setup. This is baseline evidence, not evidence of passing application behavior.

No browser tests or selfCheck() execution were performed during setup. Replace Pending with actual outcomes and evidence after testing:

| README row | Verification | Outcome / evidence |
|---|---|---|
| 1 | Reload with Console open; selfCheck() reports 8/8 | Pending |
| 2 | Capture before Part A and compare after; unchanged appearance | Pending — capture before editing |
| 3 | Tab reaches enabled Add controls and Search, skips sold-out Add; orange focus ring | Pending |
| 4 | Fresh cart: T-shirt twice then sold-out Tote; Cart (2) | Pending |
| 5 | Enter on focused Add increments count by one | Pending |
| 6 | Load more then Add Belt increments count | Pending |
| 7 | After row 6, scarf and SCARF each show one card and Showing 1 of 12 products; clear restores all and clears status | Pending |
| 8 | Literal HTML-like query: no alert or image, exact no-match message | Pending |
| 9 | cap then Enter: URL unchanged and cart state retained | Pending |
| 10 | Console has no red errors | Pending |
| 11 | Review source diff and status; protected starter files unchanged | Pending final review |

For row 11, disclose the four requested documentation additions separately from original source changes. Review `git status --short`, `git diff caaa6e7 --stat`, and `git diff caaa6e7 -- README.md style.css check.js` plus the index.html/app.js diffs. Ordinary diff omits untracked additions. An empty protected-file diff verifies preservation only, not behavior.

Optional B4 evidence remains pending (or mark not attempted): three T-shirts = Cart (3) · 540.000 đ; then add loaded Belt = Cart (4) · 680.000 đ; sold-out Add leaves both values unchanged; verify zero and repeated quantities. Record actual output and arithmetic.

The ZIP contains four Markdown templates and no separate detailed rubric. Use the student's supplied weights, which total 100; confirm any official subcriteria before assigning scores. Fill in student identity, honest reflections, real test evidence and actual phase commit hashes before submission. Review whether AGENTS.md belongs in the final hand-in under the course's extra-file rules.
