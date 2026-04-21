# ETL – Extract, Transform, Load

This directory contains all materials related to the ETL (Extract, Transform, Load) process for converting the raw Norwegian registry data into the **OMOP Common Data Model (CDM)** format for the NLHR Perinatal cohort.

## Directory Structure

```
ETL/
├── README.md               # This file
├── scripts/                # ETL scripts (SQL, R, Python, etc.)
├── docs/                   # ETL design documents and specifications
└── mappings/               # Vocabulary and concept mapping tables
```

## Contents

| Subdirectory | Description |
|---|---|
| `scripts/` | ETL scripts used to transform source registry data into OMOP CDM tables |
| `docs/` | ETL specification documents, data flow diagrams, and design decisions |
| `mappings/` | Source-to-OMOP concept mapping files (drug, condition, procedure vocabularies) |

## ETL Process Overview

The ETL process follows the OMOP CDM ETL convention:

1. **Extract** – Source data is extracted from each contributing Norwegian registry within the TSD secure environment at the University of Oslo.
2. **Transform** – Source data fields are mapped to OMOP CDM tables and concepts using standard vocabularies (ATC→RxNorm, ICD-10→SNOMED CT, etc.).
3. **Load** – Transformed data are loaded into the target OMOP CDM database instance.

## Source Registries

The following registries contribute data to the ETL pipeline (see main [README](../README.md) for full details):

- Medical Birth Registry of Norway (MBRN)
- Norwegian Patient Registry (NPR)
- Norwegian Prescription Database (NorPD)
- National Population Registry
- Norwegian Cause of Death Registry

## Notes

- All ETL work is performed within the secure **TSD (Tjenester for Sensitive Data)** environment at the University of Oslo.
- No identifiable or sensitive data is included in this repository.
- Scripts and documents in this directory describe the transformation logic only.
