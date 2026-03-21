<!-- ═══════════════════════════════════════════════════════════════
     RAMI SHAMSEDDIN — GitHub Profile README
     ═══════════════════════════════════════════════════════════════ -->

<div align="center">

```
██████╗  █████╗ ███╗   ███╗██╗
██╔══██╗██╔══██╗████╗ ████║██║
██████╔╝███████║██╔████╔██║██║
██╔══██╗██╔══██║██║╚██╔╝██║██║
██║  ██║██║  ██║██║ ╚═╝ ██║██║
╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝╚═╝
```

### Full-Stack Developer · AI Engineer · Lebanon 🇱🇧

[![Email](https://img.shields.io/badge/chamseddinerami@gmail.com-0a0a0a?style=for-the-badge&logo=gmail&logoColor=white)](mailto:chamseddinerami@gmail.com)
[![Zygoflow](https://img.shields.io/badge/zygoflow.com-f59e0b?style=for-the-badge&logo=lightning&logoColor=black)](https://zygoflow.com)

</div>

---

<div align="center">

## 🤖 Zygoflow Agent Factory

### *The AI platform that OpenAI and Anthropic can't build — because it runs entirely on your machine.*

**[zygoflow.com/agents](https://zygoflow.com/agents)**

</div>

> Zygoflow is a local-first AI automation platform. You describe a goal in plain English — Brain plans it, writes the code, executes it, and learns from every run. No cloud dependency. No data leaving your machine. No rate limits killing your workflow.

---

### 🧠 Brain — Autonomous AI Planner with Long-Term Memory

The centerpiece of Zygoflow. Brain is not a chatbot — it's an autonomous agent that thinks, plans, executes, and **gets smarter over time**.

| Capability | What it does |
|---|---|
| **Goal Decomposition** | Converts a plain English goal into an executable multi-step plan automatically |
| **Long-Term Memory** | Stores every successful workflow in a local ChromaDB vector database — recalls similar past workflows when you describe new goals |
| **Verified Code Memory** | `🧠 Teach Brain` button — manually verify working agent code and Brain reuses that exact pattern forever |
| **Error Memory** | Every auto-fix Brain performs is saved — same errors never slow it down twice |
| **Workflow Mode** | Decomposes goals into parallel pipelines that run simultaneously and coordinate via shared blackboard |
| **RAG Skill Matching** | Each subtask matched to the most relevant Skills via vector embeddings |
| **Self-Healing** | If a subtask fails, Brain automatically fixes the code and retries up to 3 times |
| **Autonomous Execution** | Generates and executes code per subtask without human intervention |

**How memory makes Brain smarter:**
```
Run 1:  "Scrape a website and save SEO keywords to Word doc"
        → 🧠 No memories found — creating fresh plan
        → ✅ Completed → saved to memory

Run 2:  "Fetch a webpage and extract the most common keywords as docx"
        → 💭 Recalling similar workflows...
        → 🧠 Found: similarity 0.89 — reusing proven structure
        → ⚡ Generates correct pipeline instantly
```

---

### 🗂 Workflow Engine — Parallel Pipeline Orchestration

Multi-pipeline workflows where agents run **simultaneously** and coordinate through a shared blackboard system.

```
input-pipe     → asks user for URLs → pm_push("urls_list")
                          ↓ wakes up all 3 scrapers simultaneously
scraper-pipe-1 → pm_wait("urls_list") → scrapes URL 1 → pm_push("content_1")
scraper-pipe-2 → pm_wait("urls_list") → scrapes URL 2 → pm_push("content_2")  
scraper-pipe-3 → pm_wait("urls_list") → scrapes URL 3 → pm_push("content_3")
                          ↓ output-pipe wakes when all 3 complete
output-pipe    → pm_wait × 3 → combines → saves Word report
```

| Feature | Description |
|---|---|
| **PipelineManager Blackboard** | Thread-safe shared key-value store — pipelines push/wait for data across threads |
| **Fan-out / Fan-in** | One input feeds N parallel workers, N workers feed one output |
| **Per-Pipeline Stop Flags** | Stopping one pipeline never affects others running concurrently |
| **Live Status Panel** | Real-time execution dashboard — color-coded cards per pipeline, elapsed timers, live blackboard snapshot |
| **Workflow Groups** | Save named groups of pipelines — one click runs the entire multi-pipeline system |

---

### 🧩 Agent Architecture

| Feature | Description |
|---|---|
| **Sub-Agents** | Each agent is composed of atomic sub-agents, each doing exactly one thing |
| **Code Generation** | Each sub-agent generates executable Python from a natural language prompt |
| **Inline Code Editor** | View, edit and re-run generated code per sub-agent without leaving the app |
| **Skills Library** | Reusable blueprints that teach the AI exactly how to perform specific tasks |
| **X-Mode (RAG)** | Auto-selects the most semantically relevant Skills per sub-agent using vector embeddings |
| **🧠 Teach Brain** | Click to permanently teach Brain a working code pattern — recalled forever in future generations |

---

### 🔗 Pipeline & Orchestration

| Feature | Description |
|---|---|
| **Sequential Pipelines** | Chain agents step-by-step with fully shared memory between steps |
| **Auto-Run Mode** | Pipelines loop until `is_done = True` — fully autonomous execution |
| **Dynamic Routing** | Agents route to any other agent using `next_agent = "exact name"` |
| **Multi-Round** | Run for N rounds or loop indefinitely in auto mode |
| **Saved Pipelines** | Save, edit, re-run any pipeline — full CRUD with version control |

---

### ⏰ Triggers & Automation

| Feature | Description |
|---|---|
| **Interval Triggers** | Run pipelines every X minutes or hours automatically |
| **Daily Triggers** | Schedule pipelines at a specific time every day |
| **Folder Watch** | Auto-trigger when a new file appears in a monitored folder |
| **Webhook Triggers** | Expose any pipeline as an HTTP endpoint — trigger from Zapier, Make, or any service |
| **ngrok Integration** | Auto-generates a public webhook URL — zero server setup |

---

### 🖥️ Execution Environments

| Feature | Description |
|---|---|
| **Local Execution** | Agents run via `exec()` with full access to local files, APIs, and desktop tools |
| **Cloud Execution (E2B)** | Webhook/scheduled triggers execute in secure E2B cloud sandboxes |
| **Export as App** | One-click export of any pipeline as a standalone CustomTkinter desktop app |
| **Local LLM (Ollama)** | Run agents fully offline with local models — zero API costs |

---

### 🔌 Integrations

| Integration | Capabilities |
|---|---|
| **OpenAI GPT-4o** | Default model for Brain, code generation, and agent execution |
| **Anthropic Claude** | Alternative model — switchable per sub-agent |
| **Google Workspace** | Sheets (read/write/append/clear), Docs (read/create/append), Drive (list/upload/download) |
| **SendGrid** | Email sending with attachment support |
| **Custom APIs** | Define any API — AI auto-generates the callable function, injected into all agents |
| **Zygoflow Website** | Agents read/write directly to your Zygoflow website's live database |
| **Playwright** | Full browser automation and JS-rendered web scraping |

---

### 🌐 Zygoflow AI Website Builder

**[zygoflow.com](https://zygoflow.com)**

Natural language → instant data-driven web components with real-time database sync. Describe what you want, get a live website component that reads and writes to a real database.

---

### 🎮 Published Games

| Game | Platform |
|---|---|
| [World War 2: Defending Battle](https://play.google.com/store/apps/details?id=com.rsGaming.WorldWar2Defendingbattle) | Google Play |
| [Scream Hunter](https://play.google.com/store/apps/details?id=com.rsgaming.screamhunter) | Google Play |

---

### 🛠 Tech Stack

<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" width="40" height="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" width="40" height="40"/>
<img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" width="40" height="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" width="40" height="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" width="40" height="40"/>
<img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" width="40" height="40"/>
<img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" width="40" height="40"/>
<img src="https://www.vectorlogo.zone/logos/unity3d/unity3d-icon.svg" width="40" height="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" width="40" height="40"/>
<img src="https://www.microsoft.com/en-us/sql-server" width="40" height="40"/>
</p>

**AI/ML:** ChromaDB · OpenAI Embeddings · Playwright · CustomTkinter · E2B  
**Web:** Next.js · Node.js · Firebase · Supabase · Vercel  
**Languages:** Python · JavaScript · C# · Java · HTML/CSS

---

<div align="center">

*"I think I'm funny ⚡"*

**[zygoflow.com](https://zygoflow.com)** · **[zygoflow.com/agents](https://zygoflow.com/agents)** · **chamseddinerami@gmail.com**

</div>
