# Student Data Automation Pipeline

An automated Python ETL (Extract, Transform, Load) script designed to ingest, clean, and merge disparate student data sources to streamline administrative workflows for educators.

## Overview
Managing classroom data across multiple systems often leads to fragmented records. This tool automates the synchronization between two primary data streams:
1. **Student Information System (SIS):** Raw student demographics, physical addresses, home phone numbers, and parent/guardian contact info originating from Infinite Campus.
2. **Google Classroom:** Active student email addresses.

The script processes and merges these streams to generate two targeted outputs:
- **Central Reference Dashboard (Google Sheet):** A unified master sheet for teacher reference.
- **Google Contacts CSV Output:** A formatted CSV structure containing student and parent contact details designed for seamless import into Google Contacts and Gmail.

## Key Features
- **Data Integration & Merging:** Combines records from separate institutional systems into structured Google Sheets via the `gspread` API.
- **Smart Data Cleaning & Edge-Case Handling:** Implements robust string-parsing algorithms to handle complex name variations—including multi-surname formats common among Latino students—and checks for discrepancies between source rosters.
- **Automated Contact Formatting:** Transforms raw data into clean, import-ready contact structures to eliminate manual administrative data entry.

## Requirements
- Python 3.x
- `gspread` library
- `oauth2client` library

## Note on Data Privacy & Execution
Due to student data privacy regulations (FERPA) and institutional security, raw data spreadsheets, personal credentials, and production `.json` key files have been excluded from this repository. The source code is provided to showcase backend ETL logic, API integration, and custom string-parsing architecture.
