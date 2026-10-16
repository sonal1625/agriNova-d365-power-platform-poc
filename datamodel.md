# AgriNova 360 — Dataverse Data Model

## 1. Purpose

This document defines the initial data model for the AgriNova 360 Dynamics 365 Customer Engagement and Power Platform POC.

The model reuses standard Dynamics 365 tables wherever possible and introduces a custom Equipment Registration table to track individual physical equipment units.

## 2. Tables

| Table | Type | Purpose |
|---|---|---|
| Account | Standard | Customer companies and dealers |
| Contact | Standard | Customer representatives and individuals |
| Lead | Standard | Prospective customers |
| Opportunity | Standard | Potential sales |
| Product | Standard | Equipment models and spare parts |
| Opportunity Product | Standard | Products and quantities associated with an opportunity |
| Case | Standard | Customer service requests |
| Equipment Registration | Custom | Individual units registered to customers |

## 3. Custom Table: Equipment Registration

**Display name:** Equipment Registration  
**Schema name:** agn_EquipmentRegistration  
**Primary name:** Registration Name  
**Ownership:** User or team owned

### Columns

| Column | Type | Requirement |
|---|---|---|
| Registration Name | Primary name text | Required |
| Serial Number | Text | Business required |
| Purchase Date | Date only | Optional |
| Warranty Start Date | Date only | Optional |
| Warranty End Date | Date only | Optional |
| Equipment Status | Choice | Business required |
| Account | Lookup to Account | Business required |
| Contact | Lookup to Contact | Optional |
| Product | Lookup to Product | Business required |

### Equipment Status choices

- Registered
- Active
- Under Repair
- Retired

### Business rules

1. Each equipment registration must reference a customer Account and Product.
2. The serial number must follow the agreed uniqueness rule.
3. Warranty End Date must not precede Warranty Start Date.
4. Equipment Status must use a defined Choice value.
5. Contact association is optional because a company may own equipment without assigning a single individual as its user.

## 4. Relationships

| Parent | Child | Cardinality | Implementation |
|---|---|---|---|
| Account | Contact | 1:N | Standard relationship |
| Account | Opportunity | 1:N | Standard relationship |
| Account | Equipment Registration | 1:N | Account lookup on Equipment Registration |
| Contact | Equipment Registration | 1:N | Contact lookup on Equipment Registration |
| Product | Equipment Registration | 1:N | Product lookup on Equipment Registration |
| Opportunity | Opportunity Product | 1:N | Standard sales relationship |
| Product | Opportunity Product | 1:N | Standard sales relationship |
| Equipment Registration | Case | 1:N | Optional Equipment Registration lookup on Case |

Lead qualification uses standard Dynamics 365 behavior to create or associate Account, Contact, and optionally Opportunity records.

The Case table also uses its standard Customer and Contact columns. The additional Equipment Registration lookup identifies the physical unit related to a service request.

## 5. Data Integrity and Security

- Use an alternate key for Serial Number if the agreed uniqueness requirement is global and the column meets Dataverse key requirements.
- If serial numbers are unique only within a manufacturer, introduce the manufacturer dimension before defining the key.
- Validate warranty date consistency using appropriate business rules or server-side validation.
- Configure security roles and record access according to user responsibilities.
- Use fictional customer and equipment data only.
- Select relationship cascade behavior deliberately; avoid cascading deletion of service history or registered equipment.

## 6. Implementation Status

This document describes the intended design. Each table, column, relationship, and rule will be marked implemented only after it has been created and tested in the development environment.

## 7. Validation Checklist

- [ ] Equipment Registration table created.
- [ ] Required columns created.
- [ ] Choice values configured.
- [ ] Account lookup tested.
- [ ] Contact lookup tested.
- [ ] Product lookup tested.
- [ ] Case lookup tested.
- [ ] Serial number uniqueness strategy validated.
- [ ] Warranty date validation tested.
- [ ] Data model reviewed and committed to GitHub.

