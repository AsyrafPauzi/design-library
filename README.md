# Design Library

A simple design system for AI-generated screens (Figma AI, Cursor, etc.).

**Before generating any screen, read this repo:**
1. `tokens/` — colors, typography, spacing
2. `components/` — button, input, card specs
3. `AI-INSTRUCTIONS.md` — copy-paste rules for Figma AI

---

## Quick start (Figma AI)

1. Open this repo on GitHub (or clone it)
2. Copy the prompt from `AI-INSTRUCTIONS.md`
3. Paste into Figma AI + add your screen requirement

Example:
```
[paste AI-INSTRUCTIONS prompt]

Create a login screen with email, password, and login button.
```

---

## Folder structure

```
design-library/
├── tokens/
│   ├── colors.json
│   ├── typography.json
│   └── spacing.json
├── components/
│   ├── button.md
│   ├── input.md
│   └── card.md
├── AI-INSTRUCTIONS.md    ← standing prompt for AI
└── README.md
```

---

## Sync to Figma (optional)

Use **Tokens Studio for Figma** plugin:
1. Install plugin in Figma
2. Connect this GitHub repo
3. Import `tokens/*.json` → creates Figma variables
4. Build components in Figma using those variables

---

## Customize

Edit the JSON files with your brand colors and fonts. Commit to GitHub. Re-import in Figma if using Tokens Studio.
