# Data Acquisition, Processing and Validation Overview

OMB has downloaded the publicly available AI inventories for agencies, processed and standardized them, and then combined them into consolidated files. This directory contains metadata on these combined data files in this repository's `data` directory, including a `data_dictionary` for the individual use case inventory.
 
## Metadata file descriptions: 

### `data_dictionary.md` and `data_dictionary.json`
Contains metadata for every column for the consolidated *individual* use case files (i.e. individually reported systems, both .xlsx and .csv format). For each data field, this dictionary notes the:
- **Column Name** (both the shorter column names in the .csv file and the longer column names in the .xlsx file)
- **Reporting Instructions** given to agencies
- **Data type** 
- **Valid selections** for the multiple choice fields
- **Recoding Table** for multiple choice fields, which describes how long strings were mapped to shorter strings in the .csv format of the file (for easier analyst manipulation and visualization)

### `data_sourcing_summary.md`
Contains metadata for the data origins for each agency for the *individual* use case inventories. For each agency, this file notes the:
- **Agency Name** 
- **Data Retrieval Method** and the **Date** of retrieval (datasets were automatically downloaded using scripts/scrapers if possible, but some were manually downloaded or emailed to OMB)
- **The URLs** utilized for data access 
- **Data format information**, including filetype and the row index for column names
- **Column Remapping Table**, which indicates which columns in the original data were mapped to which OMB required columns

### `data_standardization_report.md`
Contains metadata for the string remappings done for the *individual* use case inventory files for multiple choice questions. OMB has attempted to standardize the multiple choice responses from agencies to align with OMB's valid selections (for example, “None” -> “None of the above”). This metadata file documents all of these remappings. For each remapping, this file notes: 
- **Column Name**
- **Original string value** as it appeared in the agency's raw dataset
- **Remapped string value** in OMB's consolidated dataset
- **Reason for change**
- **Frequency of changes** across all agencies

### `data_standardization_report_COTS_AI.md`
Contains metadata for the string remappings done for the *consolidated AI commercial off the shelf* use case inventory files for multiple choice questions. OMB has attempted to standardize the multiple choice responses from agencies to align with OMB's valid selections (for example, “None” -> “None of the above”). This metadata file documents all of these remappings. For each remapping, this file notes: 
- **Column Name**
- **Original string value** as it appeared in the agency's raw dataset
- **Remapped string value** in OMB's consolidated dataset
- **Reason for change**
- **Frequency of changes** across all agencies
