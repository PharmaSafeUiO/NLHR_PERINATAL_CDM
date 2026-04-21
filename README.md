# NLHR Perinatal CDM

**Norwegian Linked Health Registries – Perinatal Cohort | Common Data Model**

> **Institution:** University of Oslo (UiO), Norway
> **EMA Data Catalogue:** [Quantitative Descriptors](https://catalogues.ema.europa.eu/node/4311/quantitative-descriptors)

---

## Overview

The **Norwegian Linked Health Registries Perinatal (NLHR Perinatal)** is a population-based data source hosted at the University of Oslo (UiO). It is constructed by record linkage of multiple national Norwegian health and administrative registries, covering all pregnancies and births in Norway over the data collection period. The dataset has been converted into the **OMOP Common Data Model (CDM)** format to enable standardised, federated pharmacoepidemiological research.

This data source was developed in the context of the [IMI ConcePTION](https://www.imi-conception.eu/) project (Innovative Medicines Initiative Horizon 2020) to support research on the safety of medicines during pregnancy and in the perinatal period. Data are held securely at **TSD (Tjenester for Sensitive Data / Services for Sensitive Data)** at the University of Oslo.

---

## Population

| Attribute | Description |
|---|---|
| **Population** | Pregnant women and their live-born offspring in Norway |
| **Coverage** | All pregnancies and births registered in Norway |
| **Data period** | 2004 – 2020 |
| **Population size** | ~900,000 pregnancies / mother–child pairs |
| **Country** | Norway 🇳🇴 |
| **Setting** | Nationwide, population-based |

The cohort includes mothers, their pregnancies, and linked offspring records. It captures prescription drug use before, during, and after pregnancy, as well as maternal and neonatal health outcomes.

---

## Linked Registries

The NLHR Perinatal CDM is derived from record linkage of the following Norwegian national registries:

| Registry | Norwegian Name | Content |
|---|---|---|
| **Medical Birth Registry of Norway (MBRN)** | Medisinsk Fødselsregister (MFR) | All births in Norway since 1967; maternal and neonatal characteristics, delivery details, and congenital anomalies |
| **Norwegian Patient Registry (NPR)** | Norsk Pasientregister | Specialist (hospital) healthcare contacts, diagnoses (ICD-10), and procedures |
| **Norwegian Prescription Database (NorPD)** | Norsk Reseptbasert Legemiddelregister | All dispensed prescriptions from Norwegian pharmacies since 2004; drug information coded in ATC classification |
| **National Population Registry** | Folkeregisteret | Demographic information, dates of birth and death, immigration/emigration, family linkages |
| **Norwegian Cause of Death Registry** | Dødsårsaksregisteret | Cause of death information (ICD-10) for all deaths registered in Norway |

Linkage across registries is performed using the unique Norwegian national identity number (*fødselsnummer*), enabling comprehensive longitudinal follow-up.

---

## Data Model

The data source follows the **OMOP CDM (Observational Medical Outcomes Partnership Common Data Model)** standard, enabling interoperability with other data sources in federated research networks. Vocabulary mappings comply with OMOP standard vocabularies, including:

- **RxNorm / ATC** for drugs
- **SNOMED CT / ICD-10** for conditions and procedures
- **LOINC** for measurements

---

## ETL Documentation

The Extract, Transform, and Load (ETL) process that converts the raw Norwegian registry data into the OMOP CDM format is documented in the [`ETL/`](./ETL/) directory. This includes:

- ETL scripts
- ETL design documents and specification files
- Vocabulary mapping tables
- Data quality reports

See the [ETL directory](./ETL/) for full details.

---

## Access and Governance

Access to the NLHR Perinatal data is subject to Norwegian data protection legislation and requires formal approval from:

- The Norwegian Data Protection Authority (*Datatilsynet*)
- Regional Ethics Committees (*REK*)
- The data custodians of each contributing registry

Data are stored and analysed within the TSD secure computing environment at the University of Oslo and are not directly transferable outside the secure platform.

---

## Citation and References

- EMA Data Catalogue entry: [https://catalogues.ema.europa.eu/node/4311/quantitative-descriptors](https://catalogues.ema.europa.eu/node/4311/quantitative-descriptors)
- IMI ConcePTION project: [https://www.imi-conception.eu/](https://www.imi-conception.eu/)
- University of Oslo, PharmaSafe research group: [https://www.med.uio.no/farmasi/english/research/groups/pharmasafe/](https://www.med.uio.no/farmasi/english/research/groups/pharmasafe/)

---

## Contact

For enquiries regarding this repository or the NLHR Perinatal CDM, please contact the PharmaSafe research group at the University of Oslo.
