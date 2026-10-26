# brief.md — CSC13008 / IA#2

> Submission copy: actual prompts only. Unsent implementation drafts were removed during final documentation cleanup; they were never treated as executed prompts. Earlier draft versions remain recoverable in Git.

## Task context and acceptance contract

Source: `README.md` (*Done means*, rows 1–11) and TODO comments in `app.js`. IA#2 is the individual Part B assignment; Part A is the required semantic HTML prerequisite (must pass `selfCheck()` 8/8 before completing Part B).

Non-negotiable conditions for all task prompts:

1. Preserve **all existing `id`, `class`, and `data-*` attributes** and the current visual appearance.
2. Do not edit `style.css`, `check.js`, or the provided `README.md`; only change the existing source files `index.html` and `app.js` as needed.
3. Keep given `moreProducts`, `loadMore()`, and its listener intact. No frameworks, libraries, dependencies, or build tools.
4. Part B1 must have **one delegated `click` listener on `#catalogue`**, not one per Add button; Load more → Add Belt must work; a disabled sold-out product must not count.
5. Part B2 uses `input` events, `hidden` for visibility and **`textContent`** (never `innerHTML`) for user-influenced status messages. Case-insensitive match, correct count, original user text in no-match status.
6. Part B3 prevents search-form navigation with `preventDefault()` and still calls `applyFilter()`; Enter must not reload the page or reset cart.
7. Part B4, if implemented, uses numeric prices from `data-price`, proper quantity multiplication, and `toLocaleString('vi-VN')`; products from Load more count too.
8. Do not declare completion based solely on generated code. The student will manually run all 11 Done means rows in a browser and inspect Console and Git diffs.
9. No secrets or personal/private data in prompts. Keep a real `AI-LOG.md` entry for every assisted part.

## Actual prompt history / follow-up corrections

### 1. 2026-10-26 — Codex (ChatGPT): documentation setup [ACTUALLY SENT]

Attached reference: IA2_documentation_pack.zip at D:/Window's Things/Downloads/IA2_documentation_pack.zip. The student's request is preserved below:

~~~text
You are a coding assistant working on CSC13008 — Session 4 / IA#2: Dynamic HTML.

Your first task is **project documentation setup only**. Do not implement Part A or B1–B4 yet.

Read the existing `README.md`, `index.html`, the TODO comments in `app.js`, and `check.js` (read-only). Follow the IA#2 rubric and the provided CSC13008 AI-LOG and Self-assessment templates.

**Step 1 — Protect the original starter**

Before making any modifications, verify whether Git has an initial commit containing the untouched starter. If not, stop and instruct me to create this commit before proceeding. Do not fabricate Git history.

**Step 2 — Initialize four files at the project root**

1. `AGENTS.md`: Define project context, technical constraints, permitted files, workflow, testing requirements, Git rules, and AI accountability. Split implementation into Part A, B1, B2, B3, and optional B4.
2. `brief.md`: Prepare detailed, actionable prompts for each implementation phase. Each prompt must specify the task, allowed changes, constraints, expected behaviour, and verification using the README Done means table. Mark prompts as drafts until actually sent; preserve the actual prompt history in order.
3. `AI-LOG.md`: Follow the course template, with one entry per AI-assisted task and these exact fields: `Tool`, `Asked for`, `Kept`, `Changed`, `Rejected`, `By hand`. Create an entry for documentation setup, leaving any unverified decisions for my review. Do not invent manual work, AI mistakes or test results.
4. `SELF_ASSESSMENT_REPORT.md`: Follow the course template for IA#2. Include `Submitted by`, `Total I claim`, the table `Criterion | Max | I claim | Evidence`, and the sections `What I did not manage` and `What I would do differently`.

Use these rubric weights:

- Behaviour (B1–B4): 45
- Scope: 10
- Brief: 15
- AI-LOG.md: 20
- Commit history: 10

Leave the claimed scores pending until tests and evidence have been reviewed.

**Step 3 — Define non-negotiable development constraints**

