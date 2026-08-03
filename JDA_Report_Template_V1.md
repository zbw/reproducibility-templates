# [Dataset DOI] — [Manuscript Title] — Replication Package Check (ZBW Journal Data Archive)

> **INSTRUCTION:** Replace bracketed placeholders. Keep INSTRUCTION blocks while you work; remove them before final report completion. 

**Journal:** [name]  
**Article DOI:** [paste DOI]
**JDA Dataset DOI:** [paste DOI]  
**Authors (paper order):** [list of names]  
**Responsible replicator:** [name]  
**Start date:** [YYYY‑MM‑DD] | **Completion date:** [YYYY‑MM‑DD]


## SUMMARY

> **INSTRUCTION:**  Leave **Classification** and **Reasons** marked below.

**Classification (pick one):**  
- [ ] Full reproduction  
- [ ] Less than full reproduction 

**Reason(s) if not "Full":**  
- [ ] Discrepancy in output  
- [ ] Fixable bugs in code  
- [ ] Code missing
- [ ] Code not functional
- [ ] Software not available  
- [ ] Insufficient time / excessive runtime  
- [ ] Data missing  
- [ ] Data confidential
- [ ] Missing or non‑compliant README  
- [ ] Others:

### Major finding and action items
> **INSTRUCTION:** This part includes 1–3 lines summrising the major findings of section 11), and then is filled be based on any [REQUIRED] and [SUGGESTED] action items that the report makes a note of below.

> **INSTRUCTION:** KEEP the next line AS-IS, WORD FOR WORD. Do not delete it, edit it, or paraphrase it, regardless of what else changes in this SUMMARY (including on a later revision round). It is the fixed transition sentence from the SUMMARY into the Action Items lists below, and must always be the last line of the SUMMARY, immediately before "action items".

In assessing compliance with our [Data and Code Availability Policy](link to the journal data and code policy), we have identified the following issues, which we ask you to address:

> **INSTRUCTION:** Copy-paste all the [REQUIRED] and [SUGGESTED] action items below in the report here.

---

## 0) Quick Start — End‑to‑end Checklist

> **INSTRUCTION:** Use this as a progress compass.

- [ ] Intake: Enter article DOI in the title and DOI spaces of the issue. **To confirm whether there is an article DOI at this stage.**
- [ ] Part A (Metadata: section 1-7): Review README, data citations, meta fields
- [ ] Part B (Static code check and replication steps: section 8-11): Confirm presence of a **master** script; map outputs to programs; replication steps.
- [ ] Environment: Record OS/versions; pin software and package versions (Stata/R/Python).
- [ ] Run: Execute end‑to‑end; log errors/fixes; re‑run clean/corrected code.
- [ ] Findings: Fill table/figure/in‑text results; classify reproducibility; list suggestions.
- [ ] Finalize: Check classification; summerise the findings.

---
Part A
## 1) GENERAL (README & documentation)

> **INSTRUCTION:** Confirm the README (or appendix) exists and has each of the following elements.

- [ ] Data Availability & Provenance Statement  
  - [ ] Rights to **use** data are clear  
  - [ ] Rights to **publish/share** data are clear (or restrictions justified)  
  - [ ] **Source details** for each input dataset  
- [ ] Dataset list (all inputs)  
- [ ] References include **data citations**
- [ ] Description of programs/code 
- [ ] Step‑by‑step instructions to replicators  
- [ ] Mapping of tables/figures to programs  
- [ ] Computational requirements  
  - [ ] Software versions & packages  
  - [ ] Controlled randomness / seeds (as needed)  
  - [ ] Memory, runtime, storage expectations  
- [ ] README completely missing

