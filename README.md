# 🚀 Antigravity Agent Repository Template

A state-of-the-art repository template for building autonomous AI agents, multi-agent systems, and deterministic workflow pipelines. Built around a **3-Layer Architecture**, integrated with **Graphify Knowledge Graphs**, and pre-loaded with **17 production-ready AI Agent Skills**.

---

## 🌟 Key Features

- **3-Layer Reliability Architecture**: Eliminates LLM error compounding by separating directives, orchestration, and execution.
- **Graphify Codebase Knowledge Graph**: Built-in AST-based knowledge graph for instant architecture navigation, GraphRAG querying, and codebase relationship tracking.
- **17 Pre-loaded Agent Skills**: Modular skills for document processing, web testing, frontend creation, Claude API SDKs, MCP server development, and skill creation.
- **Self-Annealing System**: Native error-recovery loop where broken scripts self-correct, test, and update directives automatically.

---

## 🏗️ Pre-Initialized System Architecture

This template comes pre-configured with the **3-Layer Architecture** specified in [AGENTS.md](AGENTS.md):

```
.
├── AGENTS.md               # Core agent instructions and architectural rules
├── README.md               # Project documentation
├── .env.example            # Template for environment variables and API keys
├── .gitignore              # Pre-configured rules ignoring .tmp/, .env, credentials, & graphify-out
│
├── directives/             # Layer 1: Natural language SOPs (What to do)
│   └── README.md           # Guidelines for writing directives
│
├── execution/              # Layer 3: Deterministic Python scripts (Doing the work)
│   └── README.md           # Standards for tool execution scripts
│
├── .tmp/                   # Intermediate temporary processing files (Never committed)
│   └── README.md
│
├── graphify-out/           # Pre-built Graphify Knowledge Graph
│   ├── graph.html          # Interactive visual graph view (open in browser)
│   ├── graph.json          # Raw graph data for GraphRAG querying
│   └── GRAPH_REPORT.md     # Codebase audit & structural metrics
│
└── skills/                 # 17 Bundled AI Agent Skills
```

### The 3-Layer Architecture Explained

| Layer | Component | Description |
|---|---|---|
| **Layer 1** | **Directive** (`directives/`) | SOPs written in Markdown. Defines business goals, inputs, execution tools, expected outputs, and edge cases. |
| **Layer 2** | **Orchestration** (AI Agent) | Intelligent decision-making glue. Reads directives, invokes deterministic execution tools, handles errors, and updates directives with learnings. |
| **Layer 3** | **Execution** (`execution/`) | Deterministic Python scripts. Executes API calls, data transformations, database queries, and filesystem operations reliably. |

---

## 🧰 Pre-installed Agent Skills

The template includes 17 fully configured skills in the `skills/` directory:

| Skill | Description |
|---|---|
| 🎨 **`algorithmic-art`** | Creates visual generative art and algorithmic philosophy scripts. |
| 🎨 **`brand-guidelines`** | Enforces Anthropic visual identity, color palettes, and typography rules. |
| 📐 **`canvas-design`** | Multi-page visual layout and canvas design principles. |
| 🤖 **`claude-api`** | Complete Claude API reference, SDK guidance, Managed Agents, prompt caching, and tool use. |
| 📝 **`doc-coauthoring`** | Multi-stage collaborative document draft, review, and refinement workflow. |
| 📄 **`docx`** | Word document creation, XML schema validation, track changes validation, and editing. |
| 💅 **`frontend-design`** | Production design principles, restraint, and subject-grounded UI development. |
| 📢 **`internal-comms`** | Company newsletters, 3P updates, and internal comms drafting. |
| 🔌 **`mcp-builder`** | Building, evaluating, and testing Model Context Protocol (MCP) servers in Python and TypeScript. |
| 📕 **`pdf`** | PDF generation, table/text/image extraction, form filling, and page manipulation. |
| 📊 **`pptx`** | PowerPoint slide generation, XML schema validation, themes, and chart building. |
| 🛠️ **`skill-creator`** | Creating, evaluating, benchmarking, and optimizing new agent skills. |
| 🎬 **`slack-gif-creator`** | Creating optimized Slack GIFs with custom easing curves and frame composition. |
| 🎨 **`theme-factory`** | Curated color themes (e.g., Midnight Galaxy, Desert Rose, Ocean Depths). |
| 🌐 **`web-artifacts-builder`** | Packaging single-file web artifacts with React, Tailwind CSS, and Shadcn UI components. |
| 🧪 **`webapp-testing`** | Automated browser testing, server readiness polling, and console log capture. |
| 📈 **`xlsx`** | Excel workbook creation, formula recalculation, openpyxl gotchas, and financial modeling. |

---

## 🚀 How to Use When Starting a New Project

### 1. Create a Repository from this Template
Click **"Use this template"** on GitHub or clone the repository locally:
```bash
git clone https://github.com/FinShin/Antigravity_repo_template.git my-new-agent-project
cd my-new-agent-project
```

### 2. Configure Environment
Copy the example environment file and add your API keys:
```bash
cp .env.example .env
```

### 3. Add Your First Directive and Execution Script
- Write your process standard operating procedure in `directives/my_task.md`.
- Create your deterministic tool script in `execution/my_tool.py`.
- Run your task through the AI assistant!

### 4. Query & Maintain Knowledge Graph with Graphify
This project includes `graphify` for zero-cost AST codebase exploration:

```bash
# Query the codebase graph
graphify query "How does docx validation work?"

# Update the graph after adding new code files (AST-only, fast, zero token cost)
graphify update .

# Trace relationships between components
graphify path "safe_extract" "DOCXSchemaValidator"

# Explain a specific component
graphify explain "MCPConnection"
```

View the interactive knowledge graph by opening `graphify-out/graph.html` in your browser.

---

## 🔄 Self-Annealing Workflow

When something breaks during execution:
1. **Fix the execution script** in `execution/`.
2. **Test the script** until it passes reliably.
3. **Update the directive** in `directives/` with new learnings (e.g. rate limits, timing, edge cases).
4. **Re-run `graphify update .`** to keep the architecture knowledge graph current.

---

## 📄 License

This repository template is licensed under the MIT License.
