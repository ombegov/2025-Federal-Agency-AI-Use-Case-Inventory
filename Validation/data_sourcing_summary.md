## Metadata for Agency AI Inventory Data Sources

Details the following:

- URL for data downloaded from each agency, download method, data format, and download date

- Column remappings from original file to standardized column names, whether the columns were empty, or whether the columns dropped

- Number of rows for each agency

- Additional context / notes on why response fields may be left blank or why automatical data-scraping was not feasible/effective

To see a mapping between the Shorthand Column Name in the table below and the original excel headers in OMB's reporting template, please refer to the data dictionary Markdown file.

**Note**: Most of the column remappings account for agencies changing the column names from the original OMB reporting template. A few agencies, however, did not follow the 2025 reporting formats. In order to try and include more information in the consolidated inventory for these agencies, some free text columns were remapped even though they don't correspond perfectly to a template column (i.e., "Summary of the AI Use Case" might be remapped to the "Describe the benefits of the AI system" column even though those are slightly different questions). Additional detail on this mapping is provided in the Data Standardization Report.

**Additional Note**: Not every question had to be answered for every use case. For example, the last 9 questions about risk management practices were only required for "High-Impact" AND "Deployed" use cases. Additionally, some agencies have chosen to withhold particular use case details, in line with OMB guidance, which states, "Agencies are permitted to remove any use case from their public inventory whose sharing would be inconsistent with applicable law and governmentwide policy, such as the exemptions from public disclosure provided in 5 U.S.C. § 552. Where particular details of a use case cannot be shared or released publicly, agencies must only exclude those details, while including any fields that can be shared or released. The fact that a use case is not public-facing is not an adequate justification for withholding it from public sharing, nor is a desire to conceal inefficiency, violations of law, or administrative error, or to prevent embarrassment to an organization or agency. In their public inventories, agencies may also remove the “Use Case ID” column, and replace the 'Email Address' column with an email address designated for public inquiries.” Empty columns may appear for either or both of those reasons.

### Department of Agriculture (USDA)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.usda.gov/sites/default/files/documents/usda-ai-use-case-inventory.csv
- **Download link page:** https://www.usda.gov/ai/inventory

- **Number of detected use cases / rows:** **162**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be publicly disclosed as an open government data asset, prov...' | **link_to_data** |  |  |
| 'Does this AI use case involve personally identifiable information (PII) that is maintai...' | **has_pii** |  |  |
| 'If publicly available, provide the link to the AI use case’s associated Privacy Impact ...' | **pia_url** |  |  |
| 'Which, if any, demographic variables does the AI use case explicitly use as model featu...' | **demographic_features** |  |  |
| 'Does this project include custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the publicly available source code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI use case?' | **hi_testing_conducted** | Yes - Mapped to: 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complete AI Impact Assessment' |  |
| 'Has an AI impact assessment been completed for this AI use case?' | **hi_assessment_completed** | Yes - Mapped to: 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete AI Impact Assessment' |  |
| 'What are the potential impacts of using the AI for this particular use case and how wer...' | **hi_potential_impacts** | Yes - Mapped to: 'What are the potential  impacts of using the AI for  this particular use case and  how were they identified?        Subpractice: Complete AI  Impact Assessment' |  |
| 'Has an independent review of the AI use case been conducted?' | **hi_independent_review** | Yes - Mapped to: 'Has as independent review  of the AI use case been  conducted?         Sub practice Complete AI  Impact Assessment' |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** | Yes - Mapped to: 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the performance and security of the AI functionality, as well as to privacy, civil rights, and civil liberties?  Practice: Conduct Ongoing Monitoring for Performance and Potential Adverse Impacts' |  |
| 'Has the agency established sufficient and periodic training for operators of the AI to ...' | **hi_training_established** | Yes - Mapped to: 'Has the agency established sufficient and periodic  training for operators of the  AI to interpret and act on the  its output and managed associated risks?   Practice: Ensure Adequate Human Training and Assessment' |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** | Yes - Mapped to: 'Does this AI use case have an appropriate fail-safe that minimizes the risk of significant harm?      Practice: Provide Additional Human Oversight, Intervention, and Accountability' |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** | Yes - Mapped to: 'Is there an established appeal process in the event that an impacted individual would like to appeal or  contest the AI system’s  outcome?   Practice: Offer Consistent Remedies or Appeals' |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** | Yes - Mapped to: 'What steps has the agency taken to consult and incorporate feedback from end users of this AI use case and the public?     Practice: Consult and Incorporate Feedback from End Users and the Public' |  |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
### Department of Commerce (DOC)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.commerce.gov/sites/default/files/2026-01/Artificial-Intelligence-Use-Case-Inventory-FY25.xlsx
- **Download link page:** https://www.commerce.gov/about/policies/artificial-intelligence-use-cases-inventory

