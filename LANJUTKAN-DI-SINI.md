# LANJUTKAN DI SINI — Handover Session Kiro Web (Mei 2026)

> **File ini = entry point untuk melanjutkan di percakapan baru.**
> Paste link file ini ke Kiro/ChatGPT baru + sebut "lanjut dari sini".

---

## STATUS TERAKHIR

**Tanggal:** 28 Mei 2026 (Sesi 2 — Pra-Day-1 spec sprint COMPLETE)
**Branch aktif:** `add-thread-arsi-7-hari`
**HEAD:** `f2bc902` (Wave 3.1 cleanup — drop meta verification checklist)
**Total commits sesi 28 Mei:** 10 commits (Wave 1.2 → 1.1 → 2.1 → 2.2 → handover refresh → fix Decision H1 → Wave 3.2 → Wave 4-5 → Wave 3.1 spec → Wave 3.1 cleanup)

---

## 🆕 SESI 28 MEI 2026 — HIGHLIGHTS

### 10 commits Wave 1-5 (Pra-Day-1 spec 100% locked)

| Commit | Wave | File | Path commit |
|---|---|---|---|
| `faa4683` | Wave 1.2 — Bio 4 platform | `BIO-COPY-4-PLATFORM.md` | Kiro |
| `95f58ac` | Wave 1.1 — Wordmark spec brief | `WORDMARK-SPEC-BRIEF.md` | Kiro |
| `9078943` | Wave 2.1 — Lynk.id setup brief | `LYNK-ID-SETUP-BRIEF.md` | ChatGPT |
| `896da8d` | Wave 2.2 — MailerLite automation brief | `MAILERLITE-AUTOMATION-BRIEF.md` | ChatGPT |
| `6525eb3` | — | `LANJUTKAN-DI-SINI.md` (handover refresh post-Wave 2.2) | ChatGPT |
| `3df9ec6` | — | `MAILERLITE-AUTOMATION-BRIEF.md` (fix Decision H1 cosmetic) | ChatGPT |
| `e6b0661` | Wave 3.2 — Threads pinned 8-post | `THREADS-PINNED-8-POST.md` | ChatGPT |
| `82e0c34` | Wave 4-5 — Bundle (Notion + Sheets + Dry-run + Day-1 ritual) | `WAVE-4-5-BUNDLE-BRIEF.md` | ChatGPT |
| `f3dc91d` | Wave 3.1 — Manifesto Carousel IG spec final | `MANIFESTO-CAROUSEL-IG.md` (expand) | ChatGPT |
| `f2bc902` | Wave 3.1 — Cleanup meta noise | `MANIFESTO-CAROUSEL-IG.md` (fix) | Kiro |

### Pattern hybrid — Kiro brainstorm + ChatGPT commit (credit conservation)

Sesi ini membuktikan pattern hybrid:
- Brainstorm + decision lock + draft generation = **Kiro chat** (high-value, perlu reasoning depth)
- Commit + push to GitHub = **ChatGPT** (low-value, mechanical write+push)

**Track record sesi 28 Mei:** 6/6 ChatGPT clean commit + 1 ChatGPT partial (Wave 3.1 over-paste meta) + 2 ChatGPT correct halt (anti-improvisation guard bekerja) + 1 Kiro cleanup (`f2bc902`).

**Saving:** ~4-6 Kiro tool call per ChatGPT-routed file. Sesi ini hemat ~20-30 tool call total (6 file via ChatGPT).

**Anti-improvisation guard standard untuk ChatGPT prompt:**
> "JANGAN re-generate, JANGAN polish, JANGAN tambah/hapus konten. Plain text commit only. Single markdown file."

**Lesson learned baru sesi 28 Mei (persisted as global learnings):**

1. **ZONA A/B delimiter di spec brief** (learning `991a1f2f-c8fd-4cc9-b323-c925526a823d`) — Pakai `═══ ZONA A: PASTE KE FILE (verbatim) ═══` vs `═══ ZONA B: HANYA UNTUK ANDA ═══`. Tanpa delimiter, executor cenderung paste verbatim termasuk meta (mis. VERIFICATION CHECKLIST). Insiden: Wave 3.1 spec final ke-paste 16 baris meta noise → cleanup commit follow-up.

2. **Verification target dari tool call output, bukan estimasi mental** (learning `a4f858d5-9096-43a6-9128-b8df9acc009b`) — Verification numerik (line count, grep count) wajib derive dari output `wc`/`grep` aktual. Estimasi mental rentan off-by-N → menyebabkan executor halt commit padahal hasil aktual benar. Insiden: Wave 3.1 cleanup attempt #1 halt karena saya tulis "target H2 = 15" padahal aktual = 17.

### Decision locks Wave 1-5 (semua sudah committed)

