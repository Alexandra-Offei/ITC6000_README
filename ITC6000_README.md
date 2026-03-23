# ITC 6000 — Database Management Systems

**Northeastern University · Roux Institute**  
**Course:** ITC 6000 Database Management Systems  
**Tools:** SQL · draw.io · Entity-Relationship modelling

---

## Overview

This course covered the principles of relational database design, entity-relationship modelling, normalisation, and SQL querying. Projects involved designing database schemas for real-world domains and translating business requirements into structured data models.

---

## Projects

### Healthcare Database — Entity-Relationship Diagram ⭐

A fully normalised relational database schema for a healthcare management system, designed in draw.io using crow's foot notation.

**Entities & Key Attributes:**

| Entity | Primary Key | Key Attributes |
|---|---|---|
| Patient | PatientID | Age · Gender · Income · State |
| Plan | PlanID | Plan_Type · Plan_Deductable |
| Provider | ProviderID | ProviderPubPriv |
| Facility | FacilityID | ForProfit · PublicPrivate · Location |
| Treatment | TreatmentID | Cost · Duration · Occurrence |
| Professional | ProfessionalID | Specialty |
| Dependent | DependentID | PolicyHolder · Disability · Age |

**Relationships:**
- Patient ↔ Plan (many-to-one: patients enrol in plans)
- Patient ↔ Facility (many-to-many: patients treated at facilities)
- Patient ↔ Treatment (one-to-many: patients receive treatments)
- Treatment ↔ Professional (many-to-one: treatments administered by professionals)
- Facility ↔ Professional (many-to-many: professionals work at facilities)
- Patient ↔ Dependent (one-to-many: patients have dependents)
- Plan ↔ Provider (many-to-one: plans offered by providers)

**Design decisions:**
- Crow's foot notation for cardinality
- Separation of Provider and Facility to avoid update anomalies
- Dependent linked to Patient (not Plan) to reflect real-world policy structure

---

### Movie Database — Entity-Relationship Diagram

Database schema designed from a raw CSV dataset of movie records.

**Entities:**
- **Movie** — MovieID (PK) · Name · Released · Runtime · Score · Gross · Rating · Year
- **Director** — DirectorID (PK) · Name
- Additional entities derived from CSV columns

**Skills applied:** Entity identification from raw data · primary key selection · relationship cardinality · normalisation to remove redundancy

---

## Skills Demonstrated

`Relational database design` `Entity-relationship modelling` `Crow's foot notation` `Normalisation` `SQL` `draw.io` `Schema design` `Healthcare data modelling`
