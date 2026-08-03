# Template README and Guidance 
* (JDA Version 1.1) 

* A high-quality README file is a very important part of a reproducibility package. It is the entry point for any user and reviewer and must clearly explain the project's purpose, contents, and instructions for reproducing the findings. 
* This README template is designed to be included in reproducibility packages to provide directions for replicating the results in the research paper. The sections mentioned below should be included to guide users and reviewers through the replication process. Various journals have used the structure and content of the README in a similar form. However, authors should be aware that there are many variations and complications, and should therefore feel free to adapt the template as required.
* This is a simplified version of the [social science data editors template](https://social-science-data-editors.github.io/template_README/). For more guidance and a wide range of examples, please refer to their website.
* If you prefer writing your readme online, please use the [readme generator](https://dime-worldbank.github.io/wb-reproducible-research-repository-automation/) provided by the World Bank.

## Contents

1. [Overview](#overview)
2. [Data Availability](#data-availability)
3. [Instructions for Replicators](#instructions-for-replicators)
4. [List of Exhibits](#list-of-exhibits)
5. [Requirements](#requirements)

The rest of the contents of this README file is highly desirable, but not strictly needed for reproducibility. The points above are needed.

6. [Code Description](#code-description)
7. [Folder Structure](#folder-structure)


## Overview

Begin by offering a concise overview for the reviewers and replicators regarding the materials included in the package and provide a brief guide on how to proceed from start to finish. Ensure to include any crucial information that replicators should be aware of. In addition, the authors are asked provide a list of all files included in the replication package and document the purpose and format of each individual file (e.g., in tabular form).

## Data Availability

Every README should contain a description of the origin (provenance), location and accessibility (data availability) of the data used in the article. This is crucial, especially for replicating the results, as only the same data will be able to produce consistent results. These descriptions are generally referred to as "Data Availability Statements" (DAS).  Make sure to list all the datasets used and categorize them as follows:

* \[ ] All data are publicly available.
* \[ ] Some data cannot be made publicly available.
* \[ ] No data can be made publicly available.

### Data Sources

Provide detailed information about the data sources, whether obtained from public repositories, institutional databases, or other sources. Include instructions on how others can access the data, including where it can be downloaded and the names under which it is cataloged. This is particularly important for reviewers and replicators to ensure consistent results by using the same datasets. 
Please make sure that data files are properly documented: variables/columns should have labels (long-form meaningful names), and values should be explained. This might mean generating a codebook, pointing at a public codebook, or providing data in formats that allow for a rich description. This is in particular important for data that is not distributable.

Please also [cite](https://social-science-data-editors.github.io/guidance/Guidance/Data_citation_guide.html) all data used to obtain the results of your work in the reference list of your manuscript and at the end of the Readme file.

You can use the following as a template. Make sure to fill out this information for each of the data files used. A summary in tabular form can be useful.

- **Filename:** Exact file name as shown on the source website

- **Source:** Name of the source website

- **URL:** Exact downloadable URL of the data used

- **Access year:** Date when the data was accessed. This is especially important as data can be updated, and replicators should know the exact time when the data was downloaded.

- **Provided:** Let the replicators know if you have included that data file in the replication package (TRUE/FALSE)

- **License (optional, but recommanded):** While this is not mandatory, it is great to know under which license the data is available to understand if it is public or private, or publication limitations. 

### Statement about Rights

* \[ ] I certify that the author(s) of the manuscript have legitimate access to and permission to use the data used in this manuscript.
* \[ ] I certify that the author(s) of the manuscript have documented permission to redistribute/publish the data contained within this replication package. Appropriate permission are documented in the LICENSE.txt file (if applicable).

## Instructions for Replicators

New users should follow these steps to run the package successfully:

* Users must first have access to all data files if they are not included in the reproducibility package. They should go to the mentioned links, download the listed files, and place them in the data folder.
* Update the following files with your directory paths

  * `main\_dofile.do`
* Ensure all required software and dependencies are installed as listed in the [Requirements](#requirements) section.
* Run the `main\_dofile.do` file.

Please adapt this example for non-STATA formats and programs.

## List of Exhibits

Clearly identify and document the tables and figures as they appear in the manuscript by their corresponding numbers. If file names do not correspond to exhibit numbers, provide detailed explanations.

If not all data is provided in the reproducibility package, as described in the data section, then the list of tables should clearly indicate which tables, figures, and in-text numbers can be reproduced with the public material provided.

Example template for exhibit identification:

The provided code reproduces:

* \[ ] All numbers provided in text in the paper
* \[ ] All tables and figures in the paper
* \[ ] Selected tables and figures in the paper, as explained and justified below

|Exhibit name|Output filename|Script|Note|
|-|-|-|-|
|Table 1|Balancetable.xls|02\_analysis.do (line 23)|Found in Outputs/tables/main|
|Figure 1|Regresults.png|02\_analysis.do (line 40)|Found in Outputs/figures/annex, Image Format: Portable Network Graphic (PNG)|

## Requirements

### Computational Requirements

In this section, specify operating system requirements, software dependencies, environment setup instructions, and any other relevant information essential for replicating the results. Each of these factors plays an important role in ensuring successful replication.

### Software Requirements

List all software requirements, including versions, dependencies, libraries, environment setup, and packages installed. Using different versions of the same software could lead to variations in results. If multiple software are used, include details for all.
In case of controlled randomness please also specify in which line of which program the random seed is set.

Example:

* **Stata version 15**

  * estout
  * rdrobust
* **Python 3.6.4**

  * pandas 0.24.2
  * numpy 1.16.4

### Memory and Runtime and Storage Requirements

Provide consistent information about memory resources for reliable computation. Include runtime information for replicators to assess processing times and detect potential issues with the code. It would be best to describe how much storage is required in addition to the space visible in the typical repository, for instance, because data will be unzipped, data downloaded, or temporary files written.

## Code Description

Give an overview of the program files and their purposes. For example, `main.do` sets file paths, installs necessary ADO packages, and executes all other dofiles. Meanwhile, `cleaning.do` loads data, handles missing values, and `analysis.do` performs basic statistical analysis and generate visualizations. Please remove redundant or obsolete files from the replication package.

Make sure to also include any crucial information that replicators should be aware of to facilitate a one-click run of the code.

## Folder Structure

Details about folder structure are crucial because a well-organized layout enables replicators to navigate quickly to the desired files or directories without searching through cluttered or disorganized folders. Include only the files necessary for replication and delete any unnecessary files.

An ideal folder structure for a reproducibility package should look something like this:

```
Data
  ├── Raw
  └── Cleaned
Code
  ├── Main\_dofile.do
  ├── 01\_cleaning.do
  ├── 02\_analysis.do
  └── 03\_.....do
Outputs
  ├── Main
  │   ├── Tables
  │   └── Figures
  └── Annex
      ├── Tables
      └── Manuscript
```

## References
Please provice a full list of references here - [examples: how to cite data](https://social-science-data-editors.github.io/guidance/Guidance/Data_citation_guide.html) 

## Credit and License
* This template is a modified version of the the readme-template provided by the world bank (https://github.com/worldbank/wb-reproducible-research-repository/blob/main/resources/README_Template.md) and the social science data editors [SSDE](Lars Vilhuber, Miklós Koren, Joan Llull, Marie Connolly and Peter Morrow (2022): A template README for social science replication packages. DOI: 10.5281/zenodo.7293838, latest version is availabale from https://github.com/social-science-data-editors/template_README/blob/releases/README.md). 
We would like to thank these initiatives for their exceptional contributions to developing a practical README template and improving the reproducibility of economic research. The SSDE template is available under a CC-BY-NC 4.0 International license (https://creativecommons.org/licenses/by/4.0/). This adaption follows their license conditions and is also availabale under the same CC-BY-NC 4.0 license. 


