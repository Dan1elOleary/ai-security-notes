# RAG Security Controls

This document covers security controls for **Retrieval-Augmented Generation**, also known as **RAG**.

RAG systems allow AI applications to retrieve information from external knowledge bases, documents, databases, or search indexes before generating a response.

---

## Overview

Retrieval-Augmented Generation improves AI responses by giving the model access to external information. However, it also introduces security risks because the model may retrieve sensitive, outdated, poisoned, or unauthorized content.

A secure RAG system must protect both the retrieval process and the data sources connected to it.

---

## What RAG Does

A RAG system typically works by:

1. Accepting a user question
2. Searching a knowledge base or vector database
3. Retrieving relevant content
4. Adding that content to the model prompt
5. Generating a response based on the retrieved information

Each step can introduce security risk if not properly controlled.

---

## Common RAG Security Risks

| Risk | Description |
|---|---|
| Unauthorized Data Retrieval | Users receive documents they should not access. |
| Data Poisoning | Malicious content is added to the knowledge base. |
| Prompt Injection in Documents | Retrieved documents contain malicious instructions. |
| Sensitive Data Exposure | Confidential information is included in model responses. |
| Poor Source Validation | Untrusted sources are added to the retrieval system. |
| Tenant Data Leakage | Data from one customer or group is exposed to another. |
| Stale Information | Outdated content leads to incorrect or risky answers. |

---

## Access Control

Access control is one of the most important parts of RAG security.

The system should verify:

- Who the user is
- What documents the user is allowed to access
- What tenant or department the user belongs to
- Whether the requested data is sensitive
- Whether the user has permission to retrieve the content

The model should not be responsible for enforcing access control by itself.

---

## Document-Level Authorization

RAG systems should enforce permissions at the document level.

This means users should only retrieve documents they are authorized to view.

Examples include:

- HR documents limited to HR staff
- Customer records limited to assigned support teams
- Internal policies limited to employees
- Tenant-specific files limited to the correct organization

---

## Tenant Isolation

Tenant isolation prevents data from one customer, department, or organization from being exposed to another.

Strong tenant isolation should include:

- Separate data indexes when needed
- Metadata-based filtering
- Strict access checks
- Logging of retrieval activity
- Testing for cross-tenant data exposure

---

## Data Ingestion Security

Data ingestion is the process of adding documents or information into the RAG system.

Before content is indexed, it should be reviewed for:

- Source trustworthiness
- Sensitive information
- Malicious instructions
- Outdated material
- Duplicate content
- Improper permissions

Untrusted documents should not be blindly added to the knowledge base.

---

## Prompt Injection in Retrieved Content

Retrieved documents may contain malicious instructions designed to manipulate the AI.

Examples include hidden instructions that tell the model to:

- Ignore previous rules
- Reveal confidential information
- Change its role
- Bypass restrictions
- Follow commands from the document instead of the user

The system should treat retrieved content as untrusted data, not trusted instructions.

---

## Defensive Controls

| Control | Purpose |
|---|---|
| Metadata Filtering | Restrict results based on user permissions. |
| Source Validation | Confirm documents come from trusted sources. |
| Document Review | Check content before indexing. |
| Access Control Enforcement | Prevent unauthorized document retrieval. |
| Tenant Isolation | Keep customer or department data separated. |
| Output Filtering | Prevent sensitive information from being exposed. |
| Logging | Track what was retrieved and why. |
| Monitoring | Detect unusual retrieval behavior. |

---

## Secure RAG Checklist

- Enforce access control before retrieval
- Validate document sources
- Remove sensitive data when not needed
- Review documents before indexing
- Apply metadata filters
- Separate tenant data
- Monitor retrieval activity
- Log document access
- Treat retrieved content as untrusted
- Test for prompt injection in documents

---

## Key Takeaways

- RAG systems expand the AI attack surface.
- Retrieved content can contain sensitive or malicious information.
- Access control must happen before documents are added to the model context.
- Tenant isolation is critical in business environments.
- Retrieved documents should be treated as untrusted data.
- Logging and monitoring help detect abuse.

---

## Skills Demonstrated

- RAG security awareness
- Access control design
- Document-level authorization
- Tenant isolation concepts
- Data ingestion review
- AI threat modeling
- Secure system documentation

---

## Professional Summary

RAG systems are powerful, but they must be carefully secured. These notes demonstrate an understanding of how retrieval systems can expose sensitive data and how layered controls can reduce risk in AI-enabled applications.
