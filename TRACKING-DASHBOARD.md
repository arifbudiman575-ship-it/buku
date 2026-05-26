# TRACKING DASHBOARD — KPI & Audit Operasional

> **Tujuan:** Track KPI, decision rules, audit mingguan supaya strategi data-driven, bukan vibes-driven.
>
> **Konsep dasar:** *5 menit per hari isi data, 15 menit per Senin pagi audit. Tidak boleh lebih lama.*
>
> Tool: **Google Sheets** (gratis, mobile-friendly, sync otomatis).
>
> **Bagian dari:** THE AI ARCHITECT Playbook — Chapter 4.2.

---

## STRUKTUR — 6 TAB

### TAB 1 — Daily Post Log
Isi setiap malam (~3-5 menit). 1 baris per post.

| Kolom | Format | Contoh |
|---|---|---|
| Date | YYYY-MM-DD | 2026-06-01 |
| Day# | Number 1-365 | 1 |
| Platform | Dropdown | Threads / IG-Carousel / IG-Reels / TikTok / LinkedIn / X |
| Pillar | Dropdown | P1 / P2 / P3 |
| Funnel | Dropdown | TOFU / MOFU / BOFU |
| Hook style | Dropdown | Contrarian / Confession / Callout / Question / List / Paradoks / Vulnerability |
| Hook# | Reference | #14 / #28 / NEW |
| Title | Text 1 baris | "5 tanda Anda masih operator AI" |
| Views (24h) | Number | 4.230 |
| Likes | Number | 320 |
| Saves | Number | 47 |
| Comments | Number | 18 |
| Komen substantif | Number manual | 6 |
| Follower delta (24h) | Number | +12 |
| Engagement rate | Auto-formula | 9% |
| Save rate | Auto-formula | 1.1% |
| ICP match | 1-5 manual | 4 |
| Notes | Text bebas | "Hook bagus, closing flat" |

**Auto-formula:**
- Engagement rate: `=(Likes + Saves + Comments) / Views`
- Save rate: `=Saves / Views`
- Top trigger: `=IF(EngagementRate > 0.10, "TOP", "")`

---

### TAB 2 — Weekly Audit
Isi Senin pagi (15 menit). 1 baris per minggu.

Pertanyaan dari STRATEGI Section 14.2 (Audit Asosiasi 5 ?) + Section 16.2 (Refleksi Theoderic 4 ?):

| Kolom | Tipe |
|---|---|
| Wk# | Number |
| Date | Senin tanggal |
| Asosiasi 1 — Slip akun landmine? | Y/N + catatan |
| Asosiasi 2 — Voice slip ke caps/lo-gw? | Y/N + catatan |
| Asosiasi 3 — Undangan kolaborasi? Lulus 4-cek? | Y/N + decision |
| Asosiasi 4 — Follower mismatch >30%? | % + action |
| Asosiasi 5 — Tergoda hype-language? | Y/N + trigger |
| Theoderic 1 — Purpose check OK? | Y/N |
| Theoderic 2 — Strength check (tidak meniru)? | Y/N |
| Theoderic 3 — Quality of growth OK? | Y/N |
| Theoderic 4 — Tergoda jualan/teriak? | Y/N |
| Decision Rule active | Multi-select #1-#8 |
| Action minggu depan | 1-3 kalimat |

---

### TAB 3 — Monthly Dashboard
Auto-rollup + manual review akhir bulan.

| Metrik | Target B1 | Target B2 | Target B3 | Actual |
|---|---|---|---|---|
| Followers Threads | 1.000 | 5.000 | 12.000 | (auto) |
| Followers IG | — | — | — | (manual) |
| Followers TikTok | — | — | — | (manual) |
| Email subscribers | 200 | 600 | 1.500 | (auto) |
| Engagement rate avg | >=5% | >=6% | >=7% | (auto) |
| Top post views | >=5K | >=15K | >=30K | (auto) |
| ICP match % | >=30% | >=40% | >=50% | (auto) |
| Buku terjual | 0 | 100 | 300 | (manual) |
| Cohort slot terisi | 0 | 0 | 12 | (manual) |
| Corporate inbound | 0 | 1 | 3 | (manual) |
| Revenue cumulative | Rp 0 | Rp 30JT | Rp 100JT | (auto Tab 4) |

