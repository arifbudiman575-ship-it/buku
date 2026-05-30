# WAVE 4-5 BUNDLE BRIEF — Tracking + Dry-Run + Day-1 Ritual

> Status: FINAL · Wave 4-5 Pra-Day-1 closing bundle · Hasil sesi brainstorm Kiro (BRAIN) → eksekusi user manual (HANDS, Notion + Sheets + final ritual).
> Anchor: DAY-1-LAUNCH-CHECKLIST.md Wave 4 + 5 · OPERATIONAL-SETUP.md §2.5 + §2.7 · TRACKING-DASHBOARD.md · STRATEGI-PERSONAL-BRANDING.md §0.5 (Filter 4-Lapis) · CONTENT-CALENDAR-BULAN-1.md (D1-D7 posts) · REPLY-FARM-PLAYBOOK.md (mental rehearsal).
> Decision lock: A1 + B-anchor + C-anchor + D1 + E1 + F1.
> Coverage: Wave 4.1 + 4.2 + 5.1 + 5.2 = 4 sub-wave dalam 1 brief.

---

## DECISION LOCK SUMMARY

| Letter | Decision | Locked value |
|---|---|---|
| A | Notion DB column schema | Full select fields (pillar/status/platform multi-select) untuk enable filter & sort |
| B | Sheets header schema | Verbatim dari TRACKING-DASHBOARD.md, no custom additions Day 1 |
| C | Conditional formatting | 3-color (GREEN/YELLOW/RED) per Decision Trigger di Tab 1 + Tab 3 |
| D | Test email Wave 5.1 | Email pribadi #2 user (bukan primary `arif@arifb.id`) |
| E | 7 ide Mgg 1 | Pull D1-D7 verbatim dari CONTENT-CALENDAR-BULAN-1.md |
| F | Mobile setup | Notion app + Sheets app + 2 browser bookmark + 4 homescreen shortcut |

---

## 1. WAVE 4.1 — NOTION 3-DATABASE SETUP

**Estimasi: ~45 menit**

### Step 1 — Workspace setup (5 min)
1. Login Notion (free tier sudah aktif per OPERATIONAL-SETUP)
2. Create new workspace: **"Personal Branding @arifb.id"**
3. Layout sidebar: 3 database top-level + 1 page "Quick Reference"

### Step 2 — Database 1: Idea Bank (15 min)

**Schema kolom:**

| Column | Type | Options |
|---|---|---|
| Title | Title (text) | required |
| Pillar | Select | P1 (Eduvasi) · P2 (Studi Kasus) · P3 (Filosofi) |
| Hook | Text | first-line opener post |
| Status | Select | Draft · Scheduled · Posted · Archive |
| Scheduled Date | Date | required untuk Status=Scheduled |
| Day# | Number | D1, D2, ... (untuk sort by sequence Bulan 1) |
| Platform | Multi-select | Threads · IG · TikTok · LinkedIn |

**View setup:**
- View 1 "Scheduled Week" — filter Status=Scheduled, sort Scheduled Date asc
- View 2 "By Pillar" — group by Pillar
- View 3 "Posted Archive" — filter Status=Posted

**Test entry — load 7 ide Mgg 1:**

Pull D1-D7 dari `CONTENT-CALENDAR-BULAN-1.md` (Wave anchor). Per ide:
- Title (judul post)
- Pillar (P1/P2/P3 sesuai calendar tag)
- Hook (first-line opener)
- Status: `Scheduled`
- Scheduled Date: tanggal D1, D2, ... D7 actual (tergantung Anda set Day 1 = tanggal berapa)
- Day# (1-7)
- Platform (sesuai cross-platform spec calendar)

**Acceptance:** 7 ide loaded, sorted by Day#, semua status `Scheduled`.

### Step 3 — Database 2: Komen-to-Content (10 min)

**Schema kolom:**

| Column | Type | Options |
|---|---|---|
| Source | Text | URL post / akun komen-er |
| Komen | Text | quote komen verbatim |
| Transform | Text | ide jadi konten (hook + angle) |
| Status | Select | Captured · Drafted · Posted · Discarded |
| Date Captured | Date | auto-fill |

**Test entry:** kosong saat setup. Akan terisi saat reply farm aktif Bulan 1.

### Step 4 — Database 3: Reference Library (10 min)

**Schema kolom:**

| Column | Type | Options |
|---|---|---|
| URL | URL | required |
| Title | Text | judul article/video/podcast |
| Kategori | Select | Buku/Course/Podcast/Article/Tweet/Video |
| Takeaway | Text | 1-2 kalimat insight |
| Date Added | Date | auto-fill |

