# AI-LOG.md — CSC13008 / IA#2

One entry **per task assisted by AI**. Use the actual date, tool, request, and your real decisions. Keep at least separate entries for B1, B2, and B3 if you ask AI to do those parts. Do **not** claim to have tested anything you have not tested. Log Part A, B4, and document setup too when AI helps with them.

## 2026-10-26 — Initialize IA#2 documentation

- Tool: Codex (ChatGPT)
- Asked for: Prepare `AI-LOG.md`, `SELF_ASSESSMENT_REPORT.md`, `AGENTS.md`, and `brief.md` following the provided course templates and IA#2 rubric.
- Kept:
  - After reviewing the generated documents, name what you accepted.
- Changed:
  - Pending student review: describe actual changes and reasons; no manual revisions are asserted.
- Rejected:
  - Pending student review: describe actual rejected suggestions and reasons; no AI mistakes or rejections are asserted.
- By hand:
  - State only what you personally did, such as reading the rubric or creating the starter commit.
- AI-observed evidence:
  - Read-only Git inspection found the single root commit `caaa6e7e17759b3769cc6c29f70c396ff893995c` (`starter`), exactly five tracked starter files, and a clean working tree before setup.
  - All five files matched the baseline.
  - The ZIP contains four Markdown documentation templates; weights come from the student's request, with no invented subcriteria.
  - Git inspection used a command-local safe.directory exception; global Git configuration was not changed.
  - No browser tests or `selfCheck()` execution were performed.
  - Student acceptance, manual work and all implementation decisions remain pending review.

## 2026-10-26 — Part A: semantic HTML [FOR STUDENT REVIEW]

- Tool: Codex (ChatGPT)
- Asked for: Implement Part A only in index.html, preserving all original attributes and appearance; show the diff and eight-check mapping; supply manual verification steps, prepare this log entry, and preserve the exact prompt in brief.md. Wait for confirmed results before B1.
- Kept: [Pending student review: semantic landmarks, h1/h2 headings, ul/li cards including template, associated label/form and native buttons with disabled Tote. No student acceptance is asserted.]
- Changed: AI changed only index.html among source files: toolbar/menu/page/footer to header/nav/main/footer, title to h1, product names to h2, catalogue/cards to ul/li, search to form/label, and controls to buttons. Search uses type="submit"; Add and Load more use type="button". Original layout divs remain where appropriate. AI updated this log and brief.md as requested. [Record any student revisions and reasons after review.]
- Rejected: [Pending student review; no rejected suggestions or AI mistakes are asserted.]
- By hand: [Pending student input. No manual browser verification or human edits are asserted.]

AI checks actually run: Python standard-library HTMLParser comparison of corresponding original/current elements confirmed every original attribute value is preserved (including all id/class/data-* attributes). Static assertions confirmed one each header/nav/main/footer/h1, nine h2 names and li.card elements including template, ul catalogue, form and label for q, eleven native buttons, no inline onclick, and the sold-out disabled attribute. Byte comparisons confirmed README.md, style.css, check.js and app.js unchanged against HEAD. Reviewed git diff for index.html.

Not run: browser selfCheck(), before/after screenshots and keyboard Tab/Enter verification. Static assertions do not establish a browser 8/8 result or unchanged visual appearance. No before screenshot was captured by AI before editing; if the student has none, use a separate copy exported from starter commit caaa6e7 for comparison at the same viewport/zoom. Part B behavior is unimplemented; Add does not yet update the cart and Search may submit/reload until B3. Scores remain pending. No Part A commit was created; review and verify before the separate Part A commit. Stop before B1 until student confirmation.

<!-- Add a NEW entry as soon as each task happens. Copy the exact structure below.

## YYYY-MM-DD — Part A: semantic HTML
- Tool: <actual tool / none>
- Asked for: <exact task you gave it, in one sentence>
- Kept: <what you accepted>
- Changed: <what you rewrote, why, and which Done means row identified the issue>
- Rejected: <what you did not use, why; if none, specify which rows you checked>
- By hand: <what you personally wrote or verified>

## YYYY-MM-DD — B1: add to cart
- Tool: <actual tool / none>
- Asked for: <actual request>
- Kept: <actual decision>
- Changed: <actual decision, including Done means row # where applicable>
- Rejected: <actual decision, or none with verification>
- By hand: <actual work>

Repeat a separate real entry for B2 (search), B3 (form), and B4 if attempted.
-->