> [REQUIRED] As specified in the [Policy](Link to the README policy of the journal), the README should contain  certain  required elements. We suggest using the [Journal' template README](Link to the README template of the journal).
  - All elements are required, unless a modifier is used in the above list.

---

## 2) RCT (if applicable)

- [ ] Not an RCT  
- [ ] RCT reported  
  - [ ] Registration number present **and** cited per journal style  
  - [ ] Registration present but not correctly cited  
  - [ ] Registration missing / unclear

> **INSTRUCTION:** If RCT applies, cite the RCT registry & identifier

> [SUGGESTED] This is a RCT. RCTs are reguired to be registered, the registration number be **cited** in the title page footnote.

> [SUGGESTED] Please cite the RCT wherever referenced (including title footnote).
---

## 3) IRB / ETHICS (if applicable)

- [ ] Not human subjects  
- [ ] IRB/ethics approval documented  
  - [ ] Protocol number **and** home institution included  
  - [ ] Mentioned but incomplete

> **INSTRUCTION:** If applicable and incomplete, leave **[REQUIRED] Provide full IRB details** in Suggestions.

> [REQUIRED] The data collection reported in this article seems to have required IRB approval. Please provide ethics board/IRB approval information in the titlepage footnote, including protocol number and home institution of the ethics board/IRB.

---

## 4) DATA DESCRIPTION

> **INSTRUCTION:**: If the project has any confidential or restricted data, please leave the following statement here. If not, delete it.

> [REQUIRED]  Please specify how long the data will be preserved in the restricted-access location.
  - You should describe the persistence or preservation policy of the original data provider, if known.
  - Data under your control must be preserved for at least five years following publication.

> [REQUIRED] Please provide a codebook for the data.
  - The codebook should at a minimum describe the variables obtained from the data source, in a manner that will let others verify that they have obtained a substantially similar dataset if successfully obtaining access to the data.

> **INSTRUCTION:**: For multiple data sources, copy this block and fill for each source. 

### INPUT Data Sources 
- [ ] Public in JDA
- [ ] Privately provided / restricted (not public)  
- [ ] DOI/URL works: **[paste here]**  
- [ ] Access conditions described: **[summarize]**  
- [ ] Incomplete citation or only mentioned
  - [ ] in manuscript  
  - [ ] in README  
- [ ] Data **properly** cited  
  - [ ] in manuscript  
  - [ ] in README  


### Analysis Data Files
- [ ] Not mentioned  
- [ ] Mentioned, not provided (explain)  
- [ ] Mentioned and provided (list file paths)  
- [ ] Not mentioned, but present (list file paths)

Example:
```
./Output_Empirical/data/regression_main.dta
```

> **INSTRUCTION:**: If the relevant items above are NOT checked, leave the related [REQUIRED] element here. Otherwise, delete the line.

> [REQUIRED] Please add data citations to the article. 

> [REQUIRED] Please provide a clear description of access modality and source location for this dataset. Some examples are given [on this website](https://social-science-data-editors.github.io/guidance/Requested_information_dcas.html).


---

## 5) ALL DATA FILES PROVIDED — QA 

> **INSTRUCTION:** These should be filled by the pipeline. If absent, create them manually.

- `file-paths-summary.md` — full file inventory (relative paths)  
- `duplicate-files-report.md` — hash‑based duplicates  
- `zero-byte-files-report.md` — empty files  
- `large-file-report.md` — size outliers  

---

## 6) STATED REQUIREMENTS (from authors)

- [ ] OS used: 
  - [ ] Windows 
  - [ ] macOS 
  - [ ] Linux 
  - [ ] Not specified  
- [ ] Software requirements & versions (Stata/R/Matlab/Python, packages)  
- [ ] Compute requirements (memory, runtime, storage; cluster)  
- [ ] Time requirements (e.g., ~N hours on baseline machine)  
- [ ] **Requirements are complete**
- [ ] None of the above

---
Part B
## 7) CODE DESCRIPTION (static review)

> **INSTRUCTION:** List programs; identify which create analysis files vs. outputs. Create a **cross‑walk** spreadsheet mapping each figure/table/in‑text number to the producing program/line.

| Data Preparation Program | Dataset created |             | 
|--------------------------|-----------------|-------------|
|                          |                 |             |             
|                          |                 |             |             
|                          |                 |             |             
|                          |                 |             |             
| Figure/Table #           | Program         | Line Number | 
|                          |                 |             |             
|                          |                 |             |             
|                          |                 |             |
|                          |                 |             |             
|                          |                 |             |             
| In-text numbers          | Program         | Line Number | 
      
      
- [ ] A master script exists that reproduces all outputs  
> [SUGGESTED] We strongly advise the use of a single (or a small number of) main control file(s) to automatically reproduce all figures and tables in the paper, without manual interaction.

**Common pitfalls to note here:**
- Hard‑coded absolute paths (e.g., `C:\Users\...`)  
- Missing package installs / version pins  
- Side‑effects (overwriting intermediate data)  
- Hidden manual steps (copying files, interactive prompts)

---

## 8) COMPUTING ENVIRONMENT OF THE REPLICATOR

> **INSTRUCTION:** Record precise environment used for the run: OS/CPU/RAM and exact software versions.

**Examples:**  
- macOS on Apple Silicon (M‑series), 16GB RAM; Stata/MP 18.0, R 4.x, Python 3.x  
- Linux cluster, Xeon CPUs, 128GB RAM; Matlab R2022a

**Version capture tips:**  
- **Stata:** `about` and `ssc describe` for packages; save log.  
- **R:** `sessionInfo()`; `renv::snapshot()` if used.  
- **Python:** `python --version`; `pip freeze > requirements.txt` (or `conda env export`).  
- **Matlab:** `ver` output.

---

## 9) REPLICATION STEPS (what you did)

> **INSTRUCTION:** Describe deviations from README and every error/fix, with exact error snippets. Keep full logs as attachments; link to them here. 

Example flow:
- ran `master.do` per README → step 3 failed:  
```
error: command distinct in Stata unknown
Installed missing distinct package in Stata (ssc install distinct); 
reran master.do. Step 3 now passes
```
- Fixed filename typo `superdata.dta` vs. `superdta.dta`; reran.  
- Pipeline completed; logs attached.

> [REQUIRED] Please check the fixes done by the replicator and change your code accordingly.

> [REQUIRED] Please check if your code needs to be fixed. The replicator was unable to fully run it.
---

## 10) FINDINGS

> **INSTRUCTION:** Summarize outcomes for **data prep**, **tables/figures**, and **in‑text numbers**. Use screenshots for visual comparisons. Keep the cross‑walk up to date.

### Missing Requirements (if any)
- [ ] Software (versions, packages)  
- [ ] Compute resources (RAM/disk/cluster)  
- [ ] Time requirements  

### Data Preparation Code
> e.g., `1-create-data.do` ran; `2-create-appendix-data.do` produced no output.

### Tables and Figures
> **INSTRUCTION:** Paste the cross‑walk. Describe discrepancies; add screenshot pairs where helpful.

### In‑Text Numbers
- [ ] Not verified  
- [ ] All numbers stem from tables/figures  
- [ ] Standalone in‑text numbers verified: **[list page/line context]**

> [REQUIRED] Please check discrepancies in output described in the report and consider revising the code or the paper.

---

## APPENDIX (attach or link)

- File inventory and QA reports (inventory/duplicates/zero‑byte/large/PII)  
- Table/Figure mapping spreadsheet (cross‑walk)  
- Full run logs  
- Environment details (versions, package lists)  
- Any external reproducibility report

---

## Credit and License

We would like to thank Lars Vilhuber, data editor at the American Economic Association (AEA), for his outstanding contributions to promoting reproducible research in economics and the social sciences.

This report template is also largely based on his excellent work. The latest updates can be found at https://github.com/AEADataEditor/replication-template. This template is licensed under CC-BY 4.0 (https://creativecommons.org/licenses/by/4.0/).