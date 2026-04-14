# Value Recoding Report

This table details all distinct value recodings made to agency's downloaded inventories. The goal was to standardize multiple choice responses to make downstream analysis easier. Each row details one unique mapping between values, and the rows are sorted by frequency of occurrence (most common changes first). In addition to these recodings, all values were additionally cleaned by trimming extra whitespace from the start and end of all values.



**Note**: Recodings were done for multiple choice columns only when the answers had slight spelling/formatting deviations from the valid selections and were clearly intended to match one of the valid options (i.e. mapping 'false' to 'no' or 'None' to 'None of the above'). For responses that were not similar to any of the valid options, no changes were made except for stripping excess leading/trailing whitespace (except for a small handful of occurrences in the development stage column). Lists were reformatted to use a semicolon separator and to be sorted in alphabetical order.

| Column | Original Value | New Value | Reason/Rule | Frequency |
| :--- | :--- | :--- | :--- | :--- |
| classification | Classical/Predictive Machine Learning | Classical/Predictive Machine Learning: Models trained on data to make predictions or classifications based on identified patterns or relationships. | Standardizing strings to match valid options | 1032 |
| classification | Generative AI | Generative AI: AI that generates new or synthetic content (e.g., images, videos, audio, text, code). | Standardizing strings to match valid options | 798 |
| is_withheld | No | a) No | Standardizing strings to match valid options | 668 |
| development_stage | c)  Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. \(Note: there are two spaces after 'c)' that aren't visible in markdown table\) | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 629 |
| demographic_features | None of the above | k) None of the above | Standardizing List Formatting | 403 |
| classification | Natural Language Processing (NLP) | Natural Language Processing: AI that processes, interprets, and shares information in human language. | Standardizing strings to match valid options | 356 |
| contracting_usage | a)\xa0Purchased from a vendor \(Note: the excel specific character '\xa0' was removed\) | a) Purchased from a vendor | Standardizing strings to match valid options | 325 |
| development_stage | Pre-deployment – The use case is in a development or acquisition status. | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 307 |
| topic_area | Health & Medical | Health and Medical | Standardizing strings to match valid options | 272 |
| has_pii | False | No | Standardizing strings to match valid options | 245 |
| has_custom_code | False | No | Standardizing strings to match valid options | 238 |
| have_ato | False | No | Standardizing strings to match valid options | 232 |
| development_stage | b)  Pilot – The use case has been deployed in a limited test or pilot capacity. \(Note: there are two spaces after 'b)' that aren't visible in markdown table\) | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 217 |
| classification | Computer Vision | Computer Vision: AI that processes and interprets visual data (e.g., images and videos). | Standardizing strings to match valid options | 210 |
| demographic_features | None of the Above | k) None of the above | Standardizing List Formatting | 198 |
| is_high_impact | Not high-impact | c) Not high-impact | Standardizing strings to match valid options | 192 |
| development_stage | Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 177 |
| contracting_usage | Developed in-house | b) Developed in-house | Standardizing strings to match valid options | 162 |
| development_stage | Pilot – The use case has been deployed in a limited test or pilot capacity. | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 157 |
| contracting_usage | Purchased from a vendor | a) Purchased from a vendor | Standardizing strings to match valid options | 140 |
| topic_area | Energy & the Environment | Energy and the Environment | Standardizing strings to match valid options | 131 |
| hi_failsafe_presence | Not applicable | b) Not applicable | Standardizing strings to match valid options | 126 |
| hi_training_established | Yes, sufficient and periodic training has been established | a) Yes, sufficient and periodic training has been established | Standardizing strings to match valid options | 115 |
| hi_appeal_process | Not applicable | b) Not applicable | Standardizing strings to match valid options | 110 |
| is_high_impact | b) Presumed high-impact but determined not high-impact | b) Presumed high-impact, but determined not high impact | Standardizing strings to match valid options | 102 |
| topic_area | Procurement & Financial Management | Procurement and Financial Management | Standardizing strings to match valid options | 90 |
| classification | Agentic AI | Agentic AI: AI systems that perform tasks or make decisions autonomously with minimal human intervention. | Standardizing strings to match valid options | 90 |
| contracting_usage | Developed in house | b) Developed in-house | Standardizing strings to match valid options | 87 |
| contracting_usage | Developed with both contracting and in-house resources | c) Developed with both contracting and in-house resources | Standardizing strings to match valid options | 78 |
| hi_training_established | Establishment of sufficient and periodic training is in-progress | b) Establishment of sufficient and periodic training is in-progress | Standardizing strings to match valid options | 74 |
| hi_testing_conducted | In-Progress | b) In-progress | Standardizing strings to match valid options | 73 |
| development_stage | d) Retired – The use case was reported in the agency's prior year's inventory, but its development and/or use has since been discontinued. | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 72 |
| hi_assessment_completed | In-Progress | b) In-progress | Standardizing strings to match valid options | 71 |
| hi_ongoing_monitoring | Yes, sufficient monitoring protocols have been established | a) Yes, sufficient monitoring protocols have been established | Standardizing strings to match valid options | 70 |
| development_stage | Pre-Deployment - The use case is in a development or acquisition status. | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 70 |
| development_stage | Pre-deployment | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 53 |
| hi_ongoing_monitoring | Development of monitoring protocols is in-progress | b) Development of monitoring protocols is in-progress | Standardizing strings to match valid options | 50 |
| hi_testing_conducted | Yes | a) Yes | Standardizing strings to match valid options | 47 |
| hi_public_consultation | Direct usability testing | a) Direct usability testing | Standardizing List Formatting | 43 |
| classification | Natural Language Processing | Natural Language Processing: AI that processes, interprets, and shares information in human language. | Standardizing strings to match valid options | 42 |
| hi_independent_review | In-Progress | d) In-progress | Standardizing strings to match valid options | 39 |
| hi_appeal_process | Establishment of an appropriate appeal process is in-progress | c) Establishment of an appropriate appeal process is in-progress | Standardizing strings to match valid options | 38 |
| pia_url | Not Applicable | N/A | Standardize NA and None | 36 |
| hi_failsafe_presence | Yes | a) Yes | Standardizing strings to match valid options | 35 |
| hi_independent_review | Yes – by another appropriate agency office or reviewer not directly involved in the AI's development | a) Yes – by another appropriate agency office or reviewer not directly involved in the AI’s development | Standardizing strings to match valid options | 35 |
| hi_public_consultation | Other | d) Other | Standardizing List Formatting | 34 |
| link_to_data | Not Applicable | N/A | Standardize NA and None | 34 |
| hi_independent_review | Yes – by another appropriate agency office or reviewer not directly involved in the AI’s development | a) Yes – by another appropriate agency office or reviewer not directly involved in the AI’s development | Standardizing strings to match valid options | 34 |
| have_ato | Not Applicable | N/A | Standardize NA and None | 33 |
| development_stage | a) Pre-deployment - The use case is in a development or acquisition status. | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 29 |
| hi_assessment_completed | Yes | a) Yes | Standardizing strings to match valid options | 29 |
| development_stage | Deployed - The use case is being actively authorized or utilized to support the functions or mission of an agency. | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 26 |
| have_ato | Use vendor's ATO or FedRAMP authorization | Yes | Standardizing strings to match valid options | 25 |
| hi_independent_review | In-progress | d) In-progress | Standardizing strings to match valid options | 23 |
| development_stage | Pilot - The use case has been deployed in a limited test or pilot capacity. | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 22 |
| contracting_usage | Developed with a combination of in-house and contract/external resources. | c) Developed with both contracting and in-house resources | Standardizing strings to match valid options | 21 |
| has_custom_code | Not Applicable | N/A | Standardize NA and None | 18 |
| development_stage | Deployed | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 17 |
| development_stage | c)  Deployed - The use case is being actively authorized or utilized to support the functions or mission of an agency. | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 17 |
| hi_ongoing_monitoring | Development of monitoring protocols is in-progess | b) Development of monitoring protocols is in-progress | Standardizing strings to match valid options | 17 |
| hi_public_consultation | In-progress | e) In-progress | Standardizing List Formatting | 16 |
| development_stage | Retired – The use case was reported in the agency's prior year's inventory, but its development and/or use has since been discontinued. | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 15 |
| have_ato | True | Yes | Standardizing strings to match valid options | 15 |
| contracting_usage | No contract/external resources used in development. | b) Developed in-house | Standardizing strings to match valid options | 13 |
| development_stage | Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 13 |
| hi_ongoing_monitoring | b) Development of monitoring protocols is in-progess | b) Development of monitoring protocols is in-progress | Standardizing strings to match valid options | 12 |
| demographic_features | ["None of the above"] | k) None of the above | Standardizing List Formatting | 11 |
| classification | Reinforcement Learning | Reinforcement Learning: AI trained through trial and error using rewards and penalties to optimize decision-making policies. | Standardizing strings to match valid options | 11 |
| code_url | Not applicable | N/A | Standardize NA and None | 11 |
| development_stage | c)  Deployed ñ The use case is being actively authorized or utilized to support the functions or mission of an agency. | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 11 |
| development_stage | Retired | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 11 |
| hi_appeal_process | Yes, an appropriate appeal process has been established | a) Yes, an appropriate appeal process has been established | Standardizing strings to match valid options | 9 |
| link_to_data | Not applicable | N/A | Standardize NA and None | 9 |
| has_custom_code | True | Yes | Standardizing strings to match valid options | 9 |
| development_stage | Pilot | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 8 |
| hi_ongoing_monitoring | a) Yes; sufficient monitoring protocols have been established | a) Yes, sufficient monitoring protocols have been established | Standardizing strings to match valid options | 8 |
| hi_training_established | a) Yes; sufficient and periodic training has been established | a) Yes, sufficient and periodic training has been established | Standardizing strings to match valid options | 8 |
| hi_testing_conducted | In-progress | b) In-progress | Standardizing strings to match valid options | 8 |
| contracting_usage | In-house & Contractor | c) Developed with both contracting and in-house resources | Standardizing strings to match valid options | 8 |
| contracting_usage | In-house | b) Developed in-house | Standardizing strings to match valid options | 8 |
| contracting_usage | Vendor | a) Purchased from a vendor | Standardizing strings to match valid options | 8 |
| is_withheld | b) Yes – agency has determined that there’s a risk to disclosure such as a harm to an interest protected by a FOIA exemption | b) Yes – agency has determined that there’s a risk to disclosure, such as a harm to an interest protected by a FOIA exemption | Standardizing strings to match valid options | 7 |
| development_stage | d) Retired – The use case was reported in the agency’s prior year’s inventory but its development and/or use has since been discontinued. | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 7 |
| has_pii | Yes - Employee names and communications | Yes | Standardizing strings to match valid options | 7 |
| have_ato | In-progress - ATO process underway | Yes | Standardizing strings to match valid options | 7 |
| demographic_features | Other | l) Other | Standardizing List Formatting | 6 |
| pia_url | Not applicable | N/A | Standardize NA and None | 6 |
| hi_public_consultation | General solicitations of feedback and comments from the public, Direct usability testing | a) Direct usability testing; b) General solicitations of feedback and comments from the public | Standardizing List Formatting | 5 |
| is_high_impact | b) Presumed high-impact, but determined not high-impact | b) Presumed high-impact, but determined not high impact | Standardizing strings to match valid options | 5 |
| topic_area | Internal Knowledge Management & Staff Support | Administrative Functions | Standardizing strings to match valid options | 5 |
| topic_area | Cybersecurity Operations | Cybersecurity | Standardizing strings to match valid options | 5 |
| contracting_usage | Exclusively developed with contract/external resources. | a) Purchased from a vendor | Standardizing strings to match valid options | 4 |
| hi_appeal_process | a) Yes; an appropriate appeal process has been established | a) Yes, an appropriate appeal process has been established | Standardizing strings to match valid options | 4 |
| code_url | Not Applicable | N/A | Standardize NA and None | 4 |
| topic_area | Communications & Public Affairs | Service Delivery | Standardizing strings to match valid options | 4 |
| has_pii | Yes - Customer contact and account information | Yes | Standardizing strings to match valid options | 4 |
| has_pii | No - General content generation and research | No | Standardizing strings to match valid options | 4 |
| has_pii | Yes - System logs may contain user identifiers | Yes | Standardizing strings to match valid options | 4 |
| is_high_impact | High-impact | a) High-impact | Standardizing strings to match valid options | 4 |
| classification | Generative AI; Natural Language Processing (NLP) | Generative AI: AI that generates new or synthetic content (e.g., images, videos, audio, text, code). | Standardizing strings to match valid options | 4 |
| demographic_features | Age | c) Age | Standardizing List Formatting | 3 |
| demographic_features | Sex/Gender, Age | b) Sex; c) Age | Standardizing List Formatting | 3 |
| demographic_features | Race/Ethnicity, Sex/Gender, Age | a) Race/Ethnicity; b) Sex; c) Age | Standardizing List Formatting | 3 |
| development_stage | b)  Pilot - The use case has been deployed in a limited test or pilot capacity. | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 3 |
| topic_area | Business Development & Technical Assistance | Service Delivery | Standardizing strings to match valid options | 3 |
| topic_area | Audit, Compliance & Risk Management | Service Delivery | Standardizing strings to match valid options | 3 |
| classification | Machine Learning (Classification/Prediction) | Classical/Predictive Machine Learning: Models trained on data to make predictions or classifications based on identified patterns or relationships. | Standardizing strings to match valid options | 3 |
| classification | Machine Learning | Classical/Predictive Machine Learning: Models trained on data to make predictions or classifications based on identified patterns or relationships. | Standardizing strings to match valid options | 3 |
| topic_area | Loan Program Operations | Service Delivery | Standardizing strings to match valid options | 3 |
| development_stage | Retired – The use case was reported in the agency's prior year's inventory but its development and/or use has since been discontinued. | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 3 |
| topic_area | Software Development & Engineering | Information Technology | Standardizing strings to match valid options | 3 |
| contracting_usage | a)ÝPurchased from a vendor | a) Purchased from a vendor | Standardizing strings to match valid options | 3 |
| is_high_impact | Presumed high-impact but determined not high-impact | b) Presumed high-impact, but determined not high impact | Standardizing strings to match valid options | 3 |
| demographic_features | Age; Income | c) Age; i) Income | Standardizing List Formatting | 2 |
| classification | Agentic-AI | Agentic AI: AI systems that perform tasks or make decisions autonomously with minimal human intervention. | Standardizing strings to match valid options | 2 |
| hi_public_consultation | General solicitations of feedback and comments from the public | b) General solicitations of feedback and comments from the public | Standardizing List Formatting | 2 |
| hi_assessment_completed | In-progress | b) In-progress | Standardizing strings to match valid options | 2 |
| contracting_usage | Developed with both contracting and in-house resources. | c) Developed with both contracting and in-house resources | Standardizing strings to match valid options | 2 |
| demographic_features | Race/Ethnicity; Sex; Age | a) Race/Ethnicity; b) Sex; c) Age | Standardizing List Formatting | 2 |
| hi_public_consultation | In-Progress | e) In-progress | Standardizing List Formatting | 2 |
| demographic_features | b) Sex c) Age | b) Sex; c) Age | Standardizing List Formatting | 2 |
| topic_area | Employee Productivity & Collaboration | Service Delivery | Standardizing strings to match valid options | 2 |
| has_pii | No - Code and technical documentation only | No | Standardizing strings to match valid options | 2 |
| has_pii | Yes - Loan applicant and business owner PII | Yes | Standardizing strings to match valid options | 2 |
| topic_area | Customer Service & Public Engagement | Service Delivery | Standardizing strings to match valid options | 2 |
| classification | Intelligent Automation (AIOps) | Classical/Predictive Machine Learning: Models trained on data to make predictions or classifications based on identified patterns or relationships. | Standardizing strings to match valid options | 2 |
| development_stage | d) Retired ñ The use case was reported in the agencyís prior yearís inventory, but its development and/or use has since been discontinued. | d) Retired – The use case was reported in the agency’s prior year’s inventory, but its development and/or use has since been discontinued. | Standardizing strings to match valid options | 2 |
| development_stage | a) Pre-deployment ñ The use case is in a development or acquisition status. | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 2 |
| has_pii | True | Yes | Standardizing strings to match valid options | 2 |
| pia_url | na | N/A | Standardize NA and None | 2 |
| demographic_features | Race/Ethnicity | a) Race/Ethnicity | Standardizing List Formatting | 1 |
| hi_public_consultation | Other, Direct usability testing | a) Direct usability testing; d) Other | Standardizing List Formatting | 1 |
| hi_public_consultation | Direct usability testing, Other | a) Direct usability testing; d) Other | Standardizing List Formatting | 1 |
| hi_public_consultation | General solicitations of feedback and comments from the public, Other | b) General solicitations of feedback and comments from the public; d) Other | Standardizing List Formatting | 1 |
| development_stage | b)  b)  Pilot – The use case has been deployed in a limited test or pilot capacity. | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 1 |
| topic_area | This potentially crosses all EPA business lines | Service Delivery | Standardizing strings to match valid options | 1 |
| development_stage | a) a) Pre-deployment – The use case is in a development or acquisition status. | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 1 |
| classification | Computer Vision - AI that processes and interprets visual data (e.g.; images and videos). | Computer Vision: AI that processes and interprets visual data (e.g., images and videos). | Standardizing strings to match valid options | 1 |
| topic_area | eDiscovery matters | Service Delivery | Standardizing strings to match valid options | 1 |
| topic_area | Records Management | Service Delivery | Standardizing strings to match valid options | 1 |
| demographic_features | ["Race/Ethnicity","Socioeconomic Status","Income","Age"] | a) Race/Ethnicity; c) Age; e) Socioeconomic Status; i) Income | Standardizing List Formatting | 1 |
| hi_potential_impacts | Not applicable | N/A | Standardize NA and None | 1 |
| hi_training_established | Yes; sufficient and periodic training has been established | a) Yes, sufficient and periodic training has been established | Standardizing strings to match valid options | 1 |
| contracting_usage | Developed with contracting resources. | a) Purchased from a vendor | Standardizing strings to match valid options | 1 |
| contracting_usage | Developed In house | b) Developed in-house | Standardizing strings to match valid options | 1 |
| pia_url | N/a | N/A | Standardize NA and None | 1 |
| topic_area | Other  – Economic & Financial | Other – Economic & Financial | Standardizing strings to match valid options | 1 |
| have_ato | yes | Yes | Standardizing strings to match valid options | 1 |
| development_stage | Operation and Maintenance | c) Deployed – The use case is being actively authorized or utilized to support the functions or mission of an agency. | Standardizing strings to match valid options | 1 |
| development_stage | Acquisition and/or Development | a) Pre-deployment – The use case is in a development or acquisition status. | Standardizing strings to match valid options | 1 |
| development_stage | Initiated | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 1 |
| hi_independent_review | Yes – by an agency AI oversight board not directly involved in the AI's development | b) Yes – by an agency AI oversight board not directly involved in the AI’s development | Standardizing strings to match valid options | 1 |
| hi_independent_review | Agency CAIO has waived this minimum practice and reported such waiver to OMB | e) Agency CAIO has waived this minimum practice and reported such waiver to OMB | Standardizing strings to match valid options | 1 |
| pia_url | N>A | N/A | Standardize NA and None | 1 |
| link_to_data | None. | None | Standardize NA and None | 1 |
| code_url | None. | None | Standardize NA and None | 1 |
| link_to_data | na | N/A | Standardize NA and None | 1 |
| code_url | na | N/A | Standardize NA and None | 1 |
| link_to_data | not applicable | N/A | Standardize NA and None | 1 |
| code_url | not applicable | N/A | Standardize NA and None | 1 |
| demographic_features | j) Employment Status i) Income | i) Income; j) Employment Status | Standardizing List Formatting | 1 |
| demographic_features | c) Age e) Socioeconomic Status | c) Age; e) Socioeconomic Status | Standardizing List Formatting | 1 |
| demographic_features | b) Sex c) Age | b) Sex; c) Age | Standardizing List Formatting | 1 |
| demographic_features | c) Age I) Other | c) Age; l) Other | Standardizing List Formatting | 1 |
| hi_appeal_process | d) Law; operational limitations; or governmentwide guidance precludes an opportunity for an individual to appeal | d) Law, operational limitations, or governmentwide guidance precludes an opportunity for an individual to appeal | Standardizing strings to match valid options | 1 |
| has_pii | Yes - Business and individual information in audit records | Yes | Standardizing strings to match valid options | 1 |
| topic_area | Strategic Planning & Policy Analysis | Service Delivery | Standardizing strings to match valid options | 1 |
| classification | AI-Enabled Application | Generative AI: AI that generates new or synthetic content (e.g., images, videos, audio, text, code). | Standardizing strings to match valid options | 1 |
| topic_area | IT Operations & Infrastructure Management | Information Technology | Standardizing strings to match valid options | 1 |
| topic_area | Data Analytics & Business Intelligence | Information Technology | Standardizing strings to match valid options | 1 |
| has_pii | Depends on data sources analyzed | No | Standardizing strings to match valid options | 1 |
| contracting_usage | Both, the AI was developed by a vendor but it was substantially customized in-house or by a contractor | c) Developed with both contracting and in-house resources | Standardizing strings to match valid options | 1 |
| has_pii | a) No | No | Standardizing strings to match valid options | 1 |
| has_pii | b) Yes | Yes | Standardizing strings to match valid options | 1 |
| development_stage | b)  Pilot ñ The use case has been deployed in a limited test or pilot capacity. | b) Pilot – The use case has been deployed in a limited test or pilot capacity. | Standardizing strings to match valid options | 1 |
| demographic_features | Race/Ethnicity; Sex; Age; Socioeconomic Status; Residency Status; Marital Status; Income; Employment Status | a) Race/Ethnicity; b) Sex; c) Age; e) Socioeconomic Status; g) Residency Status; h) Marital Status; i) Income; j) Employment Status | Standardizing List Formatting | 1 |
| hi_failsafe_presence | In-progress | c) In-progress | Standardizing strings to match valid options | 1 |
| pia_url | Not applicable. | N/A | Standardize NA and None | 1 |
| has_pii | Yes (incidental PII may be involved through authenticated platform users) | Yes | Standardizing strings to match valid options | 1 |
