# Project 1: The Fact-Checking Auditor – SPEC.md

## Background and Motivation
**Industry Context:** Financial institutions and audit firms often need to verify the accuracy of claims in reports, news, or documents. Manually fact-checking financial documents (earnings reports, investment prospectuses, regulatory filings) is time-consuming and error-prone. In this project, we design an AI Fact-Checking Auditor agent to automate this verification process. This agent will read statements (e.g. “Company X had a 15% profit growth in Q4”) and check them against trusted sources (like financial databases or news) to determine truthfulness. By leveraging an AI agent, we aim to improve audit reliability and speed – a critical need in finance where compliance and accuracy are paramount.

**Project Overview:** The Fact-Checking Auditor is a single-agent (or simple multi-step) system that uses an LLM to analyze text and specialized tools to fetch relevant evidence. The agent will output a report labeling each claim as Verified, Unverified, or False, along with supporting evidence. This project solidifies foundational skills: prompt engineering for fact-checking, retrieval-augmented generation, and basic sequential reasoning by an LLM agent.

## Objectives and Scope
**Objective:** Develop an autonomous agent that can ingest a document or set of claims and verify each claim’s accuracy by retrieving information from external sources. The agent should produce an audit report indicating which claims are true or false, with references.

### Scope
- **In Scope:** Financial and numerical claims in text; using a search tool or knowledge base (pseudo-API or local dataset) to find evidence; analysis via a single LLM agent; simple user interface (CLI or notebook).
- **Out of Scope:** Real-time data streaming; complex multi-agent workflows; front-end development; highly nuanced judgment calls.

## Functional Requirements
- **FR1:** Document Parsing: Accepts document or list of claims.
- **FR2:** Claim Identification: Identifies distinct factual claims.
- **FR3:** Evidence Retrieval: Uses search/API to retrieve evidence.
- **FR4:** Fact Verification Logic: Compares claims to evidence and classifies them.
- **FR5:** Report Generation: Outputs structured Audit Report in Markdown.
- **FR6:** Iterative Improvement (Optional): May retry search once per claim.
- **FR7:** User Interaction: CLI or notebook script to run the agent.

## Non-Functional Requirements
- **NFR1:** Accuracy: Must use authoritative sources.
- **NFR2:** Transparency: Report must include references.
- **NFR3:** Performance: Should process 10–20 claims in a few minutes.
- **NFR4:** Security & Compliance: Use sandboxed APIs; maintain data privacy.
- **NFR5:** Maintainability: Modular code using SDD principles.

## System Design and ADK Approach
**Architecture:** Single LLM agent enhanced with a retrieval tool.

### Workflow
1. **Claim Extraction:** LLM or regex to extract factual statements.
2. **Verification Loop:**
   - ADK Tool Agent performs search.
   - LLM evaluates claim against retrieved info.
   - Optional retry if inconclusive.
3. **Report Compilation:** Aggregate and format results.

### ADK Implementation
- **LlmAgent:** Core reasoning engine.
- **Tool (Search):** Custom or ADK-provided wrapper.
- **SequentialAgent (Optional):** Chain parsing and verification steps.

**Model:** Google Gemini (via `google.generativeai`) or equivalent.

## Technical Implementation Plan
- **Environment:** Python 3 with `google.adk` and `google.generativeai`
- **Data Source:** Search API (e.g., Bing, Wikipedia) or local KB
- **Prompt Template:**
  ```
  Fact: {claim}
  Evidence:
  {retrieved_text}
  Answer in format: True/False/Not Sure with explanation.
  ```
- **Spec-Driven Development:** Follow SPEC → DESIGN → CODE
- **Testing:** Ground-truth claims, edge cases, prompt QA

## Project Deliverables
- **Code:** Modular Python scripts (search_tool.py, fact_auditor.py)
- **Sample Reports:** Markdown/PDF audits
- **Demo Video (Optional):** Sample input-to-output walkthrough
- **Docs:** SPEC.md, README.md, design notes, and extensibility guide

## Risks and Mitigations
- **Hallucination Risk:** Prompt agent to rely only on retrieved facts.
- **Tool Failure:** Handle API errors; cache fallback.
- **Parsing Complexity:** Limit input complexity, chunk inputs.
- **Bias & Misinformation:** Use curated KB for sensitive topics.

## Success Criteria
- Audits 10+ claims with >70–80% accuracy
- Each claim has clear reference(s)
- Team explains system design and ADK usage
- Code passes Senior-Level Code Review rubric