- **Number of detected use cases / rows:** **223**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Agency' |  |  |  |
| 'Bureau' | **agency_bureau** | Yes - Mapped to: 'Bureau/Component' |  |
| 'Contact Email Address' | **contact_email** | Yes - Mapped to: 'Email Address' |  |
| 'Description' | **problem_solved** | Yes - Mapped to: 'What problem is the AI intended to solve?' |  |
| - | **is_withheld** |  | Yes |
| - | **development_stage** |  | Yes |
| - | **is_high_impact** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **topic_area** |  | Yes |
| - | **classification** |  | Yes |
| - | **benefits** |  | Yes |
| - | **system_outputs** |  | Yes |
| - | **operational_date** |  | Yes |
| - | **contracting_usage** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **link_to_data** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **has_custom_code** |  | Yes |
| - | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Department of Education (ED)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Data was contained in a zip file - manually downloaded the data and extracted it for convenience instead of writing scripting logic to extract this file.
- **URL for download:** https://www.ed.gov/sites/ed/files/2024-09/GenAI%20use%20cases%20for%20AI%20Inventory_0.zip
- **Download link page:** https://www.ed.gov/about/ed-overview/artificial-intelligence-ai-guidance

- **Number of detected use cases / rows:** **56**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Program Office' | **agency_bureau** | Yes - Mapped to: 'Bureau/Component' |  |
| 'Office Function' | **problem_solved** | Yes - Mapped to: 'What problem is the AI intended to solve?' |  |
| 'Use Case' | **use_case_name** | Yes - Mapped to: 'Use Case Name' |  |
| 'Description' | **benefits** | Yes - Mapped to: 'What are the expected benefits and positive outcomes from the AI for an agency’s mission and/or the general public?' |  |
| - | **id** |  | Yes |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
| - | **development_stage** |  | Yes |
| - | **is_high_impact** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **topic_area** |  | Yes |
| - | **classification** |  | Yes |
| - | **system_outputs** |  | Yes |
| - | **operational_date** |  | Yes |
| - | **contracting_usage** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **link_to_data** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **has_custom_code** |  | Yes |
| - | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Department of Energy (DOE)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.energy.gov/sites/default/files/2026-01/DOE%202025%20AI%20Use%20Case%20Inventory_PublicReporting.xlsx
- **Download link page:** https://www.energy.gov/cet/doe-ai-use-case-inventory

- **Number of detected use cases / rows:** **340**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
| - | **contact_email** |  | Yes |
### Department of Health and Human Services (HHS)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.hhs.gov/sites/default/files/hhs-ai-use-case-inventory-fy25.csv
- **Download link page:** https://www.hhs.gov/programs/topic-sites/ai/use-cases/index.html

- **Number of detected use cases / rows:** **447**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
| - | **id** |  | Yes |
### Department of Homeland Security (DHS)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.dhs.gov/sites/default/files/2026-01/2025_0128_ocio-dhs-ai-use-case-inventory.xlsx
- **Download link page:** https://www.dhs.gov/publication/ai-use-case-inventory-library

- **Number of detected use cases / rows:** **238**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
| - | **is_withheld** |  | Yes |
### Department of Housing and Urban Development (HUD)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - the scraping attempt continuously timed out. Navigating to the link manually raised the error that the server IP address could not be found. When link was accessed via https://www.hud.gov/ai, however, download was successful.
- **URL for download:** https://mgmt.hud.gov/sites/default/files/Main/documents/HUD-2025-AI-Use-Case-Inventory.xlsx
- **Download link page:** https://www.hud.gov/ai

- **Number of detected use cases / rows:** **11**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
| - | **contact_email** |  | Yes |
### Department of Justice (DOJ)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.justice.gov/media/1426076/dl?inline
- **Download link page:** https://www.justice.gov/ai/ai-inventory

- **Number of detected use cases / rows:** **314**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### Department of Labor (DOL)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.dol.gov/sites/dolgov/files/general/ai/AI_Use_Cases_Public_reporting-20260403.csv
- **Download link page:** https://www.dol.gov/agencies/oasam/centers-offices/ocio/ai-inventory

- **Number of detected use cases / rows:** **41**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### Department of State (STATE)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.state.gov/wp-content/uploads/2026/01/Tab-1-2025-AI-Use-Case-Inventory-Reporting-DOS.csv
- **Download link page:** https://www.state.gov/artificial-intelligence/

- **Number of detected use cases / rows:** **60**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?   Practice: Complete A...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?   Practice: Complete A...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?      Sub practice Comple...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
| - | **id** |  | Yes |
### Department of the Interior (DOI)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.doi.gov/sites/default/files/data/2025doigovfinalindividual2025aiusecaseinventory.csv
- **Download link page:** https://www.doi.gov/ai/use-case-inventory

- **Number of detected use cases / rows:** **247**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### Department of the Treasury (TREAS)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://home.treasury.gov/system/files/136/Treasury-AI-Use-Case-Inventory.csv
- **Download link page:** https://home.treasury.gov/policy-issues/financial-markets-financial-institutions-and-fiscal-service/treasury-and-artificial-intelligence

