# AI Supply Chain Risks

This document covers supply chain risks involving AI systems, including third-party models, datasets, packages, plugins, prompt templates, embeddings, and other external components.

---

## Overview

AI applications often depend on many external components. These components may come from vendors, open-source repositories, cloud services, model providers, plugin marketplaces, or public datasets.

If one component is compromised, malicious, outdated, or poorly maintained, it can create risk for the entire AI system.

---

## What Is an AI Supply Chain?

An AI supply chain includes all the components used to build, train, deploy, and operate an AI system.

Examples include:

- Models
- Datasets
- Software packages
- APIs
- Plugins
- Prompt templates
- Embedding models
- Vector databases
- Development tools
- Cloud services
- Container images

Each component should be reviewed before it is trusted.

---

## Common AI Supply Chain Risks

| Risk | Description |
|---|---|
| Malicious Packages | A dependency contains harmful code. |
| Poisoned Datasets | Training or retrieval data is manipulated. |
| Untrusted Models | A model behaves unexpectedly or includes hidden risks. |
| Vulnerable Plugins | Third-party plugins introduce security weaknesses. |
| Exposed Secrets | API keys or credentials are committed to repositories. |
| Prompt Template Manipulation | Shared templates contain malicious instructions. |
| Dependency Confusion | Applications download the wrong or malicious package. |
| Outdated Components | Old packages contain known vulnerabilities. |

---

## Third-Party Models

Third-party models may introduce risk if they are not reviewed.

Potential risks include:

- Unknown training data
- Hidden behavior
- Unsafe outputs
- Lack of transparency
- Licensing concerns
- Weak security practices from the provider

Organizations should evaluate model providers carefully before using them.

---

## Dataset Risks

Datasets are important because they influence AI behavior.

Dataset risks include:

- Poisoned training data
- Sensitive information inside datasets
- Copyright or licensing issues
- Inaccurate information
- Biased or manipulated content
- Poor source validation

Datasets should be reviewed, validated, and documented.

---

## Package and Dependency Risks

AI applications often use open-source packages.

Risks include:

- Vulnerable dependencies
- Malicious packages
- Typosquatting
- Dependency confusion
- Unmaintained libraries
- Insecure installation scripts

Security teams should scan dependencies and monitor for vulnerabilities.

---

## Plugin and Tool Risks

Plugins and tools expand what an AI system can do.

Examples include:

- Browser plugins
- Code execution tools
- Email tools
- Database connectors
- File access tools
- Ticketing system integrations
- Cloud service connectors

If a plugin is compromised or over-permissioned, it can increase the impact of an AI attack.

---

## Prompt Template Risks

Prompt templates may be reused across applications.

A malicious or poorly designed prompt template may:

- Weaken system instructions
- Encourage unsafe responses
- Expose internal logic
- Bypass restrictions
- Introduce hidden instructions
- Cause inconsistent behavior

Prompt templates should be reviewed like application code.

---

## Embedding and Vector Database Risks

AI systems that use embeddings or vector databases can also be affected by supply chain risk.

Risks include:

- Poisoned documents
- Unauthorized indexed content
- Cross-tenant data leakage
- Insecure vector database access
- Weak metadata filtering
- Inaccurate retrieval results

These systems should be secured with access control, monitoring, and source validation.

---

## Defensive Controls

| Control | Purpose |
|---|---|
| Vendor Review | Evaluate third-party providers. |
| Dependency Scanning | Detect vulnerable packages. |
| Secret Scanning | Identify exposed credentials. |
| Source Validation | Verify datasets and documents. |
| Version Pinning | Reduce unexpected dependency changes. |
| SBOM Documentation | Track software components. |
| Plugin Review | Check permissions and security risks. |
| Access Control | Limit what components can access. |
| Monitoring | Detect abnormal behavior or compromise. |

---

## Secure Supply Chain Checklist

- Review third-party AI vendors
- Scan dependencies for vulnerabilities
- Avoid using untrusted packages
- Pin package versions when possible
- Validate datasets before use
- Monitor public repositories for leaked secrets
- Review plugins before connecting them
- Limit permissions for external tools
- Track components with documentation
- Rotate exposed keys immediately

---

## Key Takeaways

- AI systems depend on many external components.
- A weak supply chain component can compromise the full application.
- Models, datasets, packages, plugins, and prompts should be reviewed.
- Secrets should never be committed to public repositories.
- Dependency scanning and vendor review reduce risk.
- Supply chain security is part of AI security.

---

## Skills Demonstrated

- AI supply chain awareness
- Third-party risk understanding
- Dependency security
- Secret management awareness
- Secure development practices
- Vendor risk evaluation
- AI threat modeling

---

## Professional Summary

AI supply chain security is important because modern AI applications rely on many external systems and components. These notes demonstrate awareness of how third-party models, datasets, plugins, and dependencies can introduce risk into AI-enabled environments.
