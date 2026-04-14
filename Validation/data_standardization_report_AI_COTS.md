# Value Recoding Report for Consolidated AI Use Cases

This table details all distinct value recodings made to agency's downloaded inventories. The goal was to standardize multiple choice responses to make downstream analysis easier. Each row details one unique mapping between values, and the rows are sorted by frequency of occurrence (most common changes first).


**Note:** Recodings were done for multiple choice columns only when the answers had slight spelling/formatting deviations from the valid selections and were clearly intended to match one of the valid options (i.e. mapping 'false' to 'no' or 'None' to 'None of the above').



|Column|Original Value|New Value|Reason/Rule|Frequency|
|-|-|-|-|-|
|Agency Use (Y/N)?|Field Left Blank|N|Standardizing strings to match valid options. This was only performed when an agency did not fill out the “Name of Commercial Product or Service Used” and “Estimated # of Licenses/Users” columns|68|
|Estimated # of Licenses/Users|5001-10;000, 10;000-50;000, or 50;000+|5001-10,000, 10,000-50,000, 50,000+|Standardizing strings to match valid options|63|
|Agency Use (Y/N)?|Field Left Blank|Y|Coding responses to “Y” if an agency also provided information to note affirmative use in the “Name of Commercial Product or Service Used” and/or “Estimated # of Licenses/Users” columns|14|
|Agency Use (Y/N)?|Marked as True|Y|Standardizing strings to match valid options. Coding responses to “Y” if an agency responded to this field with “True” and also provided information to note affirmative use in the “Name of Commercial Product or Service Used” and “Estimated # of Licenses/Users” columns|9|
|Name Of Commercial Product or Service Used|“-“ or “—"|Blank Field|Removing erroneous dashes that signified nothing to report|6|
|Agency Use (Y/N)?|Field Left Blank|Y|Coding responses to “Y” if an agency use case description was mapped to the most likely match from OMB’s valid response options|4|
|AI Use Case|LLM employed across OPM for summarization, drafting, and decision support.|Generating first drafts of documents, briefing, or communication materials using AI.|Agency response did not follow OMB’s template. Product descriptions were mapped to the most likely match from the valid response options|3|
|AI Use Case|An AI-powered tool that assists with code generation including writing, understanding, and transforming code across multiple programming languages.|Generating code using AI.|Agency response did not follow OMB’s template. Product descriptions were mapped to the most likely match from the valid response options|1|
|AI Use Case|A security platform that provides threat detection, endpoint protection and vulnerability management.|Managing or implementing security controls for information systems (e.g., cybersecurity) using AI|Agency response did not follow OMB’s template. Product descriptions were mapped to the most likely match from the valid response options|1|
|AI Use Case|A cloud security platform that gives full-stack visibility into cloud environments.|Managing or implementing security controls for information systems (e.g., cybersecurity) using AI|Agency response did not follow OMB’s template. Product descriptions were mapped to the most likely match from the valid response options|1|
|AI Use Case|A customer service and support platform that helps manage support tickets, customer inquiries, and service workflows.|Managing and prioritizing internal service or help desk tickets using AI.|Agency response did not follow OMB’s template. Product descriptions were mapped to the most likely match from the valid response options|1|