- **Number of detected use cases / rows:** **129**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  | Yes |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?' | **hi_testing_conducted** | Yes - Mapped to: 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complete AI Impact Assessment' |  |
| 'Has an AI impact assessment been completed for this AI use case?' | **hi_assessment_completed** | Yes - Mapped to: 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete AI Impact Assessment' |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** | Yes - Mapped to: 'What are the potential  impacts of using the AI for  this particular use case and  how were they identified?        Subpractice: Complete AI  Impact Assessment' |  |
| 'Has as independent review  of the AI use case been  conducted?' | **hi_independent_review** | Yes - Mapped to: 'Has as independent review  of the AI use case been  conducted?         Sub practice Complete AI  Impact Assessment' |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** | Yes - Mapped to: 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the performance and security of the AI functionality, as well as to privacy, civil rights, and civil liberties?  Practice: Conduct Ongoing Monitoring for Performance and Potential Adverse Impacts' |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** | Yes - Mapped to: 'Has the agency established sufficient and periodic  training for operators of the  AI to interpret and act on the  its output and managed associated risks?   Practice: Ensure Adequate Human Training and Assessment' |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** | Yes - Mapped to: 'Does this AI use case have an appropriate fail-safe that minimizes the risk of significant harm?      Practice: Provide Additional Human Oversight, Intervention, and Accountability' |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** | Yes - Mapped to: 'Is there an established appeal process in the event that an impacted individual would like to appeal or  contest the AI system’s  outcome?   Practice: Offer Consistent Remedies or Appeals' |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** | Yes - Mapped to: 'What steps has the agency taken to consult and incorporate feedback from end users of this AI use case and the public?     Practice: Consult and Incorporate Feedback from End Users and the Public' |  |
### Department of Transportation (DOT)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://data.transportation.gov/api/views/anj8-k6f5/rows.csv?accessType=DOWNLOAD
- **Download link page:** https://catalog-beta.data.gov/dataset/department-of-transportation-inventory-of-artificial-intelligence-use-cases

- **Number of detected use cases / rows:** **70**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case Identifier' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Agency' |  |  |  |
| 'Bureau' | **agency_bureau** | Yes - Mapped to: 'Bureau/Component' |  |
| 'Email Address' | **contact_email** |  |  |
| 'Public Reporting Indicator' | **is_withheld** | Yes - Mapped to: 'Should this AI use case be withheld from public reporting?' |  |
| 'Development Stage' | **development_stage** | Yes - Mapped to: 'Stage of Development' |  |
| 'High Impact Indicator' | **is_high_impact** | Yes - Mapped to: 'Is the AI use case high-impact?' |  |
| 'High Impact Justification' | **HI_justification** | Yes - Mapped to: 'Justification' | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'Problem Description' | **problem_solved** | Yes - Mapped to: 'What problem is the AI intended to solve?' |  |
| 'Benefit Description' | **benefits** | Yes - Mapped to: 'What are the expected benefits and positive outcomes from the AI for an agency’s mission and/or the general public?' |  |
| 'Output Description' | **system_outputs** | Yes - Mapped to: 'Describe the AI system’s outputs.' |  |
| 'Operation Date' | **operational_date** | Yes - Mapped to: 'Date when AI use case became operational or the pilot’s start date' |  |
| 'Contractor Indicator' | **contracting_usage** | Yes - Mapped to: 'Was the system involved in this use case purchased from a vendor or developed under contract(s) or in-house?' |  |
| 'Vendor Name' | **vendor_name** | Yes - Mapped to: 'Vendor(s) Name' |  |
| 'ATO Indicator' | **have_ato** | Yes - Mapped to: 'Does this AI use case have an associated Authorization to Operate (ATO)?' |  |
| 'System Name' | **system_name_ato** | Yes - Mapped to: 'System(s) Name' | Yes |
| 'Training Data Description' | **data_description** | Yes - Mapped to: 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model(s) used in this use  case.' |  |
| 'Enterprise Data Inventory URL' | **link_to_data** | Yes - Mapped to: 'If the data is required to be  publicly disclosed as an  open government data asset,  provide a link to the entry on the Federal Data Catalog.' | Yes |
| 'PII Indicator' | **has_pii** | Yes - Mapped to: 'Does this AI use case  involve personally  identifiable information (PII)  that is maintained by the  agency?' | Yes |
| 'PIA URL' | **pia_url** | Yes - Mapped to: 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact Assessment (PIA).' |  |
| 'Demographic Variable Description' | **demographic_features** | Yes - Mapped to: 'Which, if any, demographic  variables does the AI use  case explicitly use as model  features?' | Yes |
| 'Custom Code Indicator' | **has_custom_code** | Yes - Mapped to: 'Does this project include  custom-developed code?' |  |
| 'Open Source Code URL' | **code_url** | Yes - Mapped to: 'If the code is open source, provide the link for the  publicly available source  code.' | Yes |
| 'Predeployment Testing Indicator' | **hi_testing_conducted** | Yes - Mapped to: 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complete AI Impact Assessment' | Yes |
| 'AI Impact Assessment Indicator' | **hi_assessment_completed** | Yes - Mapped to: 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete AI Impact Assessment' | Yes |
| 'Potential Impact Description' | **hi_potential_impacts** | Yes - Mapped to: 'What are the potential  impacts of using the AI for  this particular use case and  how were they identified?        Subpractice: Complete AI  Impact Assessment' | Yes |
| 'Independent Review Indicator' | **hi_independent_review** | Yes - Mapped to: 'Has as independent review  of the AI use case been  conducted?         Sub practice Complete AI  Impact Assessment' | Yes |
| 'Ongoing Monitoring Indicator' | **hi_ongoing_monitoring** | Yes - Mapped to: 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the performance and security of the AI functionality, as well as to privacy, civil rights, and civil liberties?  Practice: Conduct Ongoing Monitoring for Performance and Potential Adverse Impacts' | Yes |
| 'Operator Training Indicator' | **hi_training_established** | Yes - Mapped to: 'Has the agency established sufficient and periodic  training for operators of the  AI to interpret and act on the  its output and managed associated risks?   Practice: Ensure Adequate Human Training and Assessment' | Yes |
| 'Fail Safe Indicator' | **hi_failsafe_presence** | Yes - Mapped to: 'Does this AI use case have an appropriate fail-safe that minimizes the risk of significant harm?      Practice: Provide Additional Human Oversight, Intervention, and Accountability' | Yes |
| 'Appeal Process Indicator' | **hi_appeal_process** | Yes - Mapped to: 'Is there an established appeal process in the event that an impacted individual would like to appeal or  contest the AI system’s  outcome?   Practice: Offer Consistent Remedies or Appeals' | Yes |
| 'End User Feedback Description' | **hi_public_consultation** | Yes - Mapped to: 'What steps has the agency taken to consult and incorporate feedback from end users of this AI use case and the public?     Practice: Consult and Incorporate Feedback from End Users and the Public' | Yes |
### Department of Veterans Affairs (VA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://department.va.gov/ai/wp-content/uploads/sites/26/2026/01/VA-AI-Use-Case-Inventory-2025-Web.xlsx
- **Download link page:** https://department.va.gov/ai/ai-use-case-inventory/