**Wave 1.2 BIO** — Decision lock all-default + P1 (wordmark lowercase ≠ bio Title Case = by design)
- Threads 141 / IG 129 / TT 45 / LH 165 / LinkedIn About 1272 char (semua exact match ±0)
- Signature line: `building systems, not hype.` (ENG) + `framework bukan tutorial random.` (ID)
- Audience istilah lock: "profesional & pemilik usaha"

**Wave 1.1 WORDMARK** — Decision lock A1+B1+C1+D1+E1+F1+P1
- Scope: Primary wordmark × 3 theme (Light/Dark/Mono) — defer Secondary `PROMIND/NEUROLINK` & Tertiary `@arifb.id`
- Divider: 1px · 60% width · centered · accent color · 12-16px gap
- Tracking: ARIF BUDIMAN +200 CSS · the ai architect +50 CSS
- Mono variant: `#1A1A1A` flat · NO divider line
- Delivery: 3 SVG master + 15 PNG = 18 file (atau MVP 5 file)

**Wave 2.1 LYNK.ID** — Decision lock A1+B1+C1+D3b+E1+F1+G1+H1-with-trigger
- 3 card visible Day 1: Lead Magnet → Buku waitlist → Cohort waitlist (Card 4 Corporate hidden, aktivasi Bulan 4+)
- Tagline aggregator: `building systems, not hype.`
- Lead magnet flow: redirect ke MailerLite native landing (Lynk.id no-code, no custom HTML)
- Tipografi-driven thumbnail (no wordmark dependency)
- **Free Day 1, upgrade Pro Yearly Rp 990K saat trigger M3** (Day 60 / Mgg 6 pre-buku-launch / 3+ conversion-week — whichever first)

**Wave 2.2 MAILERLITE** — Decision lock A3+B1+C1+D1+E1+F1+G1+H1+Free
- 7 worksheet: Google Docs share-only "Make a copy" template (MVP) — upgrade A1 PDF Canva saat trigger Bulan 2-3
- 9-email automation: load verbatim dari `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md` (Day 0 ~5min · Day 1-7 +24h · Day 8 +24h)
- Manual attribution di Email 0 body 3-4 baris pre-signoff
- Personalisasi `{NAMA}` only (fallback "teman")
- A/B testing OFF Day 1 — evaluate Bulan 2 baseline dulu
- **Free MailerLite Day 1**, upgrade Premium ~Rp 150K/bulan saat trigger M-MailerLite (≥800 subscriber / A/B need / Mgg 10 cohort pre-launch)

**Wave 3.2 THREADS PINNED** — Decision lock all-default
- 8 post pinned thread: 1 hook intro + 7 prinsip manifesto + 1 closing dilebur ke prinsip 7
- Char count: ≤500 char per post (Threads native limit)
- Cross-format anchor untuk D1: 19:30 WIB Threads → 20:00 IG → 20:30 LinkedIn (stagger 30 menit per platform)
- Soft CTA Post 8: invite reply → komen-as-currency seeding pattern

**Wave 3.1 MANIFESTO CAROUSEL IG** — Decision lock A1·B1·C1·D2·E2·F1·G1·H1·I2·J1·K1
- Theme: Dark `#1A1A1A` background, text `#FAFAFA` flat (no Burnt Sand pada body/symbol — reserve untuk wordmark divider only)
- Heading: Playfair Display Bold 90-110pt · Body: Inter Regular 26-30pt
- Footer komposisi: embed `wordmark-primary-dark.svg` (~120px width, bottom-center) + text counter "X/7" Inter Regular 18pt
- Filename 7 PNG: `manifesto-slide-1.png` … `manifesto-slide-7.png`
- LinkedIn long-post (D1 stagger 20:30): inline section di MANIFESTO-CAROUSEL-IG.md, ~600 kata verbatim
- Caption A/B test: OFF Day 1, single verbatim
- Output mode: expand existing file (bukan file baru)
- **Dependency:** Wave 1.1 wordmark deploy (`wordmark-primary-dark.svg` rendered di Canva) — pending render

**Wave 4-5 BUNDLE (Notion + Sheets + Dry-run + Day-1 ritual)** — Bundled di 1 brief
- Wave 4.1 Notion: 3-database (Content / Funnel / KPI) — 90-120 min eksekusi
- Wave 4.2 Sheets: 6-tab tracking — bridge ke Notion
- Wave 5.1 Dry-run: end-to-end stranger flow test — 30 min
- Wave 5.2 Day-1 ritual: launch sequence T-30min → T-0 → T+1h checkpoint

### Wave 1-5 SPEC = 100% complete (Pra-Day-1 LOCKED)

