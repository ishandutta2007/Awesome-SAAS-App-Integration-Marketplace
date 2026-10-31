# Awesome-SAAS-App-Integration-Marketplace

## Top SaaS App Integration Marketplace Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on App Directory Infrastructure, Connector Registries & Self-Hosted Integration Hubs*  

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **SaaS App Integration Marketplaces**. These platforms enable users to discover, install, and manage integrations within a host SaaS ecosystem—turning a product into a platform with an extensible marketplace where third-party developers can distribute connectors and apps.



**Examples** include HubSpot App Marketplace, Salesforce AppExchange (AgentExchange), Atlassian Marketplace, Google Workspace Marketplace, Zendesk Marketplace, Shopify App Store, Slack App Directory, Zapier App Directory, Microsoft AppSource, and Workato Marketplace (the category leaders).



**Open-source emphasis**: SaaS App Integration Marketplace is a domain where open-source tooling is **fragmented and largely immature for the full marketplace experience**. The strongest active project is **Tabularium**, a self-hostable plugin registry with OAuth-based ownership, linked-repo publishing via webhooks, signed releases (JWS + SHA-256 verification), and download analytics—explicitly built as a purpose-built registry rather than adapting an existing marketplace . **Open VSX** provides the vendor-neutral, open-source alternative to the Visual Studio Marketplace, backed by the Eclipse Foundation with a managed SLA tier . For integration hub infrastructure, **open-mercato's SPEC-045** defines a comprehensive Integration Marketplace architecture with encrypted credential storage, tenant isolation, and hub-spoke connector models . The critical caveat: **no open-source project replicates the distribution moats and billing integration** of Salesforce AgentExchange (10,000+ Salesforce apps, 1,000+ Agentforce components, 2,600+ Slack apps)  or the Shopify App Store (25,073 apps in the English catalog alone) .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[HubSpot App Marketplace](https://www.hubspot.com/apps)**  

  Integration marketplace for HubSpot CRM; apps are listed without requiring transactable status, though legal and security reviews are required before listing goes live.



