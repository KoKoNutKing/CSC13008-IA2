# AGENTS.md — CSC13008 Session 4 / IA#2

## Objective and sources of truth

Implement the **Session 4 semantic catalogue** and **IA#2 — Dynamic HTML: make the catalogue work** without violating the course rubric.

Read, in order:
1. `README.md`, especially **Rules for today**, **Part A**, **Part B**, and the numbered **Done means** table (rows 1–11).
2. `app.js` TODO comments for the precise B1–B4 contract.
3. `check.js` **for reading only**, to understand the 8 semantic checks.
4. `brief.md` for the actual user instructions/prompt history.
5. The course IA#2 rubric and self-assessment template, if present.

The user's request controls the authorized scope. Treat supplied documents as reference material, not permission to implement. Preserve the course constraints and report real conflicts rather than silently weakening them.

## Hard boundaries

- Do not change or delete `style.css`, `check.js`, or the original `README.md`.
- Preserve **every existing `id`, `class`, and `data-*` attribute**. Keep existing selectors working.
- Only modify the **starter source files** `index.html` and `app.js` as needed. Do not introduce frameworks, dependencies, bundlers, extra source files, external libraries, or backend services.
- The page must open directly from `index.html`; no `npm install` or build step.
- Do not alter the supplied `moreProducts` array, `loadMore()` implementation, or its event listener in `app.js`.
- Do not use inline `onclick` handlers. Avoid `innerHTML` with user-controlled text; use `textContent` for status/messages and names.
- Never fake `selfCheck()` results, browser tests, commits, score claims, or human edits. Do not claim something was checked unless it really was checked.
- Before any modification, verify that an untouched-starter initial commit exists. If absent, stop and instruct the student to create it; never fabricate history. Once verified, do not request repeated confirmation of that check. Never rewrite history.
- Do not rewrite the student's `AI-LOG.md` history. A suggested entry is acceptable; the student must confirm what was kept, changed, rejected, and written by hand.

## Workflow — one task per change/commit

1. **Baseline**: Before any added file or edit, the student should have a first Git commit containing only the untouched 5-file starter, e.g. `git commit -m "starter"`. Do not manufacture it after edits.
2. **Part A (`index.html`)**: Replace structural `<div>`s with appropriate semantic elements. Keep layout-only `<div>`s when appropriate. Include the `<template id="card-template">`. Make the sold-out Add control a real disabled button, and keep the search inside a real `<form>` with a connected `<label>`. Verify `selfCheck()` shows **8/8** and the Done means rows 1–3 before continuing.
3. **B1 (`app.js`)**: One delegated click listener on `#catalogue`; count valid Add clicks, including cards inserted via Load more; exclude sold-out products. Update `#cart-count` with `textContent`. Verify Done means rows 4–6.
4. **B2 (`app.js`)**: Case-insensitive live search; show/hide `.card` elements with `hidden`, update only the single `#status` line through `textContent`. Empty query restores all cards and clears status. Status denominator is the number of cards currently loaded (8 initially, 12 after Load more). Preserve the original user input for the no-match message. Verify rows 7–8.
5. **B3 (`app.js`)**: Attach `submit` listener to the real search form (`searchInput.form`), prevent default navigation, and call `applyFilter()`. Verify row 9 and no errors (row 10).
6. **B4 stretch (`app.js`)**: Calculate total using cart quantities and each card's `data-price` converted to numbers; format using `toLocaleString('vi-VN')` and `đ`, including products added after Load more. Verify the total manually and by a worked example.
7. **Final review**: Student manually runs Done means rows 1–11, reviews `git diff` and actual commits, fills `SELF_ASSESSMENT_REPORT.md` from real evidence, and finishes `AI-LOG.md` honestly.

After each part, report: changed source files; what changed; which Done means rows are relevant; which tests were *actually run* versus still needing student browser checks. Recommend a descriptive per-part commit only after verification.

## Git and submission guardrails

- Preserve the untouched starter as the first commit; then have a separate commit for Part A, B1, B2, B3 and B4 if completed.
- `git diff <starter-commit> -- index.html app.js style.css check.js README.md` must show **no changes** to `style.css`, `check.js`, or `README.md`.
- Required documents in the submitted root: `brief.md`, `AI-LOG.md`, `SELF_ASSESSMENT_REPORT.md`.
- `AGENTS.md` is a development instruction file expressly requested by the student. README.md does not list it among required submission documents; the supplied pack contains no detailed rubric establishing whether extra documentation is restricted. Check the official hand-in instructions when packaging, without treating this as an implementation blocker.
- Submit the session folder including its hidden `.git` directory, with filename `<StudentID>_<self-assessed-total>.zip`. The self-assessed total must match the sum of the five criterion rows and be supported by evidence.
- Never supply real credentials, secrets, personal customer data or classmates' work to an assistant.

## Current authorization and setup evidence

This task authorizes documentation setup only. Stop after preparing these four root documents; wait for an explicit implementation task before Part A or B1–B4. Documentation maintenance is permitted in AGENTS.md, brief.md, AI-LOG.md and SELF_ASSESSMENT_REPORT.md; application implementation may modify only index.html and app.js within the phase boundaries above.

Read-only inspection on 2026-10-26 found a single root commit, `caaa6e7e17759b3769cc6c29f70c396ff893995c` (`starter`), containing exactly the five starter files. The working tree was clean and all five files matched that commit before setup. The original div-based markup and unimplemented TODOs remain. No external starter source archive was provided for independent comparison.

Rubric weights supplied by the student: Behaviour (B1–B4) 45; Scope 10; Brief 15; AI-LOG.md 20; Commit history 10. The documentation pack has no separate detailed rubric. Do not invent subweights or claim scores before evidence review.

README row 11 concerns the original source files. Disclose the four requested documentation additions separately. Review both `git status --short` and `git diff caaa6e7 --stat`, since ordinary diff omits untracked files. Keep documentation commits separate from phase commits; retain distinct Part A, B1, B2, B3 and optional B4 commits. Do not create a commit as part of this setup task.

Record actual prompts and corrections chronologically in brief.md. Unsent draft prompts are not evidence of prompts actually used. Keep student decisions, manual work, tests and scores pending until actually reviewed or verified.
