# HR Email Inbox Agent and Power Automate Solution
Public safe demo package of a generic HR email inbox processing solution using a Power Automate flow and an HR inbox agent pattern.

This repo explains how to process inbound HR emails, route requests safely, and draft reply content using approved knowledge only.
All internal identifiers and sensitive details are removed.
This repo is not an import ready environment package.

## What this solution does
1. Watches a shared mailbox for new HR emails
2. Extracts and normalizes the newest message content
3. Routes the message into a controlled set of outcomes
4. Retrieves approved knowledge content for the routed topic
5. Drafts a reply body grounded in approved content only
6. Applies operational actions such as folder placement based on routing outcome
7. Produces run evidence so operators can validate safe behavior

## What this solution refuses to do
1. It does not invent policy content or guess when knowledge is missing
2. It does not guess targets for folders, lists, or resources
3. It does not expose tenant details, internal URLs, mailbox addresses, or secrets
4. It does not claim it performed actions it cannot prove

## Why this repo exists
Inbox automation is high risk if you do it casually.
This repo focuses on guardrails and operating discipline:
approved sources only
no invention
selection and disambiguation before targeted actions
consistent fallbacks for missing knowledge
test pack coverage for drift prevention

## Quick start
1. Read docs/01_Overview.md
2. Review guardrails in docs/03_Guardrails.md
3. Review solution_redacted/Workflow_Redacted.json for structure
4. Use setup/05_Deployment_Checklist.md to implement the pattern in your own tenant
5. Run tests/Test_Pack.md to validate behavior

## Repository layout
docs
Solution explanation, dataflow, guardrails, and ops playbook

setup
Prereqs and deployment checklist for implementing the pattern safely

solution_redacted
Redacted workflow definition for reading only

tests
Test pack with pass fail conditions

governance
Change control and change log

redaction
Checklist to keep this repo public safe

## Public safe notice
No tenant identifiers
No internal URLs
No secrets or tokens
No proprietary policy text
Examples are sanitized and illustrative only

## License
MIT
