# brief.md — CSC13008 / IA#2

> This file records the prompts used for documentation setup and implementation, in the order sent. Other documentation reviews are summarized in AI-LOG.md.

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

## Prompts used

### 1. 2026-10-26 — Documentation setup

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

### 2. 2026-10-26 — Part A — semantic HTML

~~~text
Task: PART A ONLY — semantic HTML prerequisite. Read README.md (especially Done means rows 1–3), index.html, check.js (read-only), and AGENTS.md. Only edit index.html. Convert meaningful layout from divs to semantic HTML: header/nav/main/footer, exactly one h1, product headings h2, catalogue ul with li.card elements (including the card inside #card-template), real form/associated label for #q, and real button elements for .button/.add. The sold-out Tote bag button must be truly disabled. Not all layout-only divs need replacement.

Hard rules: preserve EVERY existing id, class and data-* attribute. Do not edit style.css, check.js, README.md or app.js. Do not add libraries, inline onclick handlers, or unrelated features. The visual appearance must remain unchanged.

After editing, show me the diff and map changes to the eight selfCheck tests. Only claim tests actually run; give manual steps for selfCheck() -> 8/8, before/after screenshot and Tab/Enter focus verification (Done means 1–3). Do not proceed to B1 until I confirm the results. Prepare an honest Part A AI-LOG entry for my review, and keep the exact task prompt in brief.md.
~~~

### 3. 2026-10-26 — B1 — Add to Cart

~~~text
Task: B1 ONLY in app.js. Read its B1 TODOs, README.md (Done means 4–6), and AGENTS.md. Implement exactly ONE delegated click listener attached to #catalogue, NOT separate listeners on buttons. Only act when a click originates from/within an .add button, locate its .card via closest('.card'), read dataset.id, increment cart[id] even when initially undefined, ignore other targets and disabled/sold-out products, then renderCart(). renderCart() must update #cart-count through textContent. Existing Load more must remain unchanged; Add on the newly loaded Belt must work.

Preserve existing selectors and Part A markup. Do not modify style.css, check.js, README.md, HTML, loadMore(), moreProducts, or add dependencies. Do not implement B2, B3 or B4 yet. Show a focused diff and a specific manual test plan for Done means 4, 5, 6, including expected Cart (2) after two T-shirts and sold-out Tote bag. Explain the event delegation and why it handles inserted cards. Report real tests vs tests I still need to run. Draft a truthful AI-LOG entry for my confirmation and keep this actual prompt in brief.md.
~~~

### 4. 2026-10-26 — B2 — live search

~~~text
Task: B2 ONLY in app.js. Follow the B2 TODOs and README.md Done means rows 7–8. Implement applyFilter(): read input value, perform trim + case-insensitive matching on each current .card .name, hide/show cards using card.hidden, register an input event listener on #q. With an empty query, show all loaded products and clear the status text. If there are matches, set exactly "Showing X of Y products" where Y is the CURRENT card count (8 before, 12 after Load more). If no matches, set exactly 'No products match "<exact raw user input>"' (use the user's original text for the displayed message, not an HTML interpretation).

CRITICAL: write to #status ONLY with textContent, never innerHTML; typing <img src=x onerror=alert(1)> must not create HTML or run any alert. Keep the existing Load more logic and B1 unchanged. Do not edit other starter files and do not implement B3/B4. Show the diff, list manual tests (scarf / SCARF / clear / injected HTML string), specify expected results, and draft an accurate AI-LOG entry for my review. Record the exact prompt in brief.md.
~~~

### 5. 2026-10-26 — B3 — prevent form reload

~~~text
Task: B3 ONLY in app.js. The search input #q is inside a real form from Part A. Use searchInput.form and attach a submit listener. In the listener call event.preventDefault() and applyFilter(). Enter with cap must NOT navigate to ?q=cap, reload the page or reset Cart. Preserve B1/B2 and given Load more unchanged. Do not modify index.html, style.css, check.js, README.md or dependencies.

Show a minimal diff; tell me exactly how to verify README Done means rows 9–10 and how to detect a reload/URL change. Report actual vs pending tests; draft an honest AI-LOG entry for my review and preserve the exact prompt in brief.md. Stop after B3.
~~~

### 6. 2026-10-26 — B4 — cart totals

~~~text
Task: Implement stretch B4 ONLY in app.js, inside/around renderCart() as appropriate without changing B1–B3 or the provided Load more code. Sum each cart quantity multiplied by that product's price, reading data-price from its currently loaded .card and converting the dataset string with Number() before arithmetic. Display the count in #cart-count and the formatted total in #cart-total with the exact form " · 540.000 đ" using toLocaleString('vi-VN'). Products loaded by Load more, especially Belt, must be included.

Manual checks must include: 3 T-shirts -> Cart (3) · 540.000 đ; after adding Belt once -> Cart (4) · 680.000 đ; Sold-out Tote bag does not affect count or total. Avoid duplicated listeners. Touch app.js only; show focused diff, state what was actually checked vs pending, provide honest AI-LOG entry draft and preserve this prompt in brief.md. Stop before final audit.
~~~

## Acceptance criteria

The prompts use the README Done means table and app.js TODOs as acceptance criteria: Part A covers rows 1–3, B1 rows 4–6, B2 rows 7–8 and B3 rows 9–10. Row 11 checks the permitted source changes.

B4 adds arithmetic checks: three T-shirts total 540.000 đ; adding Belt after Load more gives 680.000 đ; sold-out Tote changes neither the count nor the total. Browser results and AI-assisted checks are recorded separately in AI-LOG.md and SELF_ASSESSMENT_REPORT.md.
