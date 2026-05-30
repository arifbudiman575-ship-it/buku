# WORDMARK SPEC BRIEF — The AI Architect

> Status: FINAL · Wave 1.1 Foundation Visual · Hasil sesi brainstorm Kiro (BRAIN) → eksekusi user manual (HANDS, Canva Pro).
> Anchor: VISUAL-BRAND-IDENTITY.md §5 (Logo/Wordmark) + §10 (Decisions Final).
> Decision lock: A1 + B1 + C1 + D1 + E1 + F1 + P1.

---

## DECISION LOCK SUMMARY

| Letter | Decision | Locked value |
|---|---|---|
| A | Variant scope | Primary wordmark × 3 theme (Light/Dark/Mono) — defer Secondary `PROMIND/NEUROLINK` & Tertiary `@arifb.id` |
| B | Divider line | 1px thick · 60% width "ARIF BUDIMAN" · centered horizontal · accent color · 12-16px gap atas-bawah |
| C | Tracking | ARIF BUDIMAN +200 CSS (≈0.2em, Canva slider ~20) · the ai architect +50 CSS (≈0.05em, Canva slider ~5) |
| D | Mono variant | `#1A1A1A` text flat on transparent · NO divider line (sengaja) |
| E | Delivery set | 1 master SVG/theme + 5 PNG export size = 3 SVG + 15 PNG = 18 file (or lazy-export PNG on-demand) |
| F | Filename convention | `wordmark-{tier}-{theme}-{size}.{ext}` kebab-case, lowercase |
| P | Brand consistency | Wordmark lowercase (visual brand) vs Bio Title Case (textual brand) — feature, not bug |

---

## 1. WORDMARK ANATOMY

```
        ARIF  BUDIMAN              ← Playfair Bold, ALL CAPS, +200 tracking
        ─────────────              ← 1px line, accent color, 60% width line atas
         the ai architect          ← Playfair Bold, lowercase, +50 tracking
```

**Proportions (size-relative, scale-invariant):**

| Element | Spec | Reference |
|---|---|---|
| Line 1 height (ARIF BUDIMAN) | 100% | reference |
| Gap atas divider | 12-16% of line 1 height | breathing room |
| Divider thickness | 1px constant (regardless of scale) | tipis premium |
| Divider width | 60% of line 1 rendered width | not full underline |
| Gap bawah divider | 12-16% of line 1 height | symmetric |
| Line 2 height (the ai architect) | ~30% of line 1 | hierarchy ratio 3.33:1 |
| Line 2 width visual | match divider width (~60% line 1) | balance |

---

## 2. COLOR SPEC PER VARIANT

### Light variant
**Use case:** landing page · email · sales page · slide deck · document PDF · light bg surfaces

| Element | Hex |
|---|---|
| Bg target | `#FAFAFA` atau transparent on light surface |
| Text (line 1 + 2) | `#1A1A1A` |
| Divider | `#1E3A5F` (Deep Navy) |

### Dark variant
**Use case:** IG Carousel · IG Reels · TikTok video · profile picture default · dark bg surfaces

| Element | Hex |
|---|---|
| Bg target | `#1A1A1A` atau transparent on dark surface |
| Text (line 1 + 2) | `#FAFAFA` |
| Divider | `#D4A574` (Burnt Sand) |

### Mono variant
**Use case:** print · watermark PDF · foto BG complex · B&W document · stamp

| Element | Hex |
|---|---|
| Bg target | transparent (assume light/varied bg di placement) |
| Text (line 1 + 2) | `#1A1A1A` |
| Divider | **DIHILANGKAN** (no divider, only text) |

> Reasoning Mono no-divider: di context complex bg (foto, photo overlay, low-contrast print), divider 1px sering hilang atau jadi clutter. Single-color flat = paling versatile fallback.

---

## 3. CANVA EXECUTION GUIDE

### Step 0 — Setup Brand Kit (1× hanya)

1. Canva Pro → Brand Hub → Brand Kit baru "The AI Architect"
2. Add brand colors:
   - `#FAFAFA` (Off-White Foundation)
   - `#1A1A1A` (Black Premium)
   - `#1E3A5F` (Deep Navy Accent — Light theme)
   - `#D4A574` (Burnt Sand Accent — Dark theme)
   - `#6B6B6B` (Muted Gray)
3. Add brand fonts:
   - Heading: Playfair Display (Bold 700)
   - Body: Inter (Regular 400, Medium 500, Bold 700)
4. Save Brand Kit → tandai sebagai default untuk semua design

### Step 1 — Master Wordmark LIGHT (SVG)

1. New design → Custom size **800×400 px** → transparent BG
2. Insert Text → ketik `ARIF BUDIMAN`
   - Font: **Playfair Display**
   - Style: **Bold (700)**
   - Size: **56pt**
   - Color: `#1A1A1A`
   - Letter spacing slider: **20** (≈ +200 CSS / 0.2em)
   - Align: center horizontal di canvas
