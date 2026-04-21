# 🧠 Claude Skills by Behdad Pedrood

> Custom skill files designed for Claude's skill system — each one encoding a domain of expertise, a personal framework, or a professional workflow into a reusable, triggerable instruction set.

---

## What Are Claude Skills?

Claude's skill system allows you to extend Claude's behavior with custom `SKILL.md` files. Each skill defines:

- **When to trigger** — keywords, contexts, and intent patterns that activate the skill
- **How to behave** — step-by-step instructions, constraints, output formats
- **What to produce** — structured, consistent, expert-level outputs

Skills live in a directory that Claude scans at runtime. When your prompt matches a skill's description, Claude loads its instructions and follows them — like plugging in a specialized expert for that task.

---

## Repository Structure

```
claude-skills/
├── README.md
├── user/                        # Personal & professional skills
│   ├── behdad-execution-engine/
│   ├── longevity-coach/
│   ├── dotnet-programming/
│   ├── excel-data-engineer/
│   ├── accounting-finance/
│   ├── social-media-admin/
│   ├── ttt-coach/
│   └── systemic-individualism/
└── public/                      # General-purpose skills
    ├── docx/
    ├── pdf/
    ├── pptx/
    ├── xlsx/
    └── frontend-design/
```

Each skill folder contains at minimum:

```
skill-name/
└── SKILL.md          # Frontmatter (name, description) + instruction body
```

Some skills include additional resources:

```
skill-name/
├── SKILL.md
├── references/       # Domain documentation loaded on demand
├── scripts/          # Executable helpers for deterministic tasks
└── assets/           # Templates, fonts, or static files
```

---

## Skills Index

### 🔴 Execution & Thinking

| Skill | Description |
|-------|-------------|
| `behdad-execution-engine` | Anti-paralysis, decision-forcing system. Breaks analysis loops and forces output when overthinking kicks in. |
| `systemic-individualism` | Analyzes systems, contracts, policies, and power structures through the lens of individual autonomy and coercion detection. |

### 🟢 Health & Performance

| Skill | Description |
|-------|-------------|
| `longevity-coach` | Integrated longevity science, neuroscience, and behavioral coaching. Covers sleep, VO2max, BDNF, Zone 2, habit formation, and more. |
| `ttt-coach` | Train-The-Trainer coaching skill. Iterative, anti-procrastination approach to becoming a better instructor and facilitator. |

### 🔵 Technical

| Skill | Description |
|-------|-------------|
| `dotnet-programming` | Expert C#, ASP.NET Core, EF Core, Blazor, SQL Server, design patterns, clean architecture, and microservices. |
| `excel-data-engineer` | Elite Excel expert + data engineering mindset. Power Query, DAX, VBA, dynamic arrays, ETL, dashboards. |
| `accounting-finance` | Financial statements, budgeting, IFRS/GAAP, ERP finance modules, financial modeling, and cash flow analysis. |

### 🟡 Communication & Content

| Skill | Description |
|-------|-------------|
| `social-media-admin` | LinkedIn, Instagram, Telegram, and multi-platform content strategy, caption writing, and community management. |

---

## How to Install

### Option 1 — Clone directly

```bash
git clone https://github.com/pedrood/claude-skills.git
```

Point your Claude skill directory to the cloned path in your setup.

### Option 2 — Copy individual skills

Copy any skill folder into your local skills directory:

```
your-skills-dir/
└── skill-name/
    └── SKILL.md
```

---

## Skill Design Philosophy

Every skill in this repository is built around three principles:

1. **Mechanism-first** — explain *why* something works, not just *what* to do
2. **Anti-fluff** — no padding, no generic advice, no motivational filler
3. **Execution-oriented** — every skill produces a concrete output or forces a decision

Skills are tested against real use cases and refined iteratively. A skill that doesn't change behavior in practice gets rewritten or removed.

---

## Contributing

This is a personal repository, but if you want to fork it and adapt skills for your own use case:

- Keep `SKILL.md` under 500 lines
- Put all triggering logic in the frontmatter `description` — not in the body
- Write descriptions that are slightly "pushy" — Claude under-triggers, so be explicit
- Test your skill against 5–10 real prompts before publishing

---

## Author

**Behdad Pedrood**  
Senior IT Professional | Software Architect | Product Manager  

- GitHub: [@pedrood](https://github.com/pedrood)
- LinkedIn: [linkedin.com/in/behdad-pedrood](https://linkedin.com/in/behdad-pedrood)

---

> Skills are live documents. They evolve as domains evolve and as edge cases are discovered. Check commit history for what changed and why.