- **Number of detected use cases / rows:** **367**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'VA Admin or Staff Office' | **agency_bureau** | Yes - Mapped to: 'Bureau/Component' |  |
| 'Development Stage' | **development_stage** | Yes - Mapped to: 'Stage of Development' |  |
| 'High-Impact Status' | **is_high_impact** | Yes - Mapped to: 'Is the AI use case high-impact?' |  |
| 'Problem to be Solved' | **problem_solved** | Yes - Mapped to: 'What problem is the AI intended to solve?' |  |
| 'Expected Benefits' | **benefits** | Yes - Mapped to: 'What are the expected benefits and positive outcomes from the AI for an agency’s mission and/or the general public?' |  |
| 'AI System Outputs' | **system_outputs** | Yes - Mapped to: 'Describe the AI system’s outputs.' |  |
| 'AI Tech Classification' | **classification** | Yes - Mapped to: 'AI Classification' |  |
| 'Topic Area' | **topic_area** | Yes - Mapped to: 'Use Case Topic Area' |  |
| 'Custom-Developed Code?' | **has_custom_code** | Yes - Mapped to: 'Does this project include  custom-developed code?' |  |
| 'Development Type' | **contracting_usage** | Yes - Mapped to: 'Was the system involved in this use case purchased from a vendor or developed under contract(s) or in-house?' |  |
| 'Federal Data Catalog Link' | **link_to_data** | Yes - Mapped to: 'If the data is required to be  publicly disclosed as an  open government data asset,  provide a link to the entry on the Federal Data Catalog.' |  |
| 'Public Open Source Link' | **code_url** | Yes - Mapped to: 'If the code is open source, provide the link for the  publicly available source  code.' |  |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **operational_date** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Environmental Protection Agency (EPA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.epa.gov/system/files/documents/2026-01/epas-2025-ai-use-cases-all-use-cases.xlsx
- **Download link page:** https://www.epa.gov/data/ai-use-case-inventory

- **Number of detected use cases / rows:** **29**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### General Services Administration (GSA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.gsa.gov/system/files/GSA-AI-use-case-inventory-2025.csv
- **Download link page:** https://www.gsa.gov/technology/government-it-initiatives/artificial-intelligence/2025-gsa-ai-use-case-inventory

- **Number of detected use cases / rows:** **49**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case Name' | **use_case_name** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| - | **id** |  | Yes |
| - | **agency_bureau** |  | Yes |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
| - | **is_high_impact** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **benefits** |  | Yes |
| - | **system_outputs** |  | Yes |
| - | **operational_date** |  | Yes |
| - | **contracting_usage** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **link_to_data** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **has_custom_code** |  | Yes |
| - | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### National Aeronautics and Space Administration (NASA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.nasa.gov/wp-content/uploads/2026/01/grid-6036111-data.xlsx?emrc=2a4257
- **Download link page:** https://www.nasa.gov/ai-inventory/

- **Number of detected use cases / rows:** **425**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  | Yes |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### National Science Foundation (NSF)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://nsf-gov-resources.nsf.gov/files/NSF-EO13960-AI-Use-Case-Inventory.xlsx
- **Download link page:** https://www.nsf.gov/policies/ai 

- **Number of detected use cases / rows:** **17**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Agency' |  |  |  |
| 'Bureau / Department' | **agency_bureau** | Yes - Mapped to: 'Bureau/Component' |  |
| 'Summary of Use Case' | **problem_solved** | Yes - Mapped to: 'What problem is the AI intended to solve?' |  |
| 'Stage of System Development Life Cycle' | **development_stage** | Yes - Mapped to: 'Stage of Development' |  |
| 'Date Implemented' | **operational_date** | Yes - Mapped to: 'Date when AI use case became operational or the pilot’s start date' |  |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
| - | **is_high_impact** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **topic_area** |  | Yes |
| - | **classification** |  | Yes |
| - | **benefits** |  | Yes |
| - | **system_outputs** |  | Yes |
| - | **contracting_usage** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **link_to_data** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **has_custom_code** |  | Yes |
| - | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Nuclear Regulatory Commission (NRC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.nrc.gov/sites/default/files/data/ai-inventory.csv
- **Download link page:** https://www.nrc.gov/ai/internally-focused

- **Number of detected use cases / rows:** **4**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Office of Personnel Management (OPM)

**No Individual Use Cases to Report**

**Reason**: Agency's website seems to only contain consolidated use cases

**Associated URLs**:
- https://www.opm.gov/ai/
### Small Business Administration (SBA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.sba.gov/sites/default/files/2026-03/SBA%202025%20AI%20Use%20Case%20Inventory_0.xlsx
- **Download link page:** https://www.sba.gov/about-sba/open-government/ai-inventory

- **Number of detected use cases / rows:** **34**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### Social Security Administration (SSA)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.ssa.gov/sites/g/files/npxnvu131/files/2026-01/SSA-Individual-AI-Inventory-2025.csv
- **Download link page:** https://www.ssa.gov/ai

- **Number of detected use cases / rows:** **33**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** | Yes - Mapped to: 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the performance and security of the AI functionality, as well as to privacy, civil rights, and civil liberties?  Practice: Conduct Ongoing Monitoring for Performance and Potential Adverse Impacts' |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
| - | **id** |  | Yes |
| - | **contact_email** |  | Yes |
### Committee for Purchase From People Who Are Blind or Severely Disabled (CPPBSD)

**No Individual Use Cases to Report**

**Reason**: Agency stated that there were no individual use cases to report

**Associated URLs**:
- https://www.abilityone.gov/ai.html
### Commodity Futures Trading Commission (CFTC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.cftc.gov/sites/default/files/2026-01/CFTC2026-AIusecaseinventory.csv
- **Download link page:** https://www.cftc.gov/ai

- **Number of detected use cases / rows:** **3**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau' | **agency_bureau** | Yes - Mapped to: 'Bureau/Component' |  |
| 'What is the intended purpose and expected benefits of the AI?' | **problem_solved** | Yes - Mapped to: 'What problem is the AI intended to solve?' |  |
| 'Stage of Development' | **development_stage** |  |  |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
| - | **is_high_impact** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **topic_area** |  | Yes |
| - | **classification** |  | Yes |
| - | **benefits** |  | Yes |
| - | **system_outputs** |  | Yes |
| - | **operational_date** |  | Yes |
| - | **contracting_usage** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **link_to_data** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **has_custom_code** |  | Yes |
| - | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Consumer Financial Protection Bureau (CFPB)

**No Individual Use Cases to Report**

**Reason**: Agency stated that there were no individual use cases to report

**Associated URLs**:
- https://www.consumerfinance.gov/ai/
### Department of Veterans Affairs Office of Inspector General (VAOIG)

**No Individual Use Cases to Report**

**Reason**: Agency only has consolidated use cases to report.

**Associated URLs**:
- https://vaoig.gov/ai
### Election Assistance Commission (EAC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.eac.gov/sites/default/files/2026-01/EAC_AI_Use_Case_Inventory_1.28.26.xlsx
- **Download link page:** https://www.eac.gov/AI

- **Number of detected use cases / rows:** **4**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### Equal Employment Opportunity Commission (EEOC)

**Data Not Available**

**Reason**: No webpage found for https://www.eeoc.gov/ai

### Export-Import Bank of the United States (EXIM)

**No Individual Use Cases to Report**

**Reason**: Agency stated that there were no individual use cases to report

**Associated URLs**:
- https://exim.gov/ai-inventory
### Farm Credit Administration (FCA)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/17/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.fca.gov/template-fca/notices/FCA_detailed_use_case_inventory_OMB_2025.xlsx
- **Download link page:** https://www.fca.gov/required-notices/fcas-use-of-artificial-intelligence

- **Number of detected use cases / rows:** **3**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  | Yes |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  | Yes |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  | Yes |
| 'Vendor(s) Name' | **vendor_name** |  | Yes |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  | Yes |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  | Yes |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  | Yes |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  | Yes |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  | Yes |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Federal Communications Commission (FCC)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/18/2026
- **Notes on Data Access:** Attempt to download data via Python script using the Requests library and inventory URL was unsuccessful - either the scraping attempt was blocked, the request timed out, or there was some other issue. Instead, dataset was downloaded manually by navigating to the download URL in a web browser.
- **URL for download:** https://www.fcc.gov/sites/default/files/fcc-ai-use-cases-full-nnventory.xlsx
- **Download link page:** https://www.fcc.gov/ai

- **Number of detected use cases / rows:** **6**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Federal Deposit Insurance Corporation (FDIC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.fdic.gov/fdic-2025-individual-ai-use-case-inventory-csv-version.csv
- **Download link page:** https://www.fdic.gov/ai

- **Number of detected use cases / rows:** **50**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  |  |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Federal Energy Regulatory Commission (FERC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.ferc.gov/sites/default/files/2026-01/grid_6035838_data%20FERC%202025%20AI%20Use%20Case%20Inventory.xlsx
- **Download link page:** https://www.ferc.gov/media/ai-use-case-inventory

- **Number of detected use cases / rows:** **6**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  |  |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  |  |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  |  |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  |  |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  |  |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  |  |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  |  |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  |  |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  |  |
### Federal Housing Finance Agency (FHFA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.fhfa.gov/document/fhfa_2025_ai_inventory.xlsx
- **Download link page:** https://www.fhfa.gov/data/artificial-intelligence-use-case-inventory

- **Number of detected use cases / rows:** **16**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Federal Maritime Commission (FMC)

**No Individual Use Cases to Report**

**Reason**: Agency has no use cases to report.

**Associated URLs**:
- https://www.fmc.gov/about/strategies-budgets-and-performance/artificial-intelligence-ai/
### Federal Reserve Board (FRB)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.federalreserve.gov/files/frb-2025-ai-use-case-inventory.xlsx
- **Download link page:** https://www.federalreserve.gov/AI-use-case-inventory.htm

- **Number of detected use cases / rows:** **38**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Agency' |  |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Provide a justification for why the use case is determined to be not high impact.' | **HI_justification** | Yes - Mapped to: 'Justification' | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system's outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date.' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to train, fine-tune, and/or evaluate performance of the model(s)...' | **data_description** |  |  |
| 'If the data is required to be publicly disclosed as an open government data asset, prov...' | **link_to_data** |  | Yes |
| 'Does this AI use case involve personally identifiable information (PII) that is maintai...' | **has_pii** |  |  |
| 'If publicly available, provide the link to the AI use case’s associated Privacy Impact ...' | **pia_url** |  |  |
| 'Which, if any, demographic variables does the AI use case explicitly use as model featu...' | **demographic_features** |  |  |
| 'Does this project include custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the publicly available source code.' | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Federal Retirement Thrift Investment Board (FRTIB)

**Data Not Available**

**Reason**: Inventory was not in excel/csv format, and only two use cases were posted with a single field on https://www.frtib.gov/data/ai_inventory/

**Associated URLs**:
- https://www.frtib.gov/data/ai_inventory/
### Federal Trade Commission (FTC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.ftc.gov/system/files/ftc_gov/data/2025%20Agency%20AI%20Use%20Case%20FTC%20public%20release%20csv.csv
- **Download link page:** https://www.ftc.gov/ai

- **Number of detected use cases / rows:** **16**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for the agency's missi...' | **benefits** |  |  |
| 'Describe the AI systemís outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilotís start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  | Yes |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use caseís associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  | Yes |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Morris K. Udall and Stewart L. Udall Foundation (UDALL)

**No Individual Use Cases to Report**

**Reason**: Agency stated that there were no individual use cases to report

**Associated URLs**:
- https://udall.gov/ai
### National Archives and Records Administration (NARA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.archives.gov/files/AI/nara-2025-ai-use-case-inventory-final-01-28-2026.xlsx
- **Download link page:** https://www.archives.gov/ai

- **Number of detected use cases / rows:** **14**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  |  |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### National Credit Union Administration (NCUA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://ncua.gov/files/artificial-intelligence/individual-ncua-ai-use-case-inventory.xlsx
- **Download link page:** https://ncua.gov/ai

- **Number of detected use cases / rows:** **6**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### National Endowment for the Arts (NEA)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.arts.gov/sites/default/files/nea_ai_use_case_inventory.xlsx
- **Download link page:** https://www.arts.gov/ai

- **Number of detected use cases / rows:** **4**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  | Yes |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  | Yes |
| 'Vendor(s) Name' | **vendor_name** |  | Yes |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  | Yes |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  | Yes |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  | Yes |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  | Yes |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  | Yes |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### National Endowment for the Humanities (NEH)

**No Individual Use Cases to Report**

**Reason**: Agency only has consolidated use cases to report.

**Associated URLs**:
- https://www.neh.gov/ai-notice
### National Indian Gaming Commission (NIGC)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 4/13/2026
- **Notes on Data Access:** Data was only available via PDF - OMB manually copy and pasted values into a .csv file.
- **URL for download:** https://www.nigc.gov/?wpdmdl=13893&ind=13894
- **Download link page:** https://www.nigc.gov/nigc-and-artificial-intelligence/

- **Number of detected use cases / rows:** **5**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  | Yes |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  | Yes |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### National Transportation Safety Board (NTSB)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.ntsb.gov/Documents/NTSB%20Specific%20AI%20Use%20Cases.csv
- **Download link page:** https://www.ntsb.gov/Pages/data.aspx

- **Number of detected use cases / rows:** **4**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Occupational Safety and Health Review Commission (OSHRC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.oshrc.gov/wp-content/uploads/Individually-Reported-AI-Use-Cases%5ERevised-01-12-2026.csv
- **Download link page:** https://www.oshrc.gov/ai/

- **Number of detected use cases / rows:** **1**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Office of Special Counsel (OSC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.osc.gov/~assets/docs/osc-2025-individual-ai-use-cases.xlsx
- **Download link page:** https://www.osc.gov/resources/ai/

- **Number of detected use cases / rows:** **1**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  | Yes |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Pension Benefit Guaranty Corporation (PBGC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.pbgc.gov/sites/default/files/documents/pbgc-individual-reported-ai-use-cases.csv
- **Download link page:** https://www.pbgc.gov/about/information-technology/artificial-intelligence

- **Number of detected use cases / rows:** **17**
- **Data Type:** CSV
- **Row Index for Column Names:** Row 1

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID' | **id** | Yes - Mapped to: 'Use Case ID  \[Agency Abbrev.\] – \[#\]' |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'Expected Benefit' | **benefits** | Yes - Mapped to: 'What are the expected benefits and positive outcomes from the AI for an agency’s mission and/or the general public?' |  |
| - | **contact_email** |  | Yes |
| - | **is_withheld** |  | Yes |
| - | **is_high_impact** |  | Yes |
| - | **HI_justification** |  | Yes |
| - | **system_outputs** |  | Yes |
| - | **operational_date** |  | Yes |
| - | **contracting_usage** |  | Yes |
| - | **vendor_name** |  | Yes |
| - | **have_ato** |  | Yes |
| - | **system_name_ato** |  | Yes |
| - | **data_description** |  | Yes |
| - | **link_to_data** |  | Yes |
| - | **has_pii** |  | Yes |
| - | **pia_url** |  | Yes |
| - | **demographic_features** |  | Yes |
| - | **has_custom_code** |  | Yes |
| - | **code_url** |  | Yes |
| - | **hi_testing_conducted** |  | Yes |
| - | **hi_assessment_completed** |  | Yes |
| - | **hi_potential_impacts** |  | Yes |
| - | **hi_independent_review** |  | Yes |
| - | **hi_ongoing_monitoring** |  | Yes |
| - | **hi_training_established** |  | Yes |
| - | **hi_failsafe_presence** |  | Yes |
| - | **hi_appeal_process** |  | Yes |
| - | **hi_public_consultation** |  | Yes |
### Securities and Exchange Commission (SEC)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.sec.gov/files/2025-sec-individual-ai-use-cases.csv
- **Download link page:** https://www.sec.gov/ai

- **Number of detected use cases / rows:** **60**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  |  |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  |  |
| 'Vendor(s) Name' | **vendor_name** |  |  |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  |  |
| 'System(s) Name' | **system_name_ato** |  |  |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  |  |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  |  |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  |  |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  |  |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  |  |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Surface Transportation Board (STB)

- **Data Retrieval Method:** Automated Download via URL on 4/13/2026 10:32am
- **URL for download:** https://www.stb.gov/wp-content/uploads/STB_-AI_Use_Cases_Public_CSV.csv
- **Download link page:** https://www.stb.gov/ai/

- **Number of detected use cases / rows:** **2**
- **Data Type:** CSV
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  |  |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  |  |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  |  |
| 'Is the AI use case high-impact?' | **is_high_impact** |  |  |
| 'Justification' | **HI_justification** |  |  |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  |  |
| 'What problem is the AI intended to solve?' | **problem_solved** |  |  |
| 'What are the expected benefits and positive outcomes from the AI for an agency’s missio...' | **benefits** |  |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  |  |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  | Yes |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  | Yes |
| 'Vendor(s) Name' | **vendor_name** |  | Yes |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  | Yes |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  | Yes |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  | Yes |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  | Yes |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  | Yes |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### Tennessee Valley Authority (TVA)

- **Data Retrieval Method:** Manual Data Download via URL or Manual Compilation on 2/11/2026
- **Notes on Data Access:** Inventory data was not available in a csv or excel format - OMB manually compiled data from an HTML table.
- **URL for download:** None
- **Download link page:** https://www.tva.com/information/tva-ai-use-case-inventory

- **Number of detected use cases / rows:** **59**
- **Data Type:** XLSX
- **Row Index for Column Names:** Row two

| **Original Column Name** | **Shorthand Colname** | **Remapped?** | **Column Left Blank or Unreported in Agency Public Inventory** |
| :--- | :--- | :--- | :--- |
| 'Use Case ID  [Agency Abbrev.] – [#]' | **id** |  | Yes |
| 'Use Case Name' | **use_case_name** |  |  |
| 'Bureau/Component' | **agency_bureau** |  |  |
| 'Email Address' | **contact_email** |  | Yes |
| 'Should this AI use case be withheld from public reporting?' | **is_withheld** |  |  |
| 'Stage of Development' | **development_stage** |  | Yes |
| 'Is the AI use case high-impact?' | **is_high_impact** |  | Yes |
| 'Justification' | **HI_justification** |  | Yes |
| 'Use Case Topic Area' | **topic_area** |  |  |
| 'AI Classification' | **classification** |  | Yes |
| 'What problem is the AI intended to solve?' | **problem_solved** |  | Yes |
| 'Intended Purpose and Expected Benefits' | **benefits** | Yes - Mapped to: 'What are the expected benefits and positive outcomes from the AI for an agency’s mission and/or the general public?' |  |
| 'Describe the AI system’s outputs.' | **system_outputs** |  | Yes |
| 'Date when AI use case became operational or the pilot’s start date' | **operational_date** |  | Yes |
| 'Was the system involved in this use case purchased from a vendor or developed under con...' | **contracting_usage** |  | Yes |
| 'Vendor(s) Name' | **vendor_name** |  | Yes |
| 'Does this AI use case have an associated Authorization to Operate (ATO)?' | **have_ato** |  | Yes |
| 'System(s) Name' | **system_name_ato** |  | Yes |
| 'Describe any data used to  train, fine-tune, and/or  evaluate performance of the  model...' | **data_description** |  | Yes |
| 'If the data is required to be  publicly disclosed as an  open government data asset,  p...' | **link_to_data** |  | Yes |
| 'Does this AI use case  involve personally  identifiable information (PII)  that is main...' | **has_pii** |  | Yes |
| 'If publicly available, provide  the link to the AI use case’s associated Privacy Impact...' | **pia_url** |  | Yes |
| 'Which, if any, demographic  variables does the AI use  case explicitly use as model  fe...' | **demographic_features** |  | Yes |
| 'Does this project include  custom-developed code?' | **has_custom_code** |  | Yes |
| 'If the code is open source, provide the link for the  publicly available source  code.' | **code_url** |  | Yes |
| 'Has pre-deployment testing been conducted for this AI  use case?      Practice: Complet...' | **hi_testing_conducted** |  | Yes |
| 'Has an AI impact assessment been completed for this AI use case?     Practice: Complete...' | **hi_assessment_completed** |  | Yes |
| 'What are the potential  impacts of using the AI for  this particular use case and  how ...' | **hi_potential_impacts** |  | Yes |
| 'Has as independent review  of the AI use case been  conducted?         Sub practice Com...' | **hi_independent_review** |  | Yes |
| 'Is there a process to conduct ongoing monitoring to identify any adverse impacts to the...' | **hi_ongoing_monitoring** |  | Yes |
| 'Has the agency established sufficient and periodic  training for operators of the  AI t...' | **hi_training_established** |  | Yes |
| 'Does this AI use case have an appropriate fail-safe that minimizes the risk of signific...' | **hi_failsafe_presence** |  | Yes |
| 'Is there an established appeal process in the event that an impacted individual would l...' | **hi_appeal_process** |  | Yes |
| 'What steps has the agency taken to consult and incorporate feedback from end users of t...' | **hi_public_consultation** |  | Yes |
### U.S. International Trade Commission (USITC)

**No Individual Use Cases to Report**

**Reason**: Agency only has consolidated use cases to report.

**Associated URLs**:
- https://www.usitc.gov/ai
