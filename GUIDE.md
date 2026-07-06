# Design Library — Setup Guide

One guide. Follow the checklist.

**Repo:** https://github.com/AsyrafPauzi/design-library  
**Tools:** Figma + **Tokens Studio** (Figma plugin) + Figma AI

---

## What you are doing

1. **Fork** this repo (templates already inside)
2. **Sync** your Figma colors to GitHub using **Tokens Studio**
3. **Edit** component files to match your Figma components
4. **Generate screens** in Figma AI using `AI-INSTRUCTIONS.md`

```
Figma (your components)
    ↓ Tokens Studio
GitHub (tokens + rules)
    ↓ copy AI-INSTRUCTIONS.md
Figma AI (new screens)
```

---

## Checklist

### A — Fork the repo (5 min)

- [ ] Open https://github.com/AsyrafPauzi/design-library
- [ ] Click **Fork** → **Create fork**
- [ ] You now have: `github.com/YOUR-USERNAME/design-library`

---

### B — Install Tokens Studio in Figma (5 min)

**Tokens Studio** = Figma plugin that syncs colors/fonts/spacing between Figma and GitHub.

- [ ] Open Figma
- [ ] Menu → **Plugins** → **Find more plugins**
- [ ] Search **Tokens Studio for Figma** → Install
- [ ] Open the plugin in your design file

---

### C — Connect Tokens Studio to your GitHub repo (10 min)

- [ ] In Tokens Studio → **Settings** (gear icon)
- [ ] **Add storage** → **GitHub**
- [ ] Log in to GitHub
- [ ] Select **your forked repo** (`YOUR-USERNAME/design-library`)
- [ ] Set folder to `tokens` if asked
- [ ] Save

---

### D — Sync colors from Figma → GitHub (10 min)

**If you use Figma Variables for colors:**

- [ ] In Tokens Studio, link your Figma color variables
- [ ] Click **Push to GitHub** (or Export)
- [ ] This updates `tokens/colors.json` automatically

**If you don't use Figma Variables — manual way:**

- [ ] Click each component in Figma → copy HEX color from **Fill**
- [ ] On GitHub, open `tokens/colors.json` → click **Edit** (pencil)
- [ ] Replace only the HEX codes after `"value":`
- [ ] **Commit changes**

Repeat for `tokens/typography.json` (fonts) and `tokens/spacing.json` (spacing) if needed.

---

### E — Match your components (15 min)

Templates are in `components/` — edit on GitHub to match your Figma:

Click your component in Figma, note the values, then edit on GitHub:

| File | What to copy from Figma |
|------|-------------------------|
| `components/button.md` | color, height, padding, corner radius |
| `components/input.md` | border, height, padding, corner radius |
| `components/card.md` | background, padding, corner radius |

- [ ] Edit `components/button.md` → **Commit**
- [ ] Edit `components/input.md` → **Commit**
- [ ] Edit `components/card.md` → **Commit**

---

### F — Update AI prompt (5 min)

- [ ] Open `AI-INSTRUCTIONS.md` on GitHub → **Edit**
- [ ] Change colors, fonts, spacing, and component rules to match your design
- [ ] **Commit changes**

---

### G — Test Figma AI (5 min)

- [ ] Open `AI-INSTRUCTIONS.md` on GitHub
- [ ] Copy everything inside the code block
- [ ] In Figma, open **Figma AI** (design agent)
- [ ] Paste the prompt, then add:

```
Create a login screen with email, password, and login button.
```

- [ ] Check result — should follow your design system
- [ ] If wrong, fix files in parts D–F and try again

---

### H — Every new screen

- [ ] Copy `AI-INSTRUCTIONS.md`
- [ ] Paste in Figma AI
- [ ] Describe the screen you need
- [ ] Tweak ~10–20% if needed

---

## Final checklist

- [ ] Forked repo
- [ ] Tokens Studio installed & connected to GitHub
- [ ] `tokens/colors.json` has my colors (via Tokens Studio or manual)
- [ ] `components/*.md` matches my Figma components
- [ ] `AI-INSTRUCTIONS.md` updated
- [ ] Tested in Figma AI — looks correct

---

## Files in this repo

| File | Purpose |
|------|---------|
| `tokens/colors.json` | Your brand colors |
| `tokens/typography.json` | Fonts & text sizes |
| `tokens/spacing.json` | Spacing scale |
| `components/button.md` | Button rules |
| `components/input.md` | Input rules |
| `components/card.md` | Card rules |
| `AI-INSTRUCTIONS.md` | Copy into Figma AI every time |

---

## Tips

- **Don't upload .fig files** to GitHub — only tokens and rules
- **Don't invent new colors** in Figma AI — always paste `AI-INSTRUCTIONS.md` first
- **Tokens Studio** keeps Figma and GitHub in sync when you change colors
- Start with 3 components (button, input, card). Add more later.

---

## TL;DR

```
Fork repo → Tokens Studio sync colors → Edit components → Update AI-INSTRUCTIONS.md → Figma AI
```
