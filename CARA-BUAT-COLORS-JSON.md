# Cara Buat `tokens/colors.json`

**3 cara — pilih yang paling senang.**

---

## Apa itu `colors.json`?

File text yang senaraikan warna brand dalam format yang AI boleh baca.

Satu warna dalam file:

```json
"default": { "value": "#2563EB", "type": "color" }
```

- `#2563EB` = kod HEX dari Figma
- Copy warna Figma → paste dalam file ni kat GitHub

---

## Cara 1 — Manual (paling senang, tak perlu plugin)

### Langkah 1: Ambil warna dari Figma

1. Buka file Figma
2. Klik element (contoh: button)
3. Panel kanan → **Fill** → klik warna
4. Copy kod **HEX** (contoh: `#2563EB`)

Catat warna penting:

| Nama | Dari mana | HEX |
|------|-----------|-----|
| Primary | Button utama | `#______` |
| Background | Latar page | `#______` |
| Text | Teks body | `#______` |
| Border | Border input | `#______` |
| Error | Mesej error | `#______` |

### Langkah 2: Buat file kat GitHub

1. Buka **repo sendiri** kat GitHub
2. **Add file** → **Create new file**
3. Nama: `tokens/colors.json`
4. Paste template ni, **tukar** HEX dengan warna kau:

```json
{
  "color": {
    "primary": {
      "default": { "value": "#WARNA_KAU", "type": "color" }
    },
    "background": {
      "default": { "value": "#WARNA_KAU", "type": "color" }
    },
    "text": {
      "primary": { "value": "#WARNA_KAU", "type": "color" }
    },
    "border": {
      "default": { "value": "#WARNA_KAU", "type": "color" }
    },
    "status": {
      "error": { "value": "#WARNA_KAU", "type": "color" }
    }
  }
}
```

5. **Commit changes**

**Peraturan edit JSON:**
- Jangan buang `"` dan `{ }`
- Cuma tukar selepas `"value": `
- Warna mesti ada `#` depan
- Setiap baris (kecuali yang last) kena ada koma `,`

---

## Cara 2 — Auto dengan Tokens Studio

**Kalau dah guna Figma Variables untuk warna.**

1. Figma → **Plugins** → install **Tokens Studio for Figma**
2. Plugin → **Settings** → connect **repo GitHub sendiri**
3. **Export / Push** → plugin auto buat `colors.json`

Tak perlu taip JSON sendiri.

---

## Cara 3 — Guna template dulu

1. Copy template dari [HOW-TO-CREATE-COLORS-JSON.md](./HOW-TO-CREATE-COLORS-JSON.md)
2. Buat file kat GitHub
3. Tukar warna bila-bila masa

---

## Pilih cara mana?

| Situasi | Guna |
|---------|------|
| Pemula, sikit warna je | **Cara 1** manual |
| Dah ada Figma Variables | **Cara 2** Tokens Studio |
| Nak setup repo dulu | **Cara 3** template |

---

## Lepas siap

Update `AI-INSTRUCTIONS.md` dengan HEX yang sama supaya Figma AI ikut warna kau.

---

## Contoh pantas

Warna button Figma = `#FF5722`

```json
"primary": {
  "default": { "value": "#FF5722", "type": "color" }
}
```

Siap.
