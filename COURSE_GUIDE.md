# AI Agent Engineering - Course Curriculum

**🔗 [Prerequisite: Common Base Ground – AI Augmented Foundations](https://github.com/jaynro/Full-Stack-Augmented/blob/main/README.md)**

## 🎓 Program Outcomes
**Welcome to the AI Agent Engineering training.**

By the end of this self-paced program, you will not just "learn" about agents—you will become a practitioner. Your journey includes:
* **3 Real-World Projects:** You will architect and build three distinct agentic systems (RAG, Orchestration, and Autonomous Loops).
* **Resume Transformation:** You will rewrite your CV to reflect in-demand skills like "Designing Multi-Agent Systems" and "Spec-Driven Development."
* **12 Mock Interviews:** You will undergo rigorous technical vetting (4 per project) to master your storytelling and technical defense.

*This course is self-directed. You are responsible for managing your own learning timeline and coordinating with colleagues for your reviews.*


---

## 📚 Curriculum Roadmap

### Level 1: The Foundations
**Project:** [Project 1 – The Fact-Checking Auditor](./project1/)
* **Concept:** Single Agent & Tool Usage.
* **Goal:** Build an agent that can use a search tool to verify claims.
* **Required Reading:** [ADK Agents Overview](https://google.github.io/adk-docs/agents/)
* **Key Class:** `LlmAgent`
* **✅ Assessments:**
    * [Mock Interview Assessment](https://github.com/jaynro/agentic-ai-level-1-foundations/blob/main/reviews/capstone-1-mock-interviews.md)
    * [Code Review Definition of Done](https://github.com/jaynro/agentic-ai-level-1-foundations/blob/main/reviews/capstone-1-rubric.md)

### Level 2: Multi-Agent Systems
**Project:** [Project 2 – The Customer Resolution Squad](./project2/)
* **Concept:** Orchestration & Routing.
* **Goal:** Coordinate three specialist agents to handle different customer queries.
* **Required Reading:** [Multi-Agent Systems](https://google.github.io/adk-docs/agents/multi-agents/)
* **Key Concept:** `Coordinator` pattern.
* **✅ Assessments:**
    * [Mock Interview Assessment](INSERT_LINK_HERE)
    * [Code Review Definition of Done](INSERT_LINK_HERE)

### Level 3: Autonomous Loops
**Project:** [Project 3 – The Self-Healing Engineer](./project3/)
* **Concept:** Iterative Reasoning & Self-Correction.
* **Goal:** Build an agent that loops through diagnosis and testing until code is fixed.
* **Required Reading:** [Loop Agents (Workflow)](https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/)
* **Key Class:** `LoopAgent`
* **✅ Assessments:**
    * [Mock Interview Assessment](INSERT_LINK_HERE)
    * [Code Review Definition of Done](INSERT_LINK_HERE)

---

## 🤝 Peer Review Process

Since this course is self-directed, **you must actively seek out 3 colleagues** to review your work for each capstone.

### How to Conduct a Review
1.  **Create an Evaluation File:** In the root of your project repository, create a file named `PEER_REVIEWS.md`.
2.  **Solicit Feedback:** Ask a peer to review your code or conduct a mock interview.
3.  **Log the Review:** The peer must open your `PEER_REVIEWS.md` file and append their feedback using the template below.
4.  **Definition of Done:** You are considered "Passed" on a project only when you have **3 distinct peer entries** in your file.

#### Peer Review Template (Copy into `PEER_REVIEWS.md`)

```markdown
### Reviewer: [Name]
**Date:** [YYYY-MM-DD]
**Project Level:** [1, 2, or 3]

**1. Interview Assessment (1-5):** [Score]
*Comment on their storytelling and concept mastery:*
> [Reviewer comments here]

**2. Code Quality (1-5):** [Score]
*Comment on architectural purity and clean code:*
> [Reviewer comments here]

**3. Final Verdict:** [Pass / Request Changes]

```

---

## 📝 Universal Rubric Standards

Peers should use the following standards when grading, regardless of which project level is being reviewed.

### 1. The "AI Professional" Interview Protocol

* **Concept Mastery:** Did the candidate explain *why* they chose specific agent patterns without over-relying on jargon?
* **Storytelling:** Did they clearly articulate the "Problem," "Action," and "Result"?
* **Resume Reality:** Does their resume accurately reflect the skills demonstrated in the project?

### 2. Code Review: The "Definition of Done"

* **Functional:** The agent solves the core problem (fixes the bug, answers the customer) without crashing.
* **Clean Code:** Adheres to Python PEP8 standards; no commented-out junk code.
* **Architectural Purity:** The code must correctly implement the specific pattern for that level (e.g., Level 3 *must* loop, not just run once).
* **Error Handling:** The system handles LLM hallucinations or API failures gracefully.

---


## General Resources

### Augmented AI Developer Fundamentals

* [Fundamentals of Generative AI](https://learn.microsoft.com/en-us/training/modules/fundamentals-generative-ai/) (1 hour)
* [Accelerate App Development using GitHub Copilot](https://learn.microsoft.com/en-us/training/paths/accelerate-app-development-using-github-copilot/) (6 hours)
* [Introduction to Prompt Engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/?WT.mc_id=academic-113596-abartolo) (1 hour)
* [Introduction to Copilot in Python](https://learn.microsoft.com/en-us/training/modules/introduction-copilot-python/?WT.mc_id=academic-113596-abartolo) (1 hour)
* [Integrate MCP with Copilot](https://github.com/skills/integrate-mcp-with-copilot) (GitHub Skill)


### Google ADK Courses

* [Introduction to Generative AI](https://www.skills.google/course_templates/536) (30 mins)
* [Create Generative AI Apps on Google Cloud](https://www.skills.google/course_templates/1120) (5 hours)
* [Create Embeddings, Vector Search, and RAG with BigQuery](https://www.skills.google/course_templates/1210) (1 hour)
* [Build Intelligent Agents with Agent Development Kit (ADK)](https://www.skills.google/course_templates/1382) (6 hours)
* **Documentation:** [Google ADK Docs](https://google.github.io/adk-docs/)


### Spec-Driven Development (SpecDD)

* **Video Training:** [Spec-Driven Development in the Real World](https://www.youtube.com/watch?v=3le-v1Pme44) (YouTube, 15 mins)
* **Core Concept:** [Readme Driven Development](https://tom.preston-werner.com/2010/08/23/readme-driven-development.html) (Article)
* **Skill Builder:** [Google Technical Writing One](https://developers.google.com/tech-writing/one) (Course)



---
## 🚀 Optional Advanced Tracks

Once you have completed the core curriculum, you may explore these specialization modules:

* **Advanced RAG Pipelines:** Implementing semantic search with vector databases (ChromaDB/Pinecone).
* **Agent Evaluation:** Using "LLM-as-a-Judge" to score your agent's performance automatically.
* **Fine-Tuning:** Customizing a small Gemini/Llama model for specific domain tasks.
* **Production Deployment:** Containerizing agents with Docker and deploying to Cloud Run.

---
