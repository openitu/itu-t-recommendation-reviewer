# Rules for reviewing definitions (Author's guide Annex B)

Apply these to every entry in clause 3.2 (and to any quoted definitions in 3.1).

## Reuse before inventing (B.3.1)
- Do not define a term if an acceptable definition already exists (check ITU Terms and Definitions database); do not redefine existing terms; new term names must not collide with already-defined term names.
- Review action: if a common industry/ITU term is redefined in 3.2, flag it and suggest moving to 3.1 with a reference.

## Three-part structure (B.3.2)
Every definition = **term** + **class of object/concept** + **distinguishing characteristics**.

Example of a compliant definition:
`cryptographic algorithm: a mathematical function that computes a result from one or several input values.`
(term) (class) (distinguishing characteristics)

Review action: definitions that jump straight to behaviour ("X is when…") or list examples instead of a class fail this test.

## Conciseness (B.3.3)
- One concept per definition; only information that makes the concept unique.
- Detailed explanation, supplementary info → NOTE / figure / equation below the definition, not inside it.
- Figures/equations supplement, not replace, the verbal definition (mathematical terms excepted).

## Clarity and accuracy (B.3.4)
- Accurate, clear, **positive** (negative definitions not acceptable).
- Not circular; must not include or paraphrase the term being defined.
- Vocabulary used must be common English or defined elsewhere in the text.

## Independence (B.3.5)
- Must stand alone: understandable without reading other parts of the Recommendation (definitions get extracted into the ITU database).

## Grammatical form (B.3.6)
- Same part of speech as the term (noun term → noun-phrase definition).

## Abbreviations, symbols, protocol elements (B.3.8–B.3.10)
- Abbreviations inside a definition must be expanded.
- Standard measurement-unit symbols not defined.
- Formal/detailed protocol-element descriptions belong in clause 6+, not in Definitions.
- Notation/representation conventions belong in clause 5, not in Definitions.

## Formatting (B.4)
- Each definition numbered (3.2.1…), term in **bold**, starting **lower-case**, followed by a **colon**; definition ends with a **period**.
- Multiple explanations separated by semicolons.
- **Alphabetical order** within each of 3.1 and 3.2.

## Quick failure patterns to search for
- "X: X is…" (circular)
- "X: not a Y…" (negative)
- "X: see clause 7" (not standalone)
- Definitions containing "shall" (requirements do not belong in definitions)
- Capitalized first letter of the term, missing colon, missing final period
- 3.1 entries quoting full text of another document's definition without a reference/copyright note