Setelah Wave 3.1 cleanup commit `f2bc902`, **Pra-Day-1 spec fully ready**. User punya brief lengkap untuk eksekusi all 5 Wave standalone tanpa balik ke Kiro:
- `BIO-COPY-4-PLATFORM.md` (Wave 1.2)
- `WORDMARK-SPEC-BRIEF.md` (Wave 1.1)
- `LYNK-ID-SETUP-BRIEF.md` (Wave 2.1)
- `MAILERLITE-AUTOMATION-BRIEF.md` (Wave 2.2)
- `MANIFESTO-CAROUSEL-IG.md` (Wave 3.1)
- `THREADS-PINNED-8-POST.md` (Wave 3.2)
- `WAVE-4-5-BUNDLE-BRIEF.md` (Wave 4.1+4.2+5.1+5.2)

**Total estimasi eksekusi 5 Wave:** ~10 jam manual work (sequential dengan dependency Wave 1.1 → 3.1).

---

## PROGRESS PLAYBOOK — 22 CHAPTER + 7 WAVE BRIEF

### Layer A — Strategi & Dokumentasi (PRE-EXISTING)

| # | Item | Layer | File | Status |
|---|---|---|---|---|
| 1-22 | 22-chapter playbook + Master Index + Day-1 Checklist | 11-23 | (full list di section bawah) | ✓ 100% |

### Layer B — Pra-Day-1 Spec Briefs (BARU DI SESI 28 MEI)

| Wave | Chapter | File | Status |
|---|---|---|---|
| 1.1 | Wordmark spec brief | `WORDMARK-SPEC-BRIEF.md` | ✓ Spec done (deploy pending) |
| 1.2 | Bio 4 platform | `BIO-COPY-4-PLATFORM.md` | ✓ Spec done (deploy pending) |
| 2.1 | Lynk.id setup brief | `LYNK-ID-SETUP-BRIEF.md` | ✓ Spec done (deploy pending) |
| 2.2 | MailerLite automation brief | `MAILERLITE-AUTOMATION-BRIEF.md` | ✓ Spec done (deploy pending) |
| 3.1 | Manifesto Carousel IG (full spec final) | `MANIFESTO-CAROUSEL-IG.md` | ✓ Spec done (deploy pending Wave 1.1) |
| 3.2 | Threads pinned 8-post | `THREADS-PINNED-8-POST.md` | ✓ Spec done (deploy pending) |
| 4.1 | Notion 3-database | `WAVE-4-5-BUNDLE-BRIEF.md` (Wave 4.1) | ✓ Spec done (deploy pending) |
| 4.2 | Sheets 6-tab tracking | `WAVE-4-5-BUNDLE-BRIEF.md` (Wave 4.2) | ✓ Spec done (deploy pending) |
| 5.1 | Dry-run end-to-end | `WAVE-4-5-BUNDLE-BRIEF.md` (Wave 5.1) | ✓ Spec done (deploy pending Wave 1-4) |
| 5.2 | Day-1 final ritual | `WAVE-4-5-BUNDLE-BRIEF.md` (Wave 5.2) | ✓ Spec done (deploy pending all previous) |

### Wave progress matrix

| Wave | Spec status | Deploy status |
|---|---|---|
| **Wave 1 — Foundation Visual** | 100% (1.1 + 1.2 done) | 0% (manual deploy pending: render Canva + paste bio 4 platform) |
| **Wave 2 — Lead Magnet Funnel** | 100% (2.1 + 2.2 done) | 0% (Lynk.id setup + MailerLite setup pending) |
| **Wave 3 — Pinned Content** | 100% (3.1 + 3.2 done) | 0% (carousel render dep Wave 1.1 + thread compose pending) |
| **Wave 4 — Tracking** | 100% (4.1 + 4.2 done, bundled) | 0% (Notion DB + Sheets tab setup pending) |
| **Wave 5 — Dry-Run** | 100% (5.1 + 5.2 done, bundled) | 0% (end-to-end test + Day-1 ritual rehearsal pending) |

---

## ⚠️ KNOWN GAPS — DOMAIN INCONSISTENCY (Layer 23 NEXT, deferred — STILL VALID)

**Issue:** `arifb.id` = username sosmed, **bukan domain**. Tapi ~30 referensi `arifb.id/[path]` tersebar di file sebagai placeholder landing page.

**File terdampak:** `LAUNCH-PACK-BUKU.md` (`/buku`, `/refund`), `LAUNCH-PACK-COHORT.md` (`/cohort`), `CORPORATE-INBOUND-PLAYBOOK.md` (`/corporate`), `CROSS-PLATFORM-PLAYBOOK.md` (bio update), `LANDING-PAGE-7-DAY-CHALLENGE.md` (`/start`), `LANJUTKAN-DI-SINI.md` (1 ref).

**User decision (sesi 27 Mei):** Opsi 2 — defer fix sampai domain di-register.

**Deadline fix:** D-30 sebelum Buku Launch Mgg 7. Tanpa domain real, sales page Cohort/Corporate susah credible.

**Note Sesi 28 Mei:** Wave 2.1 Lynk.id pakai `lynk.id/arifb.id` (sub-domain Lynk.id native, bukan custom domain) jadi Wave 2 tidak ter-block oleh gap domain.

