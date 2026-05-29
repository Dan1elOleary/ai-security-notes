OWASP LLM Top 10 Notes

This document contains notes covering the OWASP Top 10 for Large Language Model Applications. These risks focus on common security issues that affect AI-enabled systems, including prompt injection, sensitive information disclosure, insecure outputs, excessive permissions, and supply chain weaknesses.

The purpose of these notes is to document key AI security concepts and show an understanding of how LLM-based applications can be attacked, misused, and defended.

Overview

Large Language Models are often connected to applications, APIs, databases, documents, plugins, and automation tools. Because of this, securing the model alone is not enough. The entire AI application environment must be protected.

OWASP LLM risks help security professionals understand how attackers may abuse AI systems through malicious prompts, unsafe integrations, exposed data, or poorly controlled permissions.

Major Risk Areas
Risk Area	Description
Prompt Injection	Attackers manipulate the model with malicious instructions.
Sensitive Information Disclosure	The model exposes private data, credentials, or internal information.
Insecure Output Handling	Model output is trusted without validation or sanitization.
Excessive Agency	The AI system has too much permission or autonomy.
Supply Chain Vulnerabilities	Third-party models, datasets, plugins, or dependencies introduce risk.
Improper Access Control	Users can access data or actions they should not be allowed to use.
Overreliance	Users trust AI output without verification.
Data Poisoning	Training or retrieval data is manipulated to influence model behavior.
Key Concepts
Prompt Injection

Prompt injection occurs when an attacker gives the AI system instructions that override or manipulate the intended behavior of the application.

This can happen through:

Direct user prompts
Uploaded documents
Emails
Websites
Retrieved knowledge base content
Third-party data sources

Prompt injection is dangerous because LLMs process instructions and data together as text. If an application does not separate trusted instructions from untrusted content, the model may follow malicious directions.

Sensitive Information Disclosure

Sensitive information disclosure happens when an AI system reveals information that should remain private.

Examples include:

API keys
Passwords
Internal documentation
Customer records
Source code
Proprietary business logic
Confidential company data

AI systems should not be trusted to automatically know what information is sensitive. Security controls must be added around the application.

Insecure Output Handling

Insecure output handling occurs when an application accepts model output and passes it directly into another system without validation.

This can lead to:

Cross-site scripting
SQL injection
Command injection
Unsafe code execution
Unauthorized API actions
Misleading or harmful responses

LLM output should be treated as untrusted until validated.

Excessive Agency

Excessive agency occurs when an AI system is given too many permissions or too much ability to take actions.

Examples include allowing AI to:

Send emails without approval
Delete files
Modify user accounts
Access sensitive systems
Run commands
Approve financial transactions

AI systems should follow the principle of least privilege.

Supply Chain Vulnerabilities

AI systems often rely on external components, including:

Third-party models
Open-source packages
Datasets
Plugins
Prompt templates
Vector databases
Embedding models

If any of these components are compromised or untrusted, they can introduce security risks into the AI application.

Defensive Concepts
Defense	Purpose
Input Validation	Reduce malicious or unexpected input.
Output Sanitization	Prevent unsafe model responses from being executed or rendered.
Least Privilege	Limit what the AI system can access or do.
Human Approval	Require review before high-risk actions.
Logging and Monitoring	Detect suspicious use or abnormal behavior.
Secret Management	Prevent keys and credentials from being exposed.
Access Control	Ensure users only access authorized data.
Source Validation	Verify external content before using it in AI workflows.
Security Takeaways
AI systems should not be treated as fully trusted.
LLM output should be validated before being used by applications.
Sensitive information should never be placed directly into prompts unless required and protected.
AI tools should only have the permissions needed for their task.
Third-party AI components should be reviewed before use.
Logging and monitoring are important for detecting abuse.
Human oversight is needed for high-impact decisions.
Skills Demonstrated
AI security awareness
OWASP LLM Top 10 understanding
Threat identification
Secure design thinking
Access control awareness
Secure documentation
Risk analysis
Professional Summary

The OWASP LLM Top 10 provides a strong foundation for understanding modern AI security risks. These notes demonstrate awareness of how AI-enabled applications can be attacked and how organizations can reduce risk through layered security controls.