**Test entry — pre-populate 5 reference foundational:**
1. Pak Bi podcast (`pak bi.txt` source) — Kategori: Podcast
2. Theoderic interview (`ilmu Theoderic.txt`) — Kategori: Podcast
3. Caleb Ralston brand journey doc — Kategori: Course
4. Rama / @productivityboi course — Kategori: Course
5. THE AI ARCHITECT manuskrip Anda — Kategori: Buku

### Step 5 — Mobile setup (5 min)
1. Install Notion app di HP (iOS/Android)
2. Login same account
3. Pin "Personal Branding @arifb.id" workspace
4. Add Notion shortcut ke homescreen HP

---

## 2. WAVE 4.2 — GOOGLE SHEETS 6-TAB TRACKING

**Estimasi: ~50 menit**

### Step 1 — File creation (5 min)
1. Google Sheets → New blank → rename **"Tracking @arifb.id 2026"**
2. Save di folder Drive: `arifb-id / tracking`
3. Sharing: PRIVATE (only owner). Tidak share Day 1.

### Step 2 — Tab 1: Daily Post Log (10 min)

**Header columns** (verbatim dari TRACKING-DASHBOARD.md):

| Column | Notes |
|---|---|
| Date | YYYY-MM-DD |
| Day# | D1, D2, ... |
| Platform | Threads / IG / TT / LI |
| Pillar | P1 / P2 / P3 |
| Title | judul post |
| URL Post | link langsung |
| Views | manual entry T+24h |
| Likes | manual T+24h |
| Replies | manual T+24h |
| Reposts | manual T+24h |
| Quality Score | 1-5 self-rating |
| Notes | catatan refleksi |

**Conditional formatting:**
- Quality Score 4-5: ○ GREEN row
- Quality Score 3: 🟡 YELLOW row
- Quality Score 1-2: ● RED row

### Step 3 — Tab 2: Weekly Audit (10 min)

**Layout:** 5-pertanyaan Audit Asosiasi (Caleb framework) + 4-pertanyaan Refleksi Theoderic per minggu.

| Column | Type |
|---|---|
| Week# | W1, W2, ... |
| Audit Asosiasi 1: Apakah konten saya minggu ini reinforce "AI Architect = building systems, not hype"? | text response |
| Audit Asosiasi 2: Apakah ada konten yang drift ke generic AI educator? | text |
| Audit Asosiasi 3: Apakah voice "Anda" formal konsisten? | text |
| Audit Asosiasi 4: Apakah Filter 4-Lapis diterapkan setiap post? | yes/no/partial |
| Audit Asosiasi 5: Apakah ada interaksi audience yang challenge brand? | text |
| Refleksi Theoderic 1: Purpose minggu ini achieved? | yes/no/partial |
| Refleksi Theoderic 2: Strength yang paling sering dipakai? | text |
| Refleksi Theoderic 3: Drift dari authenticity? | text |
| Refleksi Theoderic 4: Action minggu depan? | text |

**Cadence:** isi setiap Senin pagi sebelum start minggu baru.

### Step 4 — Tab 3: Monthly Dashboard (10 min)

**Layout summary KPI:**

| Metric | Bulan 1 Target | Bulan 1 Actual | Status |
|---|---|---|---|
| Total post Threads | 30 | (manual) | ○/🟡/● |
| Total post IG | 12 | (manual) | sda |
| Total post TikTok | 12 | (manual) | sda |
| Total post LinkedIn | 8 | (manual) | sda |
| Subscriber baru lead magnet | 50 | (auto MailerLite) | sda |
| Buku waitlist signup | 20 | (auto) | sda |
| Cohort waitlist signup | 10 | (auto) | sda |
| Quality Score average | ≥3.5/5 | (auto AVG Tab 1) | sda |
| Reply farm 10-komen-pertama | 30 days × 1 | (manual) | sda |

**Conditional formatting:**
- Status column: ○ GREEN ≥100% target · 🟡 YELLOW 70-100% · ● RED <70%

### Step 5 — Tab 4: Revenue Tracker (5 min)

**Setup kosong sampai Mgg 7 buku launch.**

| Column | Notes |
|---|---|
| Date | transaction date |
| Product | Buku T1/T2/T3 · Cohort ARSITEK/PLUS · Corporate audit |
| Customer Email | tag-able dengan MailerLite list |
| Amount | Rp |
| Payment Method | Lynk.id / Bank transfer / VA |
| Status | Paid / Pending / Refund / Failed |
| Notes | edge case |

### Step 6 — Tab 5: Email Subscriber Tracker (5 min)

**Daily snapshot dari MailerLite:**

| Column | Notes |
|---|---|
| Date | YYYY-MM-DD |
| Total Subscriber | snapshot dari MailerLite |
| Lead Magnet Active | tag count |
| Buku Waitlist | tag count |
| Cohort Waitlist | tag count |
| Source Threads | manual attribution count |
| Source IG | sda |
| Source TikTok | sda |
| Source LinkedIn | sda |
| Source Referral | sda |
| Notes | spike anomaly |