---

## AUDIT STATUS REAL-WORLD — Pra-Day-1 (per 28 Mei 2026)

### Confirmed pre-existing (sesi 27 Mei):

| Item | Status |
|---|---|
| Tools sign-up (MailerLite/Lynk.id/Canva Pro/Notion/Sheets) | ✓ 5/5 aktif |
| Akun sosmed `@arifb.id` 4 platform | ✓ Live |
| Foto profile B&W premium | ✓ Ready |
| Manuskrip THE AI ARCHITECT | ✓ FINAL production-ready |
| Domain landing | ⚪ Deferred (Layer 23 future) |

### Spec briefs locked sesi 28 Mei:

| Item | Status |
|---|---|
| Wave 1.2 Bio 4 platform | ✓ Spec committed (`faa4683`) |
| Wave 1.1 Wordmark 3-variant | ✓ Spec committed (`95f58ac`) |
| Wave 2.1 Lynk.id 3-card aggregator | ✓ Spec committed (`9078943`) |
| Wave 2.2 MailerLite 9-email + 3 landing | ✓ Spec committed (`896da8d`) |
| Wave 3.2 Threads pinned 8-post | ✓ Spec committed (`e6b0661`) |
| Wave 4-5 Bundle (Notion + Sheets + Dry-run + Day-1 ritual) | ✓ Spec committed (`82e0c34`) |
| Wave 3.1 Manifesto Carousel IG (spec final + cleanup) | ✓ Spec committed (`f3dc91d` + cleanup `f2bc902`) |

### PENDING manual execution oleh user:

| Asset | Status | Tool tujuan | Estimasi |
|---|---|---|---|
| Bio paste deploy 4 platform (IG/TikTok/LinkedIn) | ⚪ Pending | Native masing-masing | 10 min |
| Wordmark 3-variant render Canva (MVP 5 file) | ⚪ Pending | Canva Pro | 60-90 min |
| Lynk.id Free aggregator setup (3 card + branding) | ⚪ Pending | Lynk.id Free | 60 min |
| MailerLite Free setup (3 landing + 9-email + 7 worksheet) | ⚪ Pending | MailerLite Free + Google Docs | 180 min |
| Threads pinned 8-post compose + schedule + pin | ⚪ Pending | Threads native | 20 min |
| IG Manifesto Carousel render (7 slide PNG) — dep Wave 1.1 | ⚪ Pending | Canva Pro | 90-120 min |
| Notion 3-database setup | ⚪ Pending | Notion | 90-120 min |
| Sheets 6-tab tracking setup | ⚪ Pending | Google Sheets | 60 min |
| Dry-run end-to-end stranger flow test | ⚪ Pending | Manual walkthrough | 30 min |
| Day-1 ritual rehearsal | ⚪ Pending | Manual checklist | 30 min |
| **Total sequential execution Wave 1-5 deploy** | — | — | **~10 jam** |

---

## PROGRESS PERSENTASE TERBARU (per 28 Mei 2026 — Pra-Day-1 spec 100%)

### Framing A — Menuju target 12 bulan (Rp 1M + 30K followers)

| Komponen | Bobot | Selesai | Kontribusi |
|---|---|---|---|
| Strategi + 22-chapter dokumentasi | 25% | 100% | 25% |
| Pre-launch setup (5/6 tool + 7/7 brief Wave 1-5 + foto + buku) | 10% | ~50% (foundational + Wave 1-5 spec 100%, deploy 0%) | 5% |
| Eksekusi Bulan 1-3 | 35% | 0% | 0% |
| Eksekusi Bulan 4-6 | 20% | 0% | 0% |
| Eksekusi Bulan 7-12 | 10% | 0% | 0% |
| **TOTAL** | 100% | — | **~30%** |

### Framing B — Menuju Day 1 readiness

| Komponen | Bobot | Status | Kontribusi |
|---|---|---|---|
| Dokumentasi 22 chapter + Day-1 checklist | 50% | ✓ 100% | 50% |
| Asset spec'd + deployed (Wave 1-5) | 20% | 🟡 ~60% (Wave 1-5 spec 100%, deploy 0%) | 12% |
| Tooling (5 tool aktif + domain) | 15% | ✓ 5/6 = 83% | 12.5% |
| Profile 4 platform live (handle saja) | 10% | ✓ 100% | 10% |
| End-to-end test funnel (Wave 5) | 5% | ⚪ 0% (spec done, deploy pending) | 0% |
| **TOTAL** | 100% | — | **~85%** |

### Framing C — Pra-Day-1 deployment progress (intra-Wave)

| Wave | Spec progress | Deploy progress |
|---|---|---|
| Wave 1 (Foundation Visual) | 100% | 0% |
| Wave 2 (Lead Magnet Funnel) | 100% | 0% |
| Wave 3 (Pinned Content) | 100% | 0% |
| Wave 4 (Tracking) | 100% | 0% |
| Wave 5 (Dry-Run) | 100% | 0% |
| **TOTAL deployment** | **100% spec / 0% deploy** | — |

