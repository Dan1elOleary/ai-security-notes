# AI Access Control

This document covers access control concepts for AI systems, including role-based access control, document-level authorization, least privilege, and tenant isolation.

---

## Overview

AI systems often connect to sensitive data, business tools, internal documents, APIs, and user workflows. Because of this, strong access control is critical.

An AI system should never be allowed to access or perform actions simply because a user asks it to. Access must be verified by the application and supporting security controls.

---

## Why Access Control Matters

Poor access control can allow users to:

- View restricted documents
- Access another user’s data
- Retrieve another tenant’s information
- Trigger unauthorized tool actions
- Escalate privileges
- Modify records
- Expose confidential information

AI systems must follow the same access control principles as traditional applications.

---

## Role-Based Access Control

Role-Based Access Control, or RBAC, grants permissions based on a user’s role.

Example roles may include:

| Role | Example Permissions |
|---|---|
| Standard User | Ask questions and access personal documents. |
| Support Agent | Access assigned customer tickets. |
| Manager | View team-level reports. |
| Administrator | Manage system settings and users. |
| Security Analyst | Review security logs and alerts. |

RBAC helps prevent users from accessing information outside their job responsibilities.

---

## Least Privilege

Least privilege means users and systems should only have the minimum access required to perform their tasks.

For AI systems, this means:

- Do not give broad database access unless needed
- Do not allow unrestricted tool execution
- Do not expose admin functions to normal users
- Do not allow access to every document by default
- Do not let the AI bypass existing permissions

Least privilege reduces the impact of misuse or compromise.

---

## Document-Level Authorization

Document-level authorization ensures users can only retrieve documents they are allowed to access.

This is especially important in RAG systems.

Examples:

- HR users can access HR documents
- Finance users can access finance documents
- Customers can only access their own records
- Employees can only view documents assigned to their role
- Managers can access team documents but not unrelated departments

The AI should not retrieve documents unless the user is authorized to view them.

---

## Tenant Isolation

Tenant isolation keeps data separated between different organizations, customers, departments, or groups.

This is important for multi-tenant AI applications.

Without tenant isolation, one customer could accidentally receive another customer’s data.

Tenant isolation should be enforced through:

- Separate indexes
- Metadata filters
- Access checks
- Tenant IDs
- Logging
- Security testing

---

## Tool Permission Control

AI systems may be connected to tools that can perform actions.

Examples include:

- Sending emails
- Creating tickets
- Querying databases
- Updating records
- Running scripts
- Searching files
- Calling APIs

Each tool should have scoped permissions and approval requirements when needed.

---

## Human Approval Workflows

High-risk actions should require human approval.

Examples of actions that may require approval:

- Sending external emails
- Deleting records
- Changing permissions
- Running administrative commands
- Accessing highly sensitive data
- Processing financial transactions

Human approval helps prevent the AI from taking harmful actions if manipulated.

---

## Access Control Risks

| Risk | Description |
|---|---|
| Excessive Permissions | The AI has more access than needed. |
| Broken Authorization | Users can access unauthorized data. |
| Cross-Tenant Leakage | One tenant sees another tenant’s information. |
| Tool Abuse | The AI performs actions it should not be allowed to perform. |
| Privilege Escalation | A user gains higher-level access through AI workflows. |
| Data Overexposure | Too much data is added to the model context. |

---

## Defensive Controls

| Control | Purpose |
|---|---|
| RBAC | Assign permissions based on user roles. |
| Least Privilege | Limit access to only what is required. |
| Document-Level Checks | Confirm users can access retrieved documents. |
| Tenant Isolation | Separate customer or department data. |
| Tool Scoping | Restrict what connected tools can do. |
| Human Approval | Add review for high-risk actions. |
| Audit Logging | Track access and actions. |
| Permission Testing | Verify access rules work correctly. |

---

## Key Takeaways

- AI systems must follow normal access control rules.
- The model should not decide whether a user is authorized.
- Permissions should be enforced before data reaches the model.
- Tool access should be limited and monitored.
- Tenant isolation is critical in business environments.
- Human approval helps reduce risk for sensitive actions.

---

## Skills Demonstrated

- Access control awareness
- RBAC concepts
- Least privilege principles
- RAG authorization understanding
- Tenant isolation awareness
- Secure AI workflow design

---

## Professional Summary

Access control is one of the most important security areas for AI applications. These notes demonstrate an understanding of how AI systems should enforce permissions, protect sensitive data, and prevent unauthorized actions.
