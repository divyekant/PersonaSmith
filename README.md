# PersonaSmith

A comprehensive library of research-backed AI agent persona prompts for every role in a large enterprise organization.

## What Is This?

PersonaSmith provides **production-ready system prompts** that turn AI agents into specialized enterprise professionals. Each persona is a self-contained Markdown file that can be dropped directly into any multi-agent swarm, LLM system prompt, or AI workflow.

Every persona is:
- **Self-contained** — No external dependencies. One file = one fully operational agent.
- **Research-backed** — Built from industry standards, competency frameworks, and best practices. Sources cited with backlinks.
- **Swarm-ready** — Includes collaboration maps and handoff protocols so agents know how to work together.
- **Structured consistently** — Every persona follows the same 10-section template for predictable behavior.

## How to Use a Persona

1. Browse the [Index](INDEX.md) or the `personas/` directory
2. Find the role you need
3. Copy the entire file contents into your agent's system prompt
4. The agent is now that role

Works with any LLM: Claude, GPT-4, Gemini, Llama, Mistral, and others.

### Adding Industry Context

Personas are industry-agnostic by default. To specialize for a specific industry:

1. Pick your persona (e.g., `personas/finance/cfo.md`)
2. Pick an industry overlay (e.g., `industries/healthcare.md`)
3. Combine both into your agent's system prompt: persona first, then industry overlay

```
System Prompt = [CFO Persona] + [Healthcare Industry Overlay]
→ Healthcare CFO Agent
```

See [INDUSTRY_TEMPLATE.md](INDUSTRY_TEMPLATE.md) for the industry overlay framework.

## Project Structure

```
PersonaSmith/
├── TEMPLATE.md          # Framework for creating new personas
├── INDUSTRY_TEMPLATE.md # Framework for creating industry overlays
├── INDEX.md             # Master index of all available personas
├── README.md            # You are here
├── industries/          # Industry context overlays (healthcare, fintech, etc.)
├── personas/
│   ├── executive-leadership/    # CEO, COO, CFO, CTO, CMO, CHRO, CISO, CDO
│   ├── finance/                 # Financial Analyst, Accountant, Controller, Treasury, Auditor
│   ├── engineering/             # Software Engineers, DevOps, SRE, QA, Architect, Tech Lead
│   ├── product/                 # Product Managers, Product Owner, Business Analyst
│   ├── design/                  # UX/UI Designers, UX Researcher, Design System Lead
│   ├── marketing/               # Marketing Manager, Content, SEO, Social, Brand, Growth
│   ├── sales/                   # Account Exec, SDR, Sales Manager, Sales Engineer, CS
│   ├── human-resources/         # HRBP, Recruiter, Talent, Comp & Benefits, L&D, ER
│   ├── legal/                   # General Counsel, Corporate Lawyer, Compliance, Contracts, Privacy
│   ├── customer-support/        # Support Agent, Support Manager, Tech Support, CX Manager
│   ├── operations/              # Ops Manager, Supply Chain, Facilities, Project/Program Manager
│   ├── data-analytics/          # Data Analyst, Data Engineer, Data Scientist, BI, ML Engineer
│   ├── security/                # Security Analyst, Security Engineer, Pen Tester, SecOps Manager
│   ├── procurement/             # Procurement Manager, Vendor Manager, Purchasing Specialist
│   └── quality-assurance/       # QA Manager, Quality Analyst, Process Improvement Specialist
```

## Persona Template Structure

Every persona follows a standardized 10-section framework (see [TEMPLATE.md](TEMPLATE.md)):

| Section | Purpose |
|---------|---------|
| **Identity** | Who you are — title, department, seniority, expertise |
| **Objective** | Your mission and what success looks like |
| **Responsibilities** | Core duties, what's in scope and out of scope |
| **Decision Framework** | How you reason, prioritize, and handle uncertainty |
| **Communication Style** | Tone, vocabulary, how you present information |
| **Collaboration Map** | Who you work with, handoff and escalation protocols |
| **Tools & Artifacts** | What tools you use, what you produce and consume |
| **Constraints & Rules** | Hard boundaries, compliance, things you must never do |
| **Success Metrics** | KPIs, targets, leading indicators |
| **Example Scenarios** | 2-3 realistic situations showing expected behavior |

Each persona also includes a **Sources** section with backlinks to the research used in its creation.

## Contributing

1. Read [TEMPLATE.md](TEMPLATE.md) carefully
2. Research the role thoroughly — use industry standards, professional associations, and established frameworks
3. Create a new `.md` file in the appropriate department folder
4. Follow the template exactly — fill all 10 sections
5. Include source attribution with backlinks in the `<sources>` section
6. Update [INDEX.md](INDEX.md) with the new persona
7. Submit a PR

**Rules:**
- Every claim must be research-backed
- Every persona must be fully self-contained
- File naming: `kebab-case.md` matching the role title
- Do not skip template sections

## File Format

Markdown with XML tags for internal structure. This format was chosen because:
- **Token efficient** — XML uses ~80% more tokens than Markdown for equivalent content
- **Universal LLM comprehension** — All major models understand Markdown natively
- **XML tags for precision** — Provides clear section boundaries that LLMs parse reliably
- **Human readable** — Easy to browse, edit, and review

## License

MIT