**Honest read:** Anda di **~30% menuju target 12 bulan** atau **~85% siap launch Day 1**. Bottleneck saat ini = **deploy 7 brief Wave 1-5 ke real platform** (~10 jam manual sequential, bukan parallel karena Wave 3.1 dep Wave 1.1 dan Wave 5 dep Wave 1-4). Pra-Day-1 spec phase = **CLOSED** ✅.

---

## KEPUTUSAN KUNCI YANG SUDAH FIX (UPDATED — 28 MEI)

| Keputusan | Pilihan |
|---|---|
| Target revenue 12 bulan | Rp 1 miliar |
| Mode launch | Staged (buku Mgg 7, cohort Mgg 11, corporate Bulan 4+) |
| Payment | Lynk.id + WA |
| Email tool | MailerLite (Free Day 1 → Premium saat trigger) |
| Visual theme | Light + Dark per use case |
| Accent color | Deep Navy `#1E3A5F` (light) + Burnt Sand `#D4A574` (dark) |
| Font | Playfair Display (heading) + Inter (body) |
| Wordmark primary | "ARIF BUDIMAN / the ai architect" lowercase |
| Bio signature line | `building systems, not hype.` (ENG) + `framework bukan tutorial random.` (ID) |
| Audience istilah | "profesional & pemilik usaha" |
| Brand consistency P1 | Wordmark lowercase ≠ Bio Title Case = feature, not bug |
| **Lynk.id tier** | **Free Day 1 · upgrade Pro Yearly Rp 990K saat trigger M3** |
| **MailerLite tier** | **Free Day 1 · upgrade Premium ~Rp 150K/bulan saat trigger M-MailerLite** |
| **Worksheet delivery** | **A3 Google Docs share-only Day 1 · upgrade A1 PDF Canva Bulan 2-3** |
| **Manual attribution (M1)** | **Inject Email 0 body 3-4 baris pre-signoff** |
| **Lynk.id Card 4 Corporate** | **Hidden Day 1 · aktivasi Bulan 4+** |
| **Lynk.id card order** | **Funnel logic: Lead Magnet → Buku → Cohort (TOFU → MOFU → BOFU)** |
| **A/B testing email** | **OFF Day 1 · evaluate Bulan 2 baseline dulu** |
| **Personalisasi email** | **`{NAMA}` only · fallback "teman"** |
| **Commit pattern hybrid** | **Brainstorm Kiro + commit ChatGPT (credit conservation)** |
| **Spec brief delimiter** | **ZONA A (paste ke file) vs ZONA B (hanya untuk pembaca prompt)** |
| **Verification target numerik** | **Wajib derive dari tool call output aktual, bukan estimasi mental** |
| **Wave 3.1 IG carousel theme** | **Dark `#1A1A1A` · Playfair Display + Inter · footer wordmark embed + counter X/7** |
| **Wave 3.1 carousel filename** | **`manifesto-slide-1.png` … `manifesto-slide-7.png`** |
| **Wave 3.2 Threads pinned format** | **8 post (1 hook + 7 prinsip + 1 closing dilebur ke prinsip 7), ≤500 char per post** |
| **Cross-format D1 stagger** | **19:30 WIB Threads → 20:00 IG carousel → 20:30 LinkedIn long-post** |
| **LinkedIn long-post lokasi** | **Inline section di MANIFESTO-CAROUSEL-IG.md (~600 kata verbatim)** |
| **Wave 4 tracking stack** | **Notion 3-database (Content/Funnel/KPI) + Sheets 6-tab bridge** |
| **Wave 5 dry-run scope** | **Stranger flow end-to-end test (single user persona, 30 min)** |
| Buku 3-tier | Rp 297K / Rp 547K / Rp 897K |
| Buku launch | Mgg 7 Rab D47, 19:00 WIB |
| Refund buku | 30-hari, no-question |
| Cohort 2-tier | ARSITEK Rp 4,9JT · ARSITEK PLUS Rp 7,5JT |
| Cohort format | 8 minggu, 16 sesi, cap 20 peserta |
| Cohort 1 schedule | Mgg 16-23 (Bulan 4-5) |
| Cohort waitlist | D64 → launch D71 → close D77 23:59 |
| Cohort refund | 7-hari post-sesi-1, no-question |
| Anti-FOMO buku | TETAP 90 hari · Cohort ANTI-DISCOUNT selamanya |
| Domain landing | `arifb.id/buku` · `arifb.id/cohort` (deferred) |
| Corporate audit 3-scope | Small Rp 25JT / Medium Rp 50JT / Large Rp 100JT |
| Corporate payment | 50/50 SACRED |
| Corporate cap simultaneous | Max 3 engagement |
| Corporate activation | Bulan 1-3 inactive · Bulan 4 SOFT · Bulan 5-6 FULL · Bulan 7+ STEADY |

