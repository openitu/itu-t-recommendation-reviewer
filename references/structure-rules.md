# Structure rules for pure ITU-T Recommendations

Source: ITU-T Editing Guidelines — Author's guide for drafting ITU-T Recommendations (06/2023), clauses 6–8, Annex A, Annex E. Terminology cross-checked with Rec. ITU-T A.1 (09/2019) clause 1.8.

## 1. Number, date, title (Author's guide §6)

- Unique Recommendation number: series letter + number, optional suffix (e.g., ITU-T G.108.2); dual numbers only exceptionally (e.g., ITU-T G.709/Y.1331).
- Edition identified by year (or month/year) of approval.
- Title: not unnecessarily long; indicates main topics; **unique**; **contains no acronyms**; does **not** repeat the series/sub-series titles already on the cover page.
- The title of a Recommendation must NOT be modified by an amendment or corrigendum (Annex E.4).

## 2. Introductory material (§7) — not part of the Recommendation

- Must contain **no normative requirements**.
- **Summary — mandatory.** Brief overview of purpose and contents.
- **Keywords — mandatory.** Limited number, **alphabetical order, separated by commas**.
- **Introduction — optional.** Only information not already in Summary or Scope.
- Pages of introductory material use lower-case Roman numerals (TSB handles this; do not flag in author drafts unless the author has hard-coded Arabic numbers there).

## 3. Order of elements (§8, Table 1)

Core material order (clause numbers fixed):

| Element | Clause |
|---|---|
| Title | none |
| Scope | 1 |
| References | 2 |
| Definitions | 3 |
| Abbreviations and acronyms | 4 |
| Conventions | 5 |
| Technical content | 6 onwards |
| Annexes (integral) | A onwards |
| Appendices (non-integral) | I onwards (Roman) |
| Electronic attachment | – |
| Bibliography | none |
| Index (optional, rare) | none, last |

**When a clause among 2–5 is empty it must still be present** with "None." or "This clause is intentionally left blank."

## 4. Clause-by-clause requirements

### Clause 1 — Scope
Defines, without ambiguity, intent/object and aspects covered → the limits of applicability. Must appear at the beginning of every Recommendation.

### Clause 2 — References
Must be introduced by this exact boilerplate:

> "The following ITU-T Recommendations and other references contain provisions which, through reference in this text, constitute provisions of this Recommendation. At the time of publication, the editions indicated were valid. All Recommendations and other references are subject to revision; users of this Recommendation are therefore encouraged to investigate the possibility of applying the most recent edition of the Recommendations and other references listed below. A list of the currently valid ITU-T Recommendations is regularly published. The reference to a document within this Recommendation does not give it, as a stand-alone document, the status of a Recommendation."

Rules:
- List **alphanumerically in ascending order**.
- Only **normative** references (provisions incorporated by reference from the main body including annexes). Informative material goes to the Bibliography.
- Every entry gets a citation tag in square brackets, e.g., `[ITU-T A.5]`, used for all subsequent citations.
- ITU-T/ITU-R entries: "Recommendation ITU-T A.5 (2019)," + full title.
- The **sole** reference to a normative reference must not come from an appendix (then it is informative and belongs in the Bibliography).
- Every clause-2 entry must actually be cited somewhere in the main body/annexes — unused entries are a violation.
- Referencing other-SDO documents requires ITU-T A.5 qualification (flag unfamiliar SDO references for A.5 check).

Presentation formats (match exactly):
- Dual-numbered: `[ITU-T G.709]  Recommendation ITU-T G.709/Y.1331 (2020), Interfaces for the optical transport network.`
- Common text: `[ITU-T H.222.0]  Recommendation ITU-T H.222.0 (2021) | ISO/IEC 13818-1:2022, <title>.`
- Series: `[ITU-T M.3016.x]  Recommendation ITU-T M.3016.x-series (2005), <title>.`
- SDO examples: `[IETF RFC 6038]  IETF RFC 6038 (2010), <title>.` / `[ISO/IEC 14496-3]  ISO/IEC 14496-3:2019, <title>.`

