# Pinwheel API - GraphQL Schema

This directory contains a conceptual GraphQL schema for the [Pinwheel](https://pinwheelapi.com/) payroll connectivity and income verification platform. Pinwheel provides direct integrations with 1,600+ payroll platforms, covering approximately 80% of U.S. workers, and is designated as a Consumer Reporting Agency (CRA).

The schema is derived from Pinwheel's public REST API documentation at [docs.pinwheelapi.com](https://docs.pinwheelapi.com/) and models the core resources, relationships, and operations exposed across all Pinwheel product APIs.

## Schema Source

- Provider: Pinwheel
- Source type: Conceptual (derived from REST API documentation)
- Documentation: https://docs.pinwheelapi.com/
- API Reference: https://docs.pinwheelapi.com/public/reference
- Schema file: pinwheel-api-schema.graphql

## Coverage

The schema covers all major Pinwheel product surfaces:

- **Link & Sessions** — Token minting, Link session lifecycle, LinkDetails, LinkStatus
- **End Users** — EndUser identity and account associations
- **Platforms & Employers** — Platform catalog (1,600+), PlatformType, PlatformDetails, Employer, EmployerDetails, EmployerLogo, WorkAddress
- **Accounts** — Account, EmploymentAccount, PayrollAccount, account status and metadata
- **Direct Deposit** — DirectDeposit, DirectDepositAllocation, AllocationTarget, AllocationAmount, AmountSetting, PercentSetting, NetPaySetting, DestinationAccount, BankAccount, AccountType
- **Employment** — EmploymentDetails, EmploymentType, EmploymentStatus, StartDate, CompensationType, CompensationAmount, PayPeriod, PayFrequency
- **Paystubs & Pay History** — PayStub, PayStubDetails, Paycheck, PayHistory, EarningRecord, EarningType, DeductionRecord, DeductionType, TaxRecord, NetPay
- **Income** — IncomeMetric, IncomeInsight
- **Tax Documents** — TaxDocument, W2, Form1099, DocumentType, Document
- **Identity Verification** — EmployerIDVerification
- **Jobs (Async)** — Job, JobType, JobStatus
- **Webhooks** — Webhook, WebhookEvent, WebhookEventType
- **API Keys** — APIKey
- **Analytics** — AnalyticsInsight

## Named Types

| Type | Category |
|---|---|
| Token | Link |
| Link | Link |
| LinkDetails | Link |
| LinkStatus | Link (enum) |
| EndUser | Users |
| Platform | Platforms |
| PlatformType | Platforms (enum) |
| PlatformDetails | Platforms |
| Employer | Employers |
| EmployerDetails | Employers |
| EmployerLogo | Employers |
| WorkAddress | Employers |
| Account | Accounts |
| EmploymentAccount | Accounts |
| PayrollAccount | Accounts |
| AccountType | Accounts (enum) |
| DirectDeposit | Deposit |
| DirectDepositAllocation | Deposit |
| AllocationTarget | Deposit |
| AllocationTargetType | Deposit (enum) |
| AllocationAmount | Deposit |
| AmountSetting | Deposit |
| PercentSetting | Deposit |
| NetPaySetting | Deposit |
| DestinationAccount | Deposit |
| BankAccount | Deposit |
| EmploymentDetails | Employment |
| EmploymentType | Employment (enum) |
| EmploymentStatus | Employment (enum) |
| StartDate | Employment |
| CompensationType | Employment (enum) |
| CompensationAmount | Employment |
| PayPeriod | Employment |
| PayFrequency | Employment (enum) |
| PayStub | Paystubs |
| PayStubDetails | Paystubs |
| Paycheck | Paystubs |
| PayHistory | Paystubs |
| EarningRecord | Paystubs |
| EarningType | Paystubs (enum) |
| DeductionRecord | Paystubs |
| DeductionType | Paystubs (enum) |
| TaxRecord | Paystubs |
| NetPay | Paystubs |
| IncomeMetric | Income |
| IncomeInsight | Income |
| TaxDocument | Tax |
| W2 | Tax |
| Form1099 | Tax |
| DocumentType | Tax (enum) |
| Document | Tax |
| EmployerIDVerification | Identity |
| Job | Jobs |
| JobType | Jobs (enum) |
| JobStatus | Jobs (enum) |
| Webhook | Webhooks |
| WebhookEvent | Webhooks |
| WebhookEventType | Webhooks (enum) |
| APIKey | Auth |
| AnalyticsInsight | Analytics |
| DirectDepositAllocationInput | Input |
| Query | Root |
| Mutation | Root |

## Key Relationships

- An **EndUser** has many **Accounts**; each Account is tied to a **Platform** and carries both an **EmploymentAccount** and a **PayrollAccount**.
- A **PayrollAccount** holds a **DirectDeposit** with one or more **DirectDepositAllocations**, each targeting a **DestinationAccount** (backed by a **BankAccount**).
- An **EmploymentAccount** surfaces **EmploymentDetails** including compensation, pay frequency, and employment status.
- **PayHistory** aggregates multiple **Paycheck** records; each Paycheck has a **PayStubDetails** breakdown of **EarningRecord**, **DeductionRecord**, and **TaxRecord** lines.
- **TaxDocument**, **W2**, and **Form1099** types are linked to both an **Employer** and an **EndUser**.
- **Jobs** are asynchronous operations keyed to an Account; results are delivered via **WebhookEvent** payloads.
- A **Token** scopes a **Link** session to a specific **EndUser** and set of **JobTypes**.

## Pinwheel Product API Mapping

| Pinwheel Product API | Primary GraphQL Types |
|---|---|
| Link Token API | Token, Link, LinkDetails, LinkStatus |
| Accounts API | Account, EmploymentAccount, PayrollAccount |
| Platforms API | Platform, PlatformType, PlatformDetails, Employer |
| Connected Accounts API | Account, EndUser, EmploymentDetails |
| Verify API | EmploymentDetails, IncomeMetric, PayStub, EmployerIDVerification |
| Deposit Switch API | DirectDeposit, DirectDepositAllocation, AllocationTarget |
| Taxes API | TaxDocument, W2, Form1099 |
| Bill Switch API | Job (type: BILL_SWITCH), WebhookEvent |
| Bill Manager API | AnalyticsInsight, Job (type: BILL_CANCELLATION) |
| Jobs API | Job, JobType, JobStatus |
| Webhooks API | Webhook, WebhookEvent, WebhookEventType |