---

## FLOW KERJA UPDATED (Sesi 28 Mei — pasca learning Wave 3.1)

```
1. Brainstorm + decision lock di Kiro chat (high-value reasoning)
2. Saya generate brief verbatim di chat output dengan delimiter eksplisit:
   ═══ ZONA A: PASTE KE FILE (verbatim) ═══     ← content yang masuk file
   ═══ ZONA B: HANYA UNTUK ANDA ═══             ← meta/instruksi/checklist
3. Verification target numerik (line count/grep count) WAJIB saya derive
   dari tool call output aktual, bukan estimasi mental
4. Pilih commit path:
   a. Kiro commit (proven, untuk file yang butuh char-level lock atau
      cleanup minor tanpa creative reasoning)
   b. ChatGPT commit (credit-saving, untuk spec brief descriptive)
5. Kalau ChatGPT — paste content + commit prompt (sertakan
   anti-improvisation guard + ZONA A/B delimiter)
6. Verify SHA + URL di GitHub
7. Lanjut wave berikutnya
```

**Anti-improvisation guard pattern:**
> "JANGAN re-generate, JANGAN polish, JANGAN tambah/hapus konten. Plain text commit only. Single markdown file. Patuhi delimiter ZONA A/B — jangan paste content ZONA B ke file."

**Track record halt-yang-correct:** Saat ChatGPT halt karena verification mismatch atau internal safety check, itu = guard bekerja sempurna. Bukan kegagalan ChatGPT. Switch ke Kiro cleanup kalau terus halt (diminishing returns).

---

## KONTEKS PENTING UNTUK PERCAKAPAN BARU

### Tentang Pak Arif / @arifb.id
- Founder PROMIND-NEUROLINK
- Penulis buku THE AI ARCHITECT (manuskrip final, siap launch Mgg 7)
- Target: kategori "AI Architect" Indonesia = Arif Budiman
- Voice: formal "Anda", anti-hype, tenang, premium decision-maker
- ICP: profesional & pemilik usaha (founder, C-level, manajer senior, decision-maker)
- Produk: Buku 3-tier + Cohort A.R.S.I. 2-tier + Corporate audit Rp 25-100JT (Bulan 4+)
- Lynk.id: `https://lynk.id/arifb.id` (handle reserved, KYC ✓)

### Tentang Repository
- **Repo:** `arifbudiman575-ship-it/buku`
- **Branch aktif:** `add-thread-arsi-7-hari` (HEAD `f2bc902`)
- **File baru/expand di sesi 28 Mei:**
  - `BIO-COPY-4-PLATFORM.md` (Wave 1.2 — file baru)
  - `WORDMARK-SPEC-BRIEF.md` (Wave 1.1 — file baru)
  - `LYNK-ID-SETUP-BRIEF.md` (Wave 2.1 — file baru)
  - `MAILERLITE-AUTOMATION-BRIEF.md` (Wave 2.2 — file baru)
  - `THREADS-PINNED-8-POST.md` (Wave 3.2 — file baru)
  - `WAVE-4-5-BUNDLE-BRIEF.md` (Wave 4.1+4.2+5.1+5.2 — file baru, bundled)
  - `MANIFESTO-CAROUSEL-IG.md` (Wave 3.1 — file pre-existing, EXPANDED dengan spec final + LinkedIn long-post inline)
- **File anchor playbook 22 chapter:** (lihat list lengkap di section bawah)

### Hierarki 5 Sumber (anchor di STRATEGI §0.1)
1. 🔒 Buku THE AI ARCHITECT (Arif) — Core IP sacred
2. Rama / @productivityboi — Methodology pondasi (V/K/P + TOFU/MOFU/BOFU + Value Ladder)
3. Theoderic — Purpose × strength × authenticity, dynamic persona
4. Pak Subyakto Priyojudanto (Pak Bi) — 50-tahun filosofi (network effect, storyting paradoks, brand intersubjektif)
5. Caleb Ralston — Brand journey 4Q + association map

### Filter 4-Lapis (anchor di STRATEGI §0.5) — Quality gate setiap konten
1. **Buku** — trace ke konsep di THE AI ARCHITECT (NEURO-ARC / A.R.S.I.)
2. **Asosiasi** — perkuat asosiasi "AI Architect = building systems, not hype"
3. **Voice** — formal "Anda", anti-hype, no emoji berlebihan, no CAPS clickbait
4. **Purpose** — reader habis baca → action ke salah satu funnel stage

4/4 lolos = publish. Salah satu fail = revisi atau buang.

