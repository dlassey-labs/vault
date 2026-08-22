<div align="center">

# 🔐 HashiCorp Vault — DL Labs

![HashiCorp Vault](https://img.shields.io/badge/HashiCorp_Vault-v2.0.3-black?style=flat-square&logo=vault&logoColor=white)
![Status](https://img.shields.io/badge/Status-Operational-success?style=flat-square)

> Centralized platform for secrets management, PKI, machine and workload identity, encryption, and security automation.


</div>

---

## Overview

This repository documents the implementation and evolution of **HashiCorp Vault** within the DL Labs platform.

Vault provides a centralized security foundation for managing secrets, issuing certificates, establishing machine and workload identities, and protecting sensitive data across the infrastructure.

The implementation follows an incremental approach: each capability is deployed, validated in the lab, documented, and progressively integrated with other DL Labs services.

---

## Capabilities

| Capability | Description | Status |
|---|---|---|
| [Secrets Management](secrets-management/) | Centralized secrets management using KV v2 | ✅ Operational |
| [PKI / TLS & HTTPS](pki/tls-https/) | Internal PKI and service certificate management | ✅ Operational |
| [Auto-Unseal — AGE](auto-unseal/systemd-age/) | Automated Shamir unseal using AGE and systemd | ✅ Operational |
| [Transit Auto-Unseal](auto-unseal/transit/) | Vault-to-Vault Transit Seal architecture | 🔵 Planned |
| [Azure Key Vault Auto-Unseal](auto-unseal/azure-key-vault/) | Cloud-based KMS Auto-Unseal option | 🔵 Planned |
| [mTLS](pki/mtls/) | Mutual TLS authentication between services | 🔵 Planned |
| [SSH Certificates](pki/ssh-certificates/) | Vault-backed SSH certificate authority | 🔵 Planned |
| [Vault Agent](vault-agent/) | Automated secret and certificate delivery and renewal | 🔵 Planned |
| [Transit Encryption](transit/) | Encryption-as-a-Service using the Transit secrets engine | 🔵 Planned |

---

## Security Posture

- **Centralized Secrets Management** — credentials, API keys, and sensitive configuration are centrally managed through Vault
- **PKI & Certificate Management** — internal certificate issuance and lifecycle management through the DL Labs PKI
- **Least Privilege** — Vault policies restrict access to the minimum permissions required
- **Machine & Workload Identity** — applications and automation progressively move away from human or static credentials
- **Automated Security Operations** — unseal, secret delivery, certificate renewal, and rotation are progressively automated
- **Encryption Services** — Vault Transit provides centralized cryptographic services without exposing encryption keys

---

## Repository Structure

```text
vault/
├── README.md
│
├── secrets-management/
│   └── README.md
│
├── pki/
│   ├── README.md
│   ├── tls-https/
│   │   └── README.md
│   ├── mtls/
│   └── ssh-certificates/
│
├── auto-unseal/
│   ├── README.md
│   ├── systemd-age/
│   │   └── README.md
│   ├── transit/
│   └── azure-key-vault/
│
├── vault-agent/
│
├── transit/
│
└── operations/
    ├── commands-reference.md
    ├── troubleshooting.md
    ├── backup-restore.md
    └── upgrade.md
```

---

## Documentation

### Secrets Management
- [Secrets Management](secrets-management/)

### PKI & Certificates
- [PKI](pki/)
- [TLS & HTTPS](pki/tls-https/)
- [mTLS](pki/mtls/)
- [SSH Certificates](pki/ssh-certificates/)

### Auto-Unseal
- [Auto-Unseal](auto-unseal/)
- [systemd + AGE](auto-unseal/systemd-age/)
- [Transit Auto-Unseal](auto-unseal/transit/)
- [Azure Key Vault](auto-unseal/azure-key-vault/)

### Security Automation & Encryption
- [Vault Agent](vault-agent/)
- [Transit Encryption](transit/)

### Operations
- [Operations](operations/)

---

## 👤 Author

**Dosseh Lassey**  
Founder, DL-LABS — Infrastructure · Engineering · Automation · Security · AI

---


<div align="center">

**DL-LABS — Building Modern Enterprise Platforms**  
*From Infrastructure to Intelligent Systems*

</div>
