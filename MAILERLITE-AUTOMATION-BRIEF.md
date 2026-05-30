# MAILERLITE AUTOMATION BRIEF — Wave 2.2 Lead Magnet Funnel Engine

> Status: FINAL · Wave 2.2 Lead Magnet Funnel · Hasil sesi brainstorm Kiro (BRAIN) → eksekusi user manual (HANDS, MailerLite dashboard).
> Anchor: EMAIL-SEQUENCE-7-DAY-CHALLENGE.md (9-email verbatim) + LANDING-PAGE-7-DAY-CHALLENGE.md (lead magnet landing copy) + DAY-1-LAUNCH-CHECKLIST.md Wave 2.2 + OPERATIONAL-SETUP.md §2.1 + LYNK-ID-SETUP-BRIEF.md §4 (integration spec).
> Decision lock: A3 + B1 + C1 + D1 + E1 + F1 + G1 + H1 + Free MailerLite tier.
> Pair dengan Wave 2.1: 3 MailerLite landing URL akan jadi destination redirect dari Lynk.id Card 1-2-3.

---

## DECISION LOCK SUMMARY

| Letter | Decision | Locked value |
|---|---|---|
| A | Worksheet delivery format | **A3 — 7 Google Docs share-only "Make a copy" template** (MVP). Upgrade A1 PDF Canva saat trigger Bulan 2 (≥30 subscriber + ≥30% reply Email 1 dengan filled worksheet) atau Bulan 3 (≥100 subscriber). |
| B | Buku waitlist landing copy | Heading + sub + form + CTA + microcopy minimal (verbatim Section 3.2) |
| C | Cohort waitlist landing copy | Heading + sub + form + CTA + microcopy + subtle scarcity "kursi terbatas" (verbatim Section 3.3) |
| D | Manual attribution (M1) | Inject ke Email 0 body 3-4 baris pre-signoff (verbatim Section 6) |
| E | Email branding | Light theme (#FAFAFA bg, #1A1A1A text, #1E3A5F link/CTA) · Inter font · text logo `@arifb.id` Day 1 → swap wordmark Light SVG saat Wave 1.1 deploy · footer simple |
| F | Personalisasi | `{NAMA}` only (fallback "teman" kalau optional name kosong) |
| G | A/B testing | OFF Day 1 — single-variant launch · evaluate Bulan 2 baseline open rate dulu |
| H | Test plan | 6-test automated trigger plan (~30min) — Section 9 |
| Tier | Free MailerLite Day 1, upgrade Premium ~Rp 150K/bulan saat trigger M-MailerLite (Section 11) |

---

## 1. ANCHOR REFERENCE — Source of Truth

| Wave 2.2 element | Pull verbatim dari |
|---|---|
| 9 email body (Email 0-8) | `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md` Section [E0-E8] |
| Lead magnet landing copy 8-section | `LANDING-PAGE-7-DAY-CHALLENGE.md` |
| Subject + preheader 9 email | `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md` final final lock |
| Visual brand spec | `VISUAL-BRAND-IDENTITY.md` §10 + adapt ke MailerLite limitation |

**JANGAN re-write konten dari scratch.** Setiap teks email/landing yang diload ke MailerLite = paste verbatim dari anchor. Kalau ada gap formatting (mis. anchor pakai markdown italic, MailerLite butuh HTML), convert format saja, jangan ubah kata.

---

## 2. MAILERLITE ACCOUNT SETUP — Free Tier (Step 0, ~20min)

### Sign-up & verification (kalau belum)
1. Sign up `mailerlite.com` pakai email pro `arif@arifb.id` atau email primary
2. Verify email + complete profile
3. Verify domain (kalau punya custom domain) — defer Day 1 (domain belum register), pakai default sender
4. Sender setting: "Arif Budiman" + reply-to email primary

### Brand kit setup
1. Settings → Brand Kit
2. Logo: text-only `@arifb.id` (Inter Bold, fallback) — Day 1 placeholder. Swap ke wordmark Light SVG saat Wave 1.1 deploy selesai.
3. Brand colors:
   - Primary: `#1E3A5F` (Deep Navy — link, CTA button)
   - Background: `#FAFAFA` (Off-White)
   - Text: `#1A1A1A` (Black Premium)
   - Muted: `#6B6B6B` (footer text)
4. Brand font: Inter (default web-safe sans) — Playfair likely tidak supported di email rendering

### Email defaults
1. Settings → Email defaults
2. From name: `Arif Budiman`
3. From email: pro email (verified)
4. Reply-to: same
5. Address di footer: business address atau "Arif Budiman, [Kota]" (compliance CAN-SPAM)
6. Unsubscribe link: required, leave default text

---

## 3. LANDING PAGES SPEC (3 landings)

> Verify saat eksekusi: Free tier MailerLite landing page count limit. Kalau ≤1 landing di Free, consolidate Buku + Cohort waitlist jadi 1 page dengan multi-tag form (radio button "saya tertarik dengan: [ ] Buku [ ] Cohort"). Lead magnet TETAP dedicated landing.

### 3.1 Landing #1 — Lead Magnet `7-Day AI Architect Challenge` (FULL)

**Copy source:** `LANDING-PAGE-7-DAY-CHALLENGE.md` 8-section verbatim. Port semua section:
- Section 1: Hero (headline + sub + form CTA)
- Section 2: Apa yang Anda dapat (7 day breakdown)
- Section 3: Untuk siapa challenge ini
- Section 4: Cara kerja
- Section 5: 7 FAQ
- Section 6: Testimonial section (defer Bulan 2 — Day 1 gunakan placeholder atau hide section)
- Section 7: Final CTA
- Section 8: Footer

**Form schema:**
- Field 1: `NAMA` (Optional, type: text, label "Nama (opsional)")
- Field 2: `EMAIL` (Wajib, type: email, label "Email", validation built-in)
- Submit button: `Mulai 7 Hari` (per LANDING anchor Section 1)
- Submit redirect: thank-you page native MailerLite atau custom page sederhana ("Cek inbox Anda dalam 5 menit")

**Tag applied on submit:** `lead_magnet_active`

**URL slug:** `/7-day-challenge` atau MailerLite default URL (akan jadi destination Lynk.id Card 1)

**Visual:**
- Bg: `#FAFAFA`
- Headline (Hero): largest size MailerLite allows, color `#1A1A1A`, Inter Bold (target visual Playfair, fallback Inter Bold karena email-platform limitation)
- Body: Inter Regular `#1A1A1A`
- CTA button: solid fill `#1E3A5F`, text `#FAFAFA`, no shadow, radius 4-6px max
- Footer: `@arifb.id · The AI Architect · [Unsubscribe]` di Inter Regular muted

---

### 3.2 Landing #2 — Buku Waitlist (SHORT — Decision B1)

**Copy verbatim:**

```
Heading: THE AI ARCHITECT
Sub: Coming Mgg 7 — peta dasar untuk yang membangun, bukan menggunakan.
Form field: EMAIL (wajib only, no nama)
CTA button: Email saya saat buku rilis
Microcopy below form: Tidak ada spam. 1 email saat buku siap.
```

**Tag applied:** `buku_waitlist`

**URL slug:** `/buku-waitlist`

**Visual:** Same as Landing #1 (Light theme + Inter + branded footer).

---

### 3.3 Landing #3 — Cohort Waitlist (SHORT — Decision C1)

**Copy verbatim:**

```
Heading: Cohort A.R.S.I.
Sub: Coming Mgg 11 — implementasi A.R.S.I. di pekerjaan Anda. Cohort intim, kursi terbatas.
Form field: EMAIL (wajib only)
CTA button: Email saya saat cohort buka
Microcopy below form: Tidak ada spam. 1 email saat cohort buka.
```

**Tag applied:** `cohort_waitlist`

**URL slug:** `/cohort-waitlist`

**Visual:** Same as #1 + #2.

---

## 4. FORM SCHEMA & TAG MAPPING

| Form (di Landing) | Required field | Optional field | Tag on submit | Triggers automation |
|---|---|---|---|---|
| Lead Magnet | EMAIL | NAMA | `lead_magnet_active` | YES — Email 0 → 9-email sequence |
| Buku Waitlist | EMAIL | — | `buku_waitlist` | YES — Email konfirmasi simple (1 email) |
| Cohort Waitlist | EMAIL | — | `cohort_waitlist` | YES — Email konfirmasi simple (1 email) |

**Cross-tag handling:** subscriber bisa hold multiple tags (mis. `lead_magnet_active` + `buku_waitlist`). Tidak conflict.

**Double opt-in:** SKIP Day 1 untuk speed. Indo audience tolerance reasonable. Re-evaluate Bulan 2 kalau spam complaint rate >0.1%.

---

## 5. AUTOMATION SETUP — 9-Email Sequence (per Anchor EMAIL-SEQUENCE)

### Trigger
- **Trigger condition:** subscriber receives tag `lead_magnet_active`
- **Trigger source:** Landing #1 form submission

### Email schedule

| Email | Delay from previous step | Content source |
|---|---|---|
| Email 0 (Welcome + worksheet Hari 1 link) | ~5 menit setelah subscribe | `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md` E0 |
| Email 1 (Hari 1 follow-up + worksheet Hari 2 link) | +24 jam | E1 |
| Email 2 (Hari 2 follow-up + worksheet Hari 3) | +24 jam | E2 |
| Email 3 (Hari 3 follow-up + worksheet Hari 4) | +24 jam | E3 |
| Email 4 (Hari 4 follow-up + worksheet Hari 5) | +24 jam | E4 |
| Email 5 (Hari 5 follow-up + worksheet Hari 6) | +24 jam | E5 |
| Email 6 (Hari 6 follow-up + worksheet Hari 7) | +24 jam | E6 |
| Email 7 (Hari 7 follow-up + complete) | +24 jam | E7 |
| Email 8 (D+8 wrap-up + soft buku tease) | +24 jam | E8 |

### Per email setup (di MailerLite editor)
1. Subject + preheader: copy verbatim dari EMAIL-SEQUENCE
2. Body: paste verbatim, format markdown → MailerLite block editor
3. Personalisasi: replace `{NAMA}` placeholder dengan MailerLite variable `{$name|teman}` (fallback "teman" kalau name kosong)
4. Worksheet link (Email 0-6): insert Google Docs share-only URL (per Section 7)
5. Sign-off: `Arif` (italic kalau MailerLite support, fallback regular)
6. Footer: branded `@arifb.id · The AI Architect · [Unsubscribe link mandatory]`

### Buku & Cohort waitlist automation (simple)

**Buku waitlist trigger:** subscriber receives `buku_waitlist` → 1 email konfirmasi:

```
Subject: Anda di waitlist THE AI ARCHITECT
Body: Halo {$name|teman}, terima kasih sudah masuk waitlist buku THE AI ARCHITECT. 
Saya akan kirim 1 email saat buku siap (target Mgg 7). Tidak ada email lain di antara itu.

— Arif
```

**Cohort waitlist trigger:** subscriber receives `cohort_waitlist` → 1 email konfirmasi:

```
Subject: Anda di waitlist Cohort A.R.S.I.
Body: Halo {$name|teman}, terima kasih sudah masuk waitlist Cohort A.R.S.I. 
Saya akan kirim 1 email saat cohort buka (target Mgg 11). Kursi terbatas, akan saya umumkan first-come-first-serve di waitlist.

— Arif
```

---

## 6. MANUAL ATTRIBUTION INJECTION (Decision D1)

Tambahkan **3-4 baris** ke Email 0 body, posisi: SEBELUM sign-off "Arif".

**Verbatim text yang di-inject:**

```
Sekedar ingin tahu — Anda menemukan saya dari mana?
(reply singkat: Threads / Instagram / TikTok / LinkedIn / referal teman / lainnya)

Tidak ada konsekuensi jawabannya — saya hanya ingin tahu konten di platform mana yang berguna untuk Anda.
```

**Setelah subscriber reply via email:**
- Tag manual di MailerLite per reply: `source_threads`, `source_ig`, `source_tiktok`, `source_linkedin`, `source_referral`, `source_other`
- Setiap Senin pagi (5 min): audit tag distribution → top performing platform → inform content priority untuk minggu berjalan

---

## 7. GOOGLE DOCS WORKSHEET SETUP (Decision A3, ~35min)

### Setup Google Drive folder
1. Buat folder Google Drive: `arifb-id / 7-day-challenge / worksheets`
2. Sharing setting folder: `Anyone with the link can view`
3. **JANGAN** pakai folder yang berisi data pribadi/sensitif lain

### Buat 7 worksheet template

Setiap worksheet = Google Docs baru dengan nama:
- `7day-h1-worksheet-template`
- `7day-h2-worksheet-template`
- ... sampai `7day-h7-worksheet-template`

### Template structure per worksheet (standardize)

```
[Header]
7-DAY AI ARCHITECT CHALLENGE
HARI [N] — [Judul Hari, pull dari EMAIL-SEQUENCE]

[Instruksi singkat — pull verbatim dari EMAIL-SEQUENCE Email Hari N]

[Worksheet body — 3-5 prompt question + space jawaban]
1. [Question 1]
   _____________________________________________
   _____________________________________________

2. [Question 2]
   _____________________________________________

3. [Question 3]
   _____________________________________________

[Footer]
@arifb.id · The AI Architect · framework bukan tutorial random.
```

**Sharing setting per template:** `Anyone with the link can view` (NOT edit — supaya original template tetap clean, reader pakai "File → Make a copy" untuk versi mereka)

### URL collection
Compile 7 share-only URL ke document `worksheet-urls.md` (private, untuk paste ke MailerLite saat setup automation Email 0-6).

**Naming convention:**
```
Email 0 includes link Hari 1: https://docs.google.com/document/d/[ID-H1]/view
Email 1 includes link Hari 2: ...
...
Email 6 includes link Hari 7: ...
Email 7 (Hari 7 follow-up) tidak include worksheet baru
Email 8 (D+8 wrap-up) tidak include worksheet
```

### Upgrade A1 PDF trigger (defer)

Saat trigger Bulan 2 fired (≥30 subscriber + ≥30% reply Email 1 with filled worksheet) atau Bulan 3 (≥100 subscriber):
- [ ] Render 7 PDF worksheet di Canva pakai brand kit Wave 1.1 wordmark + Light theme
- [ ] Upload ke Google Drive folder yang sama (atau folder baru `worksheets-pdf`)
- [ ] Update Email 0-6 di MailerLite: ganti link Google Docs ke link PDF Drive
- [ ] Test 1-2 email re-trigger untuk verify link replacement

---

## 8. EMAIL BRANDING SETUP DI MAILERLITE (Decision E1)

### Master template (1× setup, semua email pakai)

1. MailerLite → Templates → Create custom template
2. Name: "Arif Budiman — Master Email Template"
3. Layout:
   - Header: logo (text `@arifb.id` Inter Bold Day 1, swap wordmark Light SVG saat Wave 1.1 deploy)
   - Body: padding 24px, max-width 600px, bg `#FAFAFA`
   - Body text: Inter Regular 16px, color `#1A1A1A`, line-height 1.65
   - Headings dalam body: Inter Bold 24px (h2), 20px (h3)
   - Links: `#1E3A5F` no underline (or subtle underline on hover)
   - CTA buttons (kalau ada): solid fill `#1E3A5F`, text `#FAFAFA`, padding 12px 24px, radius 4px
   - Footer: 13px Inter Regular `#6B6B6B`, contains: `@arifb.id · The AI Architect · framework bukan tutorial random.` + unsubscribe link mandatory

4. Save sebagai default template untuk semua automation

---

## 9. TEST PLAN (Decision H1, ~30min)

### Test #1 — Lead Magnet end-to-end via Lynk.id (~10min)
1. Buka `lynk.id/arifb.id` di mobile incognito (post Wave 2.1 deploy)
2. Tap Card 1 → redirect ke MailerLite Landing #1
3. Submit form: nama "Test User", email pribadi #1 (yang TIDAK pernah subscribe)
4. Verify: thank-you page render correctly
5. Verify: Email 0 received in inbox <5 menit
6. Verify: `{NAMA}` populated as "Test User" di body
7. Verify: worksheet Hari 1 link clickable + accessible (Google Docs view-only)
8. Verify: Email 0 has manual attribution question (3-4 lines pre-signoff)
9. Verify: tag `lead_magnet_active` ada di MailerLite subscriber list

### Test #2 — Email 1 trigger Day 1 (~5min, manual fast-forward)
1. MailerLite automation editor → fast-forward subscriber test ke Email 1 step
2. Verify: Email 1 received dengan worksheet Hari 2 link
3. Verify: branding consistent (logo, color, footer)

### Test #3 — Buku waitlist via Lynk.id (~5min)
1. Buka `lynk.id/arifb.id` Card 2
2. Submit form dengan email pribadi #2
3. Verify: Email konfirmasi buku waitlist received <5 menit
4. Verify: tag `buku_waitlist` ada di MailerLite

### Test #4 — Cohort waitlist via Lynk.id (~5min)
1. Buka `lynk.id/arifb.id` Card 3
2. Submit form dengan email pribadi #3
3. Verify: Email konfirmasi cohort waitlist received
4. Verify: tag `cohort_waitlist` ada

### Test #5 — Cross-tag check (~3min)
1. MailerLite subscriber list → 3 email berbeda dengan 3 tag berbeda
2. No duplicate, no missing trigger
3. No subscriber stuck di "no tag" state

### Test #6 — Unsubscribe flow (~2min)
1. Klik unsubscribe link di Email 0 dari email pribadi #1
2. Verify: redirected ke unsubscribe confirmation page
3. Verify: subscriber #1 status berubah ke `unsubscribed` di MailerLite
4. Re-subscribe email pribadi #1 untuk testing iterasi berikutnya kalau perlu

### Pass criteria
- 6/6 test pass = Wave 2.2 status DEPLOYED ✓
- Fail handling: debug per landing/email, fix, re-test

---

## 10. ACCEPTANCE CRITERIA — Wave 2.2 SELESAI

Wave 2.2 status: **DEPLOYED ✓** ketika SEMUA point check:

- [ ] MailerLite Free account aktif + brand kit setup (logo + color + font)
- [ ] 3 landing page live: lead magnet (URL X) + buku waitlist (URL Y) + cohort waitlist (URL Z)
- [ ] Form schema correct: lead magnet (Name optional + Email), buku/cohort (Email only)
- [ ] Tag mapping correct: `lead_magnet_active`, `buku_waitlist`, `cohort_waitlist`
- [ ] 9-email automation loaded verbatim dari EMAIL-SEQUENCE-7-DAY-CHALLENGE.md
- [ ] Trigger schedule correct: Day 0 ~5min, Day 1-7 +24h, Day 8 +24h
- [ ] Personalisasi `{NAMA}` works dengan fallback "teman"
- [ ] Email 0 body has manual attribution question (3-4 lines pre-signoff)
- [ ] 7 Google Docs worksheet created + share-only URLs collected + linked di Email 0-6
- [ ] Buku waitlist + cohort waitlist konfirmasi email setup (1 email each)
- [ ] Test plan Section 9 — 6/6 test pass
- [ ] 3 MailerLite landing URL passed back ke Lynk.id Card 1-2-3 (replace placeholder)
- [ ] Lynk.id end-to-end flow re-tested post-MailerLite-integration

---

## 11. UPGRADE TRIGGER M-MailerLite (Free → Premium)

### Trigger criteria (whichever first)

| Trigger | Action |
|---|---|
| ≥800 subscriber (sebelum hit 1000 hard limit Free) | Upgrade Premium ~Rp 150K/bulan |
| Need A/B testing (Bulan 2-3 Decision G2/G3 evaluasi) | Upgrade |
| Need advanced segmentation (mis. tag combination logic untuk corporate inbound Bulan 4+) | Upgrade |
| Mgg 10 (D-7 cohort launch) | Wajib upgrade — cohort launch butuh full automation infra |
| Spam complaint rate >0.1% | Upgrade dengan double opt-in setup |

### Upgrade checklist (saat trigger fired)
- [ ] Upgrade ke Premium tier via MailerLite dashboard
- [ ] Setup A/B testing kalau Decision G2/G3 active
- [ ] Setup advanced segmentation rules (sesuai use case)
- [ ] Setup custom domain email (kalau domain sudah register)
- [ ] Re-test 9-email automation regression check
- [ ] Re-test 3 landing page regression check

---

## 12. WAVE 2.2 → DEPENDENCY UNLOCK

| Dependency | Unlocked oleh Wave 2.2 |
|---|---|
| Wave 2.1 Lynk.id Card 1-2-3 placeholder URL | Replace dengan 3 real MailerLite landing URL |
| Bio 4 platform link `arifb.id` → real funnel | Aggregator + form chain fully functional |
| Wave 3.1 Manifesto Carousel CTA | "Lihat link di bio" leads to funcional funnel (lead magnet capture) |
| Wave 3.2 Threads pinned CTA | sda |
| Email 0 manual attribution data | Bulan 1-2 source attribution data flow active |
| Pre-Mgg 7 buku launch | Buku waitlist email list ready untuk announcement |
| Pre-Mgg 11 cohort launch | Cohort waitlist email list ready untuk first-come-first-serve |
| Wave 4.1 Notion 3-database | Subscriber data export → Notion CRM |
| Wave 5.1 Dry-run end-to-end | Full funnel testable: bio → Lynk.id → MailerLite → Email 0 → worksheet |

---

## CHANGELOG

- **Sesi brainstorm:** Kiro Vibe (BRAIN), 28 Mei 2026
- **Decision lock:** A3 + B1 + C1 + D1 + E1 + F1 + G1 + H1 + Free MailerLite
- **Anchor:** EMAIL-SEQUENCE-7-DAY-CHALLENGE.md · LANDING-PAGE-7-DAY-CHALLENGE.md · DAY-1-LAUNCH-CHECKLIST.md Wave 2.2 · OPERATIONAL-SETUP.md §2.1 · LYNK-ID-SETUP-BRIEF.md §4
- **Eksekusi:** User manual di MailerLite dashboard Free tier, estimasi 3 jam total (setup 20min + 3 landing 30min + form/tag 15min + load 9 email 30min + automation trigger 20min + 7 Google Docs worksheet 35min + test 30min)
- **Output:** MailerLite Free aktif · 3 landing live · 9-email automation loaded · 7 worksheet share-only · attribution data flow active
- **Tier strategy:** Free Day 1 · upgrade Premium ~Rp 150K/bulan saat trigger M-MailerLite
- **Dependency unlock:** Wave 2.1 placeholder URL replaced, bio funnel fully functional, Wave 3+ CTA real, Bulan 1-2 attribution data, pre-launch buku & cohort waitlist
- **Next wave:** 3.1 Manifesto Carousel IG (render Canva 7-slide + caption + post + pin) — first content asset deploy after funnel infrastructure