### Tentang Playbook Structure (22 Chapter + 4 Pra-Day-1 Brief)
```
PART 0 — START HERE (3 ch): Master Index, Lanjutkan Di Sini, Ringkasan Sesi
PART 1 — STRATEGI (4 ch): Master 18 Section, BJM, Kompetitor, Filter 4-Lapis
PART 2 — KONTEN HARIAN (7 ch): Voice, Hook Bank, Visual ID, Manifesto, Cross-Platform, Calendar 12 Bulan, Long-thread Library, Pillar 3
PART 3 — LAUNCH (4 ch): Lead Magnet, Buku Launch, Cohort Launch, Corporate Inbound
PART 4 — OPERASIONAL (5 ch): Ops Setup, Tracking, Reply Farm, Anti-Burnout, Strategy Refresh
PART 5 — DAY-1 SEQUENCING (1 ch): Day-1 Launch Checklist (Layer 23, 5-wave critical path)
PART 6 — PRA-DAY-1 EXECUTION BRIEFS (7 ch baru/expanded sesi 28 Mei, Wave 1-5 spec 100%):
  - Wave 1.1 Wordmark Spec Brief
  - Wave 1.2 Bio Copy 4 Platform
  - Wave 2.1 Lynk.id Setup Brief
  - Wave 2.2 MailerLite Automation Brief
  - Wave 3.1 Manifesto Carousel IG (expanded existing file)
  - Wave 3.2 Threads Pinned 8-post
  - Wave 4-5 Bundle (Notion + Sheets + Dry-run + Day-1 ritual)
```

### File anchor playbook (UPDATED)

**Strategi:**
- `STRATEGI-PERSONAL-BRANDING.md` — 18 section master strategi
- `BRAND-JOURNEY-MAP.md` — roadmap 4 quarter (Caleb framework)
- `analisa_kompetitor.md` — 31 kompetitor T1/T2/T3

**Konten harian:**
- `CONTENT-CALENDAR-BULAN-{1,2,3}.md` — 86 post + long-thread
- `THREADS-LONGFORM-ABC-TEST.md` — 8 long-thread Bulan 1-2
- `MANIFESTO-CAROUSEL-IG.md` — carousel Day 1
- `PILLAR-3-STUDI-CASE-PAK-BI.md` — 8 post filosofi Pak Bi
- `CROSS-PLATFORM-PLAYBOOK.md` — per-platform tactics 4 platform
- `VISUAL-BRAND-IDENTITY.md` — visual standard

**Launch:**
- `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md` — 9 email lead magnet
- `LANDING-PAGE-7-DAY-CHALLENGE.md` — landing page copy
- `LAUNCH-PACK-BUKU.md` — Master ops buku launch (~2.160 lines)
- `LAUNCH-PACK-COHORT.md` — Master ops cohort launch (~2.260 lines)
- `CORPORATE-INBOUND-PLAYBOOK.md` — Master ops corporate audit Bulan 4+ (~1.330 lines)

**Operasional:**
- `OPERATIONAL-SETUP.md` — tooling stack
- `TRACKING-DASHBOARD.md` — KPI tracking
- `REPLY-FARM-PLAYBOOK.md` — komen-as-currency
- `ANTI-BURNOUT-PROTOCOL.md` — sustainability layer (831 lines)
- `STRATEGY-REFRESH-PROTOCOL.md` — quarterly recalibration (937 lines)

**Day-1 sequencing:**
- `DAY-1-LAUNCH-CHECKLIST.md` — 5-wave critical path Pra-Day-1

**Pra-Day-1 execution briefs (NEW sesi 28 Mei — 7 brief, Pra-Day-1 spec 100%):**
- `BIO-COPY-4-PLATFORM.md` — Wave 1.2 verbatim copy 4 platform
- `WORDMARK-SPEC-BRIEF.md` — Wave 1.1 Canva execution guide 3-variant
- `LYNK-ID-SETUP-BRIEF.md` — Wave 2.1 aggregator setup + 3 card spec
- `MAILERLITE-AUTOMATION-BRIEF.md` — Wave 2.2 3-landing + 9-email + 7 worksheet spec
- `MANIFESTO-CAROUSEL-IG.md` — Wave 3.1 IG carousel 7-slide spec final + LinkedIn long-post inline (expanded)
- `THREADS-PINNED-8-POST.md` — Wave 3.2 Threads pinned manifesto 8-post
- `WAVE-4-5-BUNDLE-BRIEF.md` — Wave 4.1+4.2+5.1+5.2 (Notion + Sheets + Dry-run + Day-1 ritual)

**Master index:**
- `PLAYBOOK-MASTER.md` — single navigation entry untuk seluruh 22 chapter + Day-1 + Wave briefs

---

## CARA LANJUT DI PERCAKAPAN BARU

**Mulai sesi baru? Buka dulu file ini, lalu pilih path:**

### Path A — Deploy mode (eksekusi manual ~10 jam)

