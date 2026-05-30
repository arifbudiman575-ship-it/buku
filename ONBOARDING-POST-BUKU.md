# ONBOARDING POST-BUKU — Email Sequence Pasca-Pembelian

> **Filosofi:** Onboarding pasca-pembelian = **trust deepening, BUKAN upsell agresif**. Pembeli sudah membayar (high intent), tapi belum tentu sudah baca + apply. Sequence ini memastikan delivery → consumption → result → trust → siap untuk tier berikutnya secara natural.
>
> **SACRED rule:** Email post-buku WAJIB dipisah dari email lead magnet nurture. Buyer ≠ subscriber lead magnet. Tag MailerLite + automation terpisah.

---

## 1. SEQUENCE MAP — DAY 0 → DAY 30

| Email | Trigger | Subjek (draft) | Tujuan utama | Cross-sell? |
|---|---|---|---|---|
| **B0** Welcome | Instan pasca-pembayaran | "Buku Anda siap — link akses di sini" | Delivery + welcome | Tidak |
| **B+2** Maximize | +48 jam | "Cara membaca THE AI ARCHITECT (3 mode)" | How-to guide | Tidak |
| **B+7** Check-in | +7 hari | "Bagaimana progress Bab 1-3 Anda?" | Engagement check + 1 question | Tidak |
| **B+14** Win-share | +14 hari | "Apa yang berubah setelah 2 minggu?" | Testimony invite + filter positif | Soft (cohort waitlist hint) |
| **B+21** Soft pitch cohort | +21 hari | "Kalau Anda siap untuk implementasi yang lebih mendalam..." | Cross-sell BOFU cohort waitlist | Soft |
| **B+30** Milestone | +30 hari | "30 hari bersama THE AI ARCHITECT — refleksi" | Milestone + refund window closing reminder | Tidak |

**Total: 6 email** dalam 30 hari. Setelah itu, buyer pindah ke segment regular newsletter (1-2x per minggu, sama dengan subscriber lead magnet completer).

---

## 2. MAILERLITE TAG LOGIC

### 2.1 Tag entry post-pembayaran

Trigger Lynk.id webhook → MailerLite → assign tag berdasarkan tier:

| Tier dibeli | Tag MailerLite | Automation yang dijalankan |
|---|---|---|
| Buku Standard (Rp 297K) | `buyer-buku-standard` | Onboarding sequence B0-B30 (varian standard) |
| Buku Plus (Rp 547K) | `buyer-buku-plus` | Onboarding sequence + bonus modul access |
| Buku Premium (Rp 897K) | `buyer-buku-premium` | Onboarding sequence + 30-min konsultasi scheduler |

### 2.2 Tag transition

| Trigger | From tag | To tag |
|---|---|---|
| Beli buku tier apapun | `subscriber-active` (kalau ada) | `buyer-buku-{tier}` (additional, bukan replace) |
| Email B0 sent | `buyer-buku-{tier}` | + `onboarding-day0` |
| Email B+7 click rate >50% | `onboarding-engaged` | + `engaged-reader` |
| Email B+14 reply with testimony | `onboarding-engaged` | + `testimony-positive-candidate` |
| Email B+21 click cohort waitlist link | — | + `cohort-waitlist-warm-from-buku` |
| Refund 30-hari | `buyer-buku-{tier}` | swap to `buyer-refunded` |
| Day 30 reach without unsubscribe | `onboarding-day0` removed | promoted to `buyer-converted-30day` |

### 2.3 Branch logic (penting)

**IF buyer juga subscriber lead magnet (`subscriber-7day`):**
- Pause email sequence lead magnet (Day 8+ nurture) saat onboarding aktif
- Resume sequence lead magnet pasca-Day-30 (kalau buyer tidak naik ke cohort)

**IF buyer refund di window:**
- Stop semua onboarding email immediately (B+N yang belum kirim)
- Kirim 1 closing email (refund confirmation, sudah ada di REFUND-SAVING-SCRIPT.md)
- Tag swap, subscriber tetap aktif di list (bukan auto-unsubscribe)

**IF buyer beli cohort di tengah onboarding (mis. di B+14):**
- Stop sisa email onboarding buku
- Pindah ke onboarding cohort (terpisah, scope lain)

---

## 3. EMAIL TEMPLATES

### 3.1 Email B0 — Welcome + Delivery (instan)

**Trigger:** Lynk.id status PAID → MailerLite tag `buyer-buku-{tier}`
**Send time:** Instan (otomatis)
**Subjek:** Buku Anda siap — link akses di sini