**Cadence:** isi setiap Senin pagi (snapshot mingguan).

### Step 7 — Tab 6: Idea Bank & Komen Promised (5 min)

**Backup mirror Notion DB 1 + DB 2.** Setiap Sabtu malam, copy-paste rows dari Notion ke Sheets sebagai backup.

### Step 8 — Mobile setup (5 min)
1. Install Google Sheets app
2. Pin file "Tracking @arifb.id 2026" di favorites
3. Add bookmark URL Sheets ke browser HP
4. Homescreen shortcut

---

## 3. WAVE 5.1 — DRY-RUN END-TO-END (30 menit)

**Prereq:** Wave 1-4 deployed (bio paste + wordmark Canva + Lynk.id setup + MailerLite setup + Threads scheduled + Notion + Sheets ready).

### Test sequence (sequential)

**Test #1 — Stranger flow simulation (15 min)**
1. Buka browser **incognito mode** (atau handphone teman, log out semua akun)
2. Visit `threads.net/@arifb.id` → verify pinned 8-post visible
3. Klik bio link `arifb.id` → redirect ke `lynk.id/arifb.id`
4. Verify aggregator: foto + nama + tagline + 3 card visible
5. Klik **Card 1 Lead Magnet** → redirect ke MailerLite landing
6. Submit form: nama "Test User", email = email pribadi #2 (Anda specify)
7. Verify thank-you page render

**Test #2 — Email delivery + rendering (10 min)**
1. Cek inbox email pribadi #2 — Email 0 masuk dalam 5 menit
2. Verify rendering Gmail web: foto/logo OK, link OK, no broken format
3. Verify rendering Gmail mobile: responsive, readable
4. Verify rendering Outlook (kalau punya account) — fallback baseline
5. Klik link worksheet Hari 1 di Email 0 — verify Google Docs accessible view-only
6. Verify manual attribution question visible 3-4 lines pre-signoff

**Test #3 — Tracking verification (5 min)**
1. Buka Lynk.id analytics (Free tier basic counter) — verify visit + Card 1 click ter-track
2. Buka MailerLite dashboard → subscriber list — verify email pribadi #2 muncul dengan tag `lead_magnet_active`
3. Buka MailerLite automation — verify Email 0 sent + Email 1 scheduled +24h

### Pass criteria
- 3/3 test pass = Wave 5.1 status DEPLOYED ✓
- Fail handling: debug per stage (Lynk.id redirect / MailerLite trigger / email rendering / tracking)

### Edge case handling
- Kalau Email 0 tidak masuk inbox dalam 5 menit:
  1. Check spam folder
  2. Check MailerLite automation status (active vs draft)
  3. Check sender domain reputation (kalau pakai pro email)
  4. Re-trigger manual via MailerLite "send test"

---

## 4. WAVE 5.2 — DAY-1 FINAL RITUAL (30 menit, malam D-1)

**Timing:** D-1 jam 20:00-21:00 WIB (malam sebelum Day 1 launch jam 19:30 WIB)

### Ritual checklist (6 step)

**Step 1 — Re-read Filter 4-Lapis (5 min)**
1. Buka `STRATEGI-PERSONAL-BRANDING.md` §0.5
2. Re-read 4 lapis (Buku → Asosiasi → Voice → Purpose) sampai hafal urutan
3. Self-affirm: "Setiap post Day 1 dan seterusnya akan saya filter lewat 4 lapis ini"

**Step 2 — Lock 7 post Mgg 1 (10 min)**
1. Buka Notion Idea Bank
2. Verify 7 ide D1-D7 status `Scheduled` dengan Scheduled Date correct
3. Re-check tiap ide: hook punch? pillar tepat? platform tepat?
4. Kalau ada 1 ide ragu → revisi sekarang ATAU swap dengan ide cadangan dari calendar

**Step 3 — Set HP alarm (1 min)**
1. Set alarm HP: **Day 1 jam 18:00 WIB** (1.5 jam before Threads thread auto-publish 19:30)
2. Label alarm: "Day 1 Launch — battery + WiFi + mental ready"

**Step 4 — Mental rehearsal Reply Farm (10 min)**
1. Buka `REPLY-FARM-PLAYBOOK.md` Section "10-komen-pertama protokol"
2. Read 1× sampai paham target: 10 komen pertama dalam 30 menit (60 menit red line)
3. Simulasi mental: visualize Day 1 thread post → komen pertama masuk → Anda reply dalam 30 menit dengan tone formal, Filter 4-Lapis lolos

