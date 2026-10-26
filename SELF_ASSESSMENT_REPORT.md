# Self-assessment — IA#2

Submitted by: 24127044 — Lê Nguyễn Quốc Học

Total I claim: **98 / 100**

| Criterion | Max | I claim | Evidence |
|---|---:|---:|---|
| Behaviour (B1–B4) | 45 | 45 | I tested the README Done means checklist and confirmed that it passed, including selfCheck() 8/8 and the B4 totals. B1 uses one delegated catalogue listener; B2 filters the current cards and writes status through textContent; B3 prevents form reload; B4 multiplies quantities by numeric data-price values, including loaded products. Results are listed below. |
| Scope | 10 | 10 | Compared with starter caaa6e7, only index.html and app.js changed among the five original files. README.md, style.css and check.js are byte-identical to the starter. Existing attributes and the supplied Load more implementation were preserved. |
| Brief | 15 | 15 | brief.md contains the actual setup and A/B1/B2/B3/B4 prompts in chronological order; documentation discussions are summarized in AI-LOG.md. The prompts specify file/selector constraints, event delegation, textContent, no form reload and Done means verification. Unsent drafts and unrelated conversation details are omitted. |
| AI-LOG.md | 20 | 18 | Separate entries cover setup, A, B1, B2, B3, B4 and documentation reviews. Each records Tool, Asked for, Kept, Changed, Rejected and By hand. Browser testing is distinguished from AI checks. I reserve two points because the documentation summaries were completed during the final review and the submitted evidence does not include saved browser screenshots or a step-by-step test record. |
| Commit history | 10 | 10 | The repository contains the untouched starter and separate descriptive commits for A and each B phase. The verified hashes are listed below. |
| **Total** | **100** | **98** | **45 + 10 + 15 + 18 + 10 = 98.** |

## Verification results

I confirmed the browser checks during the final review on 2026-10-26. The browser results below are based on my testing. Codex performed syntax checks, source comparisons and Node VM tests with simulated DOM objects; its browser tool could not open the local file, so those checks are not presented as independent browser tests.

| README row | Result | Verification |
|---|---|---|
| 1 | Pass | selfCheck() reports 8/8 after reload. |
| 2 | Pass | Part A preserves the page's appearance. No before/after screenshot is included in the submitted evidence. |
| 3 | Pass | Tab reaches Search and enabled Add buttons, skips the sold-out Tote, and displays the orange focus ring. |
| 4 | Pass | Two T-shirt additions followed by an attempted Tote addition leave Cart (2). With B4, the total is 360.000 đ. |
| 5 | Pass | Enter on a focused enabled Add button increments the count once. |
| 6 | Pass | Load more followed by Add on Belt increments the count once. |
| 7 | Pass | After Load more, scarf and SCARF each show one card and Showing 1 of 12 products. Clearing the input restores all 12 cards and clears the status. |
| 8 | Pass | The HTML-like query creates no image or alert and is displayed literally in the no-match message. |
| 9 | Pass | Typing cap and pressing Enter preserves the URL and cart without reloading. |
| 10 | Pass | No red JavaScript errors appear in the browser Console. |
| 11 | Verified by repository comparison | Only index.html/app.js differ among the original starter files; README.md/style.css/check.js are unchanged. |

Row 8 displays:

~~~text
No products match "<img src=x onerror=alert(1)>"
~~~

B4 checks:

- Three T-shirts: `Cart (3) · 540.000 đ`.
- Load more, then Belt once: `Cart (4) · 680.000 đ`.
- Attempting to add the sold-out Tote changes neither the count nor the total.

The AI-assisted checks also covered trimmed and whitespace-only queries, the 8/12 product counts, loading products during an active search, repeated quantities and totals for cards hidden by a filter. These additional simulated checks are documented in AI-LOG.md.

## Source and commit evidence

The starter comparison used `git diff --name-status caaa6e7 HEAD -- README.md index.html app.js style.css check.js`, direct byte comparisons for the protected files, and a comparison of the original HTML attributes and supplied Load more section. The implementation adds no dependencies, frameworks or build tools. Assignment documentation was added separately from the source changes.

| Stage | Commit | Message |
|---|---|---|
| Starter | caaa6e7 | starter |
| Documentation setup | ccb74c0 | docs: initialize AI workflow |
| Part A | 80639ee | feat: complete Part A semantic HTML |
| B1 | 13235eb | B1: delegated add-to-cart |
| B2 | a592a9a | B2: case-insensitive live search |
| B3 | 8dc4f1b | B3: prevent search form reload |
| B4 | 6009744 | B4: calculate cart total |

## What I did not manage

I completed A and B1–B4 and confirmed the acceptance checks passed. My evidence collection was less complete: I did not supply saved screenshots or a detailed browser test record with the final confirmation. The documentation review summaries were completed during the final review rather than recorded in detail as each discussion occurred. I have allowed for these documentation limitations in my self-assessed score.

## What I would do differently

I would save the baseline screenshot before Part A and record each Done means result immediately after testing a phase. I would also write the Kept, Changed, Rejected and By hand notes at that point, rather than completing them during the final review. I would keep the separate A/B1/B2/B3/B4 commit structure used in this assignment.
