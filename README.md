# 🧠 SKILL Library

A curated collection of **AI agent skills** — reusable prompt modules and knowledge packs that extend the capabilities of AI coding assistants (Claude, Gemini, and others). Each skill is a self-contained directory with a `SKILL.md` file that defines a specialized persona, workflow, and knowledge set for a focused domain.

---

## About

The SKILL Library turns your AI assistant from a general-purpose chatbot into a team of specialized engineers. Instead of writing long, repetitive system prompts, you install a skill and instantly get expert-level guidance in that domain.

**How it works:**
- Each skill lives in its own directory containing a `SKILL.md` (the core prompt/persona definition) and optional `resources/`, `references/`, `examples/`, and `workflows/` sub-folders.
- Skills are composable — combine multiple skills to handle complex, multi-phase tasks.
- Skills specify which AI model is best suited for the task (`inherit`, `sonnet`, `opus`, `gemini`, etc.) and which tools they need.

---

## 📁 Repository Structure

```
SKILL-Library/
├── _core/                          # Foundational skills used by all others
│   ├── reasoning/                  # Logical analysis & decision frameworks
│   ├── writing/                    # Structured content generation
│   ├── debugging/                  # Systematic issue identification
│   └── validation/                 # Quality & correctness checking
│
├── agentic-engineering/            # Orchestrating AI agents effectively
├── antigravity-workflows/          # Multi-skill orchestration workflows
├── api-design-principles/          # REST & GraphQL API design
├── api-documentation-generator/    # Auto-generate API docs from code
├── api-documenter/                 # OpenAPI specs & developer portals
├── api-fuzzing-bug-bounty/         # API security testing & penetration
├── api-patterns/                   # REST vs GraphQL vs tRPC selection
├── api-security-best-practices/    # Auth, input validation, rate limiting
├── api-testing-observability-api-mock/ # API mocking & test environments
├── architecture/                   # Architectural decision records (ADRs)
├── architecture-patterns/          # Clean/Hexagonal/DDD architectures
├── aws-skills/                     # AWS infrastructure & cloud patterns
├── backend-architect/              # Scalable API & microservice design
├── backend-dev-guidelines/         # Backend coding standards
├── backend-development-feature-development/ # End-to-end feature delivery
├── bash-linux/                     # Bash/Linux terminal patterns
├── blockchain-developer/           # Web3, smart contracts, DeFi, NFTs
├── career-counseling/              # Career guidance & job search support
├── design-md/                      # Stitch design system synthesis
├── enhance-prompt/                 # UI prompt enhancement for Stitch
├── find-skills/                    # Skill discovery & installation helper
├── react-components/               # Stitch → React/Vite component conversion
├── remotion/                       # Video generation from Stitch projects
├── shadcn-ui/                      # shadcn/ui integration & customization
└── stitch-design/                  # Unified Stitch design entry point
```

---

## 🗂️ Skill Categories

### 🔧 Core Skills
Foundational reasoning and quality frameworks that support all other skills.

| Skill | Description |
|-------|-------------|
| `_core/reasoning` | Chain-of-thought analysis, trade-off evaluation, causal reasoning |
| `_core/writing` | Structured content generation: docs, reports, READMEs, changelogs |
| `_core/debugging` | Systematic root-cause analysis, reproduction, and fix verification |
| `_core/validation` | Quality and correctness checking across outputs |

### 🌐 API Skills
Everything you need to design, document, test, and secure APIs.

| Skill | Description |
|-------|-------------|
| `api-design-principles` | REST & GraphQL API design patterns and best practices |
| `api-patterns` | API style selection: REST vs GraphQL vs tRPC, versioning, pagination |
| `api-documentation-generator` | Auto-generate OpenAPI docs from existing codebases |
| `api-documenter` | Build developer portals, SDKs, and interactive API references |
| `api-security-best-practices` | Auth, authorization, input validation, rate limiting, OWASP protection |
| `api-testing-observability-api-mock` | Mock APIs for parallel development and integration testing |
| `api-fuzzing-bug-bounty` | API penetration testing, IDOR discovery, bug bounty techniques |

