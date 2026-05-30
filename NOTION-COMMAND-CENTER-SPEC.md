# NOTION COMMAND CENTER — SPEC

> Tempat **review + keputusan + idea capture**. Bukan tempat angka (itu Sheets). Notion = naratif & relasi.
>
> **Wajib pre-Day 1?** TIDAK. Setup Day 8-10 (Week 2). Minggu 1 catat manual di Sheets Trigger Log.

---

## 0. PRINSIP

1. **Notion bukan Sheets.** Sheets = angka. Notion = naratif.
2. **4 database, tidak lebih.** Solo creator gampang over-build Notion.
3. **Template-driven.** Setiap weekly review pakai template fix supaya cepat.
4. **Single workspace, single user.** Tidak share view ke siapapun Bulan 1.

---

## 1. ARSITEKTUR — 4 DATABASE

| Database | Tipe | Frekuensi entry |
|---|---|---|
| **Content Pipeline** | Linked records ke 30 post | Weekly snapshot |
| **Weekly Review** | 1 page per minggu | Setiap Senin pagi |
| **Decision Log** | Audit trail keputusan | Saat keputusan diambil |
| **Idea Capture** | Inbox raw | Bebas, weekly triage |

---

## 2. DATABASE 1 — CONTENT PIPELINE

### Properties

| Property | Tipe | Sumber |
|---|---|---|
| Title | Text | Day# + 1-baris hook (e.g., "D1 — AI Architect Manifesto") |
| Day | Number (1-30) | manual |
| Pillar | Select (P1/P2/P3) | manual |
| Funnel | Select (TOFU/MOFU/BOFU) | manual |
| Status | Select (Draft / Published / Measured / Archived) | manual |
| Slot WIB | Text | manual |
| Link Sheets row | URL (ke baris Tab 1 Tracker) | manual |
| Top komen | Text (1 kalimat highlight) | manual T+24jam |
| Lessons | Text | manual T+24jam |

### View

- **By Status:** kanban — Draft, Published, Measured, Archived
- **By Day:** sorted ASC
- **By Pillar:** filter — cek distribusi 60/30/10

---

## 3. DATABASE 2 — WEEKLY REVIEW

> 1 page per minggu (Minggu 1-4). Template mandatory.

### Template page

```
# Weekly Review — Minggu [N] (Day [X]-[X+6])

## Snapshot Numbers (dari Sheets Tab 2)
- Followers cumulative: ___
- Email opt-in cumulative: ___
- Engagement avg: ___%
- Top post Day#: ___ (___K views)

## Audit Asosiasi (5 pertanyaan §14.2)
1. Slip akun landmine? Y/N — note: ___
2. Voice slip? Y/N — note: ___
3. Undangan kolab masuk? — protokol 4-cek pass? ___
4. Follower mismatch? %___ — action: ___
5. Tergoda hype-language? Y/N — note: ___

## Refleksi Theoderic (4 pertanyaan §16.2)
1. Purpose check — sesuai BJM Q1? Y/N — note: ___
2. Strength check — pakai strength sendiri atau meniru? ___
3. Quality of growth — audience akan beli 6 bulan lagi? Y/N — ___
4. Anti-erosion — moment tergoda? Trigger: ___

## Decision Rules Triggered (link ke Sheets Tab 3)
- [ ] Rule #1 — engagement <3% — action: ___
- [ ] Rule #2 — follower flat — action: ___
- [ ] (dst — kalau aktif)

## Top 3 Post Minggu Ini
1. D__ — judul — alasan: ___
2. D__ — judul — alasan: ___
3. D__ — judul — alasan: ___

## Bottom 1 Post Minggu Ini
- D__ — judul — diagnosis: voice slip / topik mismatch / hook lemah / format salah

## Aksi Minggu Depan
1. ___
2. ___
3. ___
```

### Aturan Weekly Review

- Senin pagi 06:30 — 15-20 menit
- Snapshot numbers **copy dari Sheets**, jangan re-hitung
- Aksi minggu depan max 3 — kalau lebih, prioritas lemah

---

## 4. DATABASE 3 — DECISION LOG

> Audit trail keputusan. Setiap pivot, ganti hook, geser slot, drop format = 1 entry.

### Properties

| Property | Tipe |
|---|---|
| Title | Text (ringkas, e.g., "Ganti hook Contrarian -> Confession Minggu 3") |
| Tanggal | Date |
| Konteks | Long text (apa yang ter-observe) |
| Opsi yang dipertimbangkan | Long text (2-3 opsi) |
| Pilihan | Text (1 baris) |
| Alasan | Long text |
| Trigger Rule # | Select (1, 2, 3, 6, 7, 8, custom) |
| Hasil 30 hari | Long text (diisi T+30 hari) |
| Status | Select (Active / Closed / Reverted) |

### Aturan

- **1 keputusan = 1 entry.** Tidak menggabung.
- **Hasil 30 hari wajib diisi.** Reminder kalender.
- **Reverted entries tetap disimpan.** Pelajaran dari pivot yang gagal sama berharganya.

---

## 5. DATABASE 4 — IDEA CAPTURE

> Inbox raw. Tanpa filter. Weekly triage ke Content Pipeline.

### Properties

| Property | Tipe |
|---|---|
| Title | Text (1 baris, raw thought) |
| Source | Select (Komen Threads / DM / Buku / Filsafat / Klien / Lainnya) |
| Tanggal capture | Date (auto) |
| Pillar potensial | Select (P1/P2/P3/Belum tahu) |
| Hook potensial | Text (kalau sudah punya) |
| Status | Select (Inbox / Triage / Promoted to Pipeline / Discarded) |

### Aturan triage mingguan (5 menit Senin)

- Buka filter Status = Inbox
- Per ide: Promote (ke Content Pipeline) / Discard / Stay (cukup matang belum)
- **Aturan 30 hari:** kalau ide tetap "Stay" 30 hari -> auto Discard. Pattern muncul: kalau tidak tergerak 30 hari, tidak akan tergerak.

---

## 6. WORKFLOW HARIAN — TIPIS

| Kapan | Aksi Notion |
|---|---|
| Pagi | (tidak ada) |
| Saat ide muncul | 1-tap ke Idea Capture (mobile app) |
| Malam (setelah Sheets) | Update status post hari ini di Content Pipeline |
| Senin 06:30 | Weekly Review entry baru (15-20 menit) |
| Saat keputusan | Decision Log entry |

---

## 7. SETUP CHECKLIST (Day 8-10)

- [ ] Notion workspace baru: `arifb.id Command Center`
- [ ] 4 database dibuat dengan properties di atas
- [ ] Weekly Review template page disimpan
- [ ] Content Pipeline pre-fill dengan 30 entry dari kalender (link ke Sheets)
- [ ] Mobile app install + login
- [ ] Test entry ke Idea Capture dari mobile

---

## 8. ANTI-PATTERN

1. **Database ke-5 atau ke-6.** Lock 4. Bulan 2 evaluasi.
2. **Notion sebagai tempat tracker angka.** Sheets jauh lebih cepat untuk angka.
3. **Sub-page hierarchy 3 level.** Maksimal 2 level (database -> entry).
4. **Public share.** Bulan 1 internal saja.

---

> **Notion adalah tempat berpikir, bukan tempat ribet.** Kalau setup > 2 jam, simplify.
