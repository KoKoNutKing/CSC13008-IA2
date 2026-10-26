# AI-LOG.md — CSC13008 / IA#2

I used Codex (ChatGPT) for documentation, implementation and review. The entries below summarize the work kept for the assignment. I confirmed the browser acceptance checks; AI syntax checks, source comparisons and Node VM checks are listed separately. Documentation discussions are summarized after the implementation entries.

## 2026-10-26 — Documentation setup

- Tool: Codex (ChatGPT).

- Asked for: Prepare AGENTS.md, brief.md, AI-LOG.md and SELF_ASSESSMENT_REPORT.md using the course templates and IA#2 weights; verify the starter commit before editing.

- Kept: The four-document structure, phase boundaries and development constraints.

- Changed: AI adapted the supplied templates to the catalogue and left scores and test results open until evidence was available.

- Rejected: No rejected suggestion was recorded for this task.

- By hand: I supplied the documentation requirements and later confirmed my identity and the prompt labels.

Verification: AI verified root starter caaa6e7 and that the five original files matched it before documentation setup. No application code or browser tests were involved.

## 2026-10-26 — Part A — semantic HTML

- Tool: Codex (ChatGPT).

- Asked for: Implement Part A only in index.html, preserve all existing attributes and appearance, and map the changes to selfCheck and Done means rows 1–3.

- Kept: The semantic landmarks, h1/h2 headings, ul/li product list, associated label/form and native buttons, including the template and disabled Tote.

- Changed: AI replaced the relevant div tags, retained layout-only divs, used type="submit" for Search and type="button" for Add/Load more. No specific manual code rewrite was reported.

- Rejected: No rejected implementation or failing row was reported.

- By hand: I tested the page and confirmed that the requested acceptance checks passed during the final review.

Verification: AI compared original/current HTML attributes using Python HTMLParser: all original values were preserved. Static assertions covered landmarks, headings, nine cards including the template, eleven native buttons, label/form association and disabled Tote. Protected-file byte comparisons passed. Rows 1–3 are based on my browser confirmation; AI did not run the page in a browser.

## 2026-10-26 — B1 — delegated Add to Cart

- Tool: Codex (ChatGPT).

- Asked for: Implement one delegated catalogue click listener, ignore unrelated or disabled clicks, update the count through textContent and support dynamically loaded Belt.

- Kept: The single listener on #catalogue and quantity-based count rendering.

- Changed: AI used closest('button.add'), closest('.card'), containment/disabled guards and (cart[id] || 0) + 1. renderCart() sums quantities. No specific manual code rewrite was reported.

- Rejected: No rejected implementation or failing row was reported.

- By hand: I tested Add, sold-out exclusion, keyboard activation and Load more/Belt, and confirmed the checklist passed.

Verification: AI ran node --check and actual app.js in a Node VM with DOM stubs. It checked first/repeated Add, disabled property/class guards, unrelated/outside and nested clicks, actual loadMore() followed by Belt, and one remaining catalogue listener. Rows 4–6 were confirmed by my browser testing.

## 2026-10-26 — B2 — live search

- Tool: Codex (ChatGPT).

- Asked for: Implement trimmed, case-insensitive input filtering with current card counts and literal no-match text written only through textContent.

- Kept: applyFilter(), the input listener, card.hidden visibility and exact status messages.

- Changed: AI kept raw input separately from the normalized query and queried current cards on every filter call. Load more stayed unchanged. No specific manual code rewrite was reported.

- Rejected: No rejected implementation or failing row was reported.

- By hand: I tested scarf, SCARF, clear and the HTML-like query, and confirmed the acceptance checklist passed.

Verification: AI ran syntax and Node VM checks for case/trim matching, whitespace/clear reset, 8/12 denominators, loading during an active Belt query and exact raw no-match text. A throwing innerHTML setter and alert stub detected no unsafe calls in that simulated run. Rows 7–8 were confirmed by my browser testing; stub execution was not treated as real browser execution.

## 2026-10-26 — B3 — prevent search reload

- Tool: Codex (ChatGPT).

- Asked for: Attach submit through searchInput.form, call preventDefault() then applyFilter(), and preserve URL and cart state.

- Kept: The minimal submit handler in app.js.

- Changed: AI replaced only the B3 TODO. B1/B2, B4 and the given Load more code were unchanged at that phase. No specific manual code rewrite was reported.

- Rejected: No rejected implementation or failing row was reported.

- By hand: I tested cap followed by Enter and checked that the URL/cart were retained and the Console was clear, then confirmed the checklist passed.

Verification: AI ran syntax and Node VM checks confirming one form submit listener, preventDefault before actual filtering, Cap visibility and retained cart object/count. Real navigation and Console results for rows 9–10 come from my browser confirmation.

## 2026-10-26 — B4 — cart totals

- Tool: Codex (ChatGPT).

- Asked for: Calculate quantity times numeric data-price from loaded cards, format the total with vi-VN and include Belt without adding listeners.

- Kept: The total calculation in renderCart() and the initial zero-cart render.

- Changed: AI added Number(card.dataset.price), quantity multiplication and textContent formatting. The original count calculation, B1–B3 and Load more were preserved. No specific manual code rewrite was reported.

- Rejected: No rejected implementation or failing row was reported.

- By hand: I confirmed that three T-shirts showed Cart (3) · 540.000 đ, then Belt showed Cart (4) · 680.000 đ, and sold-out Tote changed neither value.

Verification: AI ran syntax and Node VM checks for zero, those two totals, disabled Tote, repeated Belt, hidden-card totals and unchanged listener count. File/source comparisons verified the implementation boundary. The required browser outcomes were confirmed by me.

## 2026-10-26 — Documentation review

- Tool: Codex (ChatGPT).

- Asked for: Review the project documentation and rubric evidence, prepare the self-assessment, and edit the submission wording and Markdown formatting.

- Kept: The project constraints, implementation records, verified commit references and the 98-point self-assessment.

- Changed: AI summarized the documentation discussions, kept the actual setup/implementation prompts in brief.md, updated the report after my testing confirmation, and formatted the log fields as separate bullet points. These summaries were completed during the final review.

- Rejected: I asked to remove the report's internal submission checklist and unnecessary conversation details. No rejected application implementation was reported.

- By hand: I supplied my identity, confirmed that the code passed my tests, reviewed the submission wording and requested these documentation edits.

Verification: Repository comparisons confirmed that the protected starter files and supplied Load more code were unchanged, with separate commits for A and B1–B4. The AI browser could not open file://; browser results in the report are based on my confirmation. No application failure or specific personal code rewrite was reported.

## Commit references

| Stage | Commit |
|---|---|
| Starter | caaa6e7 |
| Documentation setup | ccb74c0 |
| Part A | 80639ee |
| B1 | 13235eb |
| B2 | a592a9a |
| B3 | 8dc4f1b |
| B4 | 6009744 |
