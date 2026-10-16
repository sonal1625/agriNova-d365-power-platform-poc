# AgriNova 360 — Dynamics 365 & Power Platform POC

**An end-to-end CRM solution for Sales, Customer Service, workflow automation, and business intelligence.**

## Overview

AgriNova 360 is a portfolio Proof of Concept (POC) designed to demonstrate how Microsoft Dynamics 365 Customer Engagement and the Power Platform can solve real-world business problems.

The fictional company, AgriNova, sells agricultural equipment and manages customer enquiries, sales opportunities, and after-sales service requests.

This project demonstrates the end-to-end solution lifecycle, including requirements gathering, data modeling, CRM configuration, process automation, custom development, reporting, testing, and solution deployment.

## Business Objectives

- Centralize customer and sales information.
- Standardize lead qualification and opportunity management.
- Track customer service requests and their resolution.
- Automate business notifications and follow-up activities.
- Provide visibility into sales performance and service operations.
- Demonstrate maintainable, secure, and scalable solution design.

## Technology Stack

| Technology | Purpose |
|---|---|
| Dynamics 365 Sales | Lead, account, contact, and opportunity management |
| Dynamics 365 Customer Service | Case management and service processes |
| Microsoft Dataverse | Data model, relationships, and business logic |
| Power Apps | Model-driven CRM application and Canvas app |
| Power Automate | Workflow automation and notifications |
| JavaScript | Client-side form validation and user experience |
| C# and .NET | Dataverse plug-in development |
| Dataverse Web API | Data operations and integration |
| Azure Functions | Optional serverless integration demonstration |
| Power BI | Sales and customer service reporting |
| GitHub | Source control, documentation, and project tracking |

## Solution Architecture

The proposed architecture uses Dataverse as the central data platform. Dynamics 365 model-driven apps provide the primary user experience, while Power Automate orchestrates workflows and Power BI provides analytical insights.

Custom JavaScript and C# plug-ins extend standard CRM behavior where appropriate. An optional Azure Function demonstrates integration with an external system.

> Architecture and implementation status will be documented separately. Components will be marked as implemented only after they have been built and tested.

## Core Features

### 1. Sales Management
- Lead qualification and conversion.
- Account and contact management.
- Opportunity pipeline tracking.
- Product and estimated revenue management.
- Business process guidance for sales users.

### 2. Customer Service
- Customer service case registration and tracking.
- Case priority and ownership management.
- Service follow-up and escalation.
- Case resolution reporting.

### 3. Dataverse Design
- Custom tables and columns.
- One-to-many and many-to-many relationships where appropriate.
- Business rules and data validation.
- Security roles and record access design.

### 4. Workflow Automation
- Notifications for high-value opportunities.
- Follow-up reminders for overdue activities.
- Case assignment or escalation based on defined rules.
- Error handling and flow run monitoring.

### 5. Custom Development
- JavaScript form validation.
- C# plug-in enforcing a server-side business rule.
- Dataverse Web API integration example.
- Optional Azure Function integration with appropriate authentication and error handling.

### 6. Reporting and User Experience
- Sales performance dashboard.
- Open cases and service resolution metrics.
- Canvas app for service staff.
- Power BI reporting using appropriate sample data.

## Repository Structure

```text
agriNova-d365-power-platform-poc/
├── README.md
├── docs/
│   ├── business-requirements.md
│   ├── solution-architecture.md
│   ├── data-model.md
│   ├── security-design.md
│   ├── test-cases.md
│   └── deployment-guide.md
├── dataverse/
├── power-apps/
├── power-automate/
├── plugins/
├── javascript/
├── integrations/
├── power-bi/
├── screenshots/
└── releases/
```

Folders and artifacts will be added as the implementation progresses.

## Implementation Roadmap

- [ ] Document business requirements and acceptance criteria.
- [ ] Design the Dataverse data model.
- [ ] Build the Dynamics 365 model-driven application.
- [ ] Configure business rules, forms, views, and business process flows.
- [ ] Implement and test Power Automate flows.
- [ ] Develop and test JavaScript validation.
- [ ] Implement and test a C# Dataverse plug-in.
- [ ] Document and test the integration example.
- [ ] Build the Canvas app and Power BI dashboard.
- [ ] Add test results, screenshots, and deployment instructions.
- [ ] Prepare a solution export and source-control workflow.

## Testing Strategy

Testing will cover:

- Functional requirements and acceptance criteria.
- Positive and negative validation scenarios.
- Plug-in execution and exception handling.
- Power Automate success and failure paths.
- Security and record access.
- Integration failures and retry behavior, where applicable.
- Solution deployment and environment-specific configuration.

## Security and Responsible Development

- Use fictional data only.
- Never commit passwords, access tokens, connection secrets, or confidential employer/client information.
- Use environment variables and connection references where appropriate.
- Validate access permissions and authentication for integrations.
- Document prerequisites and deployment configuration.

## Project Status

**Current phase:** Foundation and requirements.

This repository is a work in progress. Features will be marked complete only after implementation and testing. Screenshots, code samples, and deployment instructions will be added as evidence of progress.

## About This Project

This project is intended to demonstrate functional consulting, Dynamics 365 configuration, Dataverse data modeling, Power Platform automation, custom development, integration design, reporting, and application lifecycle management.

## Learning Resources

- [Microsoft Power Platform](https://learn.microsoft.com/power-platform/)
- [Dynamics 365 documentation](https://learn.microsoft.com/dynamics365/)
- [Dataverse developer documentation](https://learn.microsoft.com/power-apps/developer/data-platform/)
- [Power Platform CLI solution commands](https://learn.microsoft.com/power-platform/developer/cli/reference/solution)
