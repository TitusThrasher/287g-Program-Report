# Contributing to 287g-Program-Report

Thanks for your interest in helping to improve this project. This repository tracks the ongoing growth of Immigration and Customs Enforcement (ICE)'s 287(g) agreement program, reconstructed from published ICE participating agency lists. Corrections, bug reports, and documentation fixes are all welcome.

Please read this short guide before opening an issue or pull request.

## How the data is maintained

The published datasets are maintained by Andrew Thrasher ([Titus Consulting](https://tituslegaldesign.com/287g-program) / [Maxwell Commons](https://maxwellcommons.substack.com)).

---

## Reporting a data error

Use the **Data correction** issue template (`.github/ISSUE_TEMPLATE/data-correction.md`). A useful report includes:

1. **The record.** Agency name, state, and the file and row (or `last_listed` / `first_absent` dates) where the error appears.
2. **What's wrong.** For example: a wrong date, a misclassified cancellation, a duplicate record, or a misspelled agency name.
3. **What you think is correct.**
4. **Evidence.** A link or citation. Strong sources include:
   - an archived ICE participating-agency list (ICE.gov or a Wayback Machine capture)
   - a signed memorandum of agreement, or a termination letter
   - meeting minutes, a resolution or a press release from the agency or local government
   - news reporting that cites any of the above

Reports without evidence are still welcome, especially if something just looks off, but they may take longer to resolve.

### What happens next

- The maintainer checks the claim against the snapshot record, corresponding Memorandum of Agreement (if available), and additional sources you provided.
- Confirmed corrections are made upstream and the change is logged in `Agreement-Corrections.md` (_coming soon_), with credit to the reporter (unless you'd rather not be named — just say so in the issue).
- If the claim can't be confirmed, the issue stays open with a note about what evidence would settle it, or gets closed with an explanation.

---

## Other contributions (pull requests welcome)

Pull requests are welcome for:

- **Documentation:** typos, unclear wording, broken links, and gaps in `README.md`, `docs/` or `data/README.md`
- **Data dictionary and source notes**

For anything larger than a small fix, such as a new analysis, a schema change or a new output file, please **open an issue to discuss it first**. The published schemas are cited by outside reporting, so changes are made deliberately and versioned.

### Pull request checklist

- [ ] Fork the repo and create a branch from `main`.
- [ ] Keep each PR focused on one change.
- [ ] No changes to `data/`.
- [ ] Write a clear PR description: what changed, and why.

---

## Questions, tips and things that aren't errors

- **Methodology questions or disagreements:** open an issue labeled `question` or `methodology`. Reasonable disagreement about classification is welcome, and the reasoning will be explained.
- **Tips or documents you'd rather not share publicly** (for example, records about an agency's agreement status): don't put them in a public issue. Contact the maintainer through [tituslegaldesign.com](https://tituslegaldesign.com) or by email <info@tituslegaldesign.com> instead.
- **Press and citation:** see `CITATION.cff`.

---

## Licensing

This project is released under the MIT License (see `LICENSE`). By contributing, you agree that your contributions are licensed under the same terms. Third-party resources referenced, as well as ICE source documents archived here, are not subject to copyright.

---

## Conduct

Be respectful, assume good faith, and keep the discussion about the data and the code. This project covers immigration enforcement, a subject that directly affects people's lives. Please keep that in mind in issues and comments. The maintainer may edit, lock or remove comments that are abusive, off-topic, or that expose personal information about private individuals.
