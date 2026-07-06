# How to Add Your Figma Components to GitHub

**For beginners — no coding needed.**

You already made components in Figma. This guide shows how to put those rules into the GitHub repo so Figma AI can follow them.

---

## Important to understand first

| What | Where it lives |
|------|----------------|
| **Real Figma components** (the actual buttons, cards you click and drag) | Stay in **Figma** |
| **Design rules** (colors, sizes, how button should look) | Go in **GitHub** as text + JSON |

You are **not uploading Figma files** to GitHub.  
You are **writing down the rules** from your Figma so AI can read them.

```
Your Figma components  →  you copy the values  →  GitHub (rules for AI)
```

---

## What you need

- [ ] Figma account (you already have this)
- [ ] **Your own** GitHub repo (create it first — see [CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md))
- [ ] 30–60 minutes (one time setup)

**You do NOT need:** Git installed, VS Code, or coding skills.  
You can edit everything **inside the GitHub website**.

> **Important:** Use **your own** repo (`github.com/YOUR-USERNAME/design-library`).  
> Do not use someone else's repo — create yours first.

---

## Part 0 — Create your repo (if you haven't yet)

Follow **[CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md)** step by step.  
Come back here after your repo exists.

---

## Part 1 — Add your colors (15 min)

### Step 1: Find your colors in Figma

1. Open your Figma design system file
2. Click a component (e.g. your primary button)
3. Look at the **Fill** color on the right panel
4. Click the color → copy the **HEX code** (example: `#2563EB`)

Write down your main colors:

| Name | Your HEX code |
|------|---------------|
| Primary (main brand color) | `#______` |
| Background | `#______` |
| Text | `#______` |
| Border | `#______` |
| Error (red) | `#______` |

### Step 2: Put colors in GitHub

1. Go to **your** repo: `https://github.com/YOUR-USERNAME/design-library`
2. Click `tokens` folder → click `colors.json`
3. Click the **pencil icon** (Edit this file) on the top right
4. Change the HEX values to **your** colors

Example — change this:

```json
"default": { "value": "#2563EB", "type": "color" }
```

To your color:

```json
"default": { "value": "#YOUR_COLOR", "type": "color" }
```

5. Scroll down → click **Commit changes** → **Commit changes** again

Done. Your colors are now on GitHub.

---

## Part 2 — Add your fonts (10 min)

### Step 1: Find fonts in Figma

1. Select a heading text in Figma
2. Note on the right panel:
   - **Font name** (e.g. Inter, Poppins)
   - **Size** (e.g. 32)
   - **Weight** (e.g. Bold = 700)

### Step 2: Put fonts in GitHub

1. Go to `tokens/typography.json` → click **Edit** (pencil)
2. Update font name and sizes to match your Figma
3. Click **Commit changes**

Also update `AI-INSTRUCTIONS.md` — find the TYPOGRAPHY section and change the font name and sizes to match.

---

## Part 3 — Add your spacing (5 min)

### In Figma

Check what spacing you use between elements (8, 16, 24, etc.).  
Use Figma's spacing or measure gap between items.

### In GitHub

1. Open `tokens/spacing.json` → **Edit**
2. Change values if yours are different
3. **Commit changes**

---

## Part 4 — Add your components (most important)

Do this for each component: **Button**, **Input**, **Card**, etc.

### Step 1: Inspect your component in Figma

Click your **Button** in Figma. Write down:

| Property | Your value |
|----------|------------|
| Background color | `#______` |
| Text color | `#______` |
| Corner radius | `__` px |
| Padding (top/bottom, left/right) | `__` px |
| Height | `__` px |
| Font size | `__` px |

### Step 2: Update the component file on GitHub

1. Go to `components/button.md` → **Edit**
2. Replace the example values with **your** values from Figma
3. **Commit changes**

Repeat for:
- `components/input.md` — your input field rules
- `components/card.md` — your card rules

### Step 3: Add new components (if you have more)

Example: you have a **Navbar** in Figma.

1. In GitHub repo, click **Add file** → **Create new file**
2. Name it: `components/navbar.md`
3. Write the rules (copy format from `button.md`):

```markdown
# Navbar

## Default
- Background: #FFFFFF
- Height: 64px
- Padding: 16px 24px
- Border bottom: 1px #E2E8F0

## Usage
- Logo on left, menu items on right
```

4. **Commit changes**

---

## Part 5 — Update the AI prompt (5 min)

After you change colors and components, update the copy-paste prompt:

1. Open `AI-INSTRUCTIONS.md` → **Edit**
2. Change colors, fonts, and component rules to match what you wrote
3. **Commit changes**

Now when you copy this file into Figma AI, it uses **your** design system.

---

## Part 6 — Use with Figma AI

Every time you create a screen:

1. Open `AI-INSTRUCTIONS.md` on GitHub
2. Copy the text inside the code block
3. Paste into Figma AI
4. Add your request:

```
[paste prompt]

Create a login screen with email, password, and login button.
```

---

## Easier way for colors only: Tokens Studio plugin

If you use **Figma Variables** for colors:

1. In Figma: **Plugins** → search **Tokens Studio for Figma** → Install
2. Open the plugin → **Settings** → connect to GitHub
3. Repo: `YOUR-USERNAME/design-library` (your own repo)
4. **Export** your Figma tokens → saves to `tokens/` folder automatically

This syncs colors/spacing without typing JSON by hand.  
You still need to write component rules in `components/*.md` yourself.

---

## Checklist — am I done?

- [ ] `tokens/colors.json` — my brand colors
- [ ] `tokens/typography.json` — my fonts
- [ ] `tokens/spacing.json` — my spacing
- [ ] `components/button.md` — matches my Figma button
- [ ] `components/input.md` — matches my Figma input
- [ ] `components/card.md` — matches my Figma card
- [ ] `AI-INSTRUCTIONS.md` — updated with my values
- [ ] Tested in Figma AI with copy-paste prompt

---

## Common questions

**Q: Do I upload my .fig file to GitHub?**  
No. Keep the Figma file in Figma. Only put the **rules** (colors, sizes) on GitHub.

**Q: Will Figma AI automatically read GitHub?**  
Not always. That’s why you **copy-paste** from `AI-INSTRUCTIONS.md` each time.

**Q: I don’t understand JSON. What do I do?**  
Only change the part inside quotes after `"value":`. Example: `"value": "#FF0000"` for red. Don’t remove commas or brackets. Or ask someone to help once with `colors.json`.

**Q: I have 20 components. Do I need all of them?**  
Start with the **5 most used** (Button, Input, Card, Navbar, Modal). Add more later.

**Q: Someone on my team updates Figma. How do we stay in sync?**  
When Figma changes, update the same values in GitHub (or re-export with Tokens Studio).

---

## Visual summary

```
FIGMA (you already have this)
├── Button component     ──┐
├── Input component      ──┼──→  Look at values (color, size, padding)
├── Card component       ──┘
                                    │
                                    ▼
GITHUB (you fill this in)
├── tokens/colors.json
├── tokens/typography.json
├── components/button.md
├── components/input.md
└── AI-INSTRUCTIONS.md  ──→  Copy into Figma AI when making screens
```

---

## Need help?

Share your repo with someone technical — they can help you fill in `colors.json` once from your Figma file. After that, you can maintain the `.md` files yourself using GitHub’s website editor.

**Haven't created a repo yet?** Start with [CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md)
