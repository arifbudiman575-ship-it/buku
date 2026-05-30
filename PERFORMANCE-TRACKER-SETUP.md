# PERFORMANCE TRACKER — BULAN 1

> Tempat tunggal untuk mencatat angka per post, agregat mingguan, dan log trigger Decision Rules.
>
> **Source of truth angka.** Notion dan repo bukan tempat angka — keduanya menampung naratif & keputusan.
>
> **Free-first:** Google Sheets gratis. Manual entry. Tidak butuh tools berbayar Bulan 1.

---

## 0. PRINSIP

1. **Tracker harus aktif sejak Day 1.** Tanpa data Day 1, baseline hilang permanen.
2. **Manual entry, bukan otomasi.** Bulan 1 = Anda merasakan ritme + pattern. Otomasi Bulan 2.
3. **5 menit per malam, max.** Kalau lebih, tracker terlalu rumit — sederhanakan kolom.
4. **Mingguan: agregat & trigger check.** Senin pagi 15 menit (sebelum audit asosiasi).
5. **Angka memandu, bukan menentukan.** Voice & purpose tetap di atas angka. Lihat Section 12 Decision Rules — semua action ada konteksnya.

---

## 1. STRUKTUR SHEET — 4 TAB

Buat 1 Google Sheet baru. Nama file: `arifb.id Performance Tracker — Bulan 1`. 4 tab:

| Tab | Fungsi | Frekuensi entry |
|---|---|---|
| **1. Daily Posts** | 1 baris per post (30 baris pre-filled) | Setiap malam, 5 menit |
| **2. Weekly Snapshot** | 1 baris per minggu (4 baris) | Setiap Senin pagi, 5 menit |
| **3. Trigger Log** | Log Decision Rule yang terpicu | Saat trigger, ad-hoc |
| **4. Lead Magnet Funnel** | Funnel profile -> opt-in -> completion | Mingguan, 5 menit |

---

## 2. TAB 1 — DAILY POSTS (struktur kolom)

Pre-fill 30 baris dari `MASTER OVERVIEW — 30 HARI` di kalender. Kolom yang harus ada:

| Kol | Nama | Tipe | Sumber awal | Diisi kapan |
|---|---|---|---|---|
| A | Day | Number (1-30) | pre-fill | — |
| B | Tanggal | Date | pre-fill saat tahu Day 1 | — |
| C | Hari | Sen-Min | pre-fill | — |
| D | Slot WIB | "19:30" / "12:30" / dll | pre-fill | — |
| E | Pillar | P1 / P2 / P3 | pre-fill | — |
| F | Funnel | TOFU / MOFU / BOFU | pre-fill | — |
| G | Hook (1 baris) | Text | pre-fill | — |
| H | CTA | None / Soft / Lead Magnet | pre-fill | — |
| I | Published | Y / N | manual | hari H, setelah publish |
| J | Views | Number | manual | T+24 jam |
| K | Likes | Number | manual | T+24 jam |
| L | Komen total | Number | manual | T+24 jam |
| M | **Komen substantif** | Number | manual + judgment | T+24 jam |
| N | Save | Number | manual | T+24 jam |
| O | Follower delta hari ini | Number (bisa negatif) | manual | hari H +1 pagi |
| P | Engagement % | Formula: (K+L+N) / J × 100 | auto | otomatis |
| Q | ICP match Y/N (top 3 follower baru) | Y / N / Mixed | manual judgment | T+24 jam |
| R | Top komen (1 kalimat) | Text | manual | T+24 jam |
| S | Voice slip? | Y / N | manual judgment | hari H, setelah publish |
| T | Notes | Text bebas | manual | bebas |

### Definisi operasional kolom yang ambigu

- **Komen substantif (M)** = komen yang menambah konteks, bertanya substansi, atau menceritakan pengalaman. **Bukan** "keren bro!", emoji-only, "follow back". Anda yang menilai.
- **ICP match (Q)** = ambil 3 follower baru terakhir, klik profil, judgment cepat: decision-maker / profesional senior / praktisi serius = match. Pelajar / pengamat / tactical seeker = mismatch.
- **Voice slip (S)** = post Anda hari itu ada elemen yang melanggar Voice §5.3 (lo/gue, caps lock, emoji berlebih, bahasa hype). Y bahkan kalau kecil — track honestly.