```
Halo {NAMA},

Selamat datang. Pembelian buku THE AI ARCHITECT (tier {TIER}) Anda
sudah saya konfirmasi. Berikut yang Anda dapatkan:

[Buku digital PDF]
{LINK-PDF-BUKU}

[Bonus material — kalau Anda beli tier Plus atau Premium]
{LINK-BONUS-MATERIAL atau "Tidak applicable untuk tier Anda"}

[Sesi konsultasi 30-menit — Premium only]
{LINK-CALENDLY-SCHEDULER atau "Tidak applicable untuk tier Anda"}

—

3 hal yang saya ingin Anda lakukan SEBELUM mulai baca:

1. Save link akses di tempat aman — link tetap valid selama Anda
   pemilik buku
2. Buka PDF di device yang nyaman untuk membaca panjang (tablet/laptop
   lebih recommended dari phone untuk mode deep reading)
3. Block 90 menit untuk Bab 1 — itu pondasi untuk semua bab setelahnya

Saya akan kirim panduan "cara membaca buku ini" dalam 2 hari ke depan,
plus check-in singkat di hari ke-7 dan 14.

Pertanyaan apapun: balas email ini langsung. Saya yang baca, bukan tim.

Selamat membaca.

Arif Budiman
the AI Architect
@arifb.id

P.S. — Refund window 30 hari berlaku tanpa pertanyaan. Kalau di
tengah jalan Anda merasa buku ini tidak cocok, kirim email balasan
ini dengan subjek "Refund Buku" + ID transaksi {ID-TRX} dan saya
proses dalam 7 hari kerja. Tidak akan saya tanya alasan.
```

### 3.2 Email B+2 — Cara Membaca (3 Mode)

**Trigger:** 48 jam pasca-Email B0
**Subjek:** Cara membaca THE AI ARCHITECT (3 mode)

```
Halo {NAMA},

Buku THE AI ARCHITECT bukan buku yang sebaiknya dibaca cover-to-cover
secara linear. Ada 3 mode membaca yang saya rekomendasi:

—

Mode 1: SCAN (90 menit, hari ke-1)

Tujuan: dapat peta utuh sebelum dive deep.
- Baca daftar isi + Prolog + Bab 1 sampai selesai
- Skim Bab 2-7 cukup baca subjudul + bullet point
- Baca Penutup (Bab terakhir)
- Catat 3 framework yang paling resonate untuk Anda

Output: tahu mana bab yang prioritas re-read.

—

Mode 2: DEEP (per bab, 60-90 menit per sesi)

Tujuan: master 1 framework sebelum lanjut.
- Pilih bab yang paling resonate dari Mode 1
- Baca 1 bab penuh + lakukan 1 latihan praktis di akhir bab
- Tunggu 24 jam, lalu refleksi: apa yang berubah dari pemahaman
  Anda sebelum dan sesudah?
- Lanjut ke bab prioritas berikutnya

Output: 1 framework benar-benar Anda kuasai per minggu.

—

Mode 3: APPLY (saat menghadapi case real)

Tujuan: buku jadi reference, bukan teori.
- Saat Anda menghadapi proyek nyata yang butuh struktur AI
- Buka bab yang relevan (misalnya: brief klien yang tidak jelas →
  Bab tentang A.R.S.I. step "Asses")
- Pakai framework langsung di proyek itu
- Catat hasil + adjustment yang Anda lakukan

Output: framework Anda internalisasi melalui pengalaman.

—

Saran saya: Mode 1 minggu ini, Mode 2 minggu depan, Mode 3 saat real
case muncul. Jangan loncat ke Mode 3 tanpa Mode 1.

Pertanyaan tentang bab tertentu: balas email ini.

Arif

P.S. — Kalau Anda sudah selesai Mode 1 dan butuh diskusi 1-on-1
tentang prioritas bab Anda (khusus pembeli tier Premium), reply
email ini untuk schedule sesi 30-menit Anda.
```

### 3.3 Email B+7 — Check-in + 1 Question

**Trigger:** 7 hari pasca-Email B0
**Subjek:** Bagaimana progress Bab 1-3 Anda?

```
Halo {NAMA},

Sudah seminggu sejak Anda dapat akses buku THE AI ARCHITECT.

Saya tidak akan tanya panjang — cukup 1 pertanyaan:

Mana 1 framework dari Bab 1-3 yang paling resonate untuk Anda?

(Boleh balas dengan 1-2 kalimat, atau bahkan cukup nama framework-nya
saja — saya yang baca.)

Alasan saya tanya: itu jadi sinyal apa yang akan saya tulis lebih
dalam di edisi/produk berikutnya. Insights dari pembaca minggu pertama
adalah fondasi terbaik untuk perbaikan.

—

Plus, kalau Anda stuck di mana pun:
- Tidak punya waktu baca? Lakukan Mode 1 (90 menit) di weekend.
- Ide-ide yang belum sambung? Wajar. Tunggu sampai Bab 5, biasanya
  semua jadi terangkai di sana.
- Tidak relate dengan use case di buku? Coba pilih 1 dari 347 prompt
  appendix dan eksekusi 1 saja minggu ini.

Bisa balas, bisa tidak. Sama-sama ok.

Arif
```