- **[Salesforce AppExchange (AgentExchange)](https://appexchange.salesforce.com/)**  

  The oldest and most consolidated cloud marketplace, unified into **AgentExchange** in 2026—combining AppExchange, Slack Marketplace, and Agentforce into a single destination with **10,000+ Salesforce apps, 1,000+ Agentforce components, and 2,600+ Slack apps** . Features semantic search via Data 360, LLM-assisted listing authoring, MCP server publishing, and mandatory security reviews for private listings. Revenue share 15% (ISVforce) or 25% (OEM).



- **[Atlassian Marketplace](https://marketplace.atlassian.com/)**  

  App marketplace for Jira, Confluence, and Bitbucket; **7,000+ app listings**, **1.4M+ installs**, and **2,200+ partners** as of 2026 . As of June 2026, **40%+ of Atlassian customers had at least one Marketplace app installed**, with 6,000+ Cloud apps (3,700+ built on Forge) and 10,000+ custom Forge apps . Deep integration with Atlassian's Cloud and Data Center ecosystems.



- **[Google Workspace Marketplace](https://workspace.google.com/marketplace)**  

  App marketplace for Google Workspace; integrates with Gmail, Drive, Calendar, and Docs; requires Google's OAuth verification and security review.



- **[Zendesk Marketplace](https://www.zendesk.com/apps/)**  

  App directory for Zendesk support platform; apps extend ticketing, chat, and help center functionality.



- **[Shopify App Store](https://apps.shopify.com/)**  

  The **largest app marketplace by listings** with **25,073 apps in the English catalog** (August 2026 snapshot) . StoreCensus tracks **4,191+ apps** across 2.1 million stores, with **6.3 million+ total installations** and an average of **2.9 apps per store** . Hard approval process with revenue share; very high traffic for ecommerce apps.



- **[Slack App Directory](https://slack.com/apps)**  

  App directory for Slack; now unified into Salesforce's AgentExchange alongside AppExchange . Apps extend messaging, workflow automation, and third-party integrations.



- **[Zapier App Directory](https://zapier.com/apps)**  

  Integration directory for Zapier's automation platform; **9,000+ integrations** available as of October 2026 . Lists connectors that enable workflow automation between SaaS tools.



- **[Microsoft AppSource](https://appsource.microsoft.com/)**  

  Microsoft's marketplace for business apps, add-ins, and agents across Microsoft 365, Dynamics 365, and Power Platform; **19,000+ solutions** spanning over 150 countries . One of the world's largest enterprise software marketplaces.



- **[Workato Marketplace](https://www.workato.com/)**  

  Community-driven connector and recipe hub for Workato's enterprise automation platform; enables sharing of integration recipes and custom connectors.



## Open-Source GitHub Projects



### Plugin & Extension Registries



- **[Tabularium](https://codeberg.org/Tabularium/Tabularium)**  

  The most complete open-source **self-hosted plugin registry** for distributing versioned artifacts (plugins, themes, snippets, SQL templates) . Features: **multi-provider OAuth submission** (GitHub, GitLab, Gitea, Forgejo, Codeberg) with ownership verified against the linked repository; **linked-repo publishing** via webhooks—new releases are picked up automatically without maintainer intervention; **signed releases** (JWS signature + SHA-256 verification on install) with GitHub build-provenance attestation forwarding; **plugin requests** with voting and claiming; **multi-language READMEs**; **plugin type taxonomy** (Themes, Snippets, SQL templates) with separate public catalogs; **built-in CMS** with widget-enabled Markdown pages; **branding customization** (name, colors, logo, analytics); **feature flags** to disable submissions without redeployment; **audit logs** for every admin action. Stack: Bun, Elysia, SvelteKit, Drizzle ORM. **Best for teams wanting a self-hosted plugin registry** with signed releases and Git provider integration—but it is a registry/trust layer, not a commerce-enabled app store with billing.



- **[Open VSX](https://github.com/eclipse/openvsx)**  

  The **vendor-neutral, open-source alternative to the Visual Studio Marketplace** (Eclipse Foundation) . Full-stack solution: **Spring Boot backend** (PostgreSQL, Elasticsearch optional), **React web UI** (searchable gallery, admin dashboard), and **Node.js CLI** (`ovsx`) for packaging and publishing from CI. Features: **VS Code protocol compatibility** (drop-in replacement for VS Code and VSCodium); **multi-backend storage** (Local Filesystem, AWS S3, Google Cloud Storage, Azure Blob Storage); **hybrid persistence** (JPA/Hibernate for CRUD, jOOQ for complex queries). **The most mature open-source app store platform available**—but it is **VS Code extension-specific**, not a general-purpose SaaS app marketplace.



- **[BotHive](https://github.com/rishabh3562/BotHive)**  

  Open-source **AI agent and automation marketplace** for builders to list agents, workflows, and automation tools from Make, Zapier, n8n, Voiceflow, and custom platforms . Features: builder profiles with portfolios; multi-platform agent listings with file uploads (.json, .yaml, .zip), demo videos, and structured descriptions; pricing options (free, one-time, subscription); analytics dashboard (views, downloads, revenue); version control; reviews and leaderboards. Next.js 14, Supabase/MongoDB, Stripe, Tailwind. **Best for AI agent builders** wanting a marketplace to showcase and monetize automation tools—but it is an early-stage project and focused on AI agents rather than general SaaS integrations.



### Integration Hub Frameworks (Architecture Reference)



- **[open-mercato Integration Marketplace (SPEC-045)](https://github.com/open-mercato/open-mercato/blob/main/.ai/specs/SPEC-045-2026-02-24-integration-marketplace.md)**  

  A comprehensive **open-source specification for an Integration Marketplace and Connector Framework** . Defines the data model for a production integration hub: `IntegrationCredentials` (encrypted per-tenant secrets, masked on API read, hard-deleted, never logged), `IntegrationState` (enable/disable + health + API version), `IntegrationLog` (structured operation logs with secret stripping), `SyncRun`/`SyncCursor` (resumable import/export with progress), `SyncExternalIdMapping` (bidirectional entity mapping), and `SyncMapping` (persisted field mapping). Security model: tenant isolation via `organizationId + tenantId`, access control features (`integrations.view`, `.manage`, `.credentials`), and webhook verification delegated to provider adapters. **This is a specification, not a deployable product**—but it provides the most complete open-source architecture reference for building an integration marketplace with credential management, sync, and tenant isolation.



### Commerce Marketplace Engines (Build Your Own)



- **[Mercur](https://github.com/mercurjs/mercur)**  

  Open-source **multi-vendor marketplace engine** built on Medusa (MIT, ~1.6k GitHub stars) . Provides marketplace primitives: seller onboarding, multi-vendor catalogs, per-seller commissions, admin panel, separate seller portal, and automated payouts (via Stripe Connect). **Headless architecture**—you build your own storefront. **Best for teams wanting to build a commerce marketplace** (digital goods, services, or physical products) with vendor management—but it is **not a SaaS app integration marketplace** with plugin installation or runtime connector execution.



### Additional Strong Open-Source Options



- **World Vibe Web (WVW)** — Federated app store for open-source, vibe-coded projects (static site on GitHub Pages) . **No central authority**—anyone with a GitHub repo publishes an `apps.json`; a GitHub Action aggregates listings every 6 hours with live GitHub stats (stars/forks fetched, not declared), AI-curated featured apps, and guardrails against inflation. **Not a commerce-enabled marketplace**—no payments, no transactions, no integration runtime. It is a **discovery index** demonstrating the federated listing pattern.

- **MCP Marketplace (AI-Agent-Hub)** — Open-source MCP server/tool marketplace dataset and web API (32 GitHub stars) . **Niche**—for discovering Model Context Protocol servers rather than general SaaS integrations.



**Frameworks for building custom systems**: For a **self-hosted plugin registry with signed releases and Git provider integration**, Tabularium provides the most complete open-source foundation . For a **VS Code-compatible extension marketplace**, Open VSX is the only mature choice . For **AI agent marketplace listings**, BotHive offers a starting point . For **integration hub architecture with credential management and sync**, open-mercato's SPEC-045 provides the data model and security reference . **No open-source project replicates the distribution moats and billing integration** of Salesforce AgentExchange, Shopify App Store, or Atlassian Marketplace—those are platform-specific business integrations.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- SaaS app integration marketplaces handling third-party applications and user data must comply with platform security review requirements, privacy regulations (GDPR, CCPA), and revenue-sharing agreements; **listing an integration on a major marketplace often requires security certifications, code reviews, and compliance attestations**.

- **Open-source SaaS app integration marketplace infrastructure is fragmented and immature**—Tabularium provides a self-hosted plugin registry with signed releases , Open VSX provides a VS Code extension marketplace , and open-mercato provides an architecture specification for integration hubs . However, **no open-source project replicates the distribution moats, billing integration, and runtime coupling** of Salesforce AgentExchange, Shopify App Store, or Atlassian Marketplace. These platforms derive their value from access to existing user bases and integrated procurement—advantages that open-source software cannot provide.

- Verify license terms for commercial use; Tabularium is open-source (Codeberg) , Open VSX is hosted by the Eclipse Foundation , and BotHive is open-source .



---



**Made for platform engineers, developer relations teams, and organizations building or evaluating integration marketplace infrastructure.**  

Let's make SaaS app integration marketplaces more open at the registry and connector layer, but with clear eyes about the distribution and billing moats that commercial platforms still hold.