### Aturan entry harian

1. Set reminder HP **22:00 WIB** = "Update tracker."
2. Buka tab Daily Posts, scroll ke baris hari ini.
3. Isi kolom I-T. Kalau angka belum stabil (post baru 2 jam), skip — isi besok pagi T+24jam.
4. Kalau lupa 1 hari -> backfill paling lambat 48 jam. Lebih dari itu = data tidak reliable, mark "skipped" di kolom T.

---

## 3. TAB 2 — WEEKLY SNAPSHOT (struktur)

4 baris pre-filled (Minggu 1-4). Kolom:

| Kol | Nama | Sumber | Target Bulan 1 |
|---|---|---|---|
| A | Minggu | 1 / 2 / 3 / 4 | — |
| B | Range tanggal | pre-fill | — |
| C | Total followers (cumulative) | manual snapshot Senin pagi | 1.000 (Day 30) |
| D | Follower delta minggu ini | formula: C - C minggu lalu | — |
| E | Email opt-in (cumulative) | manual snapshot | 200 (Day 30) |
| F | Email delta minggu ini | formula | — |
| G | Engagement avg minggu ini | formula AVG(P) dari Daily | >= 5% |
| H | Top post views minggu ini | formula MAX(J) dari Daily | >= 5K (cumulative top) |
| I | Top post Day# | formula INDEX/MATCH | — |
| J | Komen substantif total minggu ini | formula SUM(M) | >= 21 (3/post × 7 post) |
| K | ICP match % minggu ini | formula COUNTIF(Q="Y") / COUNT(Q) | >= 30% |
| L | Voice slip count | formula COUNTIF(S="Y") | 0 — target |
| M | Decision Rule terpicu | text manual | log ID dari Tab 3 |
| N | Notes mingguan | text bebas | — |

### Aturan agregat mingguan

- Setiap **Senin pagi** sebelum audit (15 menit).
- Snapshot follower & email **dari platform**, bukan estimasi.
- Kalau formula G < 5% atau K < 30% selama 2 minggu berturut -> cek Tab 3 untuk action.

---

## 4. TAB 3 — TRIGGER LOG (struktur)

Kosong di awal. Tambah baris saat Decision Rule terpicu.

| Kol | Nama | Contoh isi |
|---|---|---|
| A | Tanggal trigger | 2026-06-15 |
| B | Rule # | 1 / 2 / 3 / 6 / 7 / 8 |
| C | Observasi (data) | "Engagement avg minggu 1 = 2.1%, minggu 2 = 2.4%. Rule #1 aktif." |
| D | Action diambil | "Ganti hook style 50% — minggu 3 fokus Confession + Question, kurangi Contrarian." |
| E | Tanggal action mulai | 2026-06-16 |
| F | Hasil 7 hari kemudian | "Engagement avg minggu 3 = 4.8%. Rule #1 reset." |
| G | Closed Y/N | Y |
| H | Lessons | "Contrarian saturate audience baru. Rotate." |

### Decision Rules aktif Bulan 1 (rujukan)

| Rule | Kondisi | Action |
|---|---|---|
| #1 | Engagement < 3% selama 2 minggu | Ganti hook style 50% |
| #2 | Follower flat 2 minggu | Audit pillar dominasi |
| #3 | Email opt-in < 2% dari profile visit | Revisi judul lead magnet |
| #6 | Views tinggi + komen rendah | JANGAN ulangi format (viral-trap) |
| #7 | > 30% follower baru ICP-mismatch | Audit hook 2 minggu |
| #8 | 3+ konten "supaya posting" | STOP 3 hari + restart filter ketat |

### Aturan Trigger Log

- **Setiap rule terpicu = 1 baris baru.** Jangan campur 2 trigger di 1 baris.
- **Kolom F (hasil) wajib diisi T+7 hari setelah action.** Reminder kalender.
- **Kalau action gagal mengubah hasil** -> eskalasi ke audit Senin minggu berikutnya, mungkin asumsi underlying salah.

---

## 5. TAB 4 — LEAD MAGNET FUNNEL (struktur)

5 baris (1 per minggu + 1 baris cumulative Day 30). Aktif sejak Lead Magnet live (sekitar Day 7-10).