**Manual review akhir bulan:**
- Top 10% post — 3 tertinggi engagement -> catat pattern -> replikasi
- Bottom 10% post — 3 terendah -> cek filter 4-lapis lulus? Voice slip?
- Decision Rules triggered — list rule aktif + action diambil

---

### TAB 4 — Revenue Tracker
Isi setiap transaksi.

| Kolom | Format |
|---|---|
| Date | YYYY-MM-DD |
| Customer name | Text |
| Email | Text (match Tab 5) |
| Product | Dropdown: Buku 297K / Buku+Workbook 547K / Buku Premium 897K / Cohort Reg 4.9JT / Cohort VIP 7.5JT / Audit 25JT / Audit 50JT / Retainer 100JT |
| Channel | Dropdown: Lynk.id / WA / Direct |
| Amount (Rp) | Number |
| Status | Paid / Pending / Refunded |
| Source attribution | Dropdown: Threads / IG / TikTok / LinkedIn / Email / WoM / Direct |
| Notes | Text bebas |

Auto-rollup ke Tab 3.

---

### TAB 5 — Email Subscriber Tracker
Isi mingguan dari export Lynk.id atau email tool.

| Kolom | Format |
|---|---|
| Email | Text |
| Date subscribed | Date |
| Source (UTM/manual tag) | Dropdown: Threads / IG / TikTok / LinkedIn / Bio link |
| Tag/Segment | Multi: 7-Day Challenge / Buku reader / Cohort waitlist / Corporate prospect |
| Last engaged | Date open email terakhir |
| Status | Active / Dormant (>30 hari no open) / Unsub |
| Note | Text |

---

### TAB 6 — Idea Bank & Komen Promised

**A. Komen substantif yang harus di-reply (commitment delivery)**

| Date | Platform | Komen | Reply by | Status |
|---|---|---|---|---|
| 2026-06-01 | Threads D6 | "Saya skor 4 dari 5..." | 2026-06-01 23:30 | Done |

**B. Pertanyaan reader -> konten depan**

| Date | Pertanyaan | Konten target | Status |
|---|---|---|---|
| 2026-06-08 | "Bagaimana audit AI tools?" | D24 calendar | Used |

**C. Hook baru dari komen** (5 hook/bulan, refresh ke STRATEGI Section 6 quarterly)

---

## DECISION TRIGGER — Conditional Formatting

Highlight merah otomatis kalau threshold lewat:

| Trigger | Threshold | Action |
|---|---|---|
| Rule #1 Engagement <3% selama 2 minggu | Auto-flag | Ganti hook style 50% |
| Rule #2 Follower flat 2 minggu (delta sum <50) | Auto-flag | Audit pillar dominasi |
| Rule #3 Email opt-in <2% dari profile visit | Auto-flag | Revisi judul lead magnet |
| Rule #6 Views >10K + komen substantif <3 | Auto-flag | JANGAN ulangi format (viral-trap) |
| Rule #7 ICP match <30% | Auto-flag | Audit hook 2 minggu |
| Rule #8 3+ post ICP rating <=2 berturut | Auto-flag | STOP 3 hari, restart filter ketat |

**Implementation Sheets:**
Conditional Format -> Custom formula -> mis. `=AND(P2<0.03, AVERAGE(P$1:P2)<0.03)` -> highlight red.

---

## ICP MATCH FRAMEWORK (kolom Tab 1)

Rate 1-5 berdasarkan profile follower baru / komen substantif:

| Rating | Tipe | Karakteristik |
|---|---|---|
| 5 | Decision-maker | Founder / pemimpin tim / C-level / direktur. Bio sebut role + perusahaan. |
| 4 | Praktisi senior | Manajer / consultant / specialist 5+ tahun. Bio professional. |
| 3 | Profesional umum | Mid-level employee. Bio standar. |
| 2 | Pelajar / pengamat | Mahasiswa / fresh grad / hobby learner. Bio personal. |
| 1 | Tactical seekers | Cari "prompt rahasia", quick hack. Bio "AI enthusiast" tanpa konteks profesional. >5% follower baru = alarm. |

**Sampling:** 5 follower baru/minggu cukup. Tidak perlu rate semua.

---

## ROUTINE

### Harian
| Waktu | Aksi | Durasi |
|---|---|---|
| 30 menit setelah publish | Reply komen pertama (commitment) | 30 menit |
| 21:00-21:05 (malam) | Isi Tab 1 Daily Post Log | 3-5 menit |

