# NDA Helper Agent

## Overview

The **NDA Helper Agent** is a multi-agent AI workflow built using **Langflow** to assist Business Development teams in quickly reviewing Non-Disclosure Agreements (NDAs).

The system analyses uploaded NDA PDFs and provides structured insights including:

* Clause extraction
* Plain-English explanations of legal language
* Risk identification and escalation triggers
* Business-level summaries of key terms

The goal is to **reduce legal review friction for non-legal users** while maintaining transparency, governance, and clear escalation to legal professionals when required.

---

## Agent Architecture

The workflow uses multiple specialised AI agents, each responsible for a specific task.

### Extractor Agent

Extracts and cleans relevant clause text from uploaded NDA documents.

### Explainer Agent

Translates complex legal terminology into **plain English explanations** suitable for business users.

### Risk Agent

Evaluates clauses to identify:

* Potential legal risks
* Non-standard or unusual terms
* Escalation triggers requiring legal review

### Response Orchestrator Agent

Combines outputs from the specialist agents into a **structured NDA assessment** suitable for business decision making.

### QA Critic Agent

Runs when confidence is low or outputs conflict to validate the response before final delivery.

---

## Example User Queries

Users can upload an NDA and ask questions such as:

* "Summarise the key terms of this NDA."
* "Explain the confidentiality obligations in plain English."
* "Does the agreement contain a non-compete clause?"
* "What clauses present potential legal risks?"
* "Should this NDA be escalated for legal review?"

### Example Comprehensive Review Prompt

Review this NDA and provide an initial business-level assessment:

1. Summarise the NDA in five key bullet points.
2. Provide a plain-English overview of the purpose of the agreement.
3. Identify the parties to the agreement and their roles.
4. Explain how confidential information is defined.
5. List any exclusions from confidentiality obligations.
6. Describe the obligations of the Receiving Party.
7. Identify any non-compete or restrictive covenants.
8. Highlight unusual or potentially high-risk clauses.
9. Recommend whether the NDA should be escalated to Legal.

---

## How to Run the Project

### 1. Install dependencies

pip install -r requirements.txt

### 2. Start Langflow

langflow run

### 3. Open the Langflow interface

Open the provided local URL in your browser.

### 4. Import the workflow

Import the exported workflow file:

nda-helper-agent.json

### 5. Run the prototype

Upload an NDA PDF and submit a query.

---

## Project Files

| File                  | Description                |
| --------------------- | -------------------------- |
| nda-helper-agent.json | Exported Langflow workflow |
| requirements.txt      | Python dependencies        |
| README.md             | Project documentation      |

---

## Governance & Safety

This system provides a **first-pass business review only** and does **not replace legal advice**.

Governance safeguards implemented include:

* Evidence-based clause extraction
* Risk identification and escalation triggers
* QA Critic validation for low-confidence outputs
* Structured summaries to reduce misinterpretation
* Human legal review required before contract approval

---

## Author

Sherry-Ann Sarabjit
Advanced AI Agents – Final Project
Product School