**Step 5 — Cek battery + WiFi + cadangan (3 min)**
1. HP charge ≥80% sebelum tidur
2. Laptop charged + adapter siap
3. WiFi rumah test speed → kalau pelan, siapkan cadangan hotspot HP
4. Confirm Threads scheduled post status "Scheduled" (bukan "Draft")

**Step 6 — Tidur cukup, tutup laptop 22:00 (1 min commitment)**
1. Tutup laptop jam 22:00 WIB
2. No social media scrolling sebelum tidur
3. Tidur minimum 7 jam → bangun Day 1 fresh
4. Day 1 butuh energi 4 jam productive (19:30-23:30 = launch + reply farm window)

### Pass criteria
- 6/6 step done = Wave 5.2 status DEPLOYED ✓
- Anda confidence — bukan ragu-ragu (per anchor DAY-1-LAUNCH-CHECKLIST §5.2)

---

## 5. ACCEPTANCE CRITERIA — Wave 4-5 SELESAI

Wave 4-5 status: **DEPLOYED ✓** ketika SEMUA point check:

### Wave 4.1 (Notion)
- [ ] Workspace "Personal Branding @arifb.id" aktif
- [ ] 3 DB live: Idea Bank + Komen-to-Content + Reference Library
- [ ] 7 ide D1-D7 loaded di Idea Bank dengan status `Scheduled`
- [ ] 5 reference foundational loaded di Reference Library
- [ ] 3 view per DB configured
- [ ] Notion app + homescreen shortcut HP

### Wave 4.2 (Sheets)
- [ ] File "Tracking @arifb.id 2026" aktif
- [ ] 6 tab created dengan header schema correct
- [ ] Tab 1 + Tab 3 conditional formatting active (3-color)
- [ ] Tab 4 (Revenue) kosong dengan column header ready
- [ ] Sheets app + bookmark + homescreen shortcut HP

### Wave 5.1 (Dry-run)
- [ ] Test #1 stranger flow: 7 step pass
- [ ] Test #2 email delivery + rendering: 6 step pass
- [ ] Test #3 tracking verification: 3 step pass
- [ ] Edge case handling rehearsed (Email 0 fail → debug protocol)

### Wave 5.2 (Day-1 ritual)
- [ ] Filter 4-Lapis re-read sampai hafal
- [ ] 7 post Mgg 1 locked di Notion
- [ ] HP alarm Day 1 18:00 WIB set
- [ ] Mental rehearsal Reply Farm done
- [ ] Battery + WiFi + cadangan ready
- [ ] Commitment tutup laptop 22:00 + tidur 7 jam

---

## 6. WAVE 4-5 → DAY 1 LAUNCH UNLOCK

| Dependency | Unlocked oleh Wave 4-5 |
|---|---|
| Notion Idea Bank | Source of truth post Bulan 1 — semua scheduled date & status visible |
| Sheets tracking | KPI dashboard live — bisa entry post Day 1 dalam 2 menit |
| Komen-to-Content DB | Reply farm Day 1 capture-able — komen audience yang punya potensi konten masuk Notion |
| Dry-run pass | Funnel proven jalan end-to-end — confidence Day 1 publish lead magnet |
| Day-1 ritual | Mental + physical readiness — energy budget + Filter 4-Lapis primed |
| **DAY 1 LAUNCH READY** | **Semua wave Pra-Day-1 = DEPLOYED ✓** |

---

## CHANGELOG

- **Sesi brainstorm:** Kiro Vibe (BRAIN), 28 Mei 2026
- **Decision lock:** A1 + B-anchor + C-anchor + D1 + E1 + F1 (mostly anchor-locked)
- **Anchor:** DAY-1-LAUNCH-CHECKLIST.md Wave 4 + 5 · OPERATIONAL-SETUP.md §2.5 + §2.7 · TRACKING-DASHBOARD.md · STRATEGI-PERSONAL-BRANDING.md §0.5 · CONTENT-CALENDAR-BULAN-1.md · REPLY-FARM-PLAYBOOK.md
- **Eksekusi:** User manual estimasi total ~3 jam (Wave 4.1 ~45min + Wave 4.2 ~50min + Wave 5.1 ~30min + Wave 5.2 ~30min + transition buffer ~25min)
- **Coverage:** 4 sub-wave (4.1 + 4.2 + 5.1 + 5.2) dalam 1 brief = closing Pra-Day-1 spec 100%
- **Output:** Notion 3-DB live + Sheets 6-tab live + dry-run pass + Day-1 ritual primed = launch-ready
- **Next milestone:** DAY 1 LAUNCH (Senin Bulan 1 Mgg 1, 19:30 WIB) — Threads thread auto-publish + reply farm 10-komen-pertama window 30-60 min
- **Post-Day-1:** Bulan 1 eksekusi 30 post + reply farm + weekly audit Senin pagi
