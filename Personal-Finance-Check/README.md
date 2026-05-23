# 💰 personal-finance-check

> A Claude skill for Persian/Iranian users — behavioral finance coaching + 47-point cost reduction system, built for people who actually want to spend less, not just feel good about budgeting.

---

## What This Skill Does

Most personal finance advice is generic. This skill is not.

`personal-finance-check` is a Claude skill that combines:
- A **47-point tactical checklist** of real cost-reduction actions (daily habits, utilities, shopping, food, transport)
- **Behavioral finance** — identifying *why* you overspend before telling you *how* to stop
- **Iranian/Persian cultural context** — Toman-denominated thinking, local platforms (Divar), Persian spending patterns like چشم و هم‌چشمی

It works in both **Persian (Farsi) and English**.

---

## How It Works

The skill uses a 3-layer framework:

```
Layer 1 — Behavioral   (highest ROI — fix the psychology first)
Layer 2 — Structural   (one-time fixes: banking setup, utilities, transport)
Layer 3 — Tactical     (daily compounding habits: grocery, shopping, food, social)
```

When you describe a spending problem, the skill runs a **4-step Spending Audit**:
1. Categorize current spend
2. Identify top 3 leak categories
3. Apply one fix per category (behavioral first)
4. Set one weekly constraint with a visible tracker

---

## Sample Triggers

The skill activates on queries like:

| Persian | English |
|---|---|
| چطور پول پس‌انداز کنم؟ | How do I save money? |
| هزینه‌هامو کم کنم | I want to reduce my expenses |
| خرج زندگیم زیاده | I'm spending too much |
| میخوام لباس بخرم | I want to buy clothes |
| حالم خوب نیست، میخوام بخرم | I feel bad and want to shop |

---

## Psychological Spending Traps Covered

| Trap | Signal | Antidote |
|---|---|---|
| Emotional spending | Shopping when sad/bored/angry | Delay 24h — you'll skip 80% of purchases |
| Social comparison (چشم و هم‌چشمی) | Buying because others have it | Ask: does this matter in 1 month? |
| Bargain hallucination | "It's on sale!" | Would you buy it at full price? If no → don't |
| Comfort buying | Stress → Digikala/Amazon | Replace with a 20-min walk |
| False economy | Cheap product, replaced often | Calculate total cost of ownership |

---

## Key Rules Inside the Skill

- **Items >200,000 Toman** → wait 1 full week before buying
- **One no-spend day per week** → cuts ~15% of discretionary spending automatically
- **End-of-season clothing sales** → 50–70% cheaper than buying in-season
- **Divar.ir** → underrated for secondhand, near-new items
- **Never shop hungry, sad, or stressed** → you buy 40% more unconsciously
- **Separate savings account from spending card** → friction prevents impulse withdrawal

---

## Related Skills

This skill integrates with:

- [`accounting-finance`](#) — for formal budgeting, P&L thinking, financial modeling
- [`longevity-coach`](https://github.com/pedrood/Claude-Skills/tree/main/Longevity-Coach) — for health-habit savings (quitting smoking, home cooking, preventive checkups)
- [`behdad-execution-engine`](#) — for breaking financial decision paralysis

---

## Installation

1. Download `personal-finance-check.skill`
2. Go to **Claude.ai → Settings → Skills**
3. Upload the `.skill` file
4. Start a conversation with `/personal-finance-check` or just ask about spending, saving, or budgeting

---

## Source

The 47-point checklist is adapted from the **BishtarAzYek.com** cost reduction checklist (بیشتر از یک نفر), extended with behavioral finance frameworks and Iranian/diaspora market context.

---

## License

MIT — use it, fork it, improve it.

---

*Built with [Claude Skills](https://claude.ai) · Maintained by [@pedrood](https://github.com/pedrood)*
