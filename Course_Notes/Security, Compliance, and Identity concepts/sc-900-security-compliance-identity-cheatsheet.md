# SC-900 Cheat Sheet
## Describe the Concepts of Security, Compliance, and Identity (10–15%)

> Quick-reference notes for the SC-900: Microsoft Security, Compliance, and Identity Fundamentals exam.

---

## Table of Contents

- [1. Security and Compliance Concepts](#1-security-and-compliance-concepts)
  - [Shared Responsibility Model](#shared-responsibility-model)
  - [Defense-in-Depth](#defense-in-depth)
  - [Zero Trust Model](#zero-trust-model)
  - [Encryption and Hashing](#encryption-and-hashing)
  - [Governance, Risk, and Compliance (GRC)](#governance-risk-and-compliance-grc)
- [2. Identity Concepts](#2-identity-concepts)
  - [Identity as the Primary Security Perimeter](#identity-as-the-primary-security-perimeter)
  - [Authentication (AuthN)](#authentication-authn)
  - [Authorization (AuthZ)](#authorization-authz)
  - [Identity Providers (IdP)](#identity-providers-idp)
  - [Directory Services & Active Directory](#directory-services--active-directory)
  - [Federation](#federation)
- [Quick-Fire Recap](#quick-fire-recap)

---

## 1. Security and Compliance Concepts

### Shared Responsibility Model
Security responsibilities are split between the cloud provider and the customer, and the split shifts depending on the service type.

| Layer | On-Prem | IaaS | PaaS | SaaS |
|---|---|---|---|---|
| Data classification & accountability | Customer | Customer | Customer | Customer |
| Client/endpoint protection | Customer | Customer | Customer | Customer |
| Identity & access management | Customer | Customer | Customer/Shared | Shared |
| Application | Customer | Customer | Shared | Provider |
| Network controls | Customer | Customer/Shared | Provider | Provider |
| Operating system | Customer | Customer | Provider | Provider |
| Physical hosts/network/datacenter | Customer | Provider | Provider | Provider |

**Key idea:** The customer *always* retains responsibility for data, devices, and identities — no matter the model.

---

### Defense-in-Depth
Layered security so that if one layer fails, others still protect the resource.

**Layers (outside → in):**
1. **Physical security** – datacenter access, locks, cameras
2. **Identity & access** – authN/authZ, conditional access
3. **Perimeter** – DDoS protection, firewalls at network edge
4. **Network** – segmentation, NSGs, restrict traffic
5. **Compute** – endpoint protection, patching, VM security
6. **Application** – secure dev (SDL), removing vulnerabilities
7. **Data** – encryption, access controls on databases/storage

> Mnemonic: **P-I-P-N-C-A-D**

---

### Zero Trust Model
Assumes breach — never trust, always verify. Replaces "trust but verify perimeter" with continuous verification.

**Three guiding principles:**
- **Verify explicitly** – always authenticate/authorize based on all available data points (identity, location, device, service, data classification, anomalies)
- **Use least privilege access** – limit access with Just-In-Time (JIT), Just-Enough-Access (JEA), risk-based adaptive policies
- **Assume breach** – minimize blast radius, segment access, use encryption, analytics for detection/response

**Six foundational pillars:** Identities, Devices, Applications, Data, Infrastructure, Networks

---

### Encryption and Hashing

| Concept | Description | Reversible? |
|---|---|---|
| **Symmetric encryption** | Same key encrypts & decrypts (fast, used for bulk data) | Yes |
| **Asymmetric encryption** | Public key encrypts, private key decrypts (used for key exchange, signing) | Yes |
| **Hashing** | Converts data to a fixed-size value (hash); used to verify integrity | **No** (one-way) |

**Encryption states:**
- **At rest** – data stored on disk (e.g., BitLocker, Storage Service Encryption)
- **In transit** – data moving over a network (e.g., TLS/SSL)
- *(SC-900 also references "in use" in some contexts, but focus is at rest/in transit)*

---

### Governance, Risk, and Compliance (GRC)

- **Governance** – policies, processes, and oversight ensuring the organization meets business/legal objectives
- **Risk Management** – identifying, assessing, and mitigating risks to the organization
- **Compliance** – adhering to laws, regulations, and standards (e.g., GDPR, ISO 27001, NIST)

**Microsoft tools supporting GRC** (good to recognize, covered more in later domains):
- Microsoft Purview Compliance Manager – assess compliance posture, get improvement actions
- Microsoft Purview (audit, eDiscovery, information protection)
- Azure Policy / Blueprints – enforce governance rules at scale

---

## 2. Identity Concepts

### Identity as the Primary Security Perimeter
Traditional perimeter = network firewall. Modern perimeter = **identity**, because users/devices now connect from anywhere, on any device, to cloud apps — the old network-edge model no longer fully protects resources.

> Identity is the new control plane; it's the common thread across Zero Trust pillars.

---

### Authentication (AuthN)
**"Who are you?"** — Proving identity.

- Verifies a user/entity is who they claim to be
- Methods: password, PIN, biometrics, MFA (multi-factor authentication), passwordless (FIDO2 keys, Microsoft Authenticator)
- Happens **before** authorization

### Authorization (AuthZ)
**"What can you do?"** — Granting access/permissions.

- Determines what resources/actions an authenticated identity can access
- Examples: RBAC (Role-Based Access Control), Conditional Access policies
- Happens **after** authentication

> Mnemonic: **AuthN = kNow who you are; AuthZ = aZ in "access"**

---

### Identity Providers (IdP)
A service that creates, manages, and verifies identity information, and provides authentication for relying applications.

- Examples: **Microsoft Entra ID** (formerly Azure AD), Google, Facebook (for consumer/social logins)
- Allows apps to outsource authentication instead of building their own
- Supports protocols like OAuth 2.0, OpenID Connect (OIDC), SAML

---

### Directory Services & Active Directory

- **Directory service** – a centralized, hierarchical database that stores information about objects on a network (users, groups, devices, computers) and enables management/lookup of those objects
- **Active Directory Domain Services (AD DS)** – Microsoft's traditional, **on-premises** directory service; uses domains, organizational units (OUs), group policy
- **Microsoft Entra ID (Azure AD)** – Microsoft's **cloud-based** identity and directory service; supports modern protocols (OAuth, SAML, OIDC), unlike legacy AD which relies on Kerberos/LDAP

| | Active Directory (AD DS) | Microsoft Entra ID |
|---|---|---|
| Location | On-premises | Cloud |
| Protocols | LDAP, Kerberos | OAuth2, SAML, OIDC |
| Structure | Domains, OUs, Forests | Flat (tenant-based) |

---

### Federation
Allows identity and access management across **separate organizations/systems** without duplicating accounts — establishes trust between identity providers so one set of credentials works across multiple systems.

- A user authenticates once with their home IdP; the trust relationship lets them access resources in another domain/organization (**Single Sign-On — SSO**)
- Example: A student logs into their university account and gains access to a partner research portal without a separate login
- Common federation protocols: **SAML, WS-Federation, OAuth/OIDC**

---

## Quick-Fire Recap

| Term | One-liner |
|---|---|
| Shared Responsibility | Security duties split between provider & customer; data/identity always yours |
| Defense-in-Depth | Multiple security layers, onion-style |
| Zero Trust | Verify explicitly, least privilege, assume breach |
| Encryption | Reversible data protection (symmetric/asymmetric) |
| Hashing | One-way, used for integrity checks |
| GRC | Governance (policy) + Risk (mitigation) + Compliance (rules) |
| Identity perimeter | Identity replaces network edge as primary boundary |
| AuthN | Proves who you are |
| AuthZ | Determines what you can access |
| IdP | Service that authenticates & manages identities |
| Directory service | Centralized database of network objects |
| AD DS vs Entra ID | On-prem/legacy vs cloud/modern |
| Federation | Trust between organizations enabling SSO across systems |

