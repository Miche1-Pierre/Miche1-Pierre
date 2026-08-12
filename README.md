<div align="center">

<img src="https://raw.githubusercontent.com/Miche1-Pierre/Miche1-Pierre/main/assets/banner.svg" width="860" alt="Pierre Michel — I build software for business outcomes" />

</div>

## Hey, I'm Pierre 👋

French software engineer, currently building in **Montréal** — and I like making things that actually get *used*. I care less about the framework than about what it's for, so **I start from the business, not the stack.** Give me an outcome a team actually needs, and I take it from framing to production: deciding what to build, what to automate, and where technical depth truly pays off.

One rule above the rest: **understand the business before you design the architecture.** It's what stops a system from being rebuilt six months later — and what turns engineering into something the business can *measure*.

Right now: **Head of Engineering & lead full-stack** — shipping AI-driven products that serve real processes, not demos, and building **Taskforce** & **Brain OS**.

---

## How I work

|  |  |
|---|---|
| 🎯 **Outcome first** | Automation that removes real cost, AI that serves an existing process, products that move a metric — not features for their own sake. |
| 🏗️ **Architecture that holds** | The business decides what has to be solid; my job is making sure it is — multi-tenant, secure, maintainable from day one. |
| 🤖 **AI where it earns its place** | Agentic systems and model-agnostic LLMs when they solve the problem, plain code when they don't. |

---

## 🛠️ Stack

<div align="center">

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=flat-square&logo=keycloak&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

</div>

| Area | Tooling |
|---|---|
| **Languages** | Java 21 · TypeScript · JavaScript · Python · SQL |
| **Backend** | Spring Boot *(Clean Architecture, multi-tenant)* · Node.js · REST APIs |
| **Frontend** | Next.js · React · React Native · TailwindCSS · Astro |
| **Databases** | PostgreSQL *(relational · pgvector / HNSW)* · MongoDB *(NoSQL)* |
| **Applied AI** | LLMs (Groq · Ollama) · RAG · AI agents · MCP servers · multi-agent orchestration · embeddings · ML/DL foundations |
| **Auth & Identity** | OAuth2 / OIDC · Keycloak · Clerk · RBAC |
| **DevOps & Infra** | Docker · Kubernetes · Jenkins · GitHub Actions · GHCR · Vercel · Nginx · MinIO · RabbitMQ · Linux · VMs · Git (GitFlow) |
| **Quality & Observability** | JUnit 5 · Jest · Playwright · SonarQube · PostHog · OWASP ZAP |
| **Security & Compliance** | 21 CFR Part 11 · GAMP 5 · RGPD / GDPR · **Loi 25** · **FINTRAC** |

---

## 🧩 Taskforce
> *The IDE executes. Taskforce orchestrates.*

**Today** — a multi-tenant work & project platform in the Linear / Plane family: workspaces, projects, issues, cycles, analytics, a wiki, chat, integrations, and an AI assistant.

**Where it's heading** — an **AI Delivery OS.** Instead of piloting an agent *inside* an IDE, Taskforce pilots the *whole* delivery pipeline — Idea → Product Spec → Architecture → Database → API → Implementation → Tests → Deploy — each stage a **validated checkpoint** you can't skip. You launch a *Run* (think GitHub Actions); coding agents (Claude Code, Cursor…) execute; Taskforce collects the logs, diffs, commits and tests, and gates each step. Every validated step **writes itself into Brain OS** — the documentation is generated *while* the product is built.

The bet: the best agent becomes a commodity as models improve. What nobody standardizes is **how an AI should deliver a project** — and that engine is model-agnostic (Claude, GPT, Gemini, all swappable underneath).

<details>
<summary><b>🔧 Architecture — a multi-tenant platform of containerized services</b></summary>

<br/>

```mermaid
%%{init: {'theme':'dark'}}%%
flowchart LR
    U([User]) --> FE["Next.js 16<br/>web app"]
    FE -->|"REST · JWT"| BE["Spring Boot 4<br/>multi-tenant API"]
    BE --> DB[("PostgreSQL 18<br/>+ pgvector · HNSW")]
    BE -->|OIDC| KC["Keycloak"]
    BE --> MQ["RabbitMQ"]
    BE --> OBJ["MinIO"]
    BE <-->|"agents · tools"| AI["AI orchestration<br/>Groq · model-agnostic"]
    AI <--> BOS["Brain OS<br/>knowledge graph"]
```

| Layer | Tech |
|---|---|
| Web / Landing | Next.js 16 · React 19 · TypeScript · Astro 5 |
| API | Spring Boot 4 · Java 21 · multi-tenant · REST / JWT |
| Auth | Keycloak · OIDC · RBAC |
| Data | PostgreSQL 18 · pgvector (HNSW) |
| Files / Queue | MinIO · RabbitMQ |
| AI | Groq (model-agnostic) · agent orchestration |
| Memory | Brain OS · knowledge graph + vector search |

</details>

📖 Full docs, ADRs, API &amp; the R&amp;D lab → **[@taskforce-project](https://github.com/taskforce-project)**

---

## 🧠 Brain OS — the research beneath the product
> *A world model of a software project.*

Brain OS is Taskforce's memory: the project's state as a **living knowledge graph** (PostgreSQL · pgvector · HNSW), readable in one pass by a human *or* an agent, and written to describe the **reality of the code** — not the intentions.

Underneath sits a genuine **R&D lab** — an honest attempt to formalize how a project *evolves*, under constraints that break the usual ML playbook:

- **State is the graph** — `S = G(V, E)`, nodes carrying *measurable* attributes, not decoration.
- **You never see the true state, only an estimate** — a POMDP framing; the graph knows it doesn't know everything.
- **A node is its state *and* its rhythm** (`ẋ`) — two cycles at 70%, one accelerating and one stalling, are not the same state.
- **Every axiom carries a falsifiable test** — an SQL query any dev can run to confirm or refute it. *No test → not an axiom, just a belief.*

The hard part is the setting: **one workspace (N ≈ 1), a non-replayable world, ~20 data points a year, near-zero compute.** That rules out learned world models (JEPA, MuZero, Dreamer) and forces a non-gradient, case-based approach. The question stops being *"which model"* and becomes **what you can honestly claim to know** about where a project is heading.

---

## 🧬 Where I'm heading

I want to point all of this — the engineering, the applied AI, the formal thinking — toward something whose stakes run deeper than performance: **health and the life sciences.** My next step is **bioinformatics** — bringing AI and solid software engineering to biological and clinical data, where the reliability of the code can matter to the people who depend on it.

---

## 🧭 How I got here

```mermaid
%%{init: {'theme':'dark'}}%%
timeline
    2024 : Software Engineering Intern — LORIA (CNRS · Inria)
    2025 : Full-Stack — SYNAPSIA
         : Full-Stack — Nancyclotep (pharmaceutical LIMS · 21 CFR Part 11)
    2026 : Head of Engineering &amp; Lead Full-Stack (Montréal)
         : Building Taskforce &amp; Brain OS
```

🎓 **Bachelor, Full-Stack Development** — Metz Numeric School (RNCP Level 6) · heading toward a **Master in bioinformatics**

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pierre-michel-work)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pierre.michel.work@gmail.com)
