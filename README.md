# Gen AI Foundations: Capstone Project 1 - Document-to-JSON Extraction Agent

## 🛑 Reviewer Instructions: Submission Checklist 🛑

**Before submitting for review**, developers **must** ensure the following requirements are met:

1.  **Repository Forking & Naming:** This repository **must be forked** to your personal GitHub account and **renamed** exactly to:
    `Agentic-AI-Foundations-Capstone-Project-1-DocumentExtraction-Agent`
2.  **Language Requirement:** All code must be implemented using **Python**.
3.  **Topic Coverage:** The implementation must cover the core concepts listed in the **Related Training Topics** section (LLMs, Agents, Tools, RAG).
4.  **Complete Documentation:** All sections of this README (Requirements, Execution, Views) must be fully completed with project-specific details, code, and screenshots.

-----

## 🌟 Project Summary

This project involves developing a **Data Extraction Agent (Document-to-JSON Extraction Agent)** using foundational frameworks like Google's **Agent Development Kit (ADK)**, **LangChain**, or basic **RAG** tools. The core objective is to take an uploaded **document** (e.g., PDF, image, DOCX), perform information extraction, and return the result in a **structured JSON format**.

This project serves as a foundational example of a **simple, reactive agent** capable of single-step tasks and structured output.

### Key Technologies:

  * **Frameworks:** ADK (Agent Development Kit), LangChain, or basic RAG tools.
  * **Model:** Gemini (used by the agent).
  * **Output Format:** Structured JSON.

-----

## 🧠 Related Training Topics

This project directly utilizes core concepts covered in the first section of the training program: **Foundations** (Agentic developer examples).

| Training Topic | Relevance to This Project | Implementation Details |
| :--- | :--- | :--- |
| **Large Language Models (LLMs)** | Core intelligence engine. | The agent relies on an LLM (e.g., Gemini) to understand the **prompt**, interpret **OCR output** from the **document**, and enforce the **JSON schema** for structured output. |
| **Agent Fundamentals** | Direct application of training. | This agent is a **simple, basic tool-call agent** that uses one tool (a **document parser**) and then utilizes the LLM for reasoning and structured formatting. |
| **Tools/Tool Calls** | Core mechanism for extraction. | The agent is equipped with a **Tool** to **read/process the document file**. The LLM decides when to use this tool call to access the document content before generating the response. |
| **Developer Tools / GitHub Copilot** | Efficiency and code generation. | **[Placeholder: Briefly describe how GitHub Copilot, VS Code, or other IDE/Dev tools were used to increase development speed or assist with boilerplate code (e.g., FastAPI routing, Pydantic models, or ADK setup).]** |

-----

## 📋 Requirements (Functional and Non-Functional)

### Functional Requirements (FR)

| ID | Requirement | Specific Description | Status |
| :--- | :--- | :--- | :--- |
| **FR01** | File Upload | The system must allow the user to upload a **document file** (e.g., PDF, JPG, PNG) via an API (FastAPI). | `PENDING` |
| **FR02** | Agent Execution | The agent must be invoked with the **document content** and an extraction prompt. | `PENDING` |
| **FR03** | JSON Output | The agent must return the extracted data in a valid, structured JSON format. | `PENDING` |
| **FR04** | Schema Handling | **[Placeholder: Specify the required JSON schema (e.g., insurance claim fields, invoice data, etc.).]** | `PENDING` |
| **FR05** | Fallback/Retry | The system must retry the extraction up to 3 times in case of failure (as implemented in the code). | `IMPLEMENTED` |

### Non-Functional Requirements (NFR)

| ID | Requirement | Category | Metric |
| :--- | :--- | :--- | :--- |
| **NFR01** | Latency | Performance | Extraction must complete in less than **X** seconds (e.g., 5s). |
| **NFR02** | Scalability | Performance | The service must support **X** concurrent requests per minute. |
| **NFR03** | Reliability | Accuracy | The accuracy of key field extraction must be above **95%**. |
| **NFR04** | Security | Security | The API must require an authentication token (e.g., API Key or JWT) for execution. |

-----

## 🚀 Implementation and Execution

### 1\. Prerequisites

Ensure you have **Python 3.9+** installed and your virtual environment configured.

  * **API Key:** Your Gemini API key must be configured in an environment variable.

    ```bash
    # In your .env file:
    GEMINI_API_KEY="AIzaSy..."
    ```

### 2\. How to Build (Install)

Install all necessary dependencies, primarily using a `requirements.txt` file.

```bash
# 1. Clone the repository
git clone [REPOSITORY_URL]
cd document-to-json-extractor

# 2. Create and activate the virtual environment
python -m venv .venv
# On Windows:
.\.venv\Scripts\activate
# On Linux/macOS:
source .venv/bin/activate

# 3. Install dependencies (FastAPI, ADK, etc.)
pip install -r requirements.txt
```

### 3\. How to Run

Start the API server using `uvicorn`.

```bash
# Run the FastAPI application
uvicorn main:app --reload
```

The server will be available at `http://localhost:8000`.

### 4\. How to Test

You can test the extraction by uploading a file or by using the default sample file.

#### A. Test with Sample File (Using `curl`)

If no file is provided, the system uses the default sample file via the `/extract` endpoint.

```bash
curl -X POST http://localhost:8000/extract
```

**Expected Result:**

```json
{
  "field_1": "extracted_value_1",
  "field_2": "extracted_value_2",
  // ... (JSON Structure)
}
```

#### B. Test with File Upload (Using an HTTP Tool)

Use tools like **Postman**, **Insomnia**, or the **Swagger UI** interface (available at `http://localhost:8000/docs`).

1.  Open `http://localhost:8000/docs`.
2.  Go to the `/extract` route.
3.  Select **"Try it out"**.
4.  Upload a **document file** (e.g., PDF, image) in the `file` field.
5.  Click **"Execute"**.

-----

## 🖼️ Project Views

Here will be the relevant screenshots of the project.

### 1\. User Interface View (Swagger/Postman)

\![Placeholder for screenshot of the file upload interface (Swagger/Postman).]

### 2\. Successful JSON Output View

\![Placeholder for screenshot of the structured JSON response.]

### 3\. Agent Flow Diagram

\![Placeholder for flow diagram showing the Runner call, tool invocation, and retry logic.]