3. Insert Text → ketik `the ai architect`
   - Font: **Playfair Display Bold 700**
   - Size: **17pt** (≈30% of 56pt)
   - Color: `#1A1A1A`
   - Letter spacing slider: **5** (≈ +50 CSS / 0.05em)
   - Align: center horizontal
4. Insert Line:
   - Tools → Lines → Straight horizontal
   - Thickness: **1pt** (smallest available — kalau Canva minimum 2pt, pakai 2pt)
   - Length: drag sampai ~**60% width** rendered "ARIF BUDIMAN" (visually estimate ≈ 280-320px untuk font size 56pt)
   - Color: `#1E3A5F` (Deep Navy)
   - Position: vertically center antara text 1 dan text 2; gap **12-16px** atas dan bawah
5. Visual check:
   - Text 1 di atas, divider di tengah, text 2 di bawah
   - Semua centered horizontal
   - Total wordmark height ≈ 56 + 14 + 1 + 14 + 17 = ~102pt ≈ 136px
   - Padding canvas atas-bawah ≈ (400 - 136) / 2 ≈ 132px each (banyak whitespace, sengaja)
6. Select all 3 elements → Group → rename "Wordmark Primary Light"
7. Download:
   - File type: **SVG** (Canva Pro feature, vector transparent)
   - Filename: `wordmark-primary-light.svg`

### Step 2 — Master Wordmark DARK (SVG)

1. Duplicate canvas Light
2. Background visual reference: ubah ke `#1A1A1A` (untuk visual check ONLY, jangan masuk export)
3. Ubah text color (line 1 + 2): `#FAFAFA`
4. Ubah divider color: `#D4A574` (Burnt Sand)
5. Group → rename "Wordmark Primary Dark"
6. Hide background reference layer (jangan delete, kunci/hide saja)
7. Download SVG → `wordmark-primary-dark.svg`

### Step 3 — Master Wordmark MONO (SVG)

1. Duplicate canvas Light
2. Text color tetap: `#1A1A1A`
3. **Hapus divider line** (Mono = no divider, lihat Section 2)
4. Group 2 elements (text 1 + text 2) → rename "Wordmark Primary Mono"
5. Download SVG → `wordmark-primary-mono.svg`

### Step 4 — PNG exports (5 size × 3 theme = 15 file)

Untuk efisiensi, buat 5 canvas template baru, masukkan master SVG, export ke PNG. Atau lazy-export PNG saat dipakai (rekomendasi untuk hemat Canva quota).

| # | Use case | Canvas size | Theme default | Filename |
|---|---|---|---|---|
| 1 | Profile picture (avatar 4 platform) | **1080×1080 sq** | Dark (premium social) | `wordmark-primary-dark-1080sq.png` |
| 2 | LinkedIn cover | **1584×396** | Light | `wordmark-primary-light-1584x396.png` |
| 3 | X / Threads / IG header | **1500×500** | Light | `wordmark-primary-light-1500x500.png` |
| 4 | OG / Open Graph (link preview) | **1200×630** | Light | `wordmark-primary-light-1200x630.png` |
| 5 | Email signature | **600×200** | Light | `wordmark-primary-light-600x200.png` |

Per canvas:
- Center wordmark vertikal + horizontal
- Padding sekitar wordmark min **60-80px**
- Untuk Profile picture (1080sq) Dark: fill bg dengan `#1A1A1A` solid (bukan transparent — harus jadi square crop)
- Untuk lainnya: bg transparent (atau `#FAFAFA` untuk Light email signature kalau platform tidak support transparent)

Export setting:
- Format: **PNG**
- Resolution: **2x retina** (Canva Pro option)
- Background: per spec di atas

Repeat for Dark theme + Mono theme = total 15 PNG.

---

## 4. ASSET MATRIX

```
File Type       | Light    | Dark     | Mono
================|==========|==========|==========
Master SVG      | ✓        | ✓        | ✓        (3 files)
1080×1080 sq    | ✓        | ✓ DEFAULT| ✓        (3 files)
1584×396        | ✓ DEFAULT| ✓        | ✓        (3 files)
1500×500        | ✓ DEFAULT| ✓        | ✓        (3 files)
1200×630        | ✓ DEFAULT| ✓        | ✓        (3 files)
600×200         | ✓ DEFAULT| ✓        | ✓        (3 files)
================|==========|==========|==========
TOTAL                                            18 files
```

**Minimum Viable (MVP set untuk Day 1 critical path):**
- 3 SVG masters (Light + Dark + Mono)
- 1 PNG profile picture 1080sq Dark
- 1 PNG email signature 600×200 Light

Total MVP = **5 file**. Sisanya 13 file boleh deferred — render saat dipakai (lazy-export).

---

## 5. ANTI-PATTERN CHECK

Sebelum wordmark dianggap final, verify:

- [ ] Tidak ada gradient di wordmark
- [ ] Tidak ada drop shadow / outer glow
- [ ] Tidak ada > 1 accent color per variant
- [ ] Divider tidak terlalu tebal (>1.5px = redesign)
- [ ] Tracking ARIF BUDIMAN tidak < +100 CSS (terlalu rapat) atau > +400 CSS (terlalu lebar)
- [ ] Line 2 "the ai architect" tidak italic (italic only untuk kutipan per VBI §3)
- [ ] Mono variant tidak punya divider (sengaja)
- [ ] Export SVG bukan hanya PNG (vector master wajib untuk scaling future)
- [ ] Filename pakai kebab-case (lowercase, dash separator)
- [ ] Tidak ada elemen lain di canvas (logo brand AI lain, emoji, ornament)

Salah satu fail → revisi sebelum upload final.

---

## 6. APPLICATION MAPPING (link ke VBI §8)

| Deliverable | Variant | File suggested |
|---|---|---|
| Profile picture (4 platform avatar) | Dark 1080sq | `wordmark-primary-dark-1080sq.png` |
| LinkedIn cover photo | Light 1584×396 | `wordmark-primary-light-1584x396.png` |
| X / Threads / IG header | Light 1500×500 | `wordmark-primary-light-1500x500.png` |
| IG Carousel footer (per slide) | Dark master SVG (scale down inline) | `wordmark-primary-dark.svg` |
| TikTok video end-frame | Dark master SVG | `wordmark-primary-dark.svg` |
| Email signature | Light 600×200 | `wordmark-primary-light-600x200.png` |
| Landing page hero header | Light master SVG | `wordmark-primary-light.svg` |
| Sales page header (buku/cohort) | Light master SVG | `wordmark-primary-light.svg` |
| Slide deck title | Light master SVG | `wordmark-primary-light.svg` |
| Workbook PDF watermark | Mono master SVG | `wordmark-primary-mono.svg` |
| Document PDF stamp | Mono master SVG | `wordmark-primary-mono.svg` |
| OG / link preview | Light 1200×630 | `wordmark-primary-light-1200x630.png` |

---

## 7. CHECKLIST EKSEKUSI

Estimasi total: **60-90 menit** (per DAY-1-LAUNCH-CHECKLIST Wave 1.1: 1-2 jam)

- [ ] Setup Canva Brand Kit (5 colors + 2 fonts) — 10 min
- [ ] Render Master Wordmark Light SVG — 15 min
- [ ] Render Master Wordmark Dark SVG (duplicate + recolor) — 5 min
- [ ] Render Master Wordmark Mono SVG (duplicate + remove divider) — 5 min
- [ ] Anti-pattern check (Section 5) — 5 min
- [ ] Render PNG profile picture 1080sq Dark — 5 min
- [ ] Render PNG email signature 600×200 Light — 5 min
- [ ] (Opsional) Render 13 PNG sisanya — 30 min
- [ ] Upload ke folder `/assets/wordmark/` (cloud Anda atau Canva Brand Kit) — 5 min
- [ ] Test placement: profile pic 1080sq sebagai avatar dummy 4 platform, readable di all sizes — 5 min

**Wave 1.1 status: DEPLOYED ✓** ketika MVP set (5 file) selesai. Sisanya boleh defer.

---

## 8. WAVE 1.1 → DEPENDENCY UNLOCK

Setelah wordmark rendered, dependencies unlock:

| Wave | Asset butuh | File dipakai |
|---|---|---|
| Wave 2.1 (Lynk.id setup) | Avatar aggregator | `wordmark-primary-dark-1080sq.png` |
| Wave 3.1 (Manifesto Carousel IG) | Footer per slide | `wordmark-primary-dark.svg` (embed) |
| Wave 3.2 (Threads pinned 8-post) | Header (kalau platform support) | `wordmark-primary-light-1500x500.png` |
| Email signature setup (MailerLite/personal) | Signature image | `wordmark-primary-light-600x200.png` |
| Landing page lead magnet | Hero header | `wordmark-primary-light.svg` |

---

## CHANGELOG

- **Sesi brainstorm:** Kiro Vibe (BRAIN), 28 Mei 2026
- **Decision lock:** A1 + B1 + C1 + D1 + E1 + F1 + P1
- **Anchor:** VISUAL-BRAND-IDENTITY.md §5 + §10 · DAY-1-LAUNCH-CHECKLIST.md Wave 1.1
- **Eksekusi:** User manual di Canva Pro, estimasi 60-90 menit
- **Output:** 3 SVG master + 15 PNG = 18 file total (MVP 5 file)
- **Dependency unlock:** Wave 2.1 Lynk.id avatar, Wave 3.1 carousel footer, Wave 3.2 Threads header, email signature
- **Next wave:** 2.1 Lynk.id setup atau 2.2 MailerLite automation (sesi Kiro berikutnya)
