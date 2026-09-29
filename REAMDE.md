# Reproducibility Templates

Templates used in reproducibility checks of replication packages published in the Journal Data Archive (JDA), maintained by ZBW – Leibniz Information Centre for Economics as part of the ReproCheck project.

This repository provides templates for authors to document their replication packages and for replicators to record the process and results of reproducibility checks.

## Contents

| File | Purpose |
|------|---------|
| [`JDA_README_Template_V1.md`](JDA_README_Template_V1.md) | Template README that **authors** should include in their replication package. Describes data availability, code, folder structure, and requirements needed to reproduce the results. |
| [`JDA_Report_Template_V1.md`](JDA_Report_Template_V1.md) | Template report used by **replicators/reviewers** to document the reproducibility check of a submitted replication package (metadata review, static code check, replication run, findings, classification). |
| [`code-check.xlsx`](code-check.xlsx) | Spreadsheet used to track/cross-walk code files, outputs, and tables/figures during a reproducibility check. |


## Who should use these templates?
 
- **Authors** preparing a replication package for the JDA: start from `JDA_README_Template_V1.md`
  and replace the guidance text in each section with your project's information.
- **Replicators** performing a reproducibility check: use `JDA_Report_Template_V1.md` together with
  `code-check.xlsx` to document the review and give a final classification
  (*Full reproduction* / *Less than full reproduction*).

## Usage
 
1. Copy the relevant template into your project or review folder.
2. Follow the guidance in the README template, or the `INSTRUCTION` blocks in the report template.
3. In the report, replace all bracketed placeholders (`[...]`) and remove the `INSTRUCTION` blocks
   before finalizing.


## Background

These templates build on and adapt established community resources, including:

- The [AEA Data Editor replication report template](https://github.com/AEADataEditor/replication-template)
- The [Social Science Data Editors README template](https://github.com/social-science-data-editors/template_README)
- The [World Bank Reproducible Research Repository README template](https://github.com/worldbank/wb-reproducible-research-repository)

## License

The templates are adapted from and licensed under the same terms as their source
projects (CC-BY 4.0 / CC-BY-NC 4.0, see individual template files for details).

## Contact

Maintained by [ZBW - Leibniz Information Centre for Economics](https://www.zbw.eu/)
as part of the ReproCheck project.