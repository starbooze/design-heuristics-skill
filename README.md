# design-heuristics

A skill for [Claude Code](https://claude.ai/code) that evaluates any UI or visual design
against Nielsen Norman Group's 10 usability heuristics and core visual design principles.

Produces a **scored, structured audit** with concrete fixes — not vague suggestions.

**Responds in the language you write in** — Russian, English, or any other.

---

## What it does

Given a Figma screenshot, a verbal description, or a rendered UI, the skill:

- Scores each of the **10 NN heuristics** on a 1–5 scale with emoji indicators:
  `✅ solid` · `🟡 minor` · `⚠️ needs attention` · `🔴 significant` · `❌ critical`
- Checks **visual design fundamentals**: contrast (WCAG AA), spacing, typography
  hierarchy, alignment, proximity, color
- Outputs a structured report:
  - Overall UX Score out of 10
  - Top 3 Issues with actionable fixes
  - Quick Wins (low effort, high impact)
  - Full heuristics breakdown (H1–H10)
  - Visual design section

---

## Example output

```
## Design Audit: Registration Form

**Overall UX Score: 2.5/10**

### Top 3 Issues
1. **Form clears on validation error** — all 8 fields are wiped on submit failure.
   Never clear fields the user filled correctly — only highlight errors inline.
2. **"Fill the form correctly" error message** — doesn't name the field or explain why.
   Replace with field-level messages: "Email must contain @", "Passwords don't match".
3. **No Privacy Policy link** — collecting DOB, phone, email without a consent checkbox
   violates GDPR and signals distrust. Add before the submit button.

### H5 — Error prevention ❌  Score: 1/5
No inline validation, no password strength indicator, no real-time match check.
Fix: validate on blur for Email and Password Confirm at minimum.
```

---

## Installation

Copy the skill folder into your Claude Code skills directory:

**macOS / Linux**
```bash
git clone https://github.com/starbooze/design-heuristics-skill
cp -r design-heuristics-skill/design-heuristics ~/.claude/skills/
```

**Windows**
```powershell
git clone https://github.com/starbooze/design-heuristics-skill
Copy-Item -Recurse design-heuristics-skill\design-heuristics $env:USERPROFILE\.claude\skills\
```

Restart Claude Code — the skill will be available immediately.

---

## Usage

Describe your design or attach a screenshot and ask naturally — no slash command needed:

```
Check this design for usability issues
```
```
Heuristics review — registration form [screenshot]
```
```
What's wrong with this screen from a UX perspective?
```
```
Проверь этот дашборд по эвристикам Нильсена [скриншот]
```

Works with Figma screenshots, code-rendered UIs, component descriptions, or full verbal
walkthroughs of a flow.

---

## Repo structure

```
design-heuristics-skill/
├── README.md
├── design-heuristics.skill        # Packaged skill file (zip)
├── .claude/
│   └── skills/
│       └── design-heuristics/
│           └── SKILL.md           # Plugin format (for future marketplace support)
└── design-heuristics/
    └── SKILL.md                   # Source — copy this folder to install
```

---

## License

MIT
