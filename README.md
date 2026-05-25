# Pinwheel (pinwheel-api)

Pinwheel is an employment and income data platform that connects banks, fintechs, and lenders directly to payroll systems. The API covers direct deposit switching (PreMatch, NativeLink), income and employment verification, paystub and shift data, tax form retrieval (W-2, 1099), bill switch, and bill manager. Pinwheel maintains direct integrations with 1,600+ payroll platforms covering an estimated 80% of U.S. workers and is the first Consumer Reporting Agency (CRA) in the payroll-connectivity space.

**URL:** [Visit APIs.json URL](https://pinwheelapi.com/)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Employment, Income, Payroll, Direct Deposit, Identity, Verification, Financial, Tax, Bill Pay

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Pinwheel Deposit Switch API

The Pinwheel Deposit Switch API automates moving a customer's direct deposit allocations from one financial institution to another by connecting directly to 17,000+ payroll providers. The product combines PreMatch (credential-less I-9 matching covering ~40% of U.S. workers), NativeLink (device-saved credentials), and Forms (pre-filled submission templates) routed by a Prime algorithm that picks the highest-converting path per user. Banks, credit unions, and fintechs use it to win banking primacy through 2X conversion lifts, 65% faster funding, and double-digit increases in average balance and lifetime value.

**Human URL:** [https://pinwheelapi.com/products/deposit-switch](https://pinwheelapi.com/products/deposit-switch)

#### Tags:

 - Direct Deposit, Switch, PreMatch, NativeLink, Payroll

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/direct-deposit-switch)

### Pinwheel Verify API

Pinwheel Verify is a payroll-connected income and employment verification API that returns identity, employment status and dates, current and historical paystubs, shifts (for hourly workers), and tax forms pulled directly from the source payroll system. Mortgage lenders, auto lenders, personal-loan and BNPL providers, property managers, and gig platforms use Verify as a real-time, consent-based alternative to Work Number / pay-stub uploads. Pinwheel operates as a Consumer Reporting Agency (CRA), making Verify reports usable for FCRA-covered underwriting decisions.

**Human URL:** [https://pinwheelapi.com/products/verify](https://pinwheelapi.com/products/verify)

#### Tags:

 - Income, Employment, Identity, Paystubs, Shifts, Verification, Lending

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/verify)

### Pinwheel Taxes API

The Pinwheel Taxes API retrieves W-2, 1099-K, 1099-MISC, and 1099-NEC documents directly from a worker's payroll provider, returning them as both PDF and structured JSON. Tax-prep software, gig platforms, and lenders use it to skip manual uploads, drive faster filing flows, power quarterly tax-estimation tools for 1099 earners, optimize W-4 withholding from historical data, and pull tax-form-based earnings totals into income and employment verification decisions.

**Human URL:** [https://pinwheelapi.com/products/taxes](https://pinwheelapi.com/products/taxes)

#### Tags:

 - Tax, W-2, 1099, Tax Forms, Payroll

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/taxes)

### Pinwheel Bill Switch API

The Pinwheel Bill Switch API updates a user's stored payment method across merchant and biller accounts (streaming, telecom, utilities, insurance, subscriptions) so that a financial institution can move recurring card-on-file payments to its own card. Issuers and challenger banks use Bill Switch alongside Deposit Switch to capture recurring spend and become the primary payment instrument for the customer's everyday obligations.

**Human URL:** [https://pinwheelapi.com/products/bill-switch](https://pinwheelapi.com/products/bill-switch)

#### Tags:

 - Bill Pay, Card Switching, Merchant, Recurring Payments

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/bill-switch)

### Pinwheel Bill Manager API

Pinwheel Bill Manager detects, organizes, and acts on a customer's recurring bills and subscriptions. It auto-identifies recurring charges with 80% greater accuracy than category-based detection, surfaces them in a manageable list, and supports targeted actions including bill switch and bill cancellation. Banks, fintechs, and personal-finance apps use it to give customers a single pane of glass for recurring obligations and to lift engagement on bill-pay surfaces.

**Human URL:** [https://pinwheelapi.com/products/bill-manager](https://pinwheelapi.com/products/bill-manager)

#### Tags:

 - Bill Pay, Recurring Payments, Bill Detection, Subscriptions, Cancellation

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/bill-manager)

### Pinwheel Switch Kit API

Switch Kit bundles Pinwheel's Deposit Switch and Bill Switch products into a single onboarding experience banks and fintechs can drop into account-opening and reactivation flows. It is the productized answer to "make this account my primary account" — moving paycheck deposits in and recurring outflows over in one consented session.

**Human URL:** [https://pinwheelapi.com/](https://pinwheelapi.com/)

#### Tags:

 - Switch Kit, Direct Deposit, Bill Pay, Onboarding, Activation

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/switch-kit)

### Pinwheel Connected Accounts API

The Pinwheel Connected Accounts API gives applications ongoing, consented access to a user's payroll and external-account data after the initial link. Builders use it to keep employment, income, and account attributes fresh for credit decisioning, account servicing, and re-underwriting workflows without forcing the end user to relink each time.

**Human URL:** [https://pinwheelapi.com/](https://pinwheelapi.com/)

#### Tags:

 - Account Linking, Employment Data, Income Data, External Accounts

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/connected-accounts)

### Pinwheel Link Token API

The Pinwheel Link Token API mints short-lived link_tokens that initialize the Pinwheel Link drop-in UI (Web, iOS, Android, React Native, Flutter, Capacitor). The token scopes the session to a specific end user, a chosen job (direct deposit switch, paystubs, employment, identity, income, shifts, tax forms, bill switch, bill cancellation), and the configured environment (sandbox or production).

**Human URL:** [https://docs.pinwheelapi.com/public/reference/post_v1-link-tokens](https://docs.pinwheelapi.com/public/reference/post_v1-link-tokens)

#### Tags:

 - Link, Tokens, Authentication, Onboarding

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/link)

### Pinwheel Accounts API

The Pinwheel Accounts API exposes the linked payroll accounts a user has connected through Pinwheel Link, surfacing account-level metadata such as platform, status, employment relationship, and supported job types so downstream services can decide what data to request next.

**Human URL:** [https://docs.pinwheelapi.com/public/reference/accounts](https://docs.pinwheelapi.com/public/reference/accounts)

#### Tags:

 - Accounts, Payroll, Employment, Linked Accounts

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/accounts)

### Pinwheel Jobs API

The Pinwheel Jobs API is the asynchronous execution surface for every Pinwheel job — direct_deposit_switch, direct_deposit_allocations, paystubs, employment, identity, income, shifts, tax_forms, bill_switch, and bill_cancellation. Clients create, monitor, and retrieve job state through this API, with results delivered via webhook callbacks and on-demand polling.

**Human URL:** [https://docs.pinwheelapi.com/public/reference/jobs](https://docs.pinwheelapi.com/public/reference/jobs)

#### Tags:

 - Jobs, Async, Status, Direct Deposit Switch, Paystubs, Employment, Identity, Income, Shifts, Tax Forms

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/jobs)

### Pinwheel Platforms API

The Pinwheel Platforms API exposes the catalog of supported payroll providers and employer-side platforms (ADP, Workday, Paychex, Paycom, Gusto, Rippling, plus 1,600+ others). Clients use it to check coverage, surface platform-specific UX cues, and route users to the correct Link experience.

**Human URL:** [https://docs.pinwheelapi.com/public/reference/platforms](https://docs.pinwheelapi.com/public/reference/platforms)

#### Tags:

 - Platforms, Payroll Providers, Coverage, Employers

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/platforms)

### Pinwheel Webhooks API

The Pinwheel Webhooks API is how the platform delivers asynchronous events — job completions, link events, account status changes, deposit switch outcomes, tax-form availability, and banking events — to client systems. It supports HMAC signature verification and optional payload encryption for sensitive event types.

**Human URL:** [https://docs.pinwheelapi.com/public/docs/webhooks](https://docs.pinwheelapi.com/public/docs/webhooks)

#### Tags:

 - Webhooks, Events, Signatures, Payload Encryption

#### Properties

- [Documentation](https://docs.pinwheelapi.com/public/docs/webhooks)

## Common Properties

- [Portal](https://pinwheelapi.com/)
- [Documentation](https://docs.pinwheelapi.com/)
- [APIReference](https://docs.pinwheelapi.com/public/reference)
- [GettingStarted](https://docs.pinwheelapi.com/public/docs/getting-started)
- [ChangeLog](https://docs.pinwheelapi.com/public/changelog)
- [StatusPage](https://www.pinwheelapistatus.com/)
- [SignUp](https://app.getpinwheel.com/signup)
- [Login](https://app.getpinwheel.com/login)
- [Sandbox](https://docs.pinwheelapi.com/public/docs/sandbox)
- [Authentication](https://docs.pinwheelapi.com/public/docs/authentication)
- [Webhooks](https://docs.pinwheelapi.com/public/docs/webhooks)
- [GitHubOrganization](https://github.com/underdog-tech)
- [LinkedIn](https://www.linkedin.com/company/pinwheel-api/)
- [Blog](https://pinwheelapi.com/blog)
- [Pinwheel iOS SDK](https://github.com/underdog-tech/pinwheel-ios-sdk)
- [Pinwheel Android SDK](https://github.com/underdog-tech/pinwheel-android-sdk)
- [Pinwheel React Native SDK](https://github.com/underdog-tech/react-native-pinwheel)
- [Pinwheel Flutter SDK](https://github.com/underdog-tech/pinwheel-flutter-sdk)
- [Pinwheel Capacitor SDK](https://github.com/underdog-tech/pinwheel-capacitor-sdk)

## Features

| Name | Description |
|------|-------------|
| Direct Deposit Switch | Move a customer's direct deposit allocations to a new institution via PreMatch (credential-less I-9 match), NativeLink (device-saved credentials), or Forms; routed by the Prime algorithm for highest conversion. |
| Income & Employment Verification (Verify) | Real-time payroll-connected verification returning identity, employment status, paystubs, shifts, and tax forms from the source payroll system. |
| Tax Form Retrieval | Pull W-2, 1099-K, 1099-MISC, and 1099-NEC documents directly from payroll providers as PDF and structured JSON. |
| Bill Switch | Update stored payment methods across merchant and biller accounts so issuers can capture recurring card-on-file spend. |
| Bill Manager | Auto-detect, organize, and act on recurring bills and subscriptions with 80% greater accuracy than category-based detection. |
| Switch Kit | Bundled Deposit Switch + Bill Switch onboarding flow productized for primary-banking activation. |
| Connected Accounts | Ongoing consented access to payroll and external account data for re-underwriting, servicing, and credential refresh. |
| Pinwheel Link | Drop-in UI for Web, iOS, Android, React Native, Flutter, and Capacitor that handles consent, MFA, and credential capture across 1,600+ payroll platforms. |
| Consumer Reporting Agency (CRA) Status | First payroll-connectivity provider designated as a CRA, allowing Verify outputs to be used directly in FCRA-governed credit decisions. |
| Coverage | 1,600+ supported payroll platforms reaching an estimated 80% of U.S. workers. |
| Webhooks with Signing & Optional Payload Encryption | Asynchronous event delivery for job completions, link events, account status changes, and banking events with HMAC signatures and optional encryption. |
| Sandbox Environment | Full-feature sandbox with synthetic users, employers, jobs, and webhook event simulation. |
| Versioned API | Dated API versions selectable via header (v2022-03-02 through v2025-07-08+). |

## Use Cases

| Name | Description |
|------|-------------|
| Banking Primacy | National banks, credit unions, and challenger banks use Deposit Switch + Bill Switch to make a newly-opened account the customer's primary financial relationship. |
| Mortgage & Auto Lending | Lenders use Verify as a real-time alternative to Work Number for payroll-direct income and employment verification. |
| Personal Loan / BNPL Underwriting | Consumer lenders use Verify and Connected Accounts to refresh income at underwriting and during re-pricing windows. |
| Tax Preparation | Tax-prep software uses the Taxes API to skip manual W-2 / 1099 uploads and pull forms directly from payroll. |
| Gig Worker Quarterly Tax Estimation | Gig platforms use prior-year 1099 retrieval to power quarterly self-employment tax estimates for their workers. |
| Property Management & Rental Screening | Property managers use Verify to confirm tenant employment and income at application time. |
| Subscription & Recurring Bill Management | Personal finance apps and challenger banks use Bill Manager to give users a single view of recurring obligations with one-click switch and cancel. |

## Integrations

| Name | Description |
|------|-------------|
| ADP | Direct payroll-provider integration for verification, paystubs, and deposit allocation. |
| Workday | Direct payroll-provider integration covering enterprise employers. |
| Paychex | SMB-focused payroll integration. |
| Paycom | Mid-market payroll integration. |
| Gusto | SMB cloud payroll integration covering startups and small employers. |
| Rippling | HRIS + payroll integration. |
| 1,600+ Additional Payroll Platforms | Long-tail coverage including local processors, government payroll, and industry-specific systems. |

## Solutions

| Name | Description |
|------|-------------|
| For Banks & Credit Unions | Primary banking activation via Switch Kit; deposit and recurring-payment capture to drive balance, engagement, and lifetime value. |
| For Lenders | FCRA-grade payroll-connected income, employment, and tax-form verification for mortgage, auto, personal loan, and BNPL underwriting. |
| For Fintechs & Challenger Banks | Drop-in Pinwheel Link plus Connected Accounts to power onboarding, direct deposit capture, and ongoing data refresh. |
| For Tax & Payroll Software | Direct W-2/1099 retrieval and tax-platform webhooks for tax-prep flows and gig-worker tax tools. |
| For Property Managers & Gig Platforms | Real-time employment and income verification at application time, plus shift data for hourly workers. |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
