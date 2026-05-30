# PRE-DEPLOY RISK REGISTER — Wave 1-5 Manual Execution

> **Untuk:** @arifb.id — Arif Budiman, The AI Architect
> **Tipe:** Risk register pre-flight untuk eksekusi manual ~10 jam Pra-Day-1
> **Anchor:** `DAY-1-LAUNCH-CHECKLIST.md` + `LANJUTKAN-DI-SINI.md` + 7 Wave brief
> **Use:** Read H-1 hari sebelum deploy. Re-check Critical risks H-0 morning. Update saat eksekusi mid-deploy kalau ada blocker baru ditemukan.

---

## TOP 5 CRITICAL RISKS

| # | Wave | Risk | Severity | Likelihood | Pre-mitigation |
|---|---|---|---|---|---|
| 1 | Wave 2.2 | 7 worksheet Google Docs content BELUM EKSIS di repo (brief hanya kasih format, bukan content) | 💥 Critical | 🔴 High | Pre-draft worksheet H-3 hari (atau pakai placeholder template-only Day 1, content fill Bulan 1 Mgg 1) |
| 2 | Wave 2.2 | MailerLite sender domain auth (DKIM/SPF) bisa makan jam-an saat first-time signup | 🔴 High | 🔴 High | Mulai signup MailerLite + verifikasi domain H-2 hari, jangan H-0 |
| 3 | Wave 3.1 | Dep Wave 1.1 wordmark deploy — kalau Wave 1.1 fail, Wave 3.1 fully blocked | 💥 Critical | 🟡 Medium | Sequential order strict: Wave 1.1 dulu, baru Wave 3.1. Pakai PNG fallback `wordmark-primary-dark-240.png` kalau SVG re-rasterize |
| 4 | Wave 1.2 | TikTok bio link tidak clickable di akun <1000 follower (TikTok native limit) | 🔴 High | 🔴 High | Re-design TikTok bio: link pakai TEXT (bukan link field), atau defer TikTok deploy sampai cross 1K follower |
| 5 | Cross-cutting | Decision drift mid-deploy — improvise spec yang sudah locked (font, wording, layout) | 🔴 High | 🟡 Medium-High | Re-read DECISION LOCK Wave 1-5 di LANJUTKAN-DI-SINI.md sebelum start. STOP saat tergoda improvise → brainstorm ulang di Kiro, jangan auto-fix |

---

## RISK GRADING SCALE

**Severity (impact kalau risk materialize):**
- 🟢 **Low** — annoyance, tidak block deploy
- 🟡 **Medium** — slow down 30-60 min, recoverable saat eksekusi
- 🔴 **High** — block 1+ Wave atau butuh recovery 1+ jam
- 💥 **Critical** — block multi-Wave, defer launch H+1, atau requires re-spec

**Likelihood (kemungkinan terjadi):**
- 🟢 **Low** — <20% chance, edge case
- 🟡 **Medium** — 20-60% chance, plausible
- 🔴 **High** — >60% chance, expected

**Mitigation depth (per learning sesi 28 Mei, decision lock D3):**
- High/Critical risks: full mitigation (pre-check + during-deploy action + recovery)
- Medium/Low risks: 1-line mitigation

---

## PRE-FLIGHT CHECKLIST H-1 (hari sebelum deploy)

