# OPERATIONAL SETUP GUIDE — Tooling, Workflow, Rhythm

> **Tujuan:** Setup infrastruktur operasional sekali, jalan 12 bulan tanpa drama.
>
> **Konsep dasar:** *Tools sesedikit mungkin yang tetap fungsional. Setup 4-6 jam Pra-Day-1, lalu autopilot.*
>
> **Bagian dari:** THE AI ARCHITECT Playbook — Chapter 4.1.

---

## 1. TOOLING STACK FINAL

| Layer | Tool | Pricing | Role |
|---|---|---|---|
| Email automation | **MailerLite** | Free <1K subs, ~$10/bulan setelah | 7-Day Challenge sequence + broadcast |
| Payment + Sales page | **Lynk.id** | Free tier / paid | Buku, cohort, lead magnet checkout |
| Visual rendering | **Canva Pro** | ~Rp 200K/bulan | Carousel, post, email header |
| Video editing | **CapCut Mobile** | Free | TikTok, IG Reels |
| Landing/Sales mockup | **Figma** | Free | Sales page advanced, slide deck |
| Tracking + Idea | **Google Sheets** | Free | Dashboard 6 tab (Chapter 4.2) |
| Idea Bank long-form | **Notion** | Free | Draft, komen-to-content, reference |
| Posting (Bulan 1-2) | Native + Threads scheduler | Free | Manual posting, learn each platform |
| Posting (Bulan 3+) | **Metricool** | ~$30/bulan | Cross-platform scheduler scale |
| PDF layout (Bulan 2+) | InDesign / Affinity | Subscription / one-time | Workbook, buku |

**Total cost Bulan 1-2:** ~Rp 200K/bulan (Canva Pro saja).
**Total cost Bulan 3+:** ~Rp 700K/bulan (+ Metricool ~$30).

---

## 2. PRA-DAY-1 CHECKLIST

Total estimated effort: **4-6 jam** dalam 1-2 hari sebelum Day 1.

### 2.1 MailerLite (~60 menit)

```
[ ] Sign up free account di mailerlite.com pakai email pro Anda
[ ] Verify domain (kalau ada) -> reduce spam score
[ ] Create form: "7-Day AI Architect Challenge"
    - Field: First name, Email
    - Tag auto: "7-day-challenge-2026"
[ ] Setup Automation Workflow:
    - Trigger: Form submit "7-Day Challenge"
    - 9 email harian (copy dari EMAIL-SEQUENCE-7-DAY-CHALLENGE.md)
    - Day 0 (welcome) -> Day 1-7 (daily) -> Day 8 (post-challenge)
[ ] Test dengan email pribadi: subscribe -> confirm 9 email masuk berurutan
[ ] Setup branding: logo, color (Deep Navy #1E3A5F), font Inter
[ ] Generate embed link untuk Lynk.id landing page
```

### 2.2 Lynk.id (~45 menit)

```
[ ] Sign up di lynk.id pakai email pro
[ ] Verify identity (KTP) -> unlock payment
[ ] Setup payment method (rekening bank receiving)
[ ] Buat halaman utama "@arifb.id" sebagai bio link aggregator:
    - Foto profile (sesuai Visual Brand Identity Section 4)
    - Bio: "AI Architect | Penulis THE AI ARCHITECT"
    - Link 1: 7-Day Challenge (lead magnet)
    - Link 2: Buku THE AI ARCHITECT (akan diaktifkan Mgg 7)
    - Link 3: Cohort A.R.S.I. (akan diaktifkan Mgg 11)
[ ] Buat landing page "7-Day Challenge":
    - Copy dari LANDING-PAGE-7-DAY-CHALLENGE.md
    - Embed MailerLite form
    - Theme: Light (sesuai Visual Brand Identity)
[ ] Test: klik link bio -> landing -> submit email -> masuk MailerLite
```

### 2.3 Canva Pro Brand Kit (~30 menit)

