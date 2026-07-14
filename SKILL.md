---
name: itu-t-recommendation-reviewer
description: Review draft ITU-T Recommendations (and ITU-T | ISO/IEC common texts) for compliance with the ITU-T Author's Guide, presentation rules, and quality checklist before submission for consent/determination/approval. Use this skill whenever the user asks to review, check, audit, proofread, or improve a draft ITU-T Recommendation, standard contribution, amendment, corrigendum, or common text — including requests phrased as "检查/审查/校对 ITU-T 建议书", "does my draft follow ITU-T rules", "prepare my draft for TSB submission", or when a user uploads a document identified as a draft Recommendation. Also use it when authors ask how to correctly structure clauses, references, definitions, figures, tables, or notes in an ITU-T text.
---

# ITU-T Recommendation Reviewer

Review draft ITU-T Recommendations against the official drafting rules so that authors, editors, and rapporteurs can fix problems **before** the text goes to TSB or is proposed for consent/determination/approval. The rules encoded here come from three authoritative sources:

1. **ITU-T Editing Guidelines — Author's guide for drafting ITU-T Recommendations (06/2023)** — the primary rulebook for pure ITU-T texts.
2. **Rules for presentation of ITU-T | ISO/IEC common text (09/2014)** — overrides the author's guide when the text is a joint ITU-T | ISO/IEC document.
3. **Recommendation ITU-T A.1 (09/2019)** — working methods; relevant for terminology (amendment/corrigendum/annex/appendix), work-item context, and submission expectations.

## Step 0 — Identify the document type FIRST

The applicable rulebook depends on the document type. Misidentifying it produces wrong review findings, so always classify before reviewing:

