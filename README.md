# 🚀 Antigravity Agent Repository Template

A state-of-the-art repository template for building autonomous AI agents, multi-agent systems, and deterministic workflow pipelines. Built around a **3-Layer Architecture**, integrated with **Graphify Knowledge Graphs**, **Ponytail Lazy Senior Dev Mode**, and pre-loaded with **23 production-ready AI Agent Skills**.

---

## 🌟 Key Features

- **3-Layer Reliability Architecture**: Eliminates LLM error compounding by separating directives, orchestration, and execution.
- **Graphify Codebase Knowledge Graph**: Built-in AST-based knowledge graph for instant architecture navigation, GraphRAG querying, and codebase relationship tracking.
- **Ponytail Lazy Senior Dev Mode**: Automatically enforces YAGNI, stdlib-first, and minimal-code discipline — cutting bloat and unnecessary abstractions before they ship.
- **23 Pre-loaded Agent Skills**: Modular skills for document processing, web testing, frontend creation, Claude API SDKs, MCP server development, code auditing, and over-engineering review.
- **Self-Annealing System**: Native error-recovery loop where broken scripts self-correct, test, and update directives automatically.

---

## 🏗️ Pre-Initialized System Architecture

This template comes pre-configured with the **3-Layer Architecture** specified in [AGENTS.md](AGENTS.md):

```
.
├── AGENTS.md               # Core agent instructions, architectural rules & Ponytail rules
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
├── .agents/                # Workspace-scoped customizations (auto-loaded by Antigravity)
│   ├── rules/              # Always-on rules: graphify.md, ponytail.md
│   └── skills/             # Auto-discovered workspace skills (ponytail, graphify, etc.)
│
├── graphify-out/           # Pre-built Graphify Knowledge Graph
│   ├── graph.html          # Interactive visual graph view (open in browser)
│   ├── graph.json          # Raw graph data for GraphRAG querying
│   └── GRAPH_REPORT.md     # Codebase audit & structural metrics
│
└── skills/                 # 23 Bundled AI Agent Skills
```

### The 3-Layer Architecture Explained

| Layer       | Component                     | Description                                                                                                                                       |
| ----------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Layer 1** | **Directive** (`directives/`) | SOPs written in Markdown. Defines business goals, inputs, execution tools, expected outputs, and edge cases.                                      |
| **Layer 2** | **Orchestration** (AI Agent)  | Intelligent decision-making glue. Reads directives, invokes deterministic execution tools, handles errors, and updates directives with learnings. |
| **Layer 3** | **Execution** (`execution/`)  | Deterministic Python scripts. Executes API calls, data transformations, database queries, and filesystem operations reliably.                     |

---

## ⚡ Built-in Agent Engines: Graphify & Ponytail

This template ships two always-on agent engines that activate automatically in **Antigravity IDE** when you open any project cloned from this template. No setup required.

---

### 🔍 Graphify — Codebase Knowledge Graph & GraphRAG

**Purpose**: Graphify converts your entire codebase into a persistent, lightweight AST-driven knowledge graph stored in `graphify-out/`. The agent queries this graph to understand architecture, trace dependencies, and navigate code relationships — without reading every raw file or burning context tokens.

**Why it matters**: On a large project, asking the agent "how does X connect to Y?" without Graphify means it either guesses or reads dozens of files. With Graphify, one query returns a scoped subgraph in milliseconds.

#### How to Prompt with Graphify in Antigravity IDE

| Goal | Prompt example |
|---|---|
| Understand how a concept works | `"graphify query 'How does execution validation flow?'"` |
| Trace the path between two components | `"graphify path 'directives/scrape_website.md' 'execution/scrape_single_site.py'"` |
| Explain a specific node in depth | `"graphify explain 'MCPBuilder'"` |
| Sync graph after code changes | `"graphify update ."` |

> After adding or modifying files, always run `graphify update .` (AST-only, zero token cost) to keep the graph current.

View the live interactive graph: open `graphify-out/graph.html` in your browser.

---

### ✂️ Ponytail — Lazy Senior Dev Mode

**Purpose**: Ponytail puts a lazy, experienced senior developer inside the agent. Lazy means **efficient**, not careless. It stops the agent from over-engineering solutions, installing unnecessary packages, or scaffolding abstractions nobody asked for — when a single standard library call or a native platform feature already works.

**Why it matters**: AI agents default to over-building. A date picker becomes an npm package. A config value becomes an injectable factory. A two-line helper becomes a class hierarchy. Ponytail enforces the 7-step ladder that stops this at every response.

#### The 7-Step Ponytail Ladder

Before writing any code, the agent stops at the first rung that holds:

1. **YAGNI** — Does this need to exist at all? If speculative, skip it.
2. **Reuse** — Does a helper/util already exist in this codebase? Use it.
3. **Stdlib** — Does the standard library do this? Use it.
4. **Native** — Does a native platform feature cover it? (`<input type="date">` over a picker lib, CSS over JS, DB constraint over app code.)
5. **Installed Dep** — Does an already-installed package solve it? Use it, don't add another.
6. **One Line** — Can it be one line? Make it one line.
7. **Minimum Code** — Only then: write the minimum code that works.

#### How to Prompt with Ponytail in Antigravity IDE

| Goal | Prompt |
|---|---|
| Activate lazy mode (default, always-on) | `"/ponytail"` or `"be lazy"` or `"ponytail mode"` |
| Escalate to YAGNI extremist mode | `"/ponytail ultra"` — challenges requirements, deletes before adding |
| Softer mode: suggest lazy alternatives | `"/ponytail lite"` — builds what's asked, names the lazier option |
| Review a diff for over-engineering | `"/ponytail-review"` or `"review this for over-engineering"` |
| Audit entire repo for bloat | `"/ponytail-audit"` or `"audit this codebase for bloat"` |
| List all deferred shortcuts | `"/ponytail-debt"` — harvests all `# ponytail:` comments into a ledger |
| See benchmark savings scoreboard | `"/ponytail-gain"` |
| Quick reference for all commands | `"/ponytail-help"` |
| Deactivate | `"stop ponytail"` or `"normal mode"` |

> **Ponytail is active by default** — it loads automatically via `.agents/rules/ponytail.md` and `.agents/skills/` when you open this repo in Antigravity IDE. No prompt needed to turn it on.

---

## 🧰 Pre-installed Agent Skills

The template includes 23 fully configured skills in `.agents/skills/` and `skills/`:

| Skill | Description |
|---|---|
| ✂️ **`ponytail`** | Lazy senior dev mode: YAGNI, stdlib first, no unrequested abstractions, minimal diffs. |
| 🔍 **`ponytail-review`** | Over-engineering diff review: finds what to delete, one finding per line. |
| 🧹 **`ponytail-audit`** | Whole-repo bloat audit: ranked list of dead code, single-caller wrappers, excess deps. |
| 📑 **`ponytail-debt`** | Collects `# ponytail:` shortcut comments into a tracked debt ledger. |
| 📊 **`ponytail-gain`** | Benchmark scoreboard: measured savings in lines, cost, and speed from Ponytail mode. |
| ❓ **`ponytail-help`** | Quick-reference card for all Ponytail intensity levels, commands, and deactivation. |
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
