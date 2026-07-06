# Start Here — Step-by-Step Checklist

Use this repo as your **template**. Everything is already set up — you only **replace** the example values with your Figma design.

**Repo:** https://github.com/AsyrafPauzi/design-library

**Time needed:** about 1 hour (one-time setup)

---

## Before you start

- [ ] You have a **Figma** account with components already made
- [ ] You have a **GitHub** account (free — sign up at https://github.com)
- [ ] You can open this repo in a browser

---

## Part A — Get your own copy of the repo

The templates are already in this repo. You need your own copy to edit.

### Option 1 — Fork (recommended)

- [ ] Open https://github.com/AsyrafPauzi/design-library
- [ ] Click **Fork** (top right)
- [ ] Click **Create fork**
- [ ] You now have: `https://github.com/YOUR-USERNAME/design-library`

### Option 2 — You were added as collaborator

- [ ] Open https://github.com/AsyrafPauzi/design-library
- [ ] You can edit files directly in this repo

> **Use your fork URL** in the steps below if you forked.  
> If you collaborate on the main repo, use `AsyrafPauzi/design-library`.

---

## Part B — Collect values from Figma (15 min)

Open your Figma design system file. Write down these values:

### Colors

- [ ] Primary button color → HEX: `#______`
- [ ] Background color → HEX: `#______`
- [ ] Main text color → HEX: `#______`
- [ ] Border color → HEX: `#______`
- [ ] Error red → HEX: `#______`

**How:** Click element → right panel **Fill** → copy HEX code

### Fonts

- [ ] Font name: `____________` (e.g. Inter, Poppins)
- [ ] Heading size: `__` px
- [ ] Body size: `__` px
- [ ] Label size: `__` px

### Spacing (gaps between elements)

- [ ] Small gap: `__` px (often 8)
- [ ] Medium gap: `__` px (often 16)
- [ ] Large gap: `__` px (often 24)

### Button (click your button in Figma)

- [ ] Background: `#______`
- [ ] Text color: `#______`
- [ ] Corner radius: `__` px
- [ ] Height: `__` px
- [ ] Padding: `__` px

### Input (click your input in Figma)

- [ ] Border color: `#______`
- [ ] Height: `__` px
- [ ] Corner radius: `__` px

### Card (if you have one)

- [ ] Background: `#______`
- [ ] Corner radius: `__` px
- [ ] Padding: `__` px

---

## Part C — Update template files on GitHub (30 min)

Go to **your repo** on GitHub. For each file: open file → click **pencil (Edit)** → change values → **Commit changes**.

### Tokens (JSON files)

- [ ] Edit `tokens/colors.json` — replace HEX codes with your colors  
      *(Only change text after `"value":` — keep `"` and `{ }` as they are)*

- [ ] Edit `tokens/typography.json` — replace font name and sizes

- [ ] Edit `tokens/spacing.json` — replace spacing values if different

### Components (markdown files)

- [ ] Edit `components/button.md` — match your Figma button

- [ ] Edit `components/input.md` — match your Figma input

- [ ] Edit `components/card.md` — match your Figma card

### AI prompt

- [ ] Edit `AI-INSTRUCTIONS.md` — update colors, fonts, spacing, and component rules to match what you wrote above

---

## Part D — Test with Figma AI (5 min)

- [ ] Open `AI-INSTRUCTIONS.md` on GitHub
- [ ] Copy everything inside the code block (between the ``` marks)
- [ ] Open Figma → start **Figma AI / Make**
- [ ] Paste the prompt
- [ ] Add your request, for example:

```
Create a login screen with email, password, and login button.
```

- [ ] Check the result — colors and components should match your design system
- [ ] If wrong, go back to Part C and fix the files

---

## Part E — Every time you design a new screen

- [ ] Open `AI-INSTRUCTIONS.md` on GitHub
- [ ] Copy the prompt
- [ ] Paste into Figma AI
- [ ] Add what screen you need (login, profile, checkout, etc.)
- [ ] Review and tweak ~10–20% if needed

---

## Final checklist — am I done?

- [ ] Forked repo (or have edit access)
- [ ] `tokens/colors.json` has **my** colors
- [ ] `tokens/typography.json` has **my** fonts
- [ ] `tokens/spacing.json` has **my** spacing
- [ ] `components/button.md` matches **my** Figma button
- [ ] `components/input.md` matches **my** Figma input
- [ ] `components/card.md` matches **my** Figma card
- [ ] `AI-INSTRUCTIONS.md` updated with **my** values
- [ ] Tested once in Figma AI — result looks mostly correct

---

## Quick reference

| What | File |
|------|------|
| Colors | `tokens/colors.json` |
| Fonts | `tokens/typography.json` |
| Spacing | `tokens/spacing.json` |
| Button rules | `components/button.md` |
| Input rules | `components/input.md` |
| Card rules | `components/card.md` |
| Copy for Figma AI | `AI-INSTRUCTIONS.md` |

**Repo:** https://github.com/AsyrafPauzi/design-library

---

## Need more detail?

- How to edit colors JSON → [HOW-TO-CREATE-COLORS-JSON.md](./HOW-TO-CREATE-COLORS-JSON.md) (Method 3)
- Malay checklist → [MULA-KAT-SINI.md](./MULA-KAT-SINI.md)

---

## TL;DR

```
1. Fork repo
2. Copy values from Figma
3. Edit template files on GitHub (replace example values)
4. Update AI-INSTRUCTIONS.md
5. Copy prompt → Figma AI → describe screen
```
