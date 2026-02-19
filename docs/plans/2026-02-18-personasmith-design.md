# PersonaSmith — Design Document

**Date:** 2026-02-18
**Status:** Approved

## Overview

PersonaSmith is a comprehensive, open library of research-backed AI agent persona prompts covering every department and role in a large enterprise organization. Each persona is a self-contained Markdown file designed to be dropped directly into any multi-agent swarm as a system prompt with zero external dependencies.

## Goals

1. Provide production-ready system prompts for every major enterprise role
2. Each persona is fully self-contained — no inheritance, no external references needed
3. Every persona is backed by research with sources attributed via backlinks
4. A standardized template ensures consistency and makes contribution easy
5. Organized by department for intuitive navigation at scale (50-100+ roles)

## Project Structure

```
PersonaSmith/
├── README.md                            # Project overview, usage guide, contribution guidelines
├── INDEX.md                             # Master index of all personas, organized by department
├── TEMPLATE.md                          # The framework every persona must follow
├── personas/
│   ├── executive-leadership/
│   │   ├── chief-executive-officer.md
│   │   ├── chief-operating-officer.md
│   │   ├── chief-financial-officer.md
│   │   ├── chief-technology-officer.md
│   │   ├── chief-marketing-officer.md
│   │   ├── chief-human-resources-officer.md
│   │   ├── chief-information-security-officer.md
│   │   └── chief-data-officer.md
│   ├── finance/
│   │   ├── financial-analyst.md
│   │   ├── accountant.md
│   │   ├── financial-controller.md
│   │   ├── treasury-manager.md
│   │   └── internal-auditor.md
│   ├── engineering/
│   │   ├── software-engineer.md
│   │   ├── senior-software-engineer.md
│   │   ├── engineering-manager.md
│   │   ├── devops-engineer.md
│   │   ├── site-reliability-engineer.md
│   │   ├── qa-engineer.md
│   │   ├── solutions-architect.md
│   │   └── technical-lead.md
│   ├── product/
│   │   ├── product-manager.md
│   │   ├── senior-product-manager.md
│   │   ├── product-owner.md
│   │   └── business-analyst.md
│   ├── design/
│   │   ├── ux-designer.md
│   │   ├── ui-designer.md
│   │   ├── ux-researcher.md
│   │   └── design-system-lead.md
│   ├── marketing/
│   │   ├── marketing-manager.md
│   │   ├── content-strategist.md
│   │   ├── seo-specialist.md
│   │   ├── social-media-manager.md
│   │   ├── brand-manager.md
│   │   └── growth-marketing-manager.md
│   ├── sales/
│   │   ├── account-executive.md
│   │   ├── sales-development-representative.md
│   │   ├── sales-manager.md
│   │   ├── sales-engineer.md
│   │   └── customer-success-manager.md
│   ├── human-resources/
│   │   ├── hr-business-partner.md
│   │   ├── recruiter.md
│   │   ├── talent-acquisition-manager.md
│   │   ├── compensation-benefits-analyst.md
│   │   ├── learning-development-specialist.md
│   │   └── employee-relations-specialist.md
│   ├── legal/
│   │   ├── general-counsel.md
│   │   ├── corporate-lawyer.md
│   │   ├── compliance-officer.md
│   │   ├── contract-manager.md
│   │   └── privacy-officer.md
│   ├── customer-support/
│   │   ├── customer-support-agent.md
│   │   ├── customer-support-manager.md
│   │   ├── technical-support-engineer.md
│   │   └── customer-experience-manager.md
│   ├── operations/
│   │   ├── operations-manager.md
│   │   ├── supply-chain-manager.md
│   │   ├── facilities-manager.md
│   │   ├── project-manager.md
│   │   └── program-manager.md
│   ├── data-analytics/
│   │   ├── data-analyst.md
│   │   ├── data-engineer.md
│   │   ├── data-scientist.md
│   │   ├── business-intelligence-analyst.md
│   │   └── machine-learning-engineer.md
│   ├── security/
│   │   ├── security-analyst.md
│   │   ├── security-engineer.md
│   │   ├── penetration-tester.md
│   │   └── security-operations-manager.md
│   ├── procurement/
│   │   ├── procurement-manager.md
│   │   ├── vendor-manager.md
│   │   └── purchasing-specialist.md
│   └── quality-assurance/
│       ├── qa-manager.md
│       ├── quality-analyst.md
│       └── process-improvement-specialist.md
```

## Template Framework (TEMPLATE.md)

Every persona file follows this exact structure using Markdown with XML tags:

### Sections

1. **Identity** — Title, expertise domain, seniority level, department
2. **Objective** — Primary mission, what success looks like for this role
3. **Responsibilities** — Specific duties, scope boundaries, what's in/out of scope
4. **Decision Framework** — How to reason, prioritize, evaluate trade-offs
5. **Communication Style** — Tone, vocabulary, formality, how to present information
6. **Collaboration Map** — Which roles to interact with, handoff protocols, escalation paths
7. **Tools & Artifacts** — Tools used, outputs produced, deliverables
8. **Constraints & Rules** — Hard boundaries, compliance requirements, things to never do
9. **Success Metrics** — KPIs, measurable outcomes, performance indicators
10. **Example Scenarios** — 2-3 realistic situations demonstrating expected behavior

### Attribution

Every persona includes a `<sources>` section at the bottom with backlinks to the research used to build the prompt.

## File Format

- Markdown (`.md`) with XML tags for internal structure
- Each file is fully self-contained
- No external dependencies or inheritance
- File naming: `kebab-case.md` matching the role title

## Research Requirements

Each persona must be built from research, not fabricated. Research sources include:
- Industry job descriptions and competency frameworks
- Professional association standards (PMI, SHRM, AICPA, etc.)
- Best practice guides from consulting firms and industry leaders
- Role-specific prompt engineering research

## Departments (15 total)

1. Executive Leadership
2. Finance
3. Engineering
4. Product
5. Design
6. Marketing
7. Sales
8. Human Resources
9. Legal
10. Customer Support
11. Operations
12. Data & Analytics
13. Security
14. Procurement
15. Quality Assurance

## Total Estimated Roles: ~75-80 personas
