---
name: "account-prioritization"
description: "Segment, score (High/Medium/Low) and group a B2B target-account list into Win-Back, Close the Gap, Net New, Nurture and Set Aside. Use whenever someone shares an account list, CRM export or ABM target list and wants prioritization, tiering, segmentation or account groups."
---

# Account prioritization

A repeatable method for turning a messy account list (CRM plus intent-style fields) into a segment, a High/Medium/Low score, a one-line reason, and a go-to-market group for every account. It was built for a privacy-software vendor, where website traffic stands in for how much consumer data a company holds, but the structure works for any B2B list with size, traffic and opportunity history.

The method is deliberately rule-based. Leaders and sales teams trust a model they can predict, and every account must land where the rules say, with no one-off judgment calls. When a case seems to need an exception, apply the rule, then flag it in the reason instead of bending the rule.

## Inputs

Expected columns (names vary; map them first): company name, domain, employees, annual revenue, industry, website monthly unique visitors (MUVs), primary competitor, primary incumbent, last opportunity close date, loss reason.

Before scoring, settle two things and state them in your reply:
- **Today's date.** All recency is measured from it.
- **Whether the data may be researched.** If the brief says company data is fictional or not to research it, use the values exactly as given. Never replace a value with an outside figure; flag implausible values instead (e.g. "$10B revenue on 300 employees").

## Step 1: Segment

Default bands (use the brief's if it gives others):
- **Enterprise:** 1,500+ employees **or** $1B+ revenue
- **Mid-Market:** 100–1,499 employees **or** $10M–$999M revenue
- **Below Mid-Market:** neither

If employees and revenue point to different bands, the **higher band wins**. If one field is missing, segment on the other. Flag any account where the two disagree sharply.

## Step 2: Fit

Fit asks: is this account worth winning? It combines segment with privacy exposure (MUVs).

| Fit | Enterprise | Mid-Market |
|---|---|---|
| Strong | 50K+ MUVs | 1M+ MUVs |
| Moderate | under 50K MUVs | 50K–1M MUVs |
| Weak | — | under 50K MUVs |

- **Missing MUVs:** not enough data to judge fit, so treat as weak, unless the exception below applies.
- **Data-heavy industry exception:** banks and lenders, insurers and health organizations hold consumer data in back-end systems, so low or missing MUVs understate their exposure. Treat them as at least moderate fit and flag it.

## Step 3: Timing

Timing asks: is now the moment? A signal is **live** when the reason we didn't win has probably changed, giving a reason to reach out now.

**The 6–24 month window applies to every loss.** A loss counts as live only if it closed **6 to 24 months ago**:
- **Under 6 months:** too soon. The decision is fresh and nothing has changed (cooling off). Not live.
- **6–24 months:** live, for the loss reasons below.
- **Over 24 months:** stale. Not live; treat the account as net new.

Live signals:
- **Timing**, closed 6–24 months ago ("not now" rather than "no"; budgets and new privacy laws move it up the list)
- **Lost to Competitor / Lost to Incumbent**, closed 6–24 months ago. Both mean the account chose another vendor; treat them the same. Contracts typically run 1–3 years, so the renewal window is opening.
- **Pricing / Budget**, closed 6–24 months ago (budgets reset yearly)
- **Product / Technical Gaps**, closed 6–24 months ago. Assume the gap has since been closed.
- **Homegrown incumbent** (manual work gets costlier as volume and regulation grow; no contract to break). This is not a loss, so the 6-month floor does not apply.

Not live: any loss under 6 months old, Non-Responsive, Education Only, Wrong Person, and any opportunity closed 2+ years ago.

Normalize loss-reason labels first ("Price" = "Pricing / Budget", spacing variants of "Product / Technical Gaps").

## Step 4: Score

- **High:** strong fit **and** a live signal
- **Medium:** strong fit with nothing live, **or** moderate fit (with or without a signal)
- **Low:** weak fit, Below Mid-Market, or not enough data to judge fit

Fit gates and timing elevates: a live signal never lifts a weak-fit account, and a moderate-fit account is never Low just because it has no opportunity history.

## Step 5: Group

Apply in this order; the first match wins:
1. **Low score → 5. Set Aside** (no paid spend; quarterly review)
2. **Lost on a product gap, any age → 2. Close the Gap** ("here's what we built"). A product-gap loss under 6 months old still lands here, but scores Medium because the signal isn't live yet.
3. **No opportunity history, or last opportunity 2+ years old → 3. Net New** (ABM, then outbound)
4. **Recent opportunity (under 2 years):** High → **1. Win-Back Now** (sales-led re-engagement; the loss closed 6–24 months ago with a live signal); Medium → **4. Nurture** (automated, timed to the account's trigger). Nurture includes losses under 6 months old: time outreach for when the account crosses 6 months.

Groups describe the relationship with the account, not the fit, which is why a strong-fit and a moderate-fit account with no history both land in Net New. Score sets priority; the group sets the motion.

## Step 6: Write the reason

One short line per account, in this order: fit level with its evidence, the timing fact, the incumbent if it matters, then any flag. Under about 25 words. Examples:
- `Strong fit (Enterprise, 4.5M MUVs). Product-gap loss 8 mo ago; gap assumed closed. OneTrust incumbent.`
- `Moderate fit (226K MUVs). 2023 timing loss is stale; treat as net new.`
- `Moderate fit (Enterprise, 23K MUVs; health data). Pricing loss 2 mo ago, still cooling off.`
- `Excluded: below Mid-Market (91 employees, $1M revenue).`
- `Exception: bank, so 44 MUVs understate its data. Pricing loss 14 mo ago. Flag: revenue missing.`

State months since close, not raw dates, so the reader can see why recency mattered.

## Output

Add four columns: **Score**, **Why**, **Group** (with its rank number, e.g. "1. Win-Back Now", so sorting puts groups in priority order) and **Segment**. Leave every original column untouched.

When writing into a live spreadsheet:
- Re-read the sheet immediately before writing. People sort and edit while you work, so match each row by company name or domain, never by a row number remembered from an earlier read.
- After writing, read the rows back and check every account has the expected values.

Then reply with the totals by score and by group, the segment rule you applied, and the main flags (implausible or missing data). Keep it short; the sheet holds the detail.

## Consistency check before finishing

- Every Low is in Set Aside; every product-gap loss that isn't Low is in Close the Gap.
- No account with a recent opportunity is in Net New; no account without one is in Win-Back or Nurture.
- No account whose loss closed under 6 months ago is High.
- Every Below Mid-Market account is Low.
- Counts by group add up to the number of accounts.

If a rule produces a result that looks wrong, say so and propose a rule change that would apply to every account, rather than adjusting one row.