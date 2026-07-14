# Contributing

Thank you for your interest in improving the ITU-T Recommendation Reviewer skill.

## Governance

This project has a single maintainer who acts as the final administrator. **Every change — including documentation fixes — must be submitted as a pull request and is merged only after the maintainer's review and explicit approval.** Direct commits to `main` are not accepted from anyone else, and no other write access is granted.

## How to contribute

1. **Open an issue first** for anything non-trivial (new rules, restructuring, behavior changes), describing the problem and citing the relevant ITU-T source clause.
2. **Fork the repository** and create a branch for your change.
3. **Make your change.** Requirements:
   - Every rule added or modified in `references/*.md` must cite its source (Author's guide clause, common-text rules clause, or ITU-T A.1 clause). Rules without a verifiable ITU-T source will not be accepted.
   - Do not add ITU publications (PDFs, Word files) to the repository — link to the official ITU permalinks instead.
   - Keep `SKILL.md` and the reference files consistent with each other.
4. **Submit a pull request** explaining what changed and why, with the ITU-T source citations.
5. **Wait for maintainer review.** The maintainer may request changes, accept, or decline the contribution.

## Scope

In scope: corrections and updates tracking new editions of the ITU-T editing guidelines, improved report structure, better examples, bug fixes in rule descriptions.

Out of scope: technical review of standards content, rules for other SDOs (ISO/IEC-only, ETSI, 3GPP, etc.) — those belong in separate skills.

## License

By contributing, you agree that your contributions are licensed under the [MIT License](./LICENSE).
