# Bina Repo Design Library Sendiri di GitHub

**Mula kat sini.** Bina repo **sendiri** — jangan guna repo orang lain.

**Perlu:** Akaun GitHub (percuma) + 20 minit. Tak perlu coding.

---

## Langkah 1 — Daftar GitHub (kalau belum ada)

1. Pergi https://github.com
2. Klik **Sign up**
3. Ikut langkah (plan percuma dah cukup)

---

## Langkah 2 — Buat repository baru

1. Log in GitHub
2. Klik icon **+** (atas kanan) → **New repository**
3. Isi:

| Field | Apa nak taip |
|-------|----------------|
| Repository name | `design-library` |
| Description | `Design system saya untuk Figma AI` |
| Public / Private | **Public** atau Private |
| Add README | ✅ **Tick kotak ni** |

4. Klik **Create repository**

Dah ada repo sendiri, contoh:  
`https://github.com/NAMA-USERNAME-KAU/design-library`

Ganti **NAMA-USERNAME-KAU** dengan username GitHub kau.

---

## Langkah 3 — Buat folder & file

### File `tokens/colors.json`

1. Klik **Add file** → **Create new file**
2. Taip nama: `tokens/colors.json`
3. Paste (nanti tukar warna ikut Figma kau):

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

4. Klik **Commit changes**

### File `tokens/typography.json` & `tokens/spacing.json`

Buat sama macam atas — tengok contoh dalam [CREATE-YOUR-OWN-REPO.md](./CREATE-YOUR-OWN-REPO.md) (English).

---

## Langkah 4 — Buat file component

### `components/button.md`

1. **Add file** → nama: `components/button.md`
2. Paste:

```markdown
# Button

## Primary
- Background: #2563EB
- Text: putih
- Padding: 12px 24px
- Border radius: 8px
- Min height: 44px
```

3. **Commit changes**

Ulang untuk `input.md` dan `card.md`.

---

## Langkah 5 — Buat `AI-INSTRUCTIONS.md`

1. **Add file** → nama: `AI-INSTRUCTIONS.md`
2. Tulis semua warna, font, component dalam satu prompt
3. **Commit changes**

Setiap kali guna Figma AI → copy file ni → paste → tambah request screen.

---

## Struktur repo kau

```
design-library/          ← REPO SENDIRI
├── tokens/
├── components/
├── AI-INSTRUCTIONS.md
└── README.md
```

---

## Lepas tu

1. Isi nilai sebenar dari Figma → [PANDUAN-FIGMA-KE-GITHUB.md](./PANDUAN-FIGMA-KE-GITHUB.md)
2. Guna dengan Figma AI → copy `AI-INSTRUCTIONS.md`

---

## Checklist

- [ ] Akaun GitHub dah ada
- [ ] Repo `design-library` bawah akaun **saya**
- [ ] Folder `tokens/` & `components/` dah buat
- [ ] `AI-INSTRUCTIONS.md` dah buat
- [ ] Nilai dah update ikut Figma saya

**URL repo kau:** `https://github.com/NAMA-USERNAME-KAU/design-library`
