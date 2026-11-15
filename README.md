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
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)** | Cloud IAM with tenant-level administration, conditional access, and hybrid identity synchronization. **P1: $6/user/month**; P2: $9/user/month adds Identity Protection and PIM. Microsoft exerts pricing pressure on the market through Entra ID bundling . | P1: **$6/user/month**; P2: **$9/user/month** | **Free edition**: basic directory and security defaults with Azure/M365 subscriptions |
| **[Okta](https://www.okta.com/)** | Enterprise workforce and customer identity with multi-tenant org management. Workforce Starter: **$6/user/month** (annual); Enterprise: $17/user/month. | Starter: **$6/user/month**; Enterprise: **$17/user/month** | No free tier for workforce; developer edition available |
| **[Ping Identity](https://www.pingidentity.com/)** | Enterprise IAM with identity governance, lifecycle management, and **PingOne DaVinci** identity orchestration for no-code authentication journeys. **PingOne Workforce: from $3/user/month** (minimum 5,000 users); Customers: from $35,000/year [citation:5][citation:7]. | Workforce: **$3/user/month** (min 5,000); Customers: **$35,000/year** | No free tier; demo via sales |
| **[OneLogin](https://www.onelogin.com/)** | Mid-market workforce access management with clean admin console. **Advanced tier: $4/user/month**; Professional: $8/user/month (verified 2026) [citation:7]. Now part of One Identity—confirm roadmap direction with sales. | Advanced: **$4/user/month**; Professional: **$8/user/month** | Free trial available |
| **[JumpCloud](https://jumpcloud.com/)** | Cloud directory combining identity, device management, and SSO. **Free to 10 users and 10 devices**; SSO package runs **$13/user/month** [citation:7]. Replaces on-prem Active Directory while adding SSO and MDM. | **Free** (10 users); SSO: **$13/user/month** | **Free forever**: 10 users, 10 devices |
| **[Google Workspace Identity](https://workspace.google.com/)** | Identity within Google Workspace. SSO available on Business and Enterprise plans. | Business Starter: **$7/user/month** | **14-day free trial**; no permanent free tier |
| **[CyberArk Identity](https://www.cyberark.com/)** | Identity security platform with SSO, MFA, and lifecycle management. Privileged access management available as separate product. | Quote-only | Free trial available |

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
