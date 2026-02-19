# PersonaSmith Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Build a comprehensive library of ~75-80 research-backed AI agent persona prompts for every major enterprise role, organized by department.

**Architecture:** Markdown files with XML tags for structure. Each persona is self-contained. A TEMPLATE.md defines the framework. An INDEX.md tracks all personas. Research first, write second — every persona is backed by web research with source attribution.

**Tech Stack:** Markdown, Git

---

### Task 1: Scaffolding — Create project structure, TEMPLATE.md, README.md

**Files:**
- Create: `TEMPLATE.md`
- Create: `README.md`
- Create: `INDEX.md`
- Create: all 15 department directories under `personas/`

**Step 1: Create all department directories**

```bash
mkdir -p personas/{executive-leadership,finance,engineering,product,design,marketing,sales,human-resources,legal,customer-support,operations,data-analytics,security,procurement,quality-assurance}
```

**Step 2: Write TEMPLATE.md**

The template framework that every contributor must follow. Contains the 10-section structure with XML tags, instructions for each section, and the sources attribution requirement.

**Step 3: Write README.md**

Project overview: what PersonaSmith is, how to use a persona (copy into agent system prompt), how to contribute (follow template), project structure, department listing.

**Step 4: Write INDEX.md**

Initial index with all 15 departments listed, with placeholder entries for each planned role. This will be updated as each persona is created.

**Step 5: Commit**

```bash
git add TEMPLATE.md README.md INDEX.md personas/
git commit -m "feat: scaffold PersonaSmith project structure, template, and index"
```

---

### Task 2: Executive Leadership Department (8 personas)

**Research → Write for each role:**
- Chief Executive Officer
- Chief Operating Officer
- Chief Financial Officer
- Chief Technology Officer
- Chief Marketing Officer
- Chief Human Resources Officer
- Chief Information Security Officer
- Chief Data Officer

**For each persona:**

1. **Research** — Web search for role best practices, competency frameworks, industry standards, decision-making frameworks specific to the role
2. **Write persona** — Follow TEMPLATE.md exactly, fill all 10 sections with research-backed content
3. **Add sources** — Include backlinks to all research sources in `<sources>` section
4. **Update INDEX.md** — Add entry with link to the new persona file
5. **Commit** — One commit per persona or batch per department

---

### Task 3: Finance Department (5 personas)

- Financial Analyst
- Accountant
- Financial Controller
- Treasury Manager
- Internal Auditor

Same research → write → attribute → index → commit flow.

---

### Task 4: Engineering Department (8 personas)

- Software Engineer
- Senior Software Engineer
- Engineering Manager
- DevOps Engineer
- Site Reliability Engineer
- QA Engineer
- Solutions Architect
- Technical Lead

---

### Task 5: Product Department (4 personas)

- Product Manager
- Senior Product Manager
- Product Owner
- Business Analyst

---

### Task 6: Design Department (4 personas)

- UX Designer
- UI Designer
- UX Researcher
- Design System Lead

---

### Task 7: Marketing Department (6 personas)

- Marketing Manager
- Content Strategist
- SEO Specialist
- Social Media Manager
- Brand Manager
- Growth Marketing Manager

---

### Task 8: Sales Department (5 personas)

- Account Executive
- Sales Development Representative
- Sales Manager
- Sales Engineer
- Customer Success Manager

---

### Task 9: Human Resources Department (6 personas)

- HR Business Partner
- Recruiter
- Talent Acquisition Manager
- Compensation & Benefits Analyst
- Learning & Development Specialist
- Employee Relations Specialist

---

### Task 10: Legal Department (5 personas)

- General Counsel
- Corporate Lawyer
- Compliance Officer
- Contract Manager
- Privacy Officer

---

### Task 11: Customer Support Department (4 personas)

- Customer Support Agent
- Customer Support Manager
- Technical Support Engineer
- Customer Experience Manager

---

### Task 12: Operations Department (5 personas)

- Operations Manager
- Supply Chain Manager
- Facilities Manager
- Project Manager
- Program Manager

---

### Task 13: Data & Analytics Department (5 personas)

- Data Analyst
- Data Engineer
- Data Scientist
- Business Intelligence Analyst
- Machine Learning Engineer

---

### Task 14: Security Department (4 personas)

- Security Analyst
- Security Engineer
- Penetration Tester
- Security Operations Manager

---

### Task 15: Procurement Department (3 personas)

- Procurement Manager
- Vendor Manager
- Purchasing Specialist

---

### Task 16: Quality Assurance Department (3 personas)

- QA Manager
- Quality Analyst
- Process Improvement Specialist

---

### Task 17: Final review and cleanup

1. Verify every persona follows TEMPLATE.md structure
2. Verify INDEX.md has links to every persona
3. Verify all source attributions are present
4. Final commit

---

## Execution Strategy

Each department task (Tasks 2-16) follows this workflow:

1. **Research batch** — Run parallel web searches for all roles in the department
2. **Write personas** — Use research to write each persona following TEMPLATE.md
3. **Attribute sources** — Add backlinks in `<sources>` section
4. **Update index** — Add all new personas to INDEX.md
5. **Commit** — One commit per department

**Parallelization:** Roles within the same department can be researched in parallel using subagents. Different departments are sequential to keep commits organized.

**Total:** 17 tasks, ~75-80 persona files
