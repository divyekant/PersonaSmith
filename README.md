# PersonaSmith

> **75 research-backed AI agent personas across 15 enterprise departments.** Drop any persona into your agent's system prompt and it becomes that professional — with the right knowledge, decision frameworks, tools, relationships, and constraints.

---

## What Is PersonaSmith?

PersonaSmith is a library of production-ready system prompts that turn AI agents into specialized enterprise professionals. Each persona is a self-contained Markdown file (~300-400 lines) covering everything an agent needs to behave authentically in that role.

Every persona is:

- **Self-contained** — One file = one fully operational agent. No config, no setup.
- **Research-backed** — Built from IEEE standards, DORA metrics, BABOK, SHRM, IAPP, OWASP, MITRE ATT&CK, and 10-12 cited authoritative sources per persona.
- **Swarm-ready** — Includes a collaboration map with key relationships, handoff protocols, and escalation rules so agents know how to work with other agents.
- **Consistently structured** — Every persona follows the same 10-section template so behavior is predictable across your fleet.
- **Industry-agnostic by default** — Combine any persona with an industry overlay (fintech, healthcare, SaaS, etc.) to specialize it.

---

## Quick Start

1. Browse the [Index](INDEX.md) or the `personas/` directory
2. Find the role you need (e.g., `personas/engineering/software-engineer.md`)
3. Copy the entire file into your agent's system prompt
4. The agent is now that role

Works with any LLM: Claude, GPT-4o, Gemini, Llama, Mistral, and others.

### Adding Industry Context

```
System Prompt = [Software Engineer persona] + [industries/fintech.md]
→ Fintech Software Engineer agent
```

See [INDUSTRY_TEMPLATE.md](INDUSTRY_TEMPLATE.md) for creating new overlays.

---

## Persona Library — 75 Roles Across 15 Departments

| Department | Count | Roles |
|-----------|-------|-------|
| **Engineering** | 8 | Software Engineer, Senior Software Engineer, Technical Lead, Engineering Manager, Solutions Architect, DevOps Engineer, Site Reliability Engineer, QA Engineer |
| **Executive Leadership** | 8 | CEO, CTO, CFO, COO, CMO, CHRO, CISO, CDO |
| **Marketing** | 6 | Marketing Manager, Content Strategist, SEO Specialist, Growth Marketer, Brand Manager, Product Marketing Manager |
| **Human Resources** | 6 | HR Business Partner, Recruiter, Talent Acquisition Manager, Compensation & Benefits Specialist, Learning & Development Manager, People Operations Specialist |
| **Finance** | 5 | Financial Analyst, Financial Controller, Accountant, Internal Auditor, Treasury Manager |
| **Sales** | 5 | Account Executive, Sales Manager, Sales Engineer, Business Development Representative, Customer Success Manager |
| **Operations** | 5 | Operations Manager, Project Manager, Business Analyst, Program Manager, Business Operations Manager |
| **Data & Analytics** | 5 | Data Analyst, Data Engineer, Data Scientist, Analytics Engineer, BI Developer |
| **Legal** | 5 | General Counsel, Contracts Manager, Compliance Officer, IP Counsel, Privacy Counsel |
| **Security** | 4 | Security Analyst, Security Engineer, Penetration Tester, SOC Analyst |
| **Customer Support** | 4 | Customer Support Agent, Support Engineer, Customer Support Team Lead, Customer Experience Manager |
| **Product** | 4 | Product Manager, Senior Product Manager, Product Analyst, UX Researcher |
| **Design** | 4 | UI Designer, UX Designer, Product Designer, Visual Designer |
| **Quality Assurance** | 3 | QA Manager, Test Automation Engineer, Quality Engineer |
| **Procurement** | 3 | Procurement Manager, Vendor Manager, Purchasing Specialist |
| **Total** | **75** | |

---

## Persona Structure

Every persona follows a standardized 10-section framework:

| Section | What It Provides |
|---------|-----------------|
| `<identity>` | Title, department, seniority, reporting line, expertise domain, role description |
| `<objective>` | Primary mission statement + 5 success criteria |
| `<responsibilities>` | Core duties by category, in-scope list, out-of-scope list with handoff guidance |
| `<decision_framework>` | How to reason, prioritize, and handle uncertainty specific to this role |
| `<communication_style>` | Tone, vocabulary, formality levels, how to present information |
| `<collaboration_map>` | Key relationships table, handoff protocols, information shared/needed |
| `<tools_and_artifacts>` | Tools the role uses, artifacts produced, artifacts consumed |
| `<constraints_and_rules>` | Hard rules, compliance requirements, ethical boundaries, things never to do |
| `<success_metrics>` | KPI tables with targets and measurement methods, leading indicators |
| `<example_scenarios>` | 2-3 detailed realistic situations with step-by-step approach and outcomes |
| `<sources>` | 10-12 cited authoritative sources with URLs |

---

## Project Structure

```
PersonaSmith/
├── README.md                # You are here
├── TEMPLATE.md              # Framework for creating new personas
├── INDUSTRY_TEMPLATE.md     # Framework for creating industry overlays
├── INDEX.md                 # Master index of all available personas
├── industries/              # Industry context overlays
│   └── (fintech, healthcare, saas, etc.)
└── personas/
    ├── customer-support/    (4 personas)
    ├── data-analytics/      (5 personas)
    ├── design/              (4 personas)
    ├── engineering/         (8 personas)
    ├── executive-leadership/(8 personas)
    ├── finance/             (5 personas)
    ├── human-resources/     (6 personas)
    ├── legal/               (5 personas)
    ├── marketing/           (6 personas)
    ├── operations/          (5 personas)
    ├── procurement/         (3 personas)
    ├── product/             (4 personas)
    ├── quality-assurance/   (3 personas)
    ├── sales/               (5 personas)
    └── security/            (4 personas)
```

---

## Use Cases

**Multi-agent simulations** — Wire up a full org chart. Each agent behaves according to its role's decision frameworks, escalation rules, and communication style.

**Enterprise copilots** — Give your AI assistant the right professional context for the user's function. A legal team copilot uses the Contracts Manager or Privacy Counsel persona.

**AI-powered role plays** — Practice stakeholder conversations, sales pitches, design critiques, or code reviews with agents that behave like real professionals.

**Agent swarms** — Personas include collaboration maps and handoff protocols, making it straightforward to build agent teams that know when to escalate, who to hand off to, and what information to share.

---

## Contributing

1. Read [TEMPLATE.md](TEMPLATE.md) carefully — follow it exactly
2. Research the role thoroughly using professional associations, industry standards, and established frameworks
3. Create a new `.md` file in the appropriate department folder using `kebab-case.md`
4. Fill all 10 sections — no section may be left empty or skeletal
5. Include 8-12 real, authoritative sources with full URLs in `<sources>`
6. Update [INDEX.md](INDEX.md) with the new persona
7. Submit a PR

**Quality bar:** Every claim must be research-backed. Every persona must be fully self-contained. Do not skip template sections.

---

## File Format

Markdown with XML-style tags for section boundaries. This format was chosen because:

- **Universal LLM comprehension** — All major models parse Markdown and XML tags natively
- **Precise section boundaries** — XML tags allow agents to extract specific sections if needed
- **Human readable** — Easy to browse, edit, diff, and review in any text editor
- **Token efficient** — Pure Markdown with minimal wrapper structure

---

## License

MIT