| Kol | Nama | Sumber | Target Bulan 1 |
|---|---|---|---|
| A | Minggu | 1 / 2 / 3 / 4 / Total | — |
| B | Profile visit (estimasi dari Threads insights) | manual | — |
| C | Klik bio | manual (link bio aggregator stats) | — |
| D | LP visit | manual (LP analytics) | — |
| E | Opt-in count | manual (email tool) | 200 cumul |
| F | Opt-in % (E/D × 100) | formula | >= 5% (target wajar) |
| G | Email Day-1 open rate | manual (email tool) | >= 40% |
| H | Email Day-7 completion (clicked CTA at least 1x) | manual | >= 25% |
| I | Notes | text | — |

### Aturan entry funnel

- Mingguan saja — funnel tidak perlu harian.
- **Decision Rule #3** memantau kolom F: kalau < 2% selama 2 minggu -> revisi judul LP.
- **Email completion rate (H)** baru reliable setelah Minggu 3.

---

## 6. PRE-FILL DATA — SHORTCUT

Untuk menghemat waktu, **copy data dari kalender** ke Tab 1 Daily Posts saat setup:

- Sumber: `CONTENT-CALENDAR-BULAN-1.md` -> section `## MASTER OVERVIEW — 30 HARI`
- Mapping kolom kalender -> tracker:
  - "#" -> A (Day)
  - "Hari" -> C
  - "Slot" -> D
  - "Pillar" -> E
  - "Funnel" -> F
  - "Hook (1 baris)" -> G
  - "CTA" -> H

Kolom B (Tanggal) diisi setelah Day 1 dikonfirmasi. Tambah +1 hari sequential.

---

## 7. OPSIONAL — DASHBOARD VIEW (Tab 5, kalau mau)

**Tidak wajib Bulan 1.** Kalau Anda nyaman dengan Sheets formula, buat tab `Dashboard`:

- Card: Total followers vs target 1.000 (progress bar)
- Card: Email opt-in vs target 200
- Chart line: Engagement weekly trend
- Chart bar: Pillar distribution actual vs target 60/30/10
- Chart bar: Funnel TOFU/MOFU/BOFU distribution

Kalau setup dashboard membuat Anda over-engineer, **skip**. Sheets raw cukup.

---

## 8. AKSES & BACKUP

- **Owner:** Anda saja. Tidak share view/edit ke siapapun Bulan 1.
- **Backup mingguan:** File -> Download -> CSV — simpan di folder `tracker-backup/` lokal Anda. 4 backup di akhir Bulan 1.
- **Mobile:** Install Google Sheets app di HP. Entry malam bisa dari HP — lebih cepat.

---

## 9. ANTI-PATTERN — JANGAN

1. **Refresh tracker > 3x sehari.** Tracker bukan untuk dipantau real-time. Itu anxiety, bukan insight.
2. **Compare per-post di hari yang sama.** Beda hari = beda audience aktif. Compare apple-to-apple = mingguan agregat.
3. **Hapus baris post yang flop.** Itu data paling berharga. Justru highlight kuning.
4. **Tambah kolom baru tiap minggu.** Lock struktur Day 1, freeze Bulan 1, evaluasi Bulan 2.

---

## 10. CHECKLIST SETUP (sebelum Day 1)

- [ ] Google Sheet baru dibuat, nama: `arifb.id Performance Tracker — Bulan 1`
- [ ] 4 tab dibuat dengan kolom sesuai Section 2-5
- [ ] 30 baris Daily Posts pre-filled dari kalender (kolom A-H)
- [ ] 4 baris Weekly Snapshot pre-filled (Minggu 1-4)
- [ ] Tab Trigger Log siap (kolom header saja, isi belum perlu)
- [ ] Tab Lead Magnet Funnel siap (5 baris kosong)
- [ ] Reminder HP 22:00 WIB harian = "Update tracker"
- [ ] Reminder HP Senin 06:30 WIB mingguan = "Weekly snapshot + audit"
- [ ] Bookmark Sheet ini di browser
- [ ] Test entry: isi kolom I-T baris D1 dengan data dummy -> cek formula P (engagement %) jalan -> hapus dummy

---

> **Selesai setup = unblock Day 1.** Tanpa tracker aktif, Day 1 ditunda.