```
Lanjut dari handover 28 Mei. State branch add-thread-arsi-7-hari HEAD f2bc902.
Pra-Day-1 spec 100% locked (7 brief Wave 1-5). Saya sedang deploy Wave [X.X].
Ada blocker di [step]. Bantu debug.

Reference brief:
- Wave 1.1 → WORDMARK-SPEC-BRIEF.md
- Wave 1.2 → BIO-COPY-4-PLATFORM.md
- Wave 2.1 → LYNK-ID-SETUP-BRIEF.md
- Wave 2.2 → MAILERLITE-AUTOMATION-BRIEF.md
- Wave 3.1 → MANIFESTO-CAROUSEL-IG.md (dep Wave 1.1)
- Wave 3.2 → THREADS-PINNED-8-POST.md
- Wave 4-5 → WAVE-4-5-BUNDLE-BRIEF.md

Recommended deploy order: 1.1 → 1.2 → 2.1 → 2.2 → 3.2 → 3.1 → 4-5.
```

### Path B — Audit deploy progress (kalau sebagian deploy sudah selesai)

```
Lanjut dari handover 28 Mei. Sudah deploy:
- [ ] Wave 1.1 Wordmark Canva render (MVP 5 file): [done/partial/no]
- [ ] Wave 1.2 Bio paste 4 platform: [done/partial/no]
- [ ] Wave 2.1 Lynk.id setup Free: [done/partial/no]
- [ ] Wave 2.2 MailerLite setup + 3 landing + 9-email + 7 worksheet: [done/partial/no]
- [ ] Wave 3.1 IG Carousel render 7 slide PNG: [done/partial/no]
- [ ] Wave 3.2 Threads pinned 8-post compose + schedule + pin: [done/partial/no]
- [ ] Wave 4.1 Notion 3-database: [done/partial/no]
- [ ] Wave 4.2 Sheets 6-tab: [done/partial/no]
- [ ] Wave 5.1 Dry-run end-to-end: [done/partial/no]
- [ ] Wave 5.2 Day-1 ritual rehearsal: [done/partial/no]

Audit state real, update progress %, identify next deploy blocker.
```

### Path C — End-to-end dry run (kalau Wave 1-4 deploy 100%)

```
Lanjut dari handover 28 Mei. Wave 1-4 deploy 100%. Saatnya Wave 5.1 Dry-Run
sesuai WAVE-4-5-BUNDLE-BRIEF.md Section 5.1.

Test stranger flow end-to-end: visit Threads bio → klik link arifb.id →
Lynk.id aggregator → klik Card 1 (Lead Magnet) → MailerLite landing →
submit form → Email 0 received → worksheet Hari 1 accessible →
reply attribution test → verify tag di MailerLite + Notion + Sheets.

Cross-format test D1: Threads pinned thread accessible · IG carousel
swipe-able 7 slide · LinkedIn long-post readable mobile/desktop.

Kalau ada gap di chain → fix → re-test → tandai pass di Wave 5.2 ritual.
```

---

## ⚠️ Catatan strategis

1. **Domain gap masih valid** — `arifb.id/[path]` placeholder di 6 file. Action D-30 sebelum buku launch Mgg 7. Wave 2 Lynk.id pakai sub-domain Lynk.id native (`lynk.id/arifb.id`) jadi tidak ter-block.

2. **Wave 1.1 wordmark = dependency Wave 3.1 untuk EKSEKUSI** — Spec Wave 3.1 sudah final di MANIFESTO-CAROUSEL-IG.md (commit `f3dc91d` + cleanup `f2bc902`), tapi render carousel di Canva butuh `wordmark-primary-dark.svg` ready. Recommended deploy order: Wave 1.1 dulu, baru Wave 3.1.

3. **Credit conservation pattern** — terbukti hemat ~20-30 tool call sesi ini (6 file via ChatGPT). Pertahankan untuk content brief; Kiro tetap untuk char-level lock + cleanup minor.

4. **~10 jam sequential execution Wave 1-5** — bisa Anda kerjakan tanpa Kiro. Pra-Day-1 spec 100% locked, brainstorm phase = CLOSED. Setelah deploy partial/full, pakai Path B (audit) untuk update state sebelum Day 1.

5. **Filter 4-Lapis re-read SACRED** — sebelum Day 1, ritual final di Wave 5.2 (per WAVE-4-5-BUNDLE-BRIEF.md).

6. **ChatGPT halt = correct behavior** — kalau ChatGPT halt karena verification mismatch atau internal safety, jangan retry blindly. Switch ke Kiro cleanup kalau task minor + deterministic (precedent: cleanup commit `f2bc902` via Kiro setelah 2× ChatGPT halt).

---

*Last updated: Sesi 28 Mei 2026 — 10 commits Wave 1-5 spec final, Pra-Day-1 spec phase CLOSED 100%. HEAD `f2bc902`. Tinggal eksekusi manual ~10 jam (Wave 1.1 → 1.2 → 2.1 → 2.2 → 3.2 → 3.1 → 4-5).*
