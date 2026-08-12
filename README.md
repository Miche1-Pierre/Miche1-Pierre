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
| 🤖 **AI where it earns its place** | Agentic systems and self-hosted LLMs when they solve the problem, plain code when they don't. |

---

## 🛠️ Stack

<div align="center">

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=flat-square&logo=keycloak&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

</div>

| Layer | Tooling |
|---|---|
| **Backend** | Java 21 · Spring Boot *(Clean Architecture, multi-tenant)* · PostgreSQL · REST APIs · Python · Node.js |
| **Frontend** | TypeScript · Next.js / React · React Native · TailwindCSS |
| **Applied AI** | LLMs · RAG · AI agents · MCP servers · multi-agent orchestration · embeddings · ML/DL foundations |
| **Security & Compliance** | OAuth2 / OIDC (Keycloak) · RBAC · OWASP ZAP · 21 CFR Part 11 · GAMP 5 · GDPR |
| **DevOps & Quality** | Docker · GitHub Actions · GHCR · Nginx · Git (GitFlow) · JUnit 5 · Jest · Playwright · SonarQube |

---

## 🧩 Taskforce
> *Describe the outcome — Taskforce orchestrates the execution.*

**The problem:** teams lose hours stitching work across the tools they already use — the *coordination*, not the work itself, is the real cost.

**The product:** an execution layer that sits on top of those tools. You describe *what* needs to happen; an **agentic core** works out the *how*, coordinates it across the team's tools, and remembers context through Brain OS. Multi-tenant from day one, with a **self-hosted LLM** so no customer data ever leaves the box.

**What I'm proud of:**
- **Strict multi-tenancy** enforced at every layer — isolation is a guarantee, not a convention.
- An **agentic core** that plans and executes across real tools — not a chatbot bolted on the side.
- A **self-hosted LLM** (Ollama · Qwen) — privacy by architecture, zero data exfiltration.
- **9 containerized services**, CI/CD, security-reviewed end to end.

<details>
<summary><b>🔧 Architecture — a multi-tenant platform of 9 containerized services</b></summary>

<br/>

```mermaid
%%{init: {'theme':'dark'}}%%
flowchart LR
    U([User]) --> FE["Next.js<br/>web app"]
    FE -->|"REST · JWT"| BE["Spring Boot<br/>backend · multi-tenant"]
    BE --> DB[("PostgreSQL")]
    BE -->|OIDC| KC["Keycloak<br/>auth"]
    BE <-->|"agents · tools"| AI["AI service<br/>self-hosted Ollama · Qwen"]
    AI <--> BOS["Brain OS<br/>memory"]
    BOS --> KG[("Knowledge graph<br/>+ vector search")]
```

| Layer | Tech |
|---|---|
| Web | Next.js · TypeScript |
| API | Spring Boot · multi-tenant · REST / JWT |
| Auth | Keycloak · OIDC · RBAC |
| Data | PostgreSQL |
| AI | self-hosted Ollama · Qwen · multi-agent orchestration |
| Memory | Brain OS · knowledge graph + vector search |

</details>

📖 Full architecture, ADRs, API &amp; security docs → **[@taskforce-project](https://github.com/taskforce-project)**

---

## 🧠 Brain OS
> *Persistent memory for LLM agents.*

**Why it matters for the product:** most "AI memory" is just a bigger prompt — costly and forgetful. Brain OS is a structured store of **state, context, and the consequences of actions**, so an agent reasons over what actually happened. The payoff: AI that stays reliable as usage grows.

<details>
<summary><b>🔧 How it's built</b></summary>

<br/>

```mermaid
%%{init: {'theme':'dark'}}%%
flowchart LR
    AG["LLM agent"] -->|"read / write"| BOS["Brain OS"]
    DEV(["Developer"]) -->|query| BOS
    BOS --> KG[("Knowledge graph")]
    BOS --> VEC[("Vector search")]
```

R&amp;D on the **architecture, not the model** — the hard part of an AI system is rarely the model call. It's the context you give it, and what you do with its answer.
</details>

---

## 🧬 Where I'm heading

I want to point all of this — the engineering, the applied AI — toward something whose stakes run deeper than performance: **health and the life sciences.** My next step is **bioinformatics** — bringing AI and solid software engineering to biological and clinical data, where the reliability of the code can matter to the people who depend on it.

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