```
[ ] Sign up Canva Pro (Rp 200K/bulan)
[ ] Brand Kit setup:
    - Color: #FAFAFA, #1A1A1A, #6B6B6B, #1E3A5F (light theme)
    - Color: #1A1A1A, #FAFAFA, #A0A0A0, #D4A574 (dark theme)
    - Font heading: Playfair Display
    - Font body: Inter
    - Logo upload: wordmark "ARIF BUDIMAN / the ai architect"
[ ] Save 3 master template:
    - IG Carousel (dark theme, 1080x1350)
    - IG Reels frame (dark theme, 1080x1920)
    - Email header (light theme, 600x200)
[ ] Test: render 1 carousel dummy -> cek konsistensi warna + font
```

### 2.4 Google Sheets (link ke Chapter 4.2)

```
[ ] Buat file baru sesuai TRACKING-DASHBOARD.md Section "Setup Awal"
[ ] 6 tab: Daily Post Log, Weekly Audit, Monthly Dashboard, Revenue, Email, Idea Bank
[ ] Pin file di Google Sheets app HP
[ ] Test entry 1 baris dummy
```

### 2.5 Notion (~30 menit)

```
[ ] Sign up Notion free account
[ ] Buat workspace "AI Architect Playbook"
[ ] Buat 3 database:

    A. IDEA BANK
       Properties: Title | Status (Idea/Drafting/Scheduled/Published) |
                  Pillar (P1/P2/P3) | Platform (Threads/IG/TikTok/LinkedIn) |
                  Hook style | Created date | Scheduled date | Notes

    B. KOMEN-TO-CONTENT
       Properties: Komen text | Platform | Reader handle | Date received |
                  Content target (link to Idea Bank) | Status | Notes

    C. REFERENCE
       Properties: Title | Type (Article/Book/Stat/Quote) | Source URL |
                  Tag (AI/Branding/Indonesia/Business) | Notes
[ ] Install Notion mobile app, login
[ ] Test: buat 1 entry dummy di Idea Bank
```

### 2.6 Social Profile Setup (~60 menit total)

```
THREADS:
[ ] Bio: "AI Architect | Penulis THE AI ARCHITECT | Membangun otak digital untuk decision-maker"
[ ] Foto profile: hitam-putih sesuai Visual Brand Identity
[ ] Link bio: lynk.id/@arifb.id
[ ] Header: wordmark "ARIF BUDIMAN — the ai architect"

IG:
[ ] Switch ke Business/Creator account
[ ] Bio: sda Threads
[ ] Foto profile: SAMA dengan Threads
[ ] Link bio: lynk.id/@arifb.id
[ ] Highlight: "Manifesto", "Buku", "Cohort", "BTS" (akan diisi)

TIKTOK:
[ ] Switch ke Business account
[ ] Bio: shorter version "AI Architect | Penulis"
[ ] Foto profile: SAMA
[ ] Link bio: lynk.id/@arifb.id

LINKEDIN:
[ ] Headline: "AI Architect | Penulis THE AI ARCHITECT | Founder PROMIND-NEUROLINK"
[ ] About: 3 paragraf positioning
[ ] Foto profile: SAMA
[ ] Banner: wordmark + tagline

X (Optional, skip kalau tidak prioritize):
[ ] Bio + foto sda
```

### 2.7 Test End-to-End Funnel (~15 menit)

```
[ ] Klik link bio Threads -> landing 7-Day Challenge tampil
[ ] Submit email dummy di landing -> konfirmasi tampil
[ ] Cek inbox dummy -> email Day 0 welcome masuk
[ ] Cek Google Sheets Tab 5 -> email subscriber tercatat (manual paste)
[ ] Cek Notion -> bisa input ide post baru
```

Semua check = ready Day 1.

---

## 3. WORKFLOW INTEGRATION

