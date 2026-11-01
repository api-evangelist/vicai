# Vic.ai

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Vic.ai builds AI-native software for enterprise Accounts Payable and finance teams, automating the end-to-end AP workflow: invoice capture from email/SFTP/API/mobile, AI extraction of header and line-level data, GL coding, purchase-order matching, approval routing, bill pay and vendor portals, corporate-card expense management, and analytics. It integrates with major ERPs (SAP, Oracle, Microsoft Dynamics, NetSuite, Workday, Coupa). The public Vic.ai API (docs.vic.ai) is an ERP-integration surface with 173 operations across invoices, purchase orders, payments, masterdata sync, and webhooks, authenticated with client-credentials Bearer JWTs. Vic.ai holds SOC 1/SOC 2 Type II and operates on an ISO 27001 framework. Backed by Cowboy Ventures, GGV Capital, and ICONIQ Capital.

**Areas:** Company · Fintech · Accounts Payable · Invoicing · Payments · ERP Integration · Artificial Intelligence · Finance Automation · Webhook

## Vic.ai on APIs.io

Everything profiled for Vic.ai is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/vicai/](https://apis.io/providers/vicai/)** — or go straight to one of the APIs or properties below.

### APIs (33)

- [Vic.ai Accounts API](https://apis.io/apis/vicai/vicai-accounts-api/) — GL (General Ledger) accounts are part of your *ERP* **Masterdata**. In order to be associated with an invoice line item, key data about the account must be…
- [Vic.ai Allowed Senders API](https://apis.io/apis/vicai/vicai-allowed-senders-api/) — Restricts which sender addresses an email endpoint will accept. Each entry is either an `exact` match (full email address) or a `domain` match (everything…
- [Vic.ai Attachments API](https://apis.io/apis/vicai/vicai-attachments-api/) — Attachments are original invoice documents that can be processed by Vic.ai. ## Supported content types - `application/msword` - `application/pdf` -…
- [Vic.ai Authentication API](https://apis.io/apis/vicai/vicai-authentication-api/) — To initiate the authentication process, send a POST request to `/v0/token` with the payload as shown in the example below: ```json { "client_id":…
- [Vic.ai Beta Features API](https://apis.io/apis/vicai/vicai-beta-features-api/) — These are features that are not quite ready for general consumption and are liable to change. We will try not to break what is provided, but we can not…
- [Vic.ai Bills API](https://apis.io/apis/vicai/vicai-bills-api/) — Bills are imported invoices that can be created and updated through the API. These operations allow you to create new bills and update existing ones that…
- [Vic.ai Companies API](https://apis.io/apis/vicai/vicai-companies-api/) — The companies in the Vic system.
- [Vic.ai Company Settings API](https://apis.io/apis/vicai/vicai-company-settings-api/) — Per-company configuration options that an integration partner can read and tune programmatically rather than by asking Vic.ai support. Requires partner…
- [Vic.ai Credit Confirmations API](https://apis.io/apis/vicai/vicai-credit-confirmations-api/) — Confirm or mark credits as failed after processing in your ERP.
- [Vic.ai CSV Reports API](https://apis.io/apis/vicai/vicai-csv-reports-api/) — Generate and retrieve reports
- [Vic.ai Dimensions API](https://apis.io/apis/vicai/vicai-dimensions-api/) — Dimensions are part of your *ERP* **Masterdata**, and represent business categories that are associated with invoice line items, that Vic.ai can…
- [Vic.ai Email Endpoints API](https://apis.io/apis/vicai/vicai-email-endpoints-api/) — Email endpoints are dedicated email addresses that Vic.ai monitors so your team can forward or send invoices, contracts, or receipts in by email. Each…
- [Vic.ai Invoice Approval Flows API](https://apis.io/apis/vicai/vicai-invoice-approval-flows-api/) — Invoice approval flows define the criteria and steps for processing invoices through an approval workflow. These operations allow you to create, update, and…
- [Vic.ai Invoices API](https://apis.io/apis/vicai/vicai-invoices-api/) — These routes give you read-only access to two types of invoices: - Invoices which have not yet been posted to the ERP system (restricted access). - Invoices…
- [Vic.ai Organizations API](https://apis.io/apis/vicai/vicai-organizations-api/) — Organizations within the Vic system. The old name for this resource is Account Firm. We are transitioning to the name of Organization.
- [Vic.ai Partners API](https://apis.io/apis/vicai/vicai-partners-api/) — Partner API for integration providers to provision new organizations and companies. Requires partner-level credentials obtained from Vic.
- [Vic.ai Payment Batches API](https://apis.io/apis/vicai/vicai-payment-batches-api/) — List and inspect payment batches.
- [Vic.ai Payment Confirmations API](https://apis.io/apis/vicai/vicai-payment-confirmations-api/) — Confirm or mark payments as failed after processing in your ERP.
- [Vic.ai Payment Terms API](https://apis.io/apis/vicai/vicai-payment-terms-api/) — Payment terms are part of your *ERP* **Masterdata**, and represent payment terms that Vic.ai can automatically assign to invoices. Some vendors may have a…
- [Vic.ai Purchase Order Line Items API](https://apis.io/apis/vicai/vicai-purchase-order-line-items-api/) — Manage individual line items within a purchase order.
- [Vic.ai Purchase Orders API](https://apis.io/apis/vicai/vicai-purchase-orders-api/) — The purchase orders.
- [Vic.ai Status API](https://apis.io/apis/vicai/vicai-status-api/) — Status requests on the state of the Vic.ai system.
- [Vic.ai Synchronizing API](https://apis.io/apis/vicai/vicai-synchronizing-api/) — Synchronization is explicit and it is up to the integration to call each resource in the order deemed appropriate. When calling any synchronization…
- [Vic.ai Tags API](https://apis.io/apis/vicai/vicai-tags-api/) — Tags are part of your *ERP* **Masterdata**, and represent business categories that are associated with certain entities, like Vendor.
- [Vic.ai Tax Codes API](https://apis.io/apis/vicai/vicai-tax-codes-api/) — The tax codes.
- [Vic.ai Training Invoices API](https://apis.io/apis/vicai/vicai-training-invoices-api/) — Training invoices are historical invoices used to train your company's AI model. By providing past invoices with their correct GL coding, vendor…
- [Vic.ai Users API](https://apis.io/apis/vicai/vicai-users-api/) — Managing users in the Vic system. You are allowed to add and remove users from companies and organizations along with managing some of their attributes.…
- [Vic.ai VAT Codes API](https://apis.io/apis/vicai/vicai-vat-codes-api/) — In some regions, VAT codes are part of your *ERP* **Masterdata**, that represent timeboxed VAT codes and VAT values that Vic.ai can automatically assign to…
- [Vic.ai Vendor Groups API](https://apis.io/apis/vicai/vicai-vendor-groups-api/) — Vendors can be grouped together in Vic.ai. This is especially useful for purchase order matching where you want to match a purchase order to a group of vendors.
- [Vic.ai Vendor Tags API](https://apis.io/apis/vicai/vicai-vendor-tags-api/) — Vendor tags are used to categorize vendors using tags.
- [Vic.ai Vendors API](https://apis.io/apis/vicai/vicai-vendors-api/) — Vendors are part of your *ERP* **Masterdata**, and represent companies that produce invoices. In order to be associated with an invoice, key data about the…
- [Vic.ai Webhook Events API](https://apis.io/apis/vicai/vicai-webhook-events-api/) — These are the `V1` events you can subscribe to. These will be sent as a `POST` to `https://yourCallbackUrl/events`. * `all` - This is a special form, that…
- [Vic.ai Webhook Subscriptions API](https://apis.io/apis/vicai/vicai-webhook-subscriptions-api/) — Webhook subscriptions control which events your system receives and where they are delivered. Each company may have one V0 subscription or multiple V2…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Vicai Webhooks](https://apis.io/asyncapis/vicai/vicai-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [vicai](https://apis.io/servers/vicai/vicai/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Vicai Agentic Access](https://apis.io/agentic-access/vicai/vicai-agentic-access/)

#### Collections (33)

Postman and Open Collection request collections.

- [Vic.ai Accounts API](https://apis.io/collections/vicai/open-vicai-accounts-api/)
- [Vic.ai Accounts Allowed Senders API](https://apis.io/collections/vicai/open-vicai-allowed-senders-api/)
- [Vic.ai Accounts Attachments API](https://apis.io/collections/vicai/open-vicai-attachments-api/)
- [Vic.ai Accounts Authentication API](https://apis.io/collections/vicai/open-vicai-authentication-api/)
- [Vic.ai Accounts Beta Features API](https://apis.io/collections/vicai/open-vicai-beta-features-api/)
- [Vic.ai Accounts Bills API](https://apis.io/collections/vicai/open-vicai-bills-api/)
- [Vic.ai Accounts Companies API](https://apis.io/collections/vicai/open-vicai-companies-api/)
- [Vic.ai Accounts Company Settings API](https://apis.io/collections/vicai/open-vicai-company-settings-api/)
- [Vic.ai Accounts Credit Confirmations API](https://apis.io/collections/vicai/open-vicai-credit-confirmations-api/)
- [Vic.ai Accounts CSV Reports API](https://apis.io/collections/vicai/open-vicai-csv-reports-api/)
- [Vic.ai Accounts Dimensions API](https://apis.io/collections/vicai/open-vicai-dimensions-api/)
- [Vic.ai Accounts Email Endpoints API](https://apis.io/collections/vicai/open-vicai-email-endpoints-api/)
- [Vic.ai Accounts Invoice Approval Flows API](https://apis.io/collections/vicai/open-vicai-invoice-approval-flows-api/)
- [Vic.ai Accounts Invoices API](https://apis.io/collections/vicai/open-vicai-invoices-api/)
- [Vic.ai Accounts Organizations API](https://apis.io/collections/vicai/open-vicai-organizations-api/)
- [Vic.ai Accounts Partners API](https://apis.io/collections/vicai/open-vicai-partners-api/)
- [Vic.ai Accounts Payment Batches API](https://apis.io/collections/vicai/open-vicai-payment-batches-api/)
- [Vic.ai Accounts Payment Confirmations API](https://apis.io/collections/vicai/open-vicai-payment-confirmations-api/)
- [Vic.ai Accounts Payment Terms API](https://apis.io/collections/vicai/open-vicai-payment-terms-api/)
- [Vic.ai Accounts Purchase Order Line Items API](https://apis.io/collections/vicai/open-vicai-purchase-order-line-items-api/)
- [Vic.ai Accounts Purchase Orders API](https://apis.io/collections/vicai/open-vicai-purchase-orders-api/)
- [Vic.ai Accounts Status API](https://apis.io/collections/vicai/open-vicai-status-api/)
- [Vic.ai Accounts Synchronizing API](https://apis.io/collections/vicai/open-vicai-synchronizing-api/)
- [Vic.ai Accounts Tags API](https://apis.io/collections/vicai/open-vicai-tags-api/)
- [Vic.ai Accounts Tax Codes API](https://apis.io/collections/vicai/open-vicai-tax-codes-api/)
- …and 8 more published on APIs.io

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Vicai Overlay](https://apis.io/overlays/vicai/vicai-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Vicai Authentication](https://apis.io/security/vicai/vicai-authentication/)
- [Vicai Domain Security](https://apis.io/security/vicai/vicai-domain-security/)
- [Vicai Trust Center](https://apis.io/security/vicai/vicai-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Vicai Plans Pricing](https://apis.io/plans/vicai/vicai-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Vicai Rate Limits](https://apis.io/rate-limits/vicai/vicai-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.vic.ai)
- [Documentation](https://docs.vic.ai)
- [Getting started](https://docs.vic.ai)
- [API reference](https://docs.vic.ai)
- [Pricing](https://www.vic.ai/pricing)
- [Sign up](https://www.vic.ai/book-a-demo)
- [Support](https://www.vic.ai/contact-us)
- [Blog](https://www.vic.ai/blog)
- [Compliance](https://www.vic.ai/trust-and-security)
- [Terms of service](https://www.vic.ai/terms-of-service)
- [Privacy policy](https://www.vic.ai/privacy-policy)
- [GitHub](https://github.com/Vic-ai)

## API Evangelist rating

**Kin Score 59.2** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 60.3 |
| Contract governance | 4.5 |
| Operational transparency | 47.4 |
| Developer ergonomics | 58.9 |
| Access clarity | 60.5 |

**Agent readiness 32.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | verified |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | — |

**Regulatory alignment 25.0** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/vicai/](https://apis.io/providers/vicai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Vic.ai: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/vicai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
