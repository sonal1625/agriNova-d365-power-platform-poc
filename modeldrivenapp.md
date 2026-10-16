# AgriNova 360 — Model-Driven App

## Purpose

The AgriNova 360 model-driven app provides a unified user experience for managing sales opportunities, customer records, products, customer service cases, and registered equipment.

## App Configuration

- **App name:** AgriNova 360
- **Solution:** AgriNova 360 Core
- **Platform:** Microsoft Power Apps model-driven app
- **Data source:** Microsoft Dataverse

## Navigation

### Sales
- Leads
- Accounts
- Contacts
- Opportunities
- Products

### Customer Service
- Cases
- Equipment Registrations

## Equipment Registration Form

The main form is organized into three sections:

1. Equipment Details — Registration Name, Serial Number, Product, Equipment Status.
2. Customer Information — Account and Contact.
3. Warranty Information — Purchase Date, Warranty Start Date, Warranty End Date.

## Equipment Registration Views

- Active Equipment
- Equipment Under Repair
- Warranty Expiring

## Opportunity Sales Process

The proposed business process flow contains four stages:

1. Qualify
2. Develop
3. Propose
4. Close

The process guides sales representatives through opportunity development while retaining standard Dynamics 365 Opportunity status and close behavior.

## Testing

- [ ] App opens successfully.
- [ ] Sales and service navigation items are available.
- [ ] Users can create and update authorized records.
- [ ] Equipment Registration form displays the expected fields.
- [ ] Required fields are enforced.
- [ ] Equipment Registration views return the correct records.
- [ ] Opportunity business process flow advances through the intended stages.
- [ ] App and form changes are published.

## Implementation Status

Update this section as each feature is built and tested. Do not mark a feature complete solely because it has been designed or documented.