### 3.4 Email B+14 — Win-share Invite

**Trigger:** 14 hari pasca-Email B0
**Subjek:** Apa yang berubah setelah 2 minggu?

```
Halo {NAMA},

2 minggu sejak Anda dapat akses buku.

Pertanyaan kali ini lebih spesifik:

Apa SATU hasil konkret yang Anda rasakan setelah apply framework
dari buku ini? (Bisa kecil — "saya jadi tahu cara struktur prompt
yang dulu random", "saya hemat 2 jam per minggu di task X", "saya
bisa lebih percaya diri pitch klien tentang AI integration".)

Kalau Anda izinkan, saya mau gunakan jawaban Anda (boleh anonim
boleh tidak) sebagai testimoni untuk pembaca berikutnya. Format:
"Setelah membaca THE AI ARCHITECT, [hasil Anda]" — {NAMA atau
inisial}.

Kenapa saya tanya:
1. Buku tanpa testimoni = pembaca berikutnya susah trust
2. Testimoni dari pembaca yang baru 2 minggu = paling jujur,
   belum di-polish hindsight bias
3. Saya bisa kasih Anda preview akses awal ke produk berikutnya
   sebagai apresiasi (cohort waitlist priority, atau template
   gratis dari edisi 2.0)

Format respon:
- Mau share + nama lengkap → reply dengan kalimat testimoni Anda
- Mau share + inisial saja → reply dengan inisial yang Anda mau
- Tidak mau share, tapi punya feedback internal → reply, tetap
  saya hargai
- Belum ada hasil konkret → wajar, lanjut baca, saya cek lagi
  di week 4

Apapun jawaban Anda, terima kasih sudah memberi buku ini kesempatan.

Arif
```

### 3.5 Email B+21 — Soft Cross-sell Cohort

**Trigger:** 21 hari pasca-Email B0
**Subjek:** Kalau Anda siap untuk implementasi yang lebih mendalam...

```
Halo {NAMA},

3 minggu Anda bersama THE AI ARCHITECT.

Saya tidak akan pitch panjang. Cukup observasi saya:

Pembaca yang dapat hasil paling besar dari buku ini biasanya
mengalami 1 dari 2 hal di week 3-4:

(A) Sudah apply 2-3 framework sukses → mau struktur yang lebih
    complete + accountability → siap untuk format cohort

(B) Apply tapi stuck di implementation gap → butuh feedback
    real-time + peer learning → siap untuk format cohort

Kalau Anda ada di salah satu posisi di atas:

—

Cohort A.R.S.I. — 8 minggu, 16 sesi live
Format yang complement buku, bukan repeat:
- Buku = framework + theory
- Cohort = implementation + case work + peer feedback
- Bukan "lebih banyak konten" — tapi "kerja sama orang yang sama
  fasenya dengan Anda"

Schedule launch berikutnya: {QUARTER atau "Mgg 11 sesi sekarang"}

Tier:
- ARSITEK (Rp 4,9JT) — full cohort, 16 sesi grup, recording, komunitas
- ARSITEK PLUS (Rp 7,5JT) — ARSITEK + 4 sesi 1-on-1 (60 menit per sesi)

Cap 20 peserta per cohort.

—

Kalau Anda berminat join waitlist (no commitment, hanya untuk dapat
notifikasi pertama saat enrollment buka):

{LINK-COHORT-WAITLIST-LYNK-ID}

Atau cukup balas email ini dengan "Tertarik cohort" — saya add manual.

Kalau belum siap atau tidak relevan: tidak masalah. Buku saja sudah
cukup untuk banyak pembaca. Anda yang paling tahu fase Anda sekarang.

Arif

P.S. — Buku tetap bisa dilanjutkan tanpa cohort. Ini option, bukan
"upgrade path wajib". Banyak pembaca yang dapat semua hasil dari
buku saja.
```

### 3.6 Email B+30 — Milestone + Refund Window Closing

**Trigger:** 30 hari pasca-Email B0
**Subjek:** 30 hari bersama THE AI ARCHITECT — refleksi

