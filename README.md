# Claude Skills by Behdad Pedrood

> Custom skill files for Claude's skill system — each one encoding a domain of expertise, a personal framework, or a professional workflow into a reusable, triggerable instruction set.

---

## What Are Claude Skills?

Claude's skill system lets you extend Claude with custom instruction packs. Each skill defines:

- **When to trigger** — keywords, contexts, and intent patterns in the frontmatter `description`
- **How to behave** — step-by-step instructions, constraints, and output formats
- **What to produce** — structured, consistent, expert-level outputs

When your prompt matches a skill's description, Claude loads its instructions and follows them — like plugging in a specialized expert for that task.

---

## Repository Structure

```
Claude-Skills/
├── README.md
├── Freedom-Formal-System/
│   ├── README.md
│   ├── SKILL.md                      # Editable source (frontmatter + body)
│   ├── freedom-formal-system.skill   # Packaged skill for upload
│   └── references/
│       └── axioms-full.md
├── Longevity-Coach/
│   ├── README.md
│   └── longevity-coach.skill
└── Personal-Finance-Check/
    ├── README.md
    └── personal-finance-check.skill
```

Each skill folder contains at minimum:

```
skill-name/
├── README.md              # Human-readable overview and examples
└── skill-name.skill       # Packaged skill file for Claude.ai upload
```

Some skills also ship editable source and supporting files:

```
skill-name/
├── README.md
├── SKILL.md               # Frontmatter (name, description) + instruction body
├── skill-name.skill
├── references/            # Domain documentation loaded on demand
├── scripts/             # Executable helpers for deterministic tasks
└── assets/              # Templates, fonts, or static files
```

---

## Skills Index

### Philosophy & Formal Systems

| Skill | Folder | Description |
|-------|--------|-------------|
| **Freedom Formal System** | [`Freedom-Formal-System/`](Freedom-Formal-System/) | Consistent axiomatic formal system for freedom and individual property rights, derived from Mohammad Ali Jannatkhah Doost's *Nazariyeh Azadi, Iran va Din* (1405). Triggers on political, legal, economic, and religious arguments about freedom, property, and the state. Includes full axiom reference in Persian and English. Source: [@jannatkhah_ir](https://x.com/jannatkhah_ir) · [@jannatkhah.ir](https://instagram.com/jannatkhah.ir) |

### Health & Behavior

| Skill | Folder | Description |
|-------|--------|-------------|
| **Longevity Coach** | [`Longevity-Coach/`](Longevity-Coach/) | Integrates longevity science, neuroscience, and life coaching — mechanism-first, anti-fluff, one concrete action per response. Covers sleep, energy, habits, stress, Zone 2, biomarkers, and behavior change barriers. |

### Personal Finance

| Skill | Folder | Description |
|-------|--------|-------------|
| **Personal Finance Check** | [`Personal-Finance-Check/`](Personal-Finance-Check/) | Behavioral finance coaching plus a 47-point cost-reduction checklist for Persian/Iranian users (Toman, Divar, local spending patterns). Works in Farsi and English. Behavioral layer first, then structural fixes, then daily tactical habits. |

See each folder's `README.md` for sample triggers, hard rules, and detailed usage.

---

## How to Install

### Option 1 — Upload a packaged skill (recommended)

1. Clone or download this repository.
2. Open **Claude.ai → Settings → Skills**.
3. Upload the `.skill` file from the skill folder you want (e.g. `Longevity-Coach/longevity-coach.skill`).
4. Start a conversation; Claude activates the skill when your prompt matches its description.

### Option 2 — Clone the repository

```bash
git clone https://github.com/pedrood/Claude-Skills.git
```

Use the `.skill` files for upload. For **Freedom Formal System**, you can also edit `SKILL.md` and repackage if you maintain your own skill build workflow.

### Option 3 — Develop from source

For skills that include `SKILL.md`, edit the markdown source, then rebuild or repackage into a `.skill` file using your Claude skill tooling. Keep triggering logic in the frontmatter `description`, not buried in the body.

---

## Skill Design Philosophy

Every skill in this repository follows three principles:

1. **Mechanism-first** — explain *why* something works, not just *what* to do
2. **Anti-fluff** — no padding, no generic advice, no motivational filler
3. **Execution-oriented** — every skill produces a concrete output or forces a decision

Skills are tested against real use cases and refined iteratively. A skill that does not change behavior in practice gets rewritten or removed.

---

## Contributing

This is a personal repository, but you are welcome to fork and adapt skills for your own use:

- Keep `SKILL.md` under 500 lines when authoring source
- Put all triggering logic in the frontmatter `description` — not in the body
- Write descriptions that are slightly "pushy" — Claude under-triggers, so be explicit
- Test your skill against 5–10 real prompts before publishing

---

## Author

**Behdad Pedrood**  
Senior IT Professional · Software Engineer · Product Manager

- GitHub: [@pedrood](https://github.com/pedrood)
- LinkedIn: [linkedin.com/in/behdad-pedrood](https://linkedin.com/in/behdad-pedrood)

---

> Skills are live documents. They evolve as domains evolve and as edge cases are discovered. Check commit history for what changed and why.
