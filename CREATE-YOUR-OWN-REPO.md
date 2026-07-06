# Create Your Own Design Library on GitHub

**Start here.** Create your own repo — do not use someone else's.

**You need:** GitHub account (free) + 20 minutes. No coding.

---

## Step 1 — Create GitHub account (if you don't have one)

1. Go to https://github.com
2. Click **Sign up**
3. Follow the steps (free plan is enough)

---

## Step 2 — Create a new repository

1. Log in to GitHub
2. Click the **+** icon (top right) → **New repository**
3. Fill in:

| Field | What to type |
|-------|----------------|
| Repository name | `design-library` |
| Description | `My design system for Figma AI` |
| Public or Private | **Public** (easier) or Private (only you see it) |
| Add README | ✅ **Check this box** |

4. Click **Create repository**

You now have your own repo, for example:  
`https://github.com/YOUR-USERNAME/design-library`

Replace **YOUR-USERNAME** with your GitHub username everywhere below.

---

## Step 3 — Create the folder structure

On your new repo page:

### Create `tokens` folder + `colors.json`

1. Click **Add file** → **Create new file**
2. In the name box, type: `tokens/colors.json`  
   (typing the `/` creates the folder automatically)
3. Paste this (change colors to yours later):

```json
{
  "color": {
    "primary": {
      "default": { "value": "#2563EB", "type": "color" }
    },
    "background": {
      "default": { "value": "#FFFFFF", "type": "color" }
    },
    "text": {
      "primary": { "value": "#0F172A", "type": "color" }
    }
  }
}
```

4. Click **Commit changes**

### Create `tokens/typography.json`

1. **Add file** → **Create new file**
2. Name: `tokens/typography.json`
3. Paste:

```json
{
  "fontFamily": {
    "sans": { "value": "Inter, sans-serif", "type": "fontFamily" }
  },
  "fontSize": {
    "base": { "value": "16px", "type": "fontSize" },
    "lg": { "value": "24px", "type": "fontSize" }
  }
}
```

4. **Commit changes**

### Create `tokens/spacing.json`

1. **Add file** → name: `tokens/spacing.json`
2. Paste:

```json
{
  "spacing": {
    "2": { "value": "8px", "type": "spacing" },
    "4": { "value": "16px", "type": "spacing" },
    "6": { "value": "24px", "type": "spacing" },
    "8": { "value": "32px", "type": "spacing" }
  }
}
```

3. **Commit changes**

---

## Step 4 — Create component files

### `components/button.md`

1. **Add file** → name: `components/button.md`
2. Paste:

```markdown
# Button

## Primary
- Background: #2563EB
- Text: white
- Padding: 12px 24px
- Border radius: 8px
- Min height: 44px

## Rules
- Do not use other colors for primary buttons
```

3. **Commit changes**

Repeat for `components/input.md` and `components/card.md` (see templates in HOW-TO-ADD-FIGMA-TO-GITHUB.md).

---

## Step 5 — Create AI instructions file

1. **Add file** → name: `AI-INSTRUCTIONS.md`
2. Copy your colors, fonts, and component rules into one prompt block
3. **Commit changes**

Use this every time you open Figma AI — copy the whole prompt, then add your screen request.

---

## Your repo should look like this

```
design-library/          ← YOUR repo
├── tokens/
│   ├── colors.json
│   ├── typography.json
│   └── spacing.json
├── components/
│   ├── button.md
│   ├── input.md
│   └── card.md
├── AI-INSTRUCTIONS.md
└── README.md
```

---

## Next steps

1. **Fill in your real values** from Figma → see [HOW-TO-ADD-FIGMA-TO-GITHUB.md](./HOW-TO-ADD-FIGMA-TO-GITHUB.md)
2. **Use with Figma AI** → copy `AI-INSTRUCTIONS.md` every time you design

---

## Checklist

- [ ] GitHub account created
- [ ] New repo `design-library` created under **my** account
- [ ] `tokens/` folder with 3 JSON files
- [ ] `components/` folder with button, input, card
- [ ] `AI-INSTRUCTIONS.md` created
- [ ] Values updated from my Figma file

**Your repo URL:** `https://github.com/YOUR-USERNAME/design-library`