```
Halo {NAMA},

Hari ini genap 30 hari sejak Anda akses buku THE AI ARCHITECT.

Dua hal yang saya ingin Anda tahu:

—

1. Refund window 30-hari berakhir hari ini.

Kalau Anda sudah baca penuh dan merasa buku ini tidak cocok untuk
Anda, balas email ini sebelum tengah malam (subjek "Refund Buku"
+ ID transaksi {ID-TRX}) dan saya proses tanpa pertanyaan.

Kalau email ini lewat tanpa balasan, refund window otomatis tutup
dan buku jadi milik Anda permanen.

—

2. Refleksi singkat (boleh dijawab boleh tidak):

Apa SATU hal yang akan Anda bawa dari buku ini ke 30 hari ke depan?

Boleh framework (mis. "A.R.S.I. step Refine"), boleh prinsip (mis.
"selalu validate prompt sebelum scale"), atau boleh shift cara pikir
(mis. "berhenti kejar tools, kejar systems").

Jawaban Anda saya simpan untuk:
- Kalau Anda kasih izin → testimoni untuk pembaca berikutnya
- Insights untuk roadmap edisi 2.0 atau cohort berikutnya
- Personal arsip — saya seneng tahu apa yang resonate dari buku saya

—

Mulai minggu depan, Anda akan masuk ke segment newsletter regular
(1-2 email per minggu) dengan content baru yang tidak ada di buku.
Kalau prefer pause atau unsubscribe, link unsubscribe selalu di
footer email saya.

Terima kasih sudah membersamai 30 hari pertama bersama THE AI ARCHITECT.

Arif
```

---

## 4. ANTI-PATTERN

### 4.1 Yang TIDAK BOLEH dilakukan di onboarding

1. **Auto-bombard >2 email per minggu** — overwhelm pembaca, brand jadi spammy
2. **Pitch cohort di B0 atau B+2** — terlalu cepat, trust belum dibangun
3. **Mengisolasi refund reminder** (mis. baru kasih tahu di B+30 saja) — harus disebut sejak B0 untuk transparency
4. **Discount cohort dari onboarding sequence** — pelanggaran SACRED rule anti-discount
5. **Ask testimoni di B+2** — terlalu cepat, pembeli belum baca/apply
6. **Email otomatis tanpa personalisasi `{NAMA}`** — formal tapi kosong
7. **Cross-promote produk eksternal** (affiliate / sponsor) di onboarding — onboarding window = bonding window, bukan revenue grab
8. **Skip Email B0 instan** — pembeli wajib dapat link akses dalam <5 menit pasca-pembayaran

### 4.2 Yang BOLEH (gentle)

1. Mention cohort sekali di B+21 (post 3-week trust)
2. Invite testimony di B+14 dengan opt-in eksplisit + filter positif
3. Ask 1 question per email (B+7 dan B+14) untuk engagement signal
4. Refund window reminder di B0 + B+30 (transparency)
5. Personalisasi `{NAMA}` + tier dibeli + tanggal transaksi

---

## 5. METRIC TARGETS (90-day window evaluation)

| Metric | Target sehat | Action kalau di bawah target |
|---|---|---|
| Email B0 open rate | >70% | Cek delivery — kemungkinan masuk spam |
| Email B+7 reply rate | >5% | Re-write subjek B+7 untuk lebih engaging |
| Email B+14 testimony submit rate | >10% | Re-frame ask, kurangi friction |
| Email B+21 cohort waitlist click rate | >8% | Cek timing relevance + soft pitch tone |
| Email B+30 open rate | >50% | Cek list hygiene — buyer mungkin sudah disengage |
| 30-day refund rate | <5% | Audit fit issue: targeting? content gap? expectation mismatch? |
| 90-day cohort conversion (buyer → cohort) | >3% | Audit cross-sell trigger + cohort offer fit |

---

## 6. ANCHOR & CROSS-REFERENCE

- `LAUNCH-PACK-BUKU.md` Section 5 — Onboarding spec master (kalau sudah ada di file ini)
- `EMAIL-SEQUENCE-7-DAY-CHALLENGE.md` — Email template style + voice reference
- `EMAIL-NURTURE-DAY8-PLUS.md` — Email post-lead-magnet (paralel sequence)
- `MAILERLITE-AUTOMATION-BRIEF.md` — Tag logic + automation setup
- `LAUNCH-PACK-COHORT.md` Section 3 — Cohort offer detail untuk Email B+21
- `REFUND-SAVING-SCRIPT.md` — Refund response untuk klaim di window
- `STRATEGY-REFRESH-PROTOCOL.md` — Quarterly review onboarding metrics

---

*Versi 1.0. Email templates di atas adalah starting point — saat A/B test aktif (Bulan 2+ baseline ready), variasi subjek/body bisa di-test. SACRED rule no-spam (max 2 email/minggu) + no-aggressive-upsell + refund-transparency tidak bisa dimodifikasi tanpa quarterly review.*