- [ ] Tools 5/5 status verify: Canva Pro / Lynk.id / MailerLite / Notion / Sheets — semua login session aktif (logout-login test untuk konfirmasi password masih valid)
- [ ] MailerLite account dibuat **H-2 hari** sebelum deploy day, sender domain auth (DKIM/SPF) selesai sebelum H-0
- [ ] **7 worksheet Google Docs CONTENT decision:** pre-draft atau pakai placeholder template-only Day 1 (Hari 1 = "Audit prompt yang sering Anda pakai" placeholder, content fill Bulan 1 Mgg 1)
- [ ] TikTok account follower count check — kalau <1000, lock TikTok bio strategy: link sebagai TEXT plain (`lynk.id/arifb.id`), bukan di link field
- [ ] Wordmark MVP 5 file render = item PERTAMA di urutan eksekusi (gating Wave 3.1)
- [ ] Block calendar: 10 jam sequential — atau split 2 hari (5+5 jam, recommended kalau pernah burnout)
- [ ] Notification silent: DND mode laptop + HP, WhatsApp mute, calls forward
- [ ] Internet primary + backup tethering HP siap (kuota cukup)
- [ ] Charger laptop + power bank HP (10 jam = battery anxiety)
- [ ] Browser incognito + secondary email/device siap untuk Wave 5.1 dry-run stranger persona
- [ ] **Re-read DECISION LOCK Wave 1-5** di `LANJUTKAN-DI-SINI.md` (anti-decision drift mid-deploy)
- [ ] **Re-read Filter 4-Lapis** di `STRATEGI-PERSONAL-BRANDING.md` §0.5 (anti-improvisation)
- [ ] Buat note "blocker log" terbuka — kalau ada blocker mid-deploy, tulis di sini bukan auto-fix yang break spec
- [ ] Sarapan/makan/kopi siap — jangan eksekusi 10 jam dengan glucose rendah
- [ ] Kabari pasangan/keluarga: "10 jam sprint, available emergency only"

---

## RISK REGISTER PER WAVE