```
                    READER JOURNEY
                          |
   +-----------------------------------------+
   | Threads/IG/TikTok/LinkedIn Post (TOFU) |  <- Konten harian
   +----------------+------------------------+
                    |
                    v
   +-----------------------------------------+
   | Klik bio -> lynk.id/@arifb.id          |  <- Bio link aggregator
   +----------------+------------------------+
                    |
                    v
   +-----------------------------------------+
   | Landing: 7-Day Challenge (MOFU)        |  <- Lead magnet
   +----------------+------------------------+
                    |
                    v
   +-----------------------------------------+
   | Submit email -> MailerLite tag         |  <- Capture
   +----------------+------------------------+
                    |
                    v
   +-----------------------------------------+
   | 9 email harian Day 0-8 (Trust 1+2)     |  <- Nurture
   +----------------+------------------------+
                    |
                    v
   +-----------------------------------------+
   | Mgg 7+: Buku launch / Mgg 11: Cohort   |  <- BOFU
   | Bulan 4+: Corporate inbound (WA)        |
   | Payment via Lynk.id                     |
   +-----------------------------------------+
```

**Flow data tracking:**
```
Post -> Sheets Tab 1 (Daily Post Log, malam yg sama)
Subscriber -> MailerLite -> export weekly -> Sheets Tab 5
Transaction -> Lynk.id -> manual entry Sheets Tab 4
Komen substantif -> Notion Komen-to-Content + Sheets Tab 6
```

---

## 4. DAILY OPERATIONAL RHYTHM

### Pagi (07:00-08:30) — 90 menit
```
07:00 - 07:30  Konsumsi reading list (1 buku 30 menit)
07:30 - 08:00  Review komen overnight di semua platform
08:00 - 08:30  Draft konten hari ini (kalau belum siap dari batching)
```

### Siang (12:00-13:00) — Posting + Reply Wave 1
```
12:00          Publish post Threads + LinkedIn (window optimal)
12:00 - 12:30  Reply 10 komen pertama (commitment)
12:30 - 13:00  IG/TikTok kalau ada (Reels = 11:00-13:00 optimal)
```

### Sore (17:00-18:00) — Reply Wave 2
```
17:00 - 17:30  Reply komen Wave 2
17:30 - 18:00  Capture komen substantif -> Notion
```

### Malam (21:00-21:15) — Tracking + Prep
```
21:00 - 21:05  Isi Sheets Tab 1 Daily Post Log
21:05 - 21:10  Cek schedule besok di Notion -> konfirmasi konten ready
21:10 - 21:15  Capture 1 ide baru ke Idea Bank kalau ada
```

**Total daily commit:** ~3-4 jam aktif (sudah include reading + reply + tracking).

---

## 5. WEEKLY OPERATIONAL RHYTHM

### Senin — Audit + Plan
```
07:00 - 07:15  Tracking Dashboard Tab 2 Weekly Audit
07:15 - 07:30  Update Sheets Tab 5 (paste export MailerLite)
07:30 - 08:00  Review action minggu lalu vs actual
```

### Selasa-Jumat — Eksekusi normal (Daily Rhythm)

### Sabtu — Batching Day
```
09:00 - 12:00  Batch produce 7 post untuk minggu depan
12:00 - 14:00  Batch render visual di Canva (sekaligus)
14:00 - 15:00  Schedule di Threads native (atau Buffer/Metricool kalau ada)
```

### Minggu — Reading + Filosofi
```
Pagi          Reading deep (1-2 jam)
Sore          Post Pillar 3 Filosofi (sesuai PILLAR-3-STUDI-CASE-PAK-BI.md)
Malam         Refleksi mingguan + Theoderic check
```

**Aturan Sabbath:** Minggu malam 8 PM sampai Senin pagi -> no platform check (kecuali emergency).

---

## 6. MONTHLY OPERATIONAL RHYTHM

### Day 28-30 — Monthly Review (~90 menit)
```
1. Review Tracking Dashboard Tab 3 Monthly Dashboard
2. Identifikasi:
   - Top 10% post -> catat pattern -> replikasi
   - Bottom 10% post -> audit filter 4-lapis
   - Decision Rules triggered -> action taken
3. Tulis 3 pelajaran utama bulan ini ke Notion -> Reference
4. Plan calendar bulan depan (atau review yg sudah ada)
5. Bulan 1 closing: lihat data -> adjust strategi sesuai BJM Q1 milestone
```