### 🏗️ Architecture Skills
Patterns and frameworks for building maintainable, scalable systems.

| Skill | Description |
|-------|-------------|
| `architecture` | Architectural decision-making and ADR documentation |
| `architecture-patterns` | Clean Architecture, Hexagonal Architecture, Domain-Driven Design |
| `backend-architect` | Microservices, service mesh, event-driven design, resilience patterns |

### ⚙️ Backend Development Skills
From coding standards to full feature delivery pipelines.

| Skill | Description |
|-------|-------------|
| `backend-dev-guidelines` | Backend coding standards and best practices |
| `backend-development-feature-development` | End-to-end feature orchestration from requirements to deployment |
| `bash-linux` | Bash scripting, terminal patterns, piping, error handling |
| `aws-skills` | AWS infrastructure automation and cloud architecture patterns |

### 🔗 Web3 & Blockchain
| Skill | Description |
|-------|-------------|
| `blockchain-developer` | Smart contracts, DeFi, NFTs, DAOs, enterprise blockchain integrations |

### 🎨 Frontend & UI Skills
Design, component generation, and video production.

| Skill | Description |
|-------|-------------|
| `stitch-design` | Unified Stitch entry point: prompt enhancement, design system, screen generation |
| `design-md` | Synthesize Stitch project design systems into `DESIGN.md` files |
| `enhance-prompt` | Transform vague UI ideas into Stitch-optimized prompts |
| `react-components` | Convert Stitch designs into modular Vite + React components |
| `shadcn-ui` | shadcn/ui component integration, customization, and best practices |
| `remotion` | Generate walkthrough videos from Stitch projects using Remotion |

### 🤖 Agentic & Workflow Skills
For orchestrating AI agents and multi-step automation.

| Skill | Description |
|-------|-------------|
| `agentic-engineering` | Principles for working effectively with AI coding agents |
| `antigravity-workflows` | Multi-skill orchestration for SaaS MVPs, security audits, AI agent builds |
| `find-skills` | Discover and install skills from the open agent skills ecosystem |

### 👔 Career & Soft Skills
| Skill | Description |
|-------|-------------|
| `career-counseling` | Structured career guidance, job search, interview prep, salary negotiation |

---

## 🚀 Getting Started

1. **Browse** the skill directories to find one matching your task.
2. **Read** the `SKILL.md` in that directory to understand what it does and when to use it.
3. **Install** the skill into your AI agent or coding assistant (method depends on your platform — e.g., copy to `.claude/skills/`, load via an agent config, or paste directly as a system prompt).
4. **Invoke** the skill by name or by describing your task to your AI agent.

### Using the `find-skills` skill

If you're unsure which skill to use, the `find-skills` skill helps you discover the right one:

```
"Find a skill for documenting my REST API"
"Is there a skill for smart contract development?"
"How do I test API security?"
```

---

## 📐 Skill File Format

Each `SKILL.md` starts with a YAML front-matter block:

```yaml
---
name: skill-name
description: When and why to invoke this skill
metadata:
  model: sonnet        # AI model preference (inherit | sonnet | opus | gemini | etc.)
  version: "1.0"
allowed-tools:         # Tools this skill is permitted to use
  - Read
  - Write
  - Bash
---
```

Followed by the skill body: persona, instructions, workflows, and examples.

---

## 🤝 Contributing

1. Create a new directory with your skill name (use `kebab-case`).
2. Add a `SKILL.md` with the YAML front-matter and skill content.
3. Optionally add `resources/`, `references/`, `examples/`, or `workflows/` sub-folders.
4. Follow the existing skill format — define clearly *when to use* and *when not to use* the skill.
5. Open a pull request with a description of what the skill does.

---

## 📄 License

See [LICENSE](LICENSE) for details.