- Preserve all existing `id`, `class`, and `data-*` attributes.
- Only modify the existing source files `index.html` and `app.js` when implementing the assignment.
- Never modify `style.css`, `check.js`, or the supplied `README.md`.
- Do not introduce dependencies, frameworks, backend services, or build tools.
- Preserve the provided Load more logic.
- Part A must pass `selfCheck()` with 8/8.
- B1 must use one delegated click listener on `#catalogue`, including dynamically loaded products; sold-out products cannot be added.
- B2 must support case-insensitive live search and update status messages safely using `textContent`, never `innerHTML`.
- B3 must prevent search form submission from reloading the page.
- B4 must calculate and format cart totals correctly, including dynamically loaded products.
- Verify all 11 rows of the README Done means table.
- Keep separate commits for Part A, B1, B2, B3, and B4 if implemented.
- Never claim that tests have passed without verification.

**Step 4 — Report the setup**

List the files created and explain what I need to review or fill in manually. Do not modify application code or claim the assignment is complete.

Stop after documentation setup and wait for an explicit implementation task.
~~~

Append future prompts and corrections verbatim below this entry, in the order actually sent. Move or copy the exact draft version used into this history when it is sent; never relabel an unused draft as executed.

### 2. 2026-10-26 — Documentation readiness review [ACTUALLY SENT; restored retrospectively]

~~~text
Check lại coi phần document này nọ đã okay chưa, bắt đầu implement được chưa
~~~

This genuine earlier request was missing from the working document and was restored from the conversation during final cleanup. It is not represented as having been logged at its original time.

### 3. 2026-10-26 — Codex (ChatGPT): Part A only [ACTUALLY SENT]