### Day 90/180/270/360 — Quarterly Refresh
Lihat **Chapter 4.5 Strategy Refresh Protocol** (Item 12 — akan dibangun).

---

## 7. EMERGENCY / TROUBLESHOOTING

| Masalah | Root Cause | Action Cepat |
|---|---|---|
| MailerLite email gak nyampe | Spam folder / domain unverified | Test 3 email provider (Gmail/Yahoo/Outlook) -> kalau spam, verify domain |
| Lynk.id payment pending | Verifikasi KTP belum complete / gateway error | Cek dashboard Lynk.id, contact support |
| Canva file corrupt / hilang | Cloud sync issue | Pakai version history (Canva: File > Version history) |
| Threads post tidak muncul | Shadow ban / TOS violation | Cek email Meta, hindari kata trigger 7-14 hari |
| Sheets formula error | Reference broken | Restore: File > Version history > pilih versi sebelumnya |
| HP rusak / hilang | Tidak ada backup | Enable Google Drive auto-sync, Notion mobile sync, MailerLite cloud (no local data) |
| Anda sakit / tidak posting 3+ hari | Burnout / sakit | Aktifkan Anti-Burnout Protocol (Chapter 4.4 — Item 10) |

---

## 8. ANTI-PATTERN — Yang TIDAK Perlu Setup

- **Custom domain email (mail@arifb.id)** — overkill Bulan 1, MailerLite sender free cukup. Setup Bulan 4+ kalau scale.
- **CRM (HubSpot, Pipedrive)** — overkill. Tab 5 Sheets + MailerLite tag cukup sampai 3K subscribers.
- **Analytics tool tambahan (Google Analytics, Mixpanel)** — overkill. Lynk.id + native platform analytics + Sheets cukup.
- **Discord / Slack community** — Bulan 1-3 tidak perlu. Cohort delivery tools dipikir saat Item 8 (Bulan 2-3).
- **Custom website (Webflow, WordPress)** — Bulan 1-6 tidak perlu. Lynk.id cukup. Custom website saat brand sudah strong (Bulan 7+).
- **Buffer/Metricool Bulan 1** — pakai native dulu. Belajar feel platform -> upgrade saat workload nyata.
- **AI tool subscription tambahan (Jasper, Copy.ai)** — Anda PUNYA voice unik, AI tool akan dilute. Pakai ChatGPT/Claude untuk research saja.
- **Project management tool (Asana, ClickUp)** — Notion cukup. Solo creator tidak butuh PM tool kompleks.

---

## 9. SACRED vs FLEXIBLE

**SACRED (jangan ubah selama 6 bulan minimum):**
- MailerLite sebagai email tool (migrate cost tinggi)
- Lynk.id sebagai payment + landing
- Google Sheets struktur 6 tab
- Daily rhythm 3-window (siang post + sore reply + malam track)
- Sabbath rule (Minggu malam -> Senin pagi)

**FLEXIBLE (boleh adjust kuartalan):**
- Scheduler choice (native -> Metricool saat scale)
- PDF tool (Canva -> InDesign saat butuh layout buku)
- Notion template detail (tambah database kalau perlu)
- Daily timing window (kalau data tunjukkan engagement window beda)
- Tools tambahan kalau ada justified ROI

---

## LINK KE FILE LAIN

- Tracking detail -> `TRACKING-DASHBOARD.md` (Chapter 4.2)
- Visual brand kit setup -> `VISUAL-BRAND-IDENTITY.md` (Chapter 2.3)
- Email sequence content -> `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md`
- Landing page content -> `LANDING-PAGE-7-DAY-CHALLENGE.md`
- Reply farm workflow -> `REPLY-FARM-PLAYBOOK.md` (Chapter 4.3 — Item 4 next)
- Anti-burnout escalation -> `ANTI-BURNOUT-PROTOCOL.md` (Chapter 4.4 — Item 10)

---

*File dibuat: Layer 14 (Mei 2026). Bagian dari THE AI ARCHITECT PERSONAL BRANDING & MONETIZATION PLAYBOOK — Chapter 4.1.*