### Mingguan
| Waktu | Aksi | Durasi |
|---|---|---|
| Senin 07:00-07:15 | Tab 2 Weekly Audit + cek decision triggers | 15 menit |
| Senin (anytime) | Update Tab 5 Email Subscriber (paste export) | 5 menit |

### Bulanan
| Waktu | Aksi | Durasi |
|---|---|---|
| Day 28-30 | Tab 3 Monthly Dashboard review + tulis 3 pelajaran | 60-90 menit |

### Quarterly
| Waktu | Aksi | Durasi |
|---|---|---|
| Day 90, 180, 270, 360 | Strategy Refresh Protocol (lihat Chapter 4.5) | 60-90 menit |

**Aturan emas:** Tidak refresh metrik > 3x sehari. Track untuk decision, bukan dopamine.

---

## SETUP AWAL — Google Sheets

### Step 1 — Buat file
1. Google Drive -> New -> Google Sheets
2. Rename: `AI-ARCHITECT-TRACKING-DASHBOARD-2026`
3. Buat 6 tab sesuai struktur di atas

### Step 2 — Setup Tab 1 (Daily Post Log)
1. Header row: copy struktur kolom
2. Format dropdown: Data -> Data validation -> List of items
3. Format date: Format -> Number -> Date
4. Auto-formula:
   - Engagement rate (kolom O): `=(J2+K2+L2)/I2`
   - Save rate (kolom P): `=K2/I2`
5. Format conditional: Cell value > AVERAGE -> highlight green

### Step 3 — Setup Tab 2-6
Sama pola. Per template di atas.

### Step 4 — Mobile setup
1. Install Google Sheets app di HP
2. Pin file ke favorite supaya akses cepat
3. Test entry 1 baris dummy untuk verify formula

### Step 5 — Backup
Auto-sync Google Drive (built-in). Tambahan: File -> Version history -> Name current version "v1.0 — Day 1 Setup".

**Estimated total setup time: 30-45 menit.**

---

## INTEGRATION DENGAN PLATFORM

| Platform | Cara dapat data |
|---|---|
| Threads | Manual entry dari Insight tab masing-masing post (~3 menit/post) |
| IG | Manual dari Insight tab (lebih lengkap) |
| TikTok | Manual dari Analytics tab |
| LinkedIn | Manual dari Post Analytics |
| Lynk.id | Export CSV mingguan -> paste ke Tab 4 |
| Email tool | Export CSV mingguan -> paste ke Tab 5 |

**Tools auto-import (untuk Bulan 4+ kalau scale):** Metricool ($30/bulan) atau Buffer Analytics — overkill untuk Bulan 1-3.

---

## ANTI-PATTERN

- Track > 30 KPI (overkill, paralisis analisis)
- Refresh metrik tiap 30 menit (dopamine, bukan decision)
- Bandingkan dengan kompetitor harian (toxic + tidak actionable)
- Hapus data lama (history valuable untuk pattern recognition)
- Skip audit Senin pagi 2x berturut (drift signal mulai dari sini)
- Tracking jadi alasan untuk tidak posting ("mau optimize dulu")

---

## LINK KE FILE LAIN

- Decision Rules -> `STRATEGI-PERSONAL-BRANDING.md` Section 12
- Audit questions -> STRATEGI Section 14.2 + 16.2
- Hook Bank untuk Tab 1 dropdown -> STRATEGI Section 6 + 6.B
- Strategy Refresh Protocol (quarterly) -> Chapter 4.5 (akan dibangun di Item 12)

---

## SACRED vs FLEXIBLE

**SACRED:**
- 6 tab structure (jangan tambah/kurangi)
- Decision triggers wajib di-encode (Rule #1, 2, 3, 6, 7, 8)
- Aturan emas "5 menit/hari, 15 menit/Senin"

**FLEXIBLE:**
- Specific KPI threshold (boleh adjust kalau target Roadmap berubah)
- Dropdown values (tambah platform baru kalau ekspansi)
- Auto-formula (tweak kalau Sheets update)

---

*File dibuat: Layer 13 (Mei 2026). Bagian dari THE AI ARCHITECT PERSONAL BRANDING & MONETIZATION PLAYBOOK — Chapter 4.2.*
*Decision rules linked ke STRATEGI Section 12. Audit questions linked ke Section 14.2 + 16.2.*
