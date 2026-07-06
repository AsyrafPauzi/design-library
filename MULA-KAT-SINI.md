# Mula Kat Sini — Checklist Langkah Demi Langkah

Guna repo ni sebagai **template**. Semua dah siap — kau cuma **tukar** nilai contoh dengan design Figma kau.

**Repo:** https://github.com/AsyrafPauzi/design-library

**Masa:** lebih kurang 1 jam (setup sekali je)

---

## Sebelum mula

- [ ] Ada akaun **Figma** dengan component dah buat
- [ ] Ada akaun **GitHub** (daftar percuma kat https://github.com)
- [ ] Boleh buka repo ni dalam browser

---

## Bahagian A — Dapatkan salinan repo

Template dah ada dalam repo ni. Kau perlukan salinan sendiri untuk edit.

### Cara 1 — Fork (disyorkan)

- [ ] Buka https://github.com/AsyrafPauzi/design-library
- [ ] Klik **Fork** (atas kanan)
- [ ] Klik **Create fork**
- [ ] Sekarang kau ada: `https://github.com/NAMA-USERNAME-KAU/design-library`

### Cara 2 — Dijemput sebagai collaborator

- [ ] Buka https://github.com/AsyrafPauzi/design-library
- [ ] Boleh edit terus dalam repo ni

---

## Bahagian B — Kumpul nilai dari Figma (15 min)

Buka file Figma kau. Tulis nilai ni:

### Warna

- [ ] Warna button utama → HEX: `#______`
- [ ] Warna background → HEX: `#______`
- [ ] Warna teks → HEX: `#______`
- [ ] Warna border → HEX: `#______`
- [ ] Warna error → HEX: `#______`

**Cara:** Klik element → panel kanan **Fill** → copy kod HEX

### Font

- [ ] Nama font: `____________`
- [ ] Saiz heading: `__` px
- [ ] Saiz body: `__` px

### Spacing

- [ ] Gap kecil: `__` px (biasanya 8)
- [ ] Gap sederhana: `__` px (biasanya 16)
- [ ] Gap besar: `__` px (biasanya 24)

### Button

- [ ] Background: `#______`
- [ ] Text: `#______`
- [ ] Corner radius: `__` px
- [ ] Height: `__` px

### Input

- [ ] Border: `#______`
- [ ] Height: `__` px

### Card

- [ ] Background: `#______`
- [ ] Padding: `__` px

---

## Bahagian C — Update file template kat GitHub (30 min)

Pergi **repo kau** kat GitHub. Setiap file: buka → klik **pensel (Edit)** → tukar nilai → **Commit changes**.

### Tokens

- [ ] Edit `tokens/colors.json` — tukar HEX dengan warna kau

- [ ] Edit `tokens/typography.json` — tukar font dan saiz

- [ ] Edit `tokens/spacing.json` — tukar spacing kalau berbeza

### Components

- [ ] Edit `components/button.md` — ikut button Figma kau

- [ ] Edit `components/input.md` — ikut input Figma kau

- [ ] Edit `components/card.md` — ikut card Figma kau

### Prompt AI

- [ ] Edit `AI-INSTRUCTIONS.md` — update semua warna, font, component ikut nilai kau

---

## Bahagian D — Test dengan Figma AI (5 min)

- [ ] Buka `AI-INSTRUCTIONS.md` kat GitHub
- [ ] Copy semua dalam code block (antara ```)
- [ ] Buka Figma → **Figma AI / Make**
- [ ] Paste prompt
- [ ] Tambah request, contoh:

```
Create a login screen with email, password, and login button.
```

- [ ] Tengok hasil — warna dan component patut ikut design system kau
- [ ] Kalau salah, balik Bahagian C dan betulkan file

---

## Bahagian E — Setiap kali buat screen baru

- [ ] Buka `AI-INSTRUCTIONS.md`
- [ ] Copy prompt
- [ ] Paste dalam Figma AI
- [ ] Tulis screen apa kau nak (login, profile, checkout, dll.)
- [ ] Review & tweak ~10–20% kalau perlu

---

## Checklist akhir — dah siap?

- [ ] Dah fork repo (atau ada akses edit)
- [ ] `tokens/colors.json` — warna **saya**
- [ ] `tokens/typography.json` — font **saya**
- [ ] `components/button.md` — sama macam Figma **saya**
- [ ] `components/input.md` — sama macam Figma **saya**
- [ ] `AI-INSTRUCTIONS.md` — dah update
- [ ] Dah test dalam Figma AI — hasil okay

---

## Rujukan pantas

| Apa | File |
|-----|------|
| Warna | `tokens/colors.json` |
| Font | `tokens/typography.json` |
| Spacing | `tokens/spacing.json` |
| Button | `components/button.md` |
| Input | `components/input.md` |
| Copy untuk Figma AI | `AI-INSTRUCTIONS.md` |

**Repo:** https://github.com/AsyrafPauzi/design-library

---

## Ringkasan

```
1. Fork repo
2. Copy nilai dari Figma
3. Edit file template kat GitHub (tukar nilai contoh)
4. Update AI-INSTRUCTIONS.md
5. Copy prompt → Figma AI → describe screen
```
