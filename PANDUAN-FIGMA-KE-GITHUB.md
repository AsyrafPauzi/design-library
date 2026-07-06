# Cara Masukkan Component Figma ke GitHub

**Untuk pemula — tak perlu tahu coding.**

Dia dah buat component dalam Figma. Panduan ni tunjuk macam mana letak **peraturan design** dalam GitHub supaya Figma AI ikut style dia.

---

## Faham dulu

| Apa | Kat mana |
|-----|----------|
| **Component Figma sebenar** (button, card yang boleh drag) | Kekal dalam **Figma** |
| **Peraturan design** (warna, saiz, spacing) | Masuk **GitHub** sebagai text + JSON |

**Tak perlu upload file Figma ke GitHub.**  
Cuma **tulis nilai-nilai** dari Figma ke GitHub supaya AI boleh baca.

---

## Apa yang diperlukan

- [ ] Akaun Figma (dah ada)
- [ ] Repo GitHub: https://github.com/AsyrafPauzi/design-library
- [ ] 30–60 minit (setup sekali je)

**Tak perlu:** install Git, VS Code, atau tahu coding.  
Semua boleh buat dalam **website GitHub** je.

---

## Bahagian 1 — Masukkan warna (15 min)

### Dalam Figma

1. Buka file design system Figma
2. Klik component (contoh: button)
3. Tengok **Fill** color panel kanan
4. Copy **HEX code** (contoh: `#2563EB`)

Tulis warna utama:

| Nama | HEX code |
|------|----------|
| Primary (warna brand) | `#______` |
| Background | `#______` |
| Text | `#______` |
| Border | `#______` |

### Dalam GitHub

1. Pergi: https://github.com/AsyrafPauzi/design-library
2. Klik folder `tokens` → klik `colors.json`
3. Klik icon **pensel** (Edit) atas kanan
4. Tukar nilai HEX kepada warna dia
5. Scroll bawah → **Commit changes** → **Commit changes** lagi

---

## Bahagian 2 — Masukkan font (10 min)

### Dalam Figma

Pilih text heading, catat:
- Nama font (contoh: Inter, Poppins)
- Saiz (contoh: 32)
- Weight (Bold = 700)

### Dalam GitHub

1. Buka `tokens/typography.json` → **Edit**
2. Tukar ikut Figma
3. **Commit changes**
4. Buka `AI-INSTRUCTIONS.md` → tukar bahagian TYPOGRAPHY juga

---

## Bahagian 3 — Masukkan component (paling penting)

Buat untuk setiap component: **Button**, **Input**, **Card**, dll.

### Dalam Figma — klik Button, catat:

| Property | Nilai |
|----------|-------|
| Warna background | `#______` |
| Warna text | `#______` |
| Corner radius | `__` px |
| Padding | `__` px |
| Height | `__` px |
| Font size | `__` px |

### Dalam GitHub

1. Buka `components/button.md` → **Edit**
2. Tukar nilai contoh kepada nilai dari Figma
3. **Commit changes**

Ulang untuk `input.md`, `card.md`.

### Component baru (contoh: Navbar)

1. GitHub → **Add file** → **Create new file**
2. Nama: `components/navbar.md`
3. Tulis peraturan (copy format dari `button.md`)
4. **Commit changes**

---

## Bahagian 4 — Update prompt AI

1. Buka `AI-INSTRUCTIONS.md` → **Edit**
2. Tukar warna, font, component ikut apa yang dah ditulis
3. **Commit changes**

Setiap kali guna Figma AI:
1. Copy text dari `AI-INSTRUCTIONS.md`
2. Paste dalam Figma AI
3. Tambah: *"Create login screen with email and password"*

---

## Cara mudah untuk warna: Tokens Studio

Kalau guna **Figma Variables**:

1. Figma → **Plugins** → cari **Tokens Studio for Figma**
2. Connect ke GitHub repo `AsyrafPauzi/design-library`
3. Export tokens → auto masuk folder `tokens/`

Component `.md` masih kena tulis manual (atau minta kawan technical tolong).

---

## Checklist

- [ ] `tokens/colors.json` — warna brand
- [ ] `tokens/typography.json` — font
- [ ] `components/button.md` — sama macam Figma
- [ ] `components/input.md` — sama macam Figma
- [ ] `AI-INSTRUCTIONS.md` — dah update
- [ ] Dah test paste dalam Figma AI

---

## Soalan lazim

**Kena upload file .fig ke GitHub?**  
Tak. File Figma kekal dalam Figma.

**Figma AI auto baca GitHub?**  
Tak selalu. Kena **copy-paste** dari `AI-INSTRUCTIONS.md` setiap kali.

**Tak faham JSON?**  
Cuma tukar bahagian dalam `"value": "#XXXXXX"`. Atau minta kawan technical tolong sekali.

---

## Ringkasan

```
FIGMA (dah ada component)
    ↓  catat warna, saiz, padding
GITHUB (isi manual atau Tokens Studio)
    ↓  copy AI-INSTRUCTIONS.md
FIGMA AI (generate screen ikut design system)
```

**Repo:** https://github.com/AsyrafPauzi/design-library  
**Panduan English:** [HOW-TO-ADD-FIGMA-TO-GITHUB.md](./HOW-TO-ADD-FIGMA-TO-GITHUB.md)
