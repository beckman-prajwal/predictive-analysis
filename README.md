Predictive Analysis Progress Report – CytoFLEX Equipment Log Data

1. Dataset Structure and Exploration

The dataset consists of multiple folders, each folder representing a unique Equipment ID.

Within each equipment folder, there are multiple log files corresponding to that equipment.

Each log file contains entries with the following attributes:

Timestamp

Error Message

Error Level (Error or Fatal)

2. Data Preprocessing

Performed parsing and splitting of log files across equipment folders to consolidate into a structured dataset.

Addressed missing values using data imputation (forward fill):

Multiple errors were often registered at the same timestamp, but some timestamps were not recognized correctly.

Forward fill ensured continuity and accurate alignment of error logs with timestamps.

Verified data quality: no significant noise was present.

Implemented RAGs (Retrieval-Augmented Generation) for enhanced exploration of log data and structured retrieval of error information.

Constructed a final unified table containing:

Timestamp

Error Message

Error Level (Fatal/Normal)

Equipment ID

File Name

3. Data Overview

After preprocessing and consolidation:

Total Parsed Entries: 1,728,570

Total Equipment: 320

Normal Errors: 1,711,047

Fatal Errors: 17,523

Unique Errors: 7,041

Unique Fatal Errors: 285

4. Database Integration

Transferred the processed and structured dataset into NoSQL (MongoDB) for scalable storage, faster retrieval, and efficient querying of error logs across multiple equipment IDs and log files.

5. Visualization and Analysis

Developed multiple visual representations to support error trend analysis and predictive insights:

Top 20 Fatal Errors – shown in both tabular and graphical format.

Top 20 Normal Errors – shown in both tabular and graphical format.

All Errors Overview – comprehensive table and visualization across equipment.

Error Trend Graphs per Equipment – tracked error counts over time for each equipment ID.

Implemented dropdown filters to toggle between:

Normal Errors

Fatal Errors

Unique Errors




