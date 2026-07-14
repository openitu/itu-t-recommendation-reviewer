# Formatting rules for ITU-T Recommendations

Source: Author's guide (06/2023), clause 9. These apply to pure ITU-T texts; for common texts see `common-text-rules.md` where rules differ.

## Fonts (§9.2) — verifiable only in .docx

- Body: serif (Times New Roman) 12 pt. Sans serif (Arial) / constant width (Courier New) / math symbol fonts where required.
- URIs in text: 8 pt Arial. ASN.1 modules/types and XML documents/schemas: 9 pt Courier New.
- Text inside figures and tables: 9 pt Times New Roman.
- Avoid unnecessary italic and bold in the text; special fonts must be embedded.
- Use the ITU-T template styles; deviations must be declared to TSB.
- From a PDF or pasted text, mark font items as "not verifiable from this format".

## Clause numbering and titles (§9.3)

- Digits in bold, separated by periods (8.3.1); no trailing period on a single number.
- Number + title on a separate line, title in bold, to the right of the number. Untitled clauses avoided.
- Common-text extra rule (also good practice): don't create x.1 unless x.2 exists.

## Lists (§9.3.3)

- ≤3 levels.
- One-level lists: dashes, bullets, or numbers; items typically end with ";" and last with ".".
- If sub-lists exist, main level at least must be numbered/lettered: a) → i), ii).

## Mathematics (§9.4)

- SI quantities/units/symbols; letter symbols explained below the expression.
- Equations on their own line(s); numbered when needed as (6-3) = third expression of clause 6, at right margin. MathType encouraged.
- Thousands separator: single quote — 1'000'000 (not commas, dots, or spaces).
- Arabic numerals and non-Latin (Greek/Cyrillic) characters not in italics.

## Figures (§9.5.1)

- Every figure explicitly referred to in the text ("see Figure 1") — orphan figures are a violation.
- Numbered with Arabic numerals from 1, independent of clause numbering (long/complex Recs may use Figure 4-3 style). In annexes/appendices: Figure B.3 / Figure II.1.
- Number + title on the same line, **centred, below** the figure; first word capitalized only.
- Two-part figures: Figure 6-a, Figure 6-b, collectively Figure 6.
- Must be legible in greyscale; ITU figure index in lower-right corner preserved when reusing ITU figures; editable source files (Visio/PowerPoint/CorelDraw) encouraged at final submission.

## Tables (§9.5.2)

- Every table explicitly referred to in the text ("see Table 1").
- Numbered from 1, independent of clauses/figures (Table 6-3 style allowed for long Recs); Table A.1 / Table IV.2 in annexes/appendices.
- Number + title **centred, above** the table; first word capitalized only.
- Column headings bold, centred, first letter capitalized.
- Longer than a page: repeat number, title and column headings each page; "(continued)" / "(concluded)" markers.
- Wider than a page: split into sub-tables with indexed rows.

## Notes and footnotes (§9.6)

- Single note in a clause: `NOTE – text` (word NOTE, space, em dash, space).
- Multiple notes in the same clause: `NOTE 1 –`, `NOTE 2 –`, … numbered consecutively **within that clause**.
- Notes and footnotes to the main text must NOT contain normative specifications ("shall" inside a NOTE = critical finding).
- Footnotes: superscript Arabic numerals, consecutive through the Recommendation, smaller font.
- Notes to tables/figures: independent numbering per table/figure; located inside the table frame / between figure and its title; MAY contain normative specifications; may use superscript lower-case letters.

## Citing (§9.7)

- Within the same Rec: "see Table 4", "see clause 5.4.7" — never page numbers.
- To another Rec: include the citation tag — "see clause 2.2.10 of [ITU-T A.5]", "see Figure 1 of [b-ITU-T A.8]".

## Language and capitalization

- Unnecessary capitalized words avoided; classes of capitalized terms declared in Conventions.
- "shall"/"must" only for mandatory provisions; compliance wording note: a Recommendation is voluntary.
- Formal-language modules in compiler-acceptable characters, constant-width font.
- ITU English style guide applies for general language questions.
