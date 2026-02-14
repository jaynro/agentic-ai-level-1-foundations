# AI Agent Engineering - Course Curriculum
**🔗((https://github.com/jaynro/Full-Stack-Augmented/blob/main/README.md))**
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
**Project:**((https://github.com/jaynro/agentic-ai-level-1-foundations/blob/main/README.md))
* **Concept:** Single Agent & Tool Usage.
* **Goal:** Build an agent that can use a search tool to verify claims.
* **Required Reading:**([https://google.github.io/adk-docs/agents/](https://google.github.io/adk-docs/agents/))
* **Key Class:** `LlmAgent`
* **✅ Assessments:**
    * [Mock Interview Assessment](https://github.com/jaynro/agentic-ai-level-1-foundations/blob/main/reviews/capstone-1-mock-interviews.md)
    *([https://github.com/jaynro/agentic-ai-level-1-foundations/blob/main/reviews/capstone-1-rubric.md](https://github.com/jaynro/agentic-ai-level-1-foundations/blob/main/reviews/capstone-1-rubric.md))
### Level 2: Multi-Agent Systems
**Project:**([https://github.com/jaynro/agentic-ai-level-2-multi-agentic-integration](https://github.com/jaynro/agentic-ai-level-2-multi-agentic-integration))
* **Concept:** Orchestration & Routing.
* **Goal:** Coordinate three specialist agents to handle different customer queries.
* **Required Reading:**([https://google.github.io/adk-docs/agents/multi-agents/](https://google.github.io/adk-docs/agents/multi-agents/))
* **Key Concept:** `Coordinator` pattern.
* **✅ Assessments:**
    * [Mock Interview Assessment](INSERT_LINK_HERE)
    *(INSERT_LINK_HERE)
### Level 3: Autonomous Loops
**Project:**([https://github.com/jaynro/agentic-ai-level-3-complex-orchestration](https://github.com/jaynro/agentic-ai-level-3-complex-orchestration))
* **Concept:** Iterative Reasoning & Self-Correction.
* **Goal:** Build an agent that loops through diagnosis and testing until code is fixed.
* **Required Reading:**([https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/](https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/))
* **Key Class:** `LoopAgent`
* **✅ Assessments:**
    * [Mock Interview Assessment](INSERT_LINK_HERE)
    *(INSERT_LINK_HERE)
---
## 🤝 Peer Review Process
Since this course is self-directed, **you must actively seek out 3 colleagues** to review your work for each capstone.
### How to Conduct a Review
1.  **Create an Evaluation File:** In the root of your project repository, create a file named `PEER_REVIEWS.md`.
2.  **Solicit Feedback:** Ask a peer to review your code or conduct a mock interview.
3.  **Log the Review:** The peer must open your `PEER_REVIEWS.md` file and append their feedback using the template below.
4.  **Definition of Done:** You are considered "Passed" on a project only when you have **3 distinct peer entries** in your file.
#### Peer Review Template (Copy into `PEER_REVIEWS.md`)
### Reviewer: [Name]
**Date:**
**Project Level:** [1, 2, or 3]
**1. Interview Assessment (1-5):**
*Comment on their storytelling and concept mastery:*
>
**2. Code Quality (1-5):**
*Comment on architectural purity and clean code:*
>
**3. Final Verdict:**
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
*([https://learn.microsoft.com/en-us/training/paths/accelerate-app-development-using-github-copilot/](https://learn.microsoft.com/en-us/training/paths/accelerate-app-development-using-github-copilot/)) (6 hours)
* [Introduction to Prompt Engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/?WT.mc_id=academic-113596-abartolo) (1 hour)


---
Here is the markdown code for that specific section so you can easily copy and paste it:

## 💰 Free Tier & Usage Notes: Development vs. Runtime Environments

When engineering Agentic AI systems, it is best practice to separate the LLMs used to *build* the software from the LLMs that *power* the software.

* **The Development Phase (The Builder):** Use an AI Coding Assistant embedded directly into your IDE to autocomplete code and refactor logic. We recommend **GitHub Copilot** for this phase.
* **The Application Phase (The Runtime Backend):** This is the reasoning engine that processes user requests and interacts with tools within your application. We recommend **Google AI Studio** for free execution.

### 1. Get GitHub Copilot for Free (Development)

For any GitHub user you can get copilot for free. It requires no credit card and no application.

1. **Sign In:** Log into your GitHub account on the web.
2. **IDE Setup:** Open VS Code or Visual Studio.
3. **Install Extension:** Search the Marketplace for "GitHub Copilot."
4. **Activate:** Click the profile icon in the bottom left of your IDE and select **"Sign in with GitHub to use Copilot."**
5. **Status:** You will be automatically enrolled in the **Copilot Free** plan.

**Important:** As of 2026, GitHub offers a **Free Tier** that includes **2,000 code completions** and **50 Chat/Premium requests** per month.

#### Best Practices to use the Free Tier

* **Use "Inline Completions" for boilerplate**, but **save your "Chat" requests for complex refactoring** to avoid hitting the 50-request cap on the Free plan.
* Completions are the "ghost" suggestions that appear as you type. **Each time you press Tab to accept a suggestion, it counts.**
* **Turn Off "Auto-Trigger":** By default, Copilot suggests code constantly. Go to your IDE settings and set it to manual or use a keyboard shortcut to trigger suggestions. This prevents "wasting" completions on simple things you could have typed yourself (like a public class declaration).
* Try to **trigger suggestions specifically for complex logic** rather than simple boilerplate.
* **Pause When Not Coding**: If you are just reading code or writing documentation in Markdown, disable Copilot via the status bar icon. This stops accidental completions from eating your 2,000-count quota.
* **Plan Before You Chat**: Never ask "Why isn't this working?" without context. That costs one request. Instead, gather your error logs and the relevant code first.
* **Use Multi-Turn Chats Wisely**: A "session" usually counts per prompt. If you can get the answer in one long, well-structured prompt (e.g., "Review this Java controller for security AND generate a unit test"), you save a request compared to asking for them separately.
* **Avoid "Agent Mode" for Small Fixes**: The Coding Agent (which edits multiple files) is powerful but can consume multiple "credits" in one go. Stick to standard Chat for simple refactoring.

### 2. Get Google AI Studio for Free (Runtime/Execution)

Google AI Studio provides a free, browser-based environment for developers to generate an API key and power their local ADK agents without needing a credit card or a paid subscription.

1. **Sign In:** Go to Google AI Studio (aistudio.google.com) and log in with your Google account.
2. **Get API Key:** In the left-hand sidebar menu, click on **"Get API key"**.
3. **Create Key:** Click the **"Create API key"** button. A default Google Cloud Project will automatically be created for you if you don't have one.
4. **Secure Your Key:** Copy the generated key. **Never commit this key to GitHub.** Always save it locally inside a `.env` file within your project directory (e.g., `GOOGLE_API_KEY="your_api_key_here"`).

#### AI Studio Free Tier Limits

* The free tier gives you access to models like **Gemini 2.5 Flash**, **Gemini 2.5 Pro**, and **Gemini 3 Pro Preview**.
* Usage is regulated through daily and per-minute quotas. As of early 2026, the free tier allows between 100 and 1,000 requests per day depending on the specific model you choose.
* **Note:** On the free tier, your prompts and data may be used by Google to improve their products.

