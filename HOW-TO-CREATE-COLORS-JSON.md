# How to Create `tokens/colors.json`

**3 ways — pick the easiest for you.**

---

## What is `colors.json`?

A text file that lists your brand colors in a format AI and tools can read.

Example — one color looks like this:

```json
"default": { "value": "#2563EB", "type": "color" }
```

- `#2563EB` = your HEX color from Figma
- You copy colors from Figma → paste into this file on GitHub

---

## Method 1 — Manual (easiest, no plugin)

**Best if:** you have a few colors and don't use Figma Variables.

### Step 1: Collect colors from Figma

Open your Figma file. For each important color, click the element and copy the HEX code from the right panel.

| Name you choose | Where in Figma | Example HEX |
|-----------------|----------------|-------------|
| Primary | Main button fill | `#2563EB` |
| Background | Page background | `#FFFFFF` |
| Text | Body text | `#0F172A` |
| Border | Input border | `#E2E8F0` |
| Error | Error message | `#DC2626` |

**How to copy HEX in Figma:**
1. Click element (e.g. button)
2. Right panel → **Fill**
3. Click the color square
4. Copy the `#` code (e.g. `#2563EB`)

### Step 2: Create the file on GitHub

1. Open **your** repo on GitHub
2. **Add file** → **Create new file**
3. Name: `tokens/colors.json`
4. Paste this template and **replace** the HEX codes with yours:

```json
{
  "color": {
    "primary": {
      "default": { "value": "#YOUR_PRIMARY", "type": "color" }
    },
    "background": {
      "default": { "value": "#YOUR_BACKGROUND", "type": "color" }
    },
    "text": {
      "primary": { "value": "#YOUR_TEXT", "type": "color" }
    },
    "border": {
      "default": { "value": "#YOUR_BORDER", "type": "color" }
    },
    "status": {
      "error": { "value": "#YOUR_ERROR", "type": "color" }
    }
  }
}
```

5. **Commit changes**

**Rules when editing JSON:**
- Keep all `"` quotes and `{ }` brackets
- Only change text after `"value": `
- Every line except the last in a group needs a comma `,` at the end
- Colors must start with `#`

---

## Method 2 — Figma Variables + Tokens Studio (automatic)

**Best if:** you already use **Figma Variables** for colors.

### Step 1: Install plugin

1. Open Figma
2. Menu → **Plugins** → **Find more plugins**
3. Search: **Tokens Studio for Figma**
4. Install

### Step 2: Connect GitHub

1. Run the plugin in your Figma file
2. Go to **Settings** (gear icon)
3. **Add storage** → **GitHub**
4. Log in and select **your** repo (`YOUR-USERNAME/design-library`)
5. Set folder to `tokens` if asked

### Step 3: Export

1. In Tokens Studio, your Figma color variables should appear
2. Click **Export** or **Push to GitHub**
3. Plugin creates/updates `colors.json` automatically

You don't type JSON by hand.

---

## Method 3 — Start from template, fill in later

**Best if:** you want to set up the repo first, add real colors later.

1. Copy the full template below
2. Create `tokens/colors.json` on GitHub
3. Replace `#2563EB` etc. with your Figma colors when ready

```json
{
  "color": {
    "primary": {
      "default": { "value": "#2563EB", "type": "color" },
      "hover": { "value": "#1D4ED8", "type": "color" }
    },
    "background": {
      "default": { "value": "#FFFFFF", "type": "color" },
      "surface": { "value": "#F8FAFC", "type": "color" }
    },
    "border": {
      "default": { "value": "#E2E8F0", "type": "color" }
    },
    "text": {
      "primary": { "value": "#0F172A", "type": "color" },
      "secondary": { "value": "#64748B", "type": "color" }
    },
    "status": {
      "error": { "value": "#DC2626", "type": "color" },
      "success": { "value": "#16A34A", "type": "color" }
    }
  }
}
```

---

## Which method to choose?

| Situation | Use |
|-----------|-----|
| Beginner, few colors | **Method 1** — manual |
| Already use Figma Variables | **Method 2** — Tokens Studio |
| Repo setup first | **Method 3** — template |

---

## After `colors.json` is done

1. Update `AI-INSTRUCTIONS.md` with the same HEX codes (so Figma AI can read them)
2. Optional: import back into Figma via Tokens Studio

---

## Common mistakes

| Mistake | Fix |
|---------|-----|
| Forgot `#` before color | Use `#2563EB` not `2563EB` |
| Removed a comma | Each line needs `,` except the last in a group |
| Used RGB instead of HEX | Figma can show HEX — switch in color picker |
| Wrong file path | Must be exactly `tokens/colors.json` |

---

## Quick example

Figma button color = `#FF5722`

In `colors.json`:

```json
"primary": {
  "default": { "value": "#FF5722", "type": "color" }
}
```

That's it.
