# Rapporteur-meeting readiness checklist (TSAG LS20 draft checklist)

## Source and status — state this in the report

- **Origin:** TSAG-C48, "Proposed checklist for efficient Rapporteur Meeting" (OKI, NICT, The University of Tokyo), TSAG meeting Geneva, 26–30 January 2026 (Study Period 2025–2028); circulated to the Study Groups as **Attachment 1 to TSAG LS20**.
- **Status:** **DRAFT.** TSAG has invited SGs to contribute common points and comments; the checklist may later be appended to the Author's Guide or issued as a separate document. Findings under this checklist must therefore be reported as *"per the draft TSAG LS20 checklist"*, not as binding Author's-guide rules — unless the same point is independently required by the Author's guide (many are; cross-references below say so).
- **Scope of applicability:** all draft **ITU-T Deliverables** — Recommendations, Supplements, and Technical Reports — before consent, determination, or approval is requested at a Rapporteur Meeting (RM). Intended reviewers: editor, Rapporteur/Associate Rapporteur, WP (Co-/Vice-)Chair.
- **Why it exists:** the same editorial comments were being repeated at every RM, crowding out technical discussion and delaying approvals to WP Plenary. Running this checklist *before* the meeting is the fix.

## Review summary header — reproduce at the top of the report's checklist table

| Field | Entry |
|---|---|
| Date | |
| Reviewed document (acronym or Rec. number) | |
| Document number or link | |
| Reviewer (name and position) | Editor / Rapporteur / Associate Rapporteur / WP (Co-)Chair / WP Vice-Chair |
| Result | Need further modifications / Need judgement |

## The checklist items

Grade each item **Yes / No / N-A** with one line of evidence. Where an item duplicates an Author's-guide rule already checked in an earlier pass, reference the earlier finding instead of repeating it.

### S — Scope

- **S1 — Scope ↔ body alignment.** Every element announced in the Scope (clause 1) must actually be treated in the main body. Untreated elements: either delete them from the Scope or note that body text must be added by future contributions. **If the Scope changed significantly at the decision (consent/determination/approval) stage, recommend postponing the decision to the next meeting — the document is not stable.** *(Overlaps Author's guide clause-1 rules in `structure-rules.md`; the postponement rule is new.)*

### R — References

- **R1 — Normative references must be used normatively.** Every document in clause 2 must be cited in the body **after clause 6** (i.e., in the technical content). A document cited only in clause 3 (as the source of a definition) is not normative — move it to the Bibliography. *(Same substance as the "every clause-2 reference cited in the body" rule in `quality-checklist.md` item 10, sharpened: clause-3-only citation is explicitly insufficient.)*
- **R2 — Ordering of the reference list.** Alphanumeric ascending order, grouped: ITU-T and ITU-R Recommendations first, then ISO, IEC, and other qualified organizations' standards. *(Matches `formatting-rules.md` citation-presentation rules.)*
- **R3 — Sufficiency of references.** If implementing the system described requires other Recommendations, those Recommendations must appear in clause 2 — insufficient referencing of existing Recommendations is a recurring RM comment.
- **R4 — A.5 justification.** Any clause-2 document not produced by ITU, ISO, or IEC needs a prepared ITU-T A.5 justification. *(Matches `quality-checklist.md` item 11.)*

### D — Definitions

- **D1 — Terms defined elsewhere (3.1) must carry a resolvable reference.** The source of every 3.1 definition must be listed; if it is cited only from clause 3, it belongs in the Bibliography. *(Extends `definitions-rules.md`.)*
- **D2 — No general terms in 3.2.** Defining generic/common-language terms in 3.2 is a recurring RM objection — reconsider or delete such terms.
- **D3 — Reusability of 3.2 terms.** Terms defined in 3.2 enter the ITU-T Terms and Definitions (vocabulary) database for reuse by future Recommendations. Ask: is each 3.2 term genuinely reusable beyond this document? If not, it probably should not be a formal definition.

### C — Conventions

- **C1 — Every convention entry must be used.** All keywords declared in clause 5 (e.g., "is required to", "is recommended to", "can optionally") must actually occur in the body. Declaring the full requirement-keyword set while using only one or two of them is a fail.
- **C2 — Graphic symbols: legend or clause-5 convention.** Where figures use shapes and line styles with special meaning (rectangle, rounded rectangle, circle; solid/dashed/bold arrows and lines), those meanings must be defined either in a per-figure legend or centrally in clause 5. Good models cited by the checklist: the Conventions clauses of **[ITU-T H.780]** and **[ITU-T Y.1910]**, which define each keyword ("is required to" = mandatory for conformance; "is recommended" = not absolutely required; "can optionally" = permitted, vendor's choice) and each symbol ("functions" = collection of functionalities; "functional block" = group of functionalities not further subdivided; solid line = required functionality/relation, dashed line = optional).

### M — Main body

- **M1 — Use cases belong in an appendix.** Use cases are informative; they must not sit in the normative main body. *(Consistent with the "no case studies in normative part" rule, `quality-checklist.md` item 4.)*
- **M2 — Differentiation from existing Recommendations.** The draft must explain what is different from, or added over, existing Recommendations — the merit of the new text must be explicit.
- **M3 — Feasibility of "required" requirements.** Too many mandatory ("is required to") requirements lowers implementability. The editor must show this has been considered — expect some requirements to be downgraded to recommended/optional, or an explanation of how feasibility is assured. Grade "No" if the requirement table is overwhelmingly mandatory with no justification.
- **M4 — Every technical term in a figure is explained in the text.** Figures must be verbally explained in the main body, covering all technical terms they contain; terms not important enough to explain should be removed from the figure to avoid confusion. *(Extends the "every figure referenced in text" rule — mere reference is not enough; the content must be explained.)*
- **M5 — Shapes and line styles in figures are defined.** Rectangles, rounded rectangles, circles; solid, bold-solid, dotted lines — undefined, they will be misread. Enforce via legend or clause 5 (see C2).
- **M6 — "Functional architecture" figures must show connections.** In a functional architecture, every functionality connects to at least one other. A figure with boxes but **no lines** is not an architecture — call it a **functional framework** instead (or add the lines).
- **M7 — Element positions in framework figures must mean something.** A framework is the precursor of an architecture; box placement should anticipate it. Typical criteria: data flowing left→right puts input-processing elements on the right/output on the left (or top→bottom analogously). State the arrangement criterion and arrange the boxes accordingly — "boxes scattered with no positional logic" is a standard RM objection.
- **M8 — "Layered structure" must be justified.** A mere sequence of functions is not a layered structure; use the term only when genuine layering semantics (service abstraction between layers) exist.

## Notes for the reviewing agent

- The original draft contains editorial slips (e.g., "Sope" for "Scope", "allow" for "arrow", the Conventions and Main-body tables both numbered I.4). The normalized content above is authoritative for this skill; do not reproduce the slips.
- Items M2, M3, M6, M7, M8 are **semi-technical** judgements: flag them with evidence and phrase them as questions to the editor where the text is defensible, rather than as hard failures. S1's postponement recommendation, by contrast, is procedural and should be stated plainly when triggered.
- When the reviewed document is a Supplement or Technical Report, clause-number references (clause 2, 3.1/3.2, 5) map to the corresponding sections of that deliverable type.
