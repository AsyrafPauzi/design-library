# Design System + Figma AI — Simple Guide

Use this guide to generate screens with Figma AI while following one consistent design system from GitHub.

**First step:** Create **your own** GitHub repo → [CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md)  
**Malay:** [BINA-REPO-SENDIRI.md](./BINA-REPO-SENDIRI.md)

---

## What this is

- **GitHub** = where design rules live (colors, fonts, spacing, components)
- **Figma AI** = generates the screen
- **You** = only give the business requirement (e.g. “login screen”)

The AI should follow the design system so you only tweak **10–20%** of the output.

---

## Repo structure

```
design-library/
├── tokens/
│   ├── colors.json        # brand colors
│   ├── typography.json    # fonts & text styles
│   └── spacing.json       # spacing & border radius
├── components/
│   ├── button.md          # button rules
│   ├── input.md           # input rules
│   └── card.md            # card rules
├── AI-INSTRUCTIONS.md     # copy-paste prompt for Figma AI
├── GUIDE.md               # this file
└── README.md
```

---

## Quick start (easiest way)

### Step 1 — Open your repo

Go to: `https://github.com/YOUR-USERNAME/design-library`  
(Don't have one yet? Follow [CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md))

### Step 2 — Copy the AI prompt

1. Open **`AI-INSTRUCTIONS.md`**
2. Copy everything inside the code block (between the ``` marks)

### Step 3 — Use Figma AI

1. Open Figma → start Figma AI / Make
2. **Paste the prompt first**
3. Add what screen you want

**Example:**

```
[paste AI-INSTRUCTIONS here]

Create a login screen with:
- Email field
- Password field
- Login button
- "Forgot password?" link
```

### Step 4 — Review

Check colors, spacing, and components match the design system. Fix only what’s off.

---

## Standing prompt (save this)

Keep this and reuse every time. Full version is in `AI-INSTRUCTIONS.md`.

```
DESIGN SYSTEM RULES — follow strictly:

COLORS: Primary #2563EB, Background #FFFFFF, Text #0F172A, Border #E2E8F0
FONT: Inter — H1 32px bold, Body 16px, Label 14px medium
SPACING: 4, 8, 16, 24, 32 px only

COMPONENTS:
- Button: blue bg, white text, 8px radius, 44px height
- Input: white bg, border, label on top, 44px height
- Card: white bg, border, 12px radius, 24px padding

RULES:
1. Do NOT invent new colors
2. Do NOT invent new component styles
3. Use spacing scale only
```

Then add your screen requirement below it.

---

## Better results (optional): sync GitHub → Figma

Figma AI works best when variables and components already exist **in Figma**.

| Step | Action |
|------|--------|
| 1 | Install **Tokens Studio for Figma** (Figma plugin) |
| 2 | Connect this GitHub repo |
| 3 | Import `tokens/colors.json`, `typography.json`, `spacing.json` |
| 4 | Create Button, Input, Card in Figma using those variables |
| 5 | Publish as a **team library** |
| 6 | When using Figma AI, enable that library + paste the standing prompt |

```
GitHub (tokens)  →  Tokens Studio  →  Figma variables  →  Figma AI
```

---

## Customize your brand

Edit these files, then commit to GitHub:

| File | What to change |
|------|----------------|
| `tokens/colors.json` | Your brand colors |
| `tokens/typography.json` | Your fonts & sizes |
| `tokens/spacing.json` | Spacing scale |
| `components/*.md` | Component rules |
| `AI-INSTRUCTIONS.md` | Update the copy-paste prompt to match |

After editing, re-import in Tokens Studio if you use Figma sync.

---

## Workflow summary

```
┌─────────────────────────┐
│  1. Design system       │  GitHub repo (setup once)
│     colors, components  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  2. Copy AI prompt      │  AI-INSTRUCTIONS.md
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  3. Figma AI            │  prompt + "create login screen"
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  4. Review & tweak      │  ~10–20% manual fixes
└─────────────────────────┘
```

---

## Do / Don't

| Do | Don't |
|----|--------|
| Paste the standing prompt every time | Let AI design from scratch |
| Start with button, input, card | Build 50 components on day one |
| Keep tokens in GitHub | Hardcode random colors in each screen |
| Use Tokens Studio for Figma sync | Expect Figma AI to read GitHub by itself |

---

## Example prompts

**Login screen**
```
[paste AI-INSTRUCTIONS]

Create a login screen with email, password, login button, and forgot password link.
```

**Profile screen**
```
[paste AI-INSTRUCTIONS]

Create a profile screen with avatar, name, email, and edit profile button.
```

**Checkout screen**
```
[paste AI-INSTRUCTIONS]

Create a checkout summary card with item list, total price, and pay now button.
```

---

## Need help?

- **Tokens:** see `tokens/` folder
- **Components:** see `components/` folder
- **AI prompt:** see `AI-INSTRUCTIONS.md`
- **Create repo:** [CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md)
- **Add Figma to GitHub:** [HOW-TO-ADD-FIGMA-TO-GITHUB.md](./HOW-TO-ADD-FIGMA-TO-GITHUB.md)

---

## TL;DR

1. Create **your own** GitHub repo  
2. Add tokens + components from your Figma  
3. Copy prompt from `AI-INSTRUCTIONS.md`  
4. Paste into Figma AI + describe the screen  
5. Done
