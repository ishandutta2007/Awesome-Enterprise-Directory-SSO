# Awesome-Enterprise-Directory-SSO

## Top Enterprise Directory & SSO Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Identity Federation, Single Sign-On & Self-Hosted Identity Providers*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Directory & SSO**. These tools help organizations centralize authentication and authorization—enabling employees and customers to access multiple applications with a single set of credentials, covering everything from hyperscale identity providers to self-hosted open-source IdPs that eliminate per-user licensing.

**Examples** include Microsoft Entra ID, Okta, Ping Identity, OneLogin, JumpCloud, Keycloak, Casdoor, ZITADEL, and Authentik (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted identity providers, open-source SSO platforms, and community-driven IAM—ideal for organizations seeking data sovereignty and avoiding per-user SaaS pricing that compounds across large workforces. The open-source landscape is genuinely mature: **Keycloak** is the most widely deployed open-source IdP with proven enterprise scale , **Casdoor** offers a lightweight Go binary with built-in LDAP/RADIUS and MCP support for AI agents , and **Authentik** provides the most flexible sign-in flow engine among open-source options [citation:1][citation:14].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global Identity and Access Management (IAM), Directory, and SSO market is estimated at approximately **$21B to $25B**, expanding at a 15–25% CAGR driven by zero-trust architectures, hybrid workforce mobility, and cloud migrations. The sector displays a **moderately concentrated top-tier** dominated by hyper-scalers and established enterprise security vendors (Microsoft, Okta, CyberArk, Ping Identity) who capture ~40% of spend via bundled ecosystems, balanced by a **heavily fragmented long-tail** of specialized providers and open-source alternatives addressing niche developer, homelab, and self-hosted data-sovereignty requirements.

## SaaS/Hosted Platforms

| Product | Company Scale (Valuation / Market Cap / Revenue) | Description | Starting Pricing | Free Tier / Trial Limits |
|---------|--------------------------------------------------|-------------|------------------|--------------------------|
| **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)** | ~$3.89 Trillion (Market Cap) | Cloud IAM with tenant-level administration, conditional access, and hybrid identity synchronization. Microsoft exerts pricing pressure on the market through Entra ID bundling. | **$6/user/month** (Entra ID P1; P2 at $9/user/month) | **Free edition forever**: Core directory, self-service password reset for cloud users, and security defaults (included with Azure/M365 accounts) |
| **[Google Workspace Identity](https://workspace.google.com/)** | ~$3.5 Trillion (Alphabet Market Cap) | Cloud Identity and access management embedded in Google Workspace and GCP, providing SAML/OIDC SSO and directory services. | **$6/user/month** (Cloud Identity Premium; Business Starter: $7/user/month) | **Free edition forever**: 50 free user licenses for Cloud Identity Free (or 14-day free trial on Workspace tiers) |
| **[Okta](https://www.okta.com/)** | ~$32 Billion (Market Cap) | Enterprise workforce and customer identity with multi-tenant org management, universal directory, and workflow automation. | **$6/user/month** (Workforce Starter, annual contract; Enterprise: $17/user/month) | **30-day free trial**: Capped at 10 active users and 5 active workflows (developer free plan available with deactivation after 90 days inactivity) |
| **[CyberArk Identity](https://www.cyberark.com/)** | ~$21.1 Billion (Acquisition Valuation) | Identity security platform providing workforce SSO, Adaptive MFA, directory integration, and privileged access security. | **$2.27/user/month** (Standalone SSO; bundled Workforce Identity starts around $4–$7.20/user/month) | **30-day free trial**: Full access to SSO and Adaptive MFA for evaluation; training virtual lab environments limited to 14 days |
| **[Ping Identity](https://www.pingidentity.com/)** | ~$2.8 Billion (Buyout Valuation; ~$1B Combined ARR) | Enterprise IAM with identity governance, lifecycle management, and PingOne DaVinci identity orchestration for no-code authentication journeys. | **$3/user/month** (PingOne Workforce; minimum 5,000 users / $15,000/year commitment; Customer IAM from $35,000/year) | **30-day free trial**: Full access to PingOne Workforce evaluation environment |
| **[JumpCloud](https://jumpcloud.com/)** | ~$2.6 Billion (Valuation; ~$100M–$200M ARR) | Cloud directory platform combining identity, device management (MDM), and SSO to replace traditional Active Directory. | **$13/user/month** (SSO Package; Core Directory starts at $11/user/month) | **Free edition forever**: Fully functional up to 10 users and 10 devices |
| **[OneLogin](https://www.onelogin.com/)** | ~$500 Million (Acquisition Valuation; ~$70M+ ARR) | Mid-market workforce access management offering cloud directory, single sign-on, and policy management under One Identity. | **$4/user/month** (Advanced plan; Professional plan: $8/user/month) | **30-day free trial**: Limited to ~10–12 test user seats for administrative POC evaluation |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Keycloak](https://github.com/keycloak/keycloak)** | [![Stars](https://img.shields.io/github/stars/keycloak/keycloak?style=social&color=white)](https://github.com/keycloak/keycloak/stargazers) | **The most widely deployed open-source identity provider with proven enterprise scale.** Apache-2.0, Java/Quarkus. **Realms provide multi-tenancy**—each manages its own users, roles, clients, and authentication policies independently. Supports OAuth 2.0, OIDC, SAML, and LDAP federation. **SCIM 2.0 server support added in 26.8** for receiving users from Entra ID and Okta [citation:1]. **Strongest for Java developers** with the most extension points (SPIs) among open-source IdPs [citation:1][citation:14]. **Best for enterprises needing battle-tested identity with deep Java customization.** |
| **[Casdoor](https://github.com/casdoor/casdoor)** | [![Stars](https://img.shields.io/github/stars/casdoor/casdoor?style=social&color=white)](https://github.com/casdoor/casdoor/stargazers) | **Lightweight Go-based IAM with the widest protocol coverage.** Apache-2.0. **Single Go binary + React UI**—no JVM, no separate worker or cache process. **Built-in CAS server, LDAP server, RADIUS server, and MCP server with OAuth 2.1 for AI agents**—no other open-source IdP offers these natively [citation:1][citation:14]. **70+ social/enterprise providers** including WeChat, DingTalk, and Lark. Multi-tenancy via Organizations. **Syncers import users from Keycloak, Okta, Entra ID, Google Workspace, and any SQL database**—enabling gradual migration [citation:14]. **Best for teams wanting a lighter, UI-first IdP with legacy protocol support and AI-agent readiness.** |
| **[Authentik](https://github.com/goauthentik/authentik)** | [![Stars](https://img.shields.io/github/stars/goauthentik/authentik?style=social&color=white)](https://github.com/goauthentik/authentik/stargazers) | **The most flexible open-source sign-in flow engine.** MIT core with paid enterprise features. Python and Go. **Flows and stages** edited in the admin interface—enables complex custom authentication logic without code. **SCIM provider (push users to other apps)**—a capability Keycloak and Casdoor lack [citation:1]. Proxy provider for Traefik, Caddy, Nginx, and Envoy. **Best for teams needing maximum sign-in flow flexibility** and SCIM provisioning to downstream apps. |
| **[ZITADEL](https://github.com/zitadel/zitadel)** | [![Stars](https://img.shields.io/github/stars/zitadel/zitadel?style=social&color=white)](https://github.com/zitadel/zitadel/stargazers) | **Event-sourced IAM with strict tenant isolation.** AGPL-3.0, Go/TypeScript. **Instances and organizations** provide hierarchical multi-tenancy. **Every mutation is an immutable event** for complete, API-accessible audit trails. Actions (scripts and webhooks) for custom logic. **Best for organizations needing the strongest audit trail and tenant hierarchy** with a modern API-first design [citation:1]. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Authelia](https://github.com/authelia/authelia)** | [![Stars](https://img.shields.io/github/stars/authelia/authelia?style=social&color=white)](https://github.com/authelia/authelia/stargazers) | **Open-source authentication and authorization server providing 2FA and SSO for web applications** (28.1k stars). Go-based. Lightweight companion for protecting internal services behind a reverse proxy [citation:11]. **Best for homelabs and small teams** needing SSO without a full IdP. |
| **[Ory Polis (BoxyHQ Jackson)](https://github.com/ory/polis)** | [![Stars](https://img.shields.io/github/stars/ory/polis?style=social&color=white)](https://github.com/ory/polis/stargazers) | **Enterprise SSO service that bridges SAML and OIDC to OAuth 2.0, with SCIM 2.0 directory sync** (2.2k stars). TypeScript. **Best for SaaS products needing to accept enterprise customer IdPs** without building SAML parsing from scratch [citation:11]. |
| **[OpenAM](https://github.com/OpenIdentityPlatform/OpenAM)** | [![Stars](https://img.shields.io/github/stars/OpenIdentityPlatform/OpenAM?style=social&color=white)](https://github.com/OpenIdentityPlatform/OpenAM/stargazers) | **Long-standing open-source access management with SSO, authorization, and federation** (876 stars). Java. Community fork of the original ForgeRock OpenAM. **Best for organizations with existing OpenAM deployments** or legacy federation requirements [citation:2][citation:11]. |

**Frameworks for building custom systems**: Choose **Keycloak** for proven enterprise identity with the broadest Java extension ecosystem , **Casdoor** for a lightweight Go binary with built-in LDAP/RADIUS and AI-agent MCP support , **Authentik** for the most flexible sign-in flows and SCIM provisioning , or **ZITADEL** for event-sourced audit trails and strict tenant isolation —all without per-user pricing that compounds across large workforces.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Enterprise directory and SSO platforms handle authentication credentials and identity data; enforce MFA, least-privilege access, and compliance with applicable regulations (GDPR, SOC 2, HIPAA where relevant). **A compromised IdP exposes every connected application.**
- **Open-source IdPs have different trade-offs across four leading projects.** **Keycloak** is the most widely deployed with the deepest Java extension points, but requires JVM expertise and is heavier to operate than single-binary alternatives [citation:1][citation:14]. **Casdoor** is the lightest to run (single Go binary) and uniquely offers **built-in LDAP/RADIUS servers and MCP support for AI agents**, but has a smaller community than Keycloak [citation:1][citation:14]. **Authentik** has the **most flexible sign-in flow engine** and the only SCIM provider among the four, but its core is MIT with enterprise features under a commercial license [citation:1]. **ZITADEL** provides the strongest audit trail through event sourcing, but its AGPL-3.0 license may matter for some organizations [citation:1]. **Commercial platforms are quote-only at enterprise scale** except Microsoft Entra ID ($6–$9/user/month), Okta ($6–$17/user/month), OneLogin ($4–$8/user/month), and JumpCloud ($13/user/month SSO) [citation:7]. **Validate protocol requirements (LDAP, RADIUS, CAS), multi-tenancy model, and operational capacity** before committing.

---

**Made for identity architects, IT administrators, and organizations building authentication infrastructure.**  
Let's make enterprise directory and SSO more open, interoperable, and secure.