~~~text
Task: PART A ONLY — semantic HTML prerequisite. Read README.md (especially Done means rows 1–3), index.html, check.js (read-only), and AGENTS.md. Only edit index.html. Convert meaningful layout from divs to semantic HTML: header/nav/main/footer, exactly one h1, product headings h2, catalogue ul with li.card elements (including the card inside #card-template), real form/associated label for #q, and real button elements for .button/.add. The sold-out Tote bag button must be truly disabled. Not all layout-only divs need replacement.

Hard rules: preserve EVERY existing id, class and data-* attribute. Do not edit style.css, check.js, README.md or app.js. Do not add libraries, inline onclick handlers, or unrelated features. The visual appearance must remain unchanged.

After editing, show me the diff and map changes to the eight selfCheck tests. Only claim tests actually run; give manual steps for selfCheck() -> 8/8, before/after screenshot and Tab/Enter focus verification (Done means 1–3). Do not proceed to B1 until I confirm the results. Prepare an honest Part A AI-LOG entry for my review, and keep the exact task prompt in brief.md.
~~~

Only index.html changed among application files. AI-LOG.md and this prompt history were updated as explicitly requested. Browser results and student acceptance are pending. Do not start B1 until the student confirms Part A results.

### 4. 2026-10-26 — Codex (ChatGPT): B1 only [ACTUALLY SENT]

~~~text
Task: B1 ONLY in app.js. Read its B1 TODOs, README.md (Done means 4–6), and AGENTS.md. Implement exactly ONE delegated click listener attached to #catalogue, NOT separate listeners on buttons. Only act when a click originates from/within an .add button, locate its .card via closest('.card'), read dataset.id, increment cart[id] even when initially undefined, ignore other targets and disabled/sold-out products, then renderCart(). renderCart() must update #cart-count through textContent. Existing Load more must remain unchanged; Add on the newly loaded Belt must work.

Preserve existing selectors and Part A markup. Do not modify style.css, check.js, README.md, HTML, loadMore(), moreProducts, or add dependencies. Do not implement B2, B3 or B4 yet. Show a focused diff and a specific manual test plan for Done means 4, 5, 6, including expected Cart (2) after two T-shirts and sold-out Tote bag. Explain the event delegation and why it handles inserted cards. Report real tests vs tests I still need to run. Draft a truthful AI-LOG entry for my confirmation and keep this actual prompt in brief.md.
~~~

### 5. 2026-10-26 — Codex (ChatGPT): B2 only [ACTUALLY SENT]

~~~text
Task: B2 ONLY in app.js. Follow the B2 TODOs and README.md Done means rows 7–8. Implement applyFilter(): read input value, perform trim + case-insensitive matching on each current .card .name, hide/show cards using card.hidden, register an input event listener on #q. With an empty query, show all loaded products and clear the status text. If there are matches, set exactly "Showing X of Y products" where Y is the CURRENT card count (8 before, 12 after Load more). If no matches, set exactly 'No products match "<exact raw user input>"' (use the user's original text for the displayed message, not an HTML interpretation).

CRITICAL: write to #status ONLY with textContent, never innerHTML; typing <img src=x onerror=alert(1)> must not create HTML or run any alert. Keep the existing Load more logic and B1 unchanged. Do not edit other starter files and do not implement B3/B4. Show the diff, list manual tests (scarf / SCARF / clear / injected HTML string), specify expected results, and draft an accurate AI-LOG entry for my review. Record the exact prompt in brief.md.
~~~

### 6. 2026-10-26 — Codex (ChatGPT): B3 only [ACTUALLY SENT]

~~~text
Task: B3 ONLY in app.js. The search input #q is inside a real form from Part A. Use searchInput.form and attach a submit listener. In the listener call event.preventDefault() and applyFilter(). Enter with cap must NOT navigate to ?q=cap, reload the page or reset Cart. Preserve B1/B2 and given Load more unchanged. Do not modify index.html, style.css, check.js, README.md or dependencies.

Show a minimal diff; tell me exactly how to verify README Done means rows 9–10 and how to detect a reload/URL change. Report actual vs pending tests; draft an honest AI-LOG entry for my review and preserve the exact prompt in brief.md. Stop after B3.
~~~

### 7. 2026-10-26 — Codex (ChatGPT): B4 only [ACTUALLY SENT]

~~~text
Task: Implement stretch B4 ONLY in app.js, inside/around renderCart() as appropriate without changing B1–B3 or the provided Load more code. Sum each cart quantity multiplied by that product's price, reading data-price from its currently loaded .card and converting the dataset string with Number() before arithmetic. Display the count in #cart-count and the formatted total in #cart-total with the exact form " · 540.000 đ" using toLocaleString('vi-VN'). Products loaded by Load more, especially Belt, must be included.

Manual checks must include: 3 T-shirts -> Cart (3) · 540.000 đ; after adding Belt once -> Cart (4) · 680.000 đ; Sold-out Tote bag does not affect count or total. Avoid duplicated listeners. Touch app.js only; show focused diff, state what was actually checked vs pending, provide honest AI-LOG entry draft and preserve this prompt in brief.md. Stop before final audit.
~~~

Only app.js was changed among source files. This history and AI-LOG.md were updated as expressly requested. Final audit is outside this task.

### 8. 2026-10-26 — Read-only submission audit [ACTUALLY SENT; restored retrospectively]

~~~text
We have completed the phases. AUDIT only; do not change source files without my approval. Read README.md Done means rows 1–11 and IA#2 rubric; inspect index.html, app.js, git log, git diff from the original starter, brief.md, AI-LOG.md and SELF_ASSESSMENT_REPORT.md. Return:
(1) 11-row acceptance checklist with expected results and actual evidence; mark anything not personally browser-tested as UNVERIFIED, never PASS by assumption.
(2) Scope audit: verify original README.md, style.css, check.js are identical to starter; only index.html/app.js among original starter files changed.
(3) Prompt audit: brief.md holds prompts actually sent, chronologically, including follow-up fix prompts.
(4) AI-LOG audit: distinct entries for documentation tasks (if assisted), A, B1, B2, B3, B4; each has Tool / Asked for / Kept / Changed / Rejected / By hand and records REAL decisions and failures/row numbers; do not fabricate rejections or human coding.
(5) Commit audit: initial untouched starter plus separate A/B1/B2/B3/B4 commits. Show actual hashes.
(6) Proposed evidence-backed SELF_ASSESSMENT_REPORT.md matching the five rubric weights and containing What I did not manage / What I would do differently. Do not automatically claim 100; identify pending evidence and ask me to confirm before any scores are finalized.
(7) ZIP packaging checklist, ensuring .git is included and name uses <StudentID>_<claimed-total>.zip. AGENTS.md is optional development guidance and should be excluded from the final archive if unnecessary to comply with strict scope.
~~~

### 9. 2026-10-26 — Final submission report request [ACTUALLY SENT as Pasted text.txt; recorded retrospectively]

~~~text
You are conducting the FINAL SUBMISSION AUDIT for CSC13008 — IA#2: Dynamic HTML — Make the Catalogue Work.

The implementation is believed to be complete. Your task is to inspect the repository, evaluate the work against the official IA#2 rubric, and fill in `SELF_ASSESSMENT_REPORT.md` accurately.

**Goal:** Maximize the justified self-assessment score through verifiable evidence, without fabricating tests, Git history, AI usage, or student contributions.

## 1. Read the project evidence

Inspect the following:

- `README.md` — requirements and the 11-row Done means table.
- `index.html` — final HTML implementation.
- `app.js` — final JavaScript implementation.
- `check.js` — read-only semantic self-check.
- `style.css` — verify it is unchanged.
- `brief.md` — actual prompts and requirements.
- `AI-LOG.md` — declared AI collaboration.
- `AGENTS.md` — development constraints, if present.
- `SELF_ASSESSMENT_REPORT.md` — existing report/template.
- Git commit history and diffs.

Treat the official IA#2 rubric as the grading authority. Do not reuse the IA#1 scoring criteria from the generic self-assessment example.

## 2. Audit the five grading criteria

### Criterion 1 — Behaviour (45 points)

Verify Part A has passed `selfCheck()` 8/8.

Evaluate all 11 rows of the README Done means table, including:

- Semantic HTML, accessibility and keyboard interactions.
- B1: Delegated Add to Cart with exactly one click listener on the catalogue list.
- Correct cart quantity updates.
- Sold-out products cannot be added.
- Load more followed by Add on Belt works.
- B2: Live search is case-insensitive.
- Clearing search restores the product list and appropriate status.
- User-controlled text is inserted safely using `textContent`, not executable HTML.
- The HTML injection test `<img src=x onerror=alert(1)>` runs no JavaScript.
- B3: Submitting search with Enter does not reload the page or reset cart state.
- B4: Cart totals are calculated correctly, including products loaded dynamically.
- No red JavaScript errors appear in the browser console.

Use browser-based interaction tests where available.

Do not mark browser tests as PASSED based solely on reading source code. If browser execution is unavailable, mark them UNVERIFIED and request my manual results.

Assign a score out of 45 according to the rubric:
- 40–45: All Done means tests pass, including B4.
- 30–39: B1–B3 pass but B4 is missing or incorrect.
- 15–29: One of B1–B3 fails.
- 0–14: Two or more fail, or an error occurs on load.

### Criterion 2 — Scope (10 points)

Inspect the Git history to identify the first untouched starter commit.

Run the equivalent of:

`git log --oneline --reverse`

`git diff --name-status <starter-commit> HEAD -- README.md index.html app.js style.css check.js`

Verify:
- Only `index.html` and `app.js` were modified among the original starter files.
- `style.css` is unchanged.
- `check.js` is unchanged.
- The original `README.md` is unchanged.
- The original starter commit exists.

Distinguish newly added assignment documentation from modifications to original starter files.

Assign a score out of 10 using the official rubric.

### Criterion 3 — Brief (15 points)

Inspect `brief.md`.

Verify:
- It contains the prompts actually sent to AI, in chronological order.
- It specifies constraints on IDs, classes and allowed files.
- It prohibits editing `style.css` and `check.js`.
- It requires event delegation.
- It requires safe use of `textContent`.
- It prevents form reload.
- It defines acceptance testing through the Done means table.
- It documents follow-up prompts where applicable.

Identify draft prompts that remain marked NOT SENT or SEND WHEN READY.

Do not silently claim those prompts were actually submitted. Ask for confirmation if necessary.

Assign a justified score out of 15.

### Criterion 4 — AI-LOG.md (20 points)

Inspect every AI-LOG entry.

Verify that at least B1, B2 and B3 have separate entries if AI was used on those tasks.

Each entry must have:
- Tool
- Asked for
- Kept
- Changed
- Rejected
- By hand

Check consistency between the log, prompts, code changes and Git history.

Pay particular attention to Changed and Rejected.

Check whether each entry records:
- What the AI contributed.
- What I accepted.
- What I modified or rejected.
- Which relevant tests were performed.
- Which decisions I personally made.

Do not invent rejected proposals, failed tests, human-written code or revisions.

If nothing went wrong, accept an honest "None" supported by specific tests.

Assign a justified score out of 20.

### Criterion 5 — Commit History (10 points)

Inspect the actual Git history.

Verify:
- The first commit contains the untouched starter.
- There is a separate commit for Part A.
- There is a separate commit for B1.
- There is a separate commit for B2.
- There is a separate commit for B3.
- There is a separate commit for B4, if implemented.
- Commit messages clearly describe the changes.
- The history is consistent with the AI-LOG.

Record the relevant real commit hashes.

Assign a justified score out of 10.

## 3. Generate the final report

Update `SELF_ASSESSMENT_REPORT.md` using this format:

# Self-assessment — IA#2

Submitted by: [Actual Student ID] — [Actual Full Name]

Total I claim: [CALCULATED TOTAL] / 100

| Criterion | Max | I claim | Evidence |
|---|---:|---:|---|
| Behaviour (B1–B4) | 45 | ... | ... |
| Scope | 10 | ... | ... |
| Brief | 15 | ... | ... |
| AI-LOG.md | 20 | ... | ... |
| Commit history | 10 | ... | ... |
| **Total** | **100** | **...** | |

## What I did not manage

Describe any unfinished features, unverified tests, imperfect documentation, missing evidence or known limitations honestly. If everything passed, state what was verified and avoid inventing limitations.

## What I would do differently

Provide a short, specific reflection grounded in the actual development workflow, testing process, AI collaboration and Git history. Avoid generic filler.

## 4. Evidence rules

Every claimed score must have concrete, verifiable evidence.

Good evidence:
- A specific source file and function.
- An exact README Done means row and its observed test result.
- A verified selfCheck result.
- An actual Git commit hash.
- A specific section of brief.md or AI-LOG.md.

Bad evidence:
- "Everything works."
- "AI implemented it successfully."
- "All requirements completed." without test results.

Never claim tests passed if they were not executed or personally confirmed.

If the student ID or full name is unavailable, preserve placeholders and ask me to fill them in. Do not invent personal information.

## 5. Output and restrictions

First, present an audit summary showing:
- Each criterion's maximum and proposed score.
- Evidence supporting that score.
- Any missing or unverified evidence.
- The total proposed score.

Then update `SELF_ASSESSMENT_REPORT.md` with confirmed findings.

Only modify `SELF_ASSESSMENT_REPORT.md`.

Do not modify application code, Git history, the rubric, or other documents.

If missing evidence could materially change the score, identify exactly what I must test or confirm rather than fabricating a result.

Do not create the submission ZIP yet.

Finally, recommend the correct ZIP filename:
`<StudentID>_<total>.zip`

Remember: the total in the filename must equal the total claimed in the report.

Start the audit now.
~~~

### 10. 2026-10-26 — Student replies during final audit [ACTUALLY SENT]

Reply to the identity/AI-log/draft-label question, verbatim:

~~~text
24127044 Lê Nguyễn Quốc Học, các prompt đánh z là đúng z thiệt
~~~

Reply to the browser-results question, verbatim:

~~~text
sao bị chặn nhỉ, tôi tự test thấy okay nhưng muốn bạn tự test lại
~~~

### 11. 2026-10-26 — Clarification about pending score [ACTUALLY SENT]

~~~text
sao pending vậy. Đang thiếu gì à
~~~

### 12. 2026-10-26 — Confirm passed code and finalize documentation [ACTUALLY SENT]

~~~text
okay chỉnh lại hết cho tôi, code tôi đã pass rồi á
~~~

This reply followed an explicit checklist covering selfCheck, Part A comparison/focus, B1–B4, injection safety, no reload and Console errors. It is recorded as student-confirmed passing results, not independent AI browser execution. The current implementation is accepted for documentation finalization. The student did not describe specific manual code changes or rejected AI proposals; none are invented.

## Verification contract for the recorded implementation tasks

Each phase prompt inherits every constraint above. Before editing, read the relevant app.js TODO comments exactly as supplied. Part A: capture the before screenshot before editing, then compare after (row 2); use proper native button types and disabled state. B1: also verify clicks on card text and empty catalogue space do nothing. B2: retain raw input separately from the trimmed lowercase match query; test whitespace-only input, 8 cards initially, 12 after Load more, and Load more during an active filter. Do not cache only the original cards.

B4 has no dedicated Done means row: add explicit arithmetic checks to regression of rows 1–11. Three T-shirts must yield Cart (3) · 540.000 đ; then loaded Belt must yield Cart (4) · 680.000 đ. Verify zero, repeated quantities and no total/count change from sold-out Add. Use textContent for the total as well.

After every phase inspect Console (row 10), review source scope (row 11), report actual versus pending checks, update the task log and actual prompt history, and keep a separate phase commit after verification. A final pass must cover all 11 rows. Disclose documentation additions separately when reviewing row 11. Stop before the next phase until explicitly tasked with it.

## Final history note

The earlier review and audit requests were restored from the available conversation on 2026-10-26. No application-fix prompt was sent and no application failure was reported in this conversation. Historical pending statements describe their original phase time; final student confirmation is recorded in entry 12 and the self-assessment report. This cleanup changes documentation only, without altering source or Git history.