| Type | How to recognize it | Rulebook |
|---|---|---|
| Pure ITU-T Recommendation | Single ITU-T number (e.g., ITU-T X.1234); "Appendix I/II…" for non-integral material | Author's guide → `references/structure-rules.md` + `references/formatting-rules.md` |
| ITU-T \| ISO/IEC common text | Dual designation "Rec. ITU-T x.nnn \| ISO/IEC nnnnn"; expression "this Recommendation \| International Standard"; non-integral **annexes** instead of appendices | Common-text rules → `references/common-text-rules.md` (it deviates from the author's guide; apply its rules where they differ) |
| Amendment / Corrigendum | Title contains "Amendment n" or "Corrigendum n" to a base text | `references/structure-rules.md` §Amendments plus common-text Annex C if it is a common text |

If the type is ambiguous, ask the user (one question) rather than guessing.

## Step 1 — Load the rules

Read the reference files relevant to the document type before making findings. Do not review from memory alone — the reference files contain the exact boilerplate wording, numbering conventions, and checklist items that findings must cite.

- `references/structure-rules.md` — mandatory elements, their order, clause-by-clause requirements (Scope, References, Definitions, Abbreviations, Conventions), annex/appendix rules, required boilerplate sentences.
- `references/formatting-rules.md` — fonts, clause numbering, lists, equations, figures, tables, notes/footnotes, citation style, shall/must usage.
- `references/definitions-rules.md` — the full best-practice rules for writing definitions (structure, conciseness, independence, grammatical form, formatting).
- `references/common-text-rules.md` — everything that differs for ITU-T | ISO/IEC joint texts.
- `references/quality-checklist.md` — the rapporteur's pre-approval checklist (Annex D) that every draft must pass, plus A.1-derived process checks.

## Step 2 — Run the review in passes

Review in this order; each pass has its own section in the report. Quote or pinpoint the exact location (clause number, figure/table number — never page number) for every finding.

**Pass 1 — Skeleton & mandatory elements.** Verify presence and correct order of: title, Summary, Keywords, (optional Introduction), Scope (clause 1), References (clause 2), Definitions (clause 3, split 3.1/3.2), Abbreviations and acronyms (clause 4), Conventions (clause 5), technical content (clause 6 onwards), Annexes, Appendices, Bibliography. Empty clauses must say "None." or "This clause is intentionally left blank." — they may not simply be absent.

**Pass 2 — Boilerplate & wording conformance.** Check that clauses 2, 3.1, 3.2, and 4 open with the exact required sentences (given verbatim in `references/structure-rules.md`), that annexes/appendices carry the correct "(This annex forms an integral part…)" line, and that "shall"/"must" appear only where a genuinely mandatory provision is intended.

**Pass 3 — References & citations.** Every entry in clause 2 must be normatively cited in the body (a reference cited only from an appendix is a violation); informative sources belong in the Bibliography with `b-` citation tags; check citation-tag format `[ITU-T A.5]` / `[b-ITU-T A.13]`, presentation format of each entry, and cross-reference style ("see clause 5.4.7", "see Figure 1 of [b-ITU-T A.8]").

**Pass 4 — Definitions & abbreviations.** Apply `references/definitions-rules.md` item by item: term–class–characteristics structure, no circularity, alphabetical order, bold lower-case term + colon, definitions end with a period, existing terms not redefined. Abbreviations: alphabetical, capitalized letters expanded, first use in text preceded by full form, plural as "ICTs" not "ICTS".

**Pass 5 — Figures, tables, equations, notes.** Numbering schemes, caption placement (figure titles below/centred; table titles above/centred), explicit in-text reference to every figure and table, note formats ("NOTE – " / "NOTE 1 – "), footnote rules, notes-to-tables placed inside the table frame, equation numbering, SI units, thousand separator as single quote.

**Pass 6 — Quality checklist & language.** Walk through `references/quality-checklist.md`: no case studies in normative parts, minimal options, no conflict with approved Recommendations, spell-check, all acronyms (including in figures/tables) expanded, unnecessary capitalization/italics/bold avoided, title contains no acronyms and does not repeat series titles.

## Step 3 — Write the review report

ALWAYS use this exact report structure (deliver in the user's working language; keep quoted rule text and suggested replacement text in English, since that is the publication language):

```
# ITU-T Draft Review Report: <document title/number>

## 1. Document profile
Type (pure ITU-T / common text / amendment / corrigendum), rulebook applied, overall verdict:
READY / MINOR REVISION / MAJOR REVISION.

## 2. Critical issues (block consent/approval)
Numbered list. Each item: [Location] — problem — governing rule (cite the guide clause,
e.g., "Author's guide §8.2") — concrete fix (give replacement text where possible).

## 3. Major issues (must fix before publication)
Same format.

## 4. Minor / editorial issues
Same format; may be grouped (e.g., "12 instances of 'may not' — replace with 'need not'").

## 5. Checklist result
The Annex D checklist as a table: item | pass/fail/N-A | evidence.

## 6. Suggested next steps
Short prose paragraph: what to fix first, and any process reminders from ITU-T A.1
(e.g., IPR declaration, six-week TD deadline, new-work-item template).
```

Severity calibration:
- **Critical** — missing mandatory element, wrong/missing boilerplate, normative reference never cited in the body, appendix mislabelled as annex (or vice versa), "shall" in notes/introductory material, common-text rules violated in a joint text.
- **Major** — defective definitions, incorrect reference presentation format, figures/tables never referenced in text, wrong numbering scheme, title violations.
- **Minor** — typography, capitalization, list punctuation, note spacing, style-guide deviations.

## Step 4 — Offer follow-through

After the report, offer (do not do unsolicited): (a) produce a corrected version of specific clauses with revision marks — remembering the Annex A/E rule that changes must be shown with revision marks and unchanged text may be replaced by ellipses; (b) rewrite the worst definitions; (c) generate the missing boilerplate ready to paste.

## Scope limits — be honest about them

- This skill checks **drafting/presentation compliance and internal consistency**, not technical correctness of the standard's subject matter. Say so in the report.
- Word-template styles (exact fonts/point sizes) can only be verified if the user supplies a .docx; from a PDF or pasted text, flag them as "not verifiable from this format" rather than guessing.
- Never claim a draft "will be approved" — approval is a membership decision under WTSA Res. 1; the verdict wording is about editorial readiness only.
