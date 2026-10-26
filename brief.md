# brief.md — CSC13008 / IA#2

> **Implementation prompts are DRAFT — NOT SENT.** The actual documentation setup request is recorded separately below.
> The rubric grades the instructions **actually given** to the assistant, not a polished summary written afterwards. When you send a prompt below, preserve the exact version sent (including changes or follow-ups) in chronological order. Remove prompts that were never sent before submission. Update this file **as you work**.

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

## Prompts prepared for the assistant

### Prompt A — Semantic HTML prerequisite [DRAFT — NOT SENT]

> Read `README.md`, `index.html`, `check.js` (read-only), and `AGENTS.md`. Perform **Part A only** in `index.html`: replace non-semantic structural `<div>`s with the correct landmarks, headings, `<ul>/<li>` product list, real `<form>` and associated `<label>`, and real `<button>` elements. Update the card inside `<template id="card-template">` too. The sold-out Add must be a disabled button; layout-only `div`s may remain. Preserve every existing `id`, `class`, and `data-*` attribute. Do not change other starter files or add inline `onclick`. Explain how to verify `selfCheck()` returns **8/8** and Done means rows **1–3**, without claiming to have run browser tests you cannot run. Stop after Part A; do not implement B1–B4 yet.

### Prompt B1 — Add to Cart [DRAFT — NOT SENT]

> Read `README.md`, `AGENTS.md`, and the B1 TODOs in `app.js`. Implement **B1 only**, editing `app.js` only: one delegated click listener on `#catalogue`, identify `.add` and its parent `.card`, ignore clicks outside Add and disabled/sold-out items, increment `cart[id]` correctly, and make `renderCart()` update `#cart-count` via `textContent`. Ensure it works for products inserted by the given Load more function. Do not change the provided Load more implementation or any HTML/CSS/checks. Explain browser verification for Done means rows **4–6**. Stop and allow review/commit before B2.

### Prompt B2 — Live Search [DRAFT — NOT SENT]

> Read the B2 TODOs in `app.js` and `README.md`. Implement **B2 only**: case-insensitive, trimmed search on every `input` event; iterate all current `.card` elements, toggle `hidden` based on `.name`; use one `#status` message via `textContent`. For empty input restore every card and clear status; for matches show `Showing X of Y products`, where Y is 8 before Load more and 12 afterwards; for no matches include the **exact text typed**, e.g. `No products match "<img src=x onerror=alert(1)>"`, without interpreting HTML. Preserve other behavior and files. Explain tests for Done means rows **7–8**. Stop before B3.

### Prompt B3 — Prevent Form Reload [DRAFT — NOT SENT]

> Read the B3 TODO in `app.js` and `README.md`. Implement **B3 only**: register `submit` on the form associated with `#q` (`searchInput.form`), call `event.preventDefault()` and then `applyFilter()`. Pressing Enter after typing `cap` must keep the current URL (no `?q=cap`) and preserve cart state. Do not change other starter files or unrelated functions. Explain tests for Done means rows **9–10**. Stop before B4.

### Prompt B4 — Cart Total (stretch) [DRAFT — NOT SENT]

> Implement the optional B4 total in `renderCart()` without breaking B1–B3. Read each product's numeric price from the loaded `.card` element's `data-price`, multiply by the quantity in `cart`, and sum all entries, including Belt added via Load more. Write formatted ` · N đ` into `#cart-total` using `toLocaleString('vi-VN')`; keep the count in `#cart-count`. Avoid string concatenation errors. Test an example of three T-shirts = `540.000 đ`, and verify the other Done means rows remain passing. Only change `app.js`.

## Actual prompt history / follow-up corrections

### 1. 2026-10-26 — Codex (ChatGPT): documentation setup [ACTUALLY SENT]

Attached reference: IA2_documentation_pack.zip at D:/Window's Things/Downloads/IA2_documentation_pack.zip. The implementation drafts above have not been sent. The student's request is preserved below:

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

## Verification contract inherited by each draft

Each phase prompt inherits every constraint above. Before editing, read the relevant app.js TODO comments exactly as supplied. Part A: capture the before screenshot before editing, then compare after (row 2); use proper native button types and disabled state. B1: also verify clicks on card text and empty catalogue space do nothing. B2: retain raw input separately from the trimmed lowercase match query; test whitespace-only input, 8 cards initially, 12 after Load more, and Load more during an active filter. Do not cache only the original cards.

B4 has no dedicated Done means row: add explicit arithmetic checks to regression of rows 1–11. Three T-shirts must yield Cart (3) · 540.000 đ; then loaded Belt must yield Cart (4) · 680.000 đ. Verify zero, repeated quantities and no total/count change from sold-out Add. Use textContent for the total as well.

After every phase inspect Console (row 10), review source scope (row 11), report actual versus pending checks, update the task log and actual prompt history, and keep a separate phase commit after verification. A final pass must cover all 11 rows. Disclose documentation additions separately when reviewing row 11. Stop before the next phase until explicitly tasked with it.