### Wave 1.1 — Wordmark render Canva (60-90 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W1.1.1 | Canva Pro subscription expired/inactive | 💥 Critical | 🟢 Low | **Pre-check H-1:** login Canva Pro, verify subscription status. **During:** kalau lapse → Figma free atau Adobe Express free (Playfair + Inter available di keduanya). **Recovery:** export Figma SVG, manual import ke Canva nanti saat subscription renew. |
| W1.1.2 | Playfair Display + Inter tidak tersedia di Canva default font | 🟡 Medium | 🟢 Low | Quick check sebelum start: ketik "Playfair" + "Inter" di Canva text font search. Default tersedia. |
| W1.1.3 | SVG export di Canva re-rasterized → blurry pas embed di Wave 3.1 carousel | 🟡 Medium | 🟡 Medium | Test SVG di smaller size (~120px) sebelum lock Wave 1.1 done. Kalau blurry → render PNG 240px sebagai fallback (tertulis di Wave 3.1 anti-pattern check #4). |
| W1.1.4 | Decision drift saat di Canva: tergoda ganti font karena "kurang menarik" | 🔴 High | 🟡 Medium | **Pre-check:** baca decision lock Wave 1.1 (B1+C1) sebelum buka Canva — Playfair Display Bold heading, Inter Regular body, NO change. **During:** STOP kalau urge muncul → screenshot canvas, tutup Canva, buka brainstorm Kiro/sesi baru. JANGAN improvise mid-deploy karena breaking change cascading ke Wave 1.2 + 3.1 + 3.2. **Recovery:** rewind Canva history, restore lock-version. |

---

### Wave 1.2 — Bio paste 4 platform (10 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W1.2.1 | TikTok bio link tidak clickable di akun <1000 follower (TikTok platform limit) | 🔴 High | 🔴 High | **Pre-check H-1:** TikTok follower count = ? Kalau <1000 → DECIDE bio strategy: (a) link as TEXT plain `lynk.id/arifb.id` di bio body, atau (b) defer TikTok deploy Day 1, fokus 3 platform aja. **During:** paste bio TikTok pakai variant yang sudah di-decide. **Recovery:** kalau salah paste → bio TikTok bisa edit unlimited times. |
| W1.2.2 | Manual paste typo cross-platform (typo Threads/IG/TT/LinkedIn) | 🟡 Medium | 🟡 Medium | Copy paste verbatim dari `BIO-COPY-4-PLATFORM.md` (jangan retype manual). Side-by-side compare di akhir. |
| W1.2.3 | Login session 4 platform timeout/expired saat butuh paste | 🟢 Low | 🟢 Low | Login pre-check H-1, paste session window biasanya valid 7+ hari. |

---

### Wave 2.1 — Lynk.id setup (60 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W2.1.1 | Lynk.id KYC tidak verified atau handle `arifb.id` sudah ke-claim | 💥 Critical | 🟢 Low | **Pre-check H-1:** login Lynk.id, verify handle `arifb.id` reserved + KYC ✓ (per handover sesi 27 Mei sudah confirmed). **During:** kalau handle hilang → fallback handle `arifbid` atau `arifbudiman`, update bio 4 platform. **Recovery:** Lynk.id support bisa restore handle kalau ada bug. |
| W2.1.2 | Lynk.id Free tier card limit (4+ card?) atau background image upload limit | 🟢 Low | 🟢 Low | Free tier biasanya unlimited card. Upload thumbnail ≤2MB per card (Lynk.id default). |
| W2.1.3 | Card 4 Corporate hidden mode — Lynk.id tidak support draft, harus delete | 🟢 Low | 🟡 Medium | Decision: hidden = delete saja Day 1, redraft Bulan 4+ saat aktivasi (5 min cost). |

---

### Wave 2.2 — MailerLite (180 min — paling lama)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W2.2.1 | MailerLite signup + sender domain auth (DKIM/SPF) bisa makan jam-an, kadang butuh DNS update via registrar | 🔴 High | 🔴 High | **Pre-check H-2 hari:** signup MailerLite, mulai sender auth process. Sender alternative: pakai email gmail/proton sebagai sender (no domain auth needed) untuk Day 1, upgrade ke `arifb.id` sender saat domain register Mgg 7. **During:** kalau auth pending H-0 → switch ke gmail sender, lanjut. **Recovery:** sender domain auth bisa update post-launch tanpa break automation. |
| W2.2.2 | 7 worksheet Google Docs CONTENT belum eksis di repo — brief Wave 2.2 hanya kasih FORMAT (Google Docs share-only "Make a copy"), bukan isi worksheet Day 1-7 | 💥 Critical | 🔴 High | **Pre-check H-3 hari:** decide — (a) pre-draft 7 worksheet content (~60 min/worksheet × 7 = 7 jam extra work), atau (b) accept placeholder Day 1: setiap worksheet = 1 page Google Docs dengan judul "Hari N — [tema]" + intro paragraf + section "Latihan" kosong (~5 min/worksheet × 7 = 35 min). **Default decision: (b) placeholder, content fill di Bulan 1 Mgg 1 saat 100 subscriber pertama.** Email Day 0 update: "worksheet akan terus di-improve seiring feedback Anda di 7 hari pertama". **Recovery:** subscriber Hari 1-7 yang complain → personal DM, kasih next iteration worksheet. |
| W2.2.3 | MailerLite Free scheduler reliability — trigger Day 0 ~5min vs Day 1 +24h precision | 🟡 Medium | 🟢 Low | Wave 5.1 dry-run akan test latency. Acceptable Day 0 = 1-15 min (bukan exact 5 min). |
| W2.2.4 | 3 landing page (Lead Magnet + Buku waitlist + Cohort waitlist) — apakah 3 unique atau template share | 🟢 Low | 🟡 Medium | Saat eksekusi: clone landing 1 (Lead Magnet) → adjust copy + form action → save sebagai landing 2/3. Template share OK, hemat 60 min. |
| W2.2.5 | 180 min estimasi blow up jadi 240+ min karena tooling detail (pop-up, exit intent, double opt-in) | 🟡 Medium | 🟡 Medium | Block 4 jam buffer di calendar, jangan rush. Skip nice-to-have (exit intent), keep MVP (form + thank-you + email automation). |

---

### Wave 3.1 — IG Carousel render (90-120 min, dep Wave 1.1)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W3.1.1 | Wave 1.1 wordmark `wordmark-primary-dark.svg` not ready → Wave 3.1 fully blocked | 💥 Critical | 🟡 Medium | **Pre-check:** Wave 1.1 done sebelum start Wave 3.1 (sequential strict). **During:** kalau Wave 1.1 partial (mis. cuma render Light, belum Dark) → STOP Wave 3.1, kembali render Dark dulu. **Recovery:** Wave 3.1 placeholder text "[WORDMARK]" di footer slide 1-7, replace SVG saat Wave 1.1 done. JANGAN publish IG carousel dengan placeholder. |
| W3.1.2 | Wordmark SVG re-rasterized di Canva → footer carousel blurry (anti-pattern check #4 brief) | 🟡 Medium | 🟡 Medium | Pakai PNG 240px fallback (`wordmark-primary-dark-240.png` dari Wave 1.1 MVP set) kalau SVG render blur. |
| W3.1.3 | 7 slide content paste verbatim — typo manual saat copy dari MANIFESTO-CAROUSEL-IG.md | 🟡 Medium | 🟡 Medium | Copy-paste verbatim per slide, side-by-side review post-render. JANGAN retype dari memory. |
| W3.1.4 | Footer counter "X/7" alignment drift per slide (slide 4 maybe geser 5px) | 🟢 Low | 🟡 Medium | Duplicate page 1 → update counter only (1/7 → 2/7 → ... → 7/7). Position lock via Canva grid snap. |

---

### Wave 3.2 — Threads pinned 8-post (20 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W3.2.1 | Threads typo permanent post-publish (Threads edit window kecil ~5 min, atau no edit at all kadang) | 🔴 High | 🟡 Medium | **Pre-check:** verify Threads native edit policy saat ini (bisa berubah). **During:** preview compose mode 8 post sebelum schedule/publish, side-by-side dengan THREADS-PINNED-8-POST.md verbatim. Kalau no edit → publish 1 post test dulu, verify edit available, baru lanjut 8 post. **Recovery:** kalau typo permanent → delete thread, repost (lose initial reach). Mitigasi paling penting: PROOFREAD before publish. |
| W3.2.2 | Char count per post ≤500 manual verify — paste 480 char, oh wait jadi 510 setelah space | 🟡 Medium | 🟡 Medium | Pakai Threads native counter (color berubah saat dekat 500). Brief sudah pre-validate ≤500, tapi double-check pas paste. |
| W3.2.3 | Native Threads scheduler vs Buffer external — pilih mana | 🟡 Medium | 🟡 Medium | Pakai Threads native scheduler (no external dependency, lebih reliable). Buffer Free tier 1 channel limit. |

---

### Wave 4.1 — Notion 3-database (90-120 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W4.1.1 | Notion template — apakah Wave 4-5 brief assume template gallery atau scratch from blank | 🔴 High | 🟡 Medium | **Pre-check:** baca WAVE-4-5-BUNDLE-BRIEF.md Section 4.1 — apakah ada Notion template URL atau "buat from scratch". **During:** kalau scratch → start dari template Notion gallery "Content Calendar" terdekat, customize (~30 min lebih cepat dari blank). **Recovery:** kalau gallery template ga match — fallback blank, accept 150 min not 90 min. |
| W4.1.2 | Notion learning curve database relation/rollup untuk first-time user | 🟡 Medium | 🔴 High | Plan 150 min not 90 min. Watch 5 min Notion tutorial "Database Relations" di YouTube sebelum start. |
| W4.1.3 | Property naming consistency dengan brief Wave 4.1 spec | 🟢 Low | 🟢 Low | Copy-paste exact dari brief, jangan rename. |

---

### Wave 4.2 — Sheets 6-tab (60 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W4.2.1 | Sheets formula complexity (IMPORTRANGE, INDEX-MATCH, ARRAYFORMULA) | 🟡 Medium | 🟡 Medium | Start simple: manual entry first 6-tab, formula automation Bulan 2+. Kalau formula gagal, fallback hardcode. |
| W4.2.2 | Notion-to-Sheets bridge — API integration vs manual export CSV | 🟡 Medium | 🟡 Medium | Day 1: manual export CSV mingguan dari Notion (5 min/minggu). Bulan 2+: automate via Make.com / Zapier kalau worth the setup. |
| W4.2.3 | 6-tab consistency formatting (header, freeze row, color code) | 🟢 Low | 🟢 Low | Buat tab 1 = template, duplicate tab 2-6, edit content only. |

---

### Wave 5.1 — Dry-run end-to-end (30 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W5.1.1 | Dependency Wave 1-4 deploy 100% — kalau gap, dry-run incomplete | 💥 Critical | 🟡 Medium | **Pre-check:** confirm semua Wave 1-4 deploy sebelum start Wave 5.1. **During:** kalau gap (mis. MailerLite belum live) — STOP, kembali Wave 2.2, JANGAN dry-run dengan gap (false positive berbahaya). **Recovery:** dry-run hanya valid kalau Wave 1-4 100%. |
| W5.1.2 | Cross-link verification chain (Threads bio → Lynk.id → MailerLite landing → Email 0) | 🔴 High | 🟡 Medium | **During:** click each link manual, log result di blocker note. Kalau 1 link broken → halt, fix, re-test full chain (bukan partial). **Recovery:** kalau 1 chain fail, defer launch H+1 sampai chain green. |
| W5.1.3 | Email Day 0 trigger latency verify — target ~5 min, actual bisa 1-15 min | 🟡 Medium | 🟡 Medium | Submit form di stranger persona, set timer. Kalau >15 min → check MailerLite automation status, mungkin pending review (Free tier sometimes review first email). |

---

### Wave 5.2 — Day-1 ritual (30 min)

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| W5.2.1 | Pre-launch nerves → decision drift, last-minute spec change | 🟡 Medium | 🟡 Medium | Re-read decision lock di LANJUTKAN-DI-SINI.md. NO improvisation H-0. |
| W5.2.2 | D-day Senin pagi unexpected — sakit, internet down, family emergency | 🔴 High | 🟢 Low | **Pre-mitigation:** pre-stagger semua post di scheduler H-1 malam (Threads native + Buffer). Kalau D-day fail → bio updated, scheduler tetap publish, recovery via DM/reply. **Recovery:** push back launch H+1 acceptable. JANGAN launch half-baked. |
| W5.2.3 | Filter 4-Lapis re-read SACRED skip karena rush | 🟡 Medium | 🟡 Medium | Non-negotiable, 5 min ritual. Block sebelum T-30. |

---

## CROSS-CUTTING RISKS

| ID | Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|---|
| CC1 | Domain gap — `arifb.id/[path]` placeholder masih valid sampai Mgg 7 buku launch | 🟡 Medium | 🔴 High | Wave 2.1 Lynk.id pakai sub-domain native (`lynk.id/arifb.id`), tidak block Day 1. Action D-30 sebelum buku launch (Mgg 4-5). |
| CC2 | Notification disruption (WhatsApp, calls, IG, email) | 🟡 Medium | 🔴 High | DND mode mandatory selama 10 jam. Notify pasangan/keluarga in advance. |
| CC3 | Decision drift mid-deploy — tergoda improvise font/wording/layout yang sudah locked | 🔴 High | 🟡 Medium-High | **Pre-check:** baca DECISION LOCK Wave 1-5 H-1. **During:** anti-drift checkpoint per Wave (pause 2 menit, reread lock sebelum lanjut). **Recovery:** kalau sudah drift → halt session, brainstorm ulang di Kiro/sesi baru, JANGAN auto-fix yang break spec cascading. |
| CC4 | 10 jam sequential split feasibility — burnout risk di jam 6-7 | 🟡 Medium | 🟡 Medium | Recommended split 2 hari (5+5 jam, mis. Sabtu Wave 1-3 + Minggu Wave 4-5). Kalau 1-day → 30-min break per 2 jam mandatory. |

---

## RECOVERY / ROLLBACK PLAN (4 SCENARIO)

### Scenario 1 — Partial Wave fail mid-deploy

| Wave fail | Action | Launch Day 1 impact |
|---|---|---|
| Wave 1.1 (wordmark) | Halt all subsequent (Wave 1.2 OK lanjut, tapi Wave 3.1 BLOCKED) | Defer Wave 3.1 publish IG, post text-only IG Day 1 |
| Wave 1.2 (bio paste) | Recoverable, edit anytime | Minimal |
| Wave 2.1 (Lynk.id) | Halt Wave 5.1 dry-run (chain broken) | Defer launch H+1 atau pakai linktr.ee emergency |
| Wave 2.2 (MailerLite) | Halt Wave 5.1 + email funnel | **CRITICAL:** kalau email funnel broken → defer launch H+1, jangan launch tanpa lead magnet |
| Wave 3.1 (IG Carousel) | Defer carousel publish ke Day 2, post text-only IG Day 1 dengan caption manifesto | Acceptable, IG fokus shift ke text |
| Wave 3.2 (Threads pinned) | Defer pin sampai functional, manifesto tetap publish via thread compose | Acceptable, no pin Day 1 |
| Wave 4.x (Tracking) | Defer ke Day 2-3, manual log eksternal sementara | Acceptable, tracking gap 1-3 hari |
| Wave 5.1 (Dry-run) | Fix gap, re-test, JANGAN launch dengan gap unverified | Defer launch H+1 sampai dry-run green |
| Wave 5.2 (Ritual) | Push back launch ke hari berikutnya (acceptable) | Defer H+1 |

### Scenario 2 — Tool/account block (auth fail, suspended)

- **MailerLite suspended:** switch ke Substack (free tier email) emergency Day 1, defer 9-email automation Bulan 1 Mgg 2
- **Lynk.id down:** temporary pakai `linktr.ee/arifb.id` atau `bio.link/arifb.id`, redirect saat Lynk.id up
- **Canva Pro lapse:** Figma free atau Adobe Express free (Playfair + Inter available di keduanya)
- **Threads/IG/LinkedIn shadowban:** check via incognito, kalau confirmed → contact platform support, content tetap publish (assume tidak shadowban di Day 1, low likelihood)

### Scenario 3 — Decision drift saat eksekusi

- **Trigger signal:** ingin ganti font/color/wording yang sudah locked di brief
- **Action:** STOP, re-read decision lock di LANJUTKAN-DI-SINI.md
- **Kalau memang butuh ganti:** halt session, brainstorm ulang di Kiro (sesi baru), commit perubahan ke spec, baru lanjut deploy
- **JANGAN improvise mid-deploy** — breaking change cascading ke Wave lain

### Scenario 4 — D-day blocker (Senin pagi sakit/emergency)

- **Pre-mitigation H-1:** semua post pre-stagger di scheduler (Threads native + IG native + LinkedIn manual hold)
- **D-day fail:** push back launch H+1 hari (acceptable, no rush)
- **Bio update fallback:** "@arifb.id launch announcement [tanggal baru]" di 4 platform bio
- **Notify warm circle:** kalau ada pre-launch waitlist email subscriber, kirim email "Launch postponed 1 day, see you Tuesday 19:30"

---

*Last updated: Sesi 28 Mei 2026 — Path F closure. Pre-deploy risk register untuk eksekusi manual ~10 jam Wave 1-5. 38 risk total (35 per-Wave + 4 cross-cutting). Top 5 critical: MailerLite sender auth, 7 worksheet content gap, Wave 3.1 dep Wave 1.1, TikTok link <1K follower, decision drift mid-deploy. Read H-1 hari sebelum deploy. Re-check Critical risks H-0 morning.*
