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
├── Skills
│   └── FR-formal-system/
```

Each skill folder contains at minimum:

```
skill-name/
├── skill-name.md            # Frontmatter (name, description) + instruction body
└── skill-name.skil          # Calude skill file to install
```

Some skills include additional resources:

```
skill-name/
├── skill-name.md
├── references/       # Domain documentation loaded on demand
├── scripts/          # Executable helpers for deterministic tasks
└── assets/           # Templates, fonts, or static files
```

---

## Skills Index

### 🔴 Execution & Thinking

| Skill | Description |
|-------|-------------|
| `FR-formal-system`         | Derived from: Jannatkhah Doost, Nazariyeh Azadi, Iran va Din (1405)<br> Status: Consistent axiomatic formal system — extracted, formalized <br> X: [@jannatkhah_ir](https://x.com/jannatkhah_ir) <br>IG:[@jannatkhah.ir](Instagram.com/jannatkhah.ir)|

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
    └── skill-name.md
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
Senior IT Professional | Software Engineer | Product Manager  

- GitHub: [@pedrood](https://github.com/pedrood)
- LinkedIn: [linkedin.com/in/behdad-pedrood](https://linkedin.com/in/behdad-pedrood)

---

> Skills are live documents. They evolve as domains evolve and as edge cases are discovered. Check commit history for what changed and why.