### Clause 3 — Definitions
- 3.1 "Terms defined elsewhere" opens with exactly: "This Recommendation uses the following terms defined elsewhere:"
- 3.2 "Terms defined in this Recommendation" opens with exactly: "This Recommendation defines the following terms:"
- Each term gets a clause number (3.1.1, 3.2.1, …).
- Terms defined elsewhere should normally carry only a normative reference to the defining document; quoting the definition verbatim is exceptional and needs copyright clearance if from another SDO.
- Full quality rules: see `definitions-rules.md`.

### Clause 4 — Abbreviations and acronyms
- Opens with exactly: "This Recommendation uses the following abbreviations and acronyms:"
- Alphabetical order; letters appearing in the acronym capitalized in the expansion (e.g., "PICS Protocol Implementation Conformance Statement").
- First appearance of any acronym in the text preceded by its unabbreviated form, e.g., "asynchronous transfer mode (ATM)".
- Plural of capitalized acronym: lower-case "s" (ICTs, not ICTS).
- SI units (kHz…) and names of ITU/major SDOs need not be listed.

### Clause 5 — Conventions
- Describes notations/assumptions/styles used. If none: "None."
- Special classes of capitalized terms must be listed here.
- Home of the shall/must policy: "shall"/"must" (and negatives) used **with care and sparingly**, only for genuinely mandatory provisions.

### Clause 6 onwards — Technical content
- Non-normative material should be moved to an appendix.

## 5. Annexes vs appendices (§8.7–8.8) — the most common structural error

| | Annex | Appendix |
|---|---|---|
| Status | **Integral** part; same approval procedure as the Rec. | **Not** integral; SG agreement suffices |
| Designation | A, B, C… (single: "Annex A") | Roman I, II, III… (single: "Appendix I") |
| Required line under title | "(This annex forms an integral part of this Recommendation.)" | "(This appendix does not form an integral part of this Recommendation.)" |
| Position | Immediately after main body | After last annex (or after body if no annexes) |
| Numbering inside | A.2, Figure B.3, Equation C-1; restarts each annex | II.3, Table IV.2, Equation III-1; restarts each appendix |

Review implications:
- Normative content in an appendix → critical (either promote to annex or make non-normative).
- The Bibliography is non-normative but is NOT labelled as an appendix and does not carry the "(This appendix…)" line.

## 6. Electronic attachments (§8.9)
Source code, test data, formal descriptions, pro formas. May be normative or informative. Copyright/patent on attachments requires TSB declaration forms — remind the author.

## 7. Bibliography (§8.10)
- For informative sources only. Tag format inserts `b-`: `[b-ITU-T A.1]`.
- Do NOT reference draft standards, TDs, contributions, or other documents unavailable to readers.
- Presentation mirrors clause 2 (see examples: supplements, books, journal articles, web-only documents with URL on its own line).

## 8. Amendments and corrigenda (Annex A, Annex E; A.1 §1.8.2)

Terminology (from ITU-T A.1):
- **amendment** — changes or additions to a published Recommendation.
- **corrigendum** — corrections to a published Recommendation.
- **erratum** — TSB-published correction of publication/editorial errors.

Presentation rules:
- Changes shown with revision marks (strikethrough/underline/revision bars); unchanged text may be replaced with ellipses "…", keeping enough context (clause titles) to locate insertion points; fixed italic header announcing this convention.
- Existing clause/figure/table numbers must NOT be renumbered; deleted numbers not reused; insertions use letter-extended numbers (6.1a, 6.1b).
- Full renumbering only in a complete revised edition.
- Title of the base Recommendation must not change.

## 9. Process reminders drawn from ITU-T A.1 (mention in "next steps" when relevant)

- Draft new/revised Recommendations planned for consent/determination should be submitted as separate TDs **at least six weeks** before the parent group's meeting (A.1 §2.3.3.6 g).
- Contributions: full text must reach TSB **at least 12 calendar days** before the meeting; ≥2 months for translation.
- New work items require the Annex A template (Question, title, base text, editor, timing, AAP/TAP, scope, summary, liaisons, supporting members).
- IPR: meetings must ask about patents/copyright/marks; contributors submitting copyrighted software must file the software copyright form.
- Draft new/substantially revised Recommendations should normally be based on written contributions from ITU-T members.
