# REFUND SAVING SCRIPT — Response SOP untuk Refund Request

> **Filosofi:** "Saving" di sini = **saving the learning**, BUKAN saving the sale. SACRED rule: refund window approve **tanpa argumen, tanpa pressure, tanpa delay**. Dialog 1-round adalah opsional invite feedback untuk product improvement — bukan upaya cegah refund.
>
> **Voice:** formal "Anda", tenang, professional, tidak defensif. Same voice seperti email nurture + reply farm.

---

## 1. FILOSOFI & SACRED RULE

### 1.1 SACRED — refund window = APPROVE tanpa pertanyaan

| Tier produk | Window | Sacred behavior |
|---|---|---|
| Buku digital | 30 hari kalender | No-question, approve dalam 7 hari kerja |
| Cohort A.R.S.I. | 7 hari kalender pasca-sesi-1 | No-question, approve dalam 14 hari kerja |
| Corporate audit | Pre-kickoff only | 100% pre-kickoff, 50% kalau notice <7 hari, NO post-kickoff |

**Aturan utama:** Kalau pelanggan minta refund dalam window, **JANGAN minta justifikasi**. Approve, proses, selesai. Itu bagian dari brand trust premium.

### 1.2 Dialog 1-round = LEARNING ASK, bukan SAVE ATTEMPT

Setelah konfirmasi approve, **boleh tambahkan 1 pertanyaan opsional** untuk feedback. Tapi:
- JANGAN minta jawaban sebelum approve
- JANGAN gunakan untuk cegah refund
- JANGAN follow-up kalau tidak dijawab
- Posisikan sebagai "membantu kami untuk produk berikutnya"

### 1.3 Anti-pattern — yang tidak boleh dilakukan

1. **Begging** — "Mohon dipertimbangkan ulang", "Apakah yakin?", "Kami sangat menghargai Anda"
2. **Defensive** — "Tapi Anda belum baca semuanya", "Banyak yang sukses dengan buku ini"
3. **Delay tactic** — "Tunggu dulu, mari kita diskusi", "Bisakah kita meeting 15 menit?"
4. **Guilt trip** — "Sayang sekali Anda menyerah", "Padahal hasilnya bagus untuk yang konsisten"
5. **Conditional refund** — "OK refund tapi tolong unsubscribe juga", "Refund tapi share testimoni dulu"

Setiap anti-pattern di atas = pelanggaran trust + brand damage. Refund cepat = trust win jangka panjang.

---

## 2. SCENARIO A — REFUND BUKU DIGITAL (30-HARI WINDOW)

### 2.1 Kondisi & approval

- Klaim dalam 30 hari kalender sejak transaksi
- Konfirmasi pembayaran via Lynk.id
- APPROVE — proses ke Lynk.id refund dalam 7 hari kerja

### 2.2 Email response template (langsung approve)

**Subjek:** Refund Buku THE AI ARCHITECT — Approved

```
Halo {NAMA},

Terima kasih atas pemberitahuan Anda. Refund untuk pembelian buku
THE AI ARCHITECT (transaksi {ID-TRX}, tier {TIER}, tanggal {TANGGAL})
telah saya approve.

Detail proses:
- Pengembalian dana: ke metode pembayaran original via Lynk.id
- Estimasi cair: 3-7 hari kerja (tergantung bank/e-wallet Anda)
- Potongan biaya admin Lynk.id: ~3-5% (sesuai kebijakan platform)
- Akses buku PDF + bonus material: dicabut hari ini

Saya akan kirim konfirmasi tracking refund ke email ini begitu
pemrosesan di Lynk.id selesai.

Apakah ada satu hal spesifik yang membuat buku ini tidak cocok
untuk Anda? Jawaban Anda murni untuk membantu saya menyempurnakan
edisi/produk berikutnya — tidak akan mempengaruhi proses refund
yang sudah jalan.

(Tidak perlu balas kalau tidak nyaman.)

Terima kasih sudah memberi kesempatan pada buku ini.

Hormat,
Arif Budiman
the AI Architect
```

### 2.3 WhatsApp response template (kalau klaim via WA)

```
Halo {NAMA}, terima kasih atas info-nya. Refund buku THE AI ARCHITECT
sudah saya approve. Pengembalian dana via Lynk.id ke metode pembayaran
original, estimasi 3-7 hari kerja. Akses PDF dicabut hari ini.

Boleh saya tanya satu hal untuk perbaikan produk berikutnya:
apa yang membuat buku ini tidak cocok untuk Anda saat ini?
(Murni feedback, tidak mempengaruhi refund yang sudah jalan.)

Tidak perlu jawab kalau tidak nyaman. Terima kasih sudah memberi
kesempatan pada buku ini.
```

### 2.4 Internal action items

1. **Email/WA respons** dalam 24 jam (target: < 4 jam pada jam kerja)
2. **Login Lynk.id dashboard** → Transactions → cari ID-TRX → Initiate Refund
3. **Update Notion DB** Funnel: status pelanggan → "refunded", note tanggal + alasan (kalau dijawab)
4. **Cabut akses MailerLite tag**: `buyer-buku-active` → `buyer-buku-refunded`
5. **Subscriber tetap aktif** di email list (kecuali user explicit unsubscribe — refund ≠ unsubscribe)
6. **Forward feedback** (kalau ada) ke retro template untuk learning batch

---

## 3. SCENARIO B — REFUND COHORT A.R.S.I. (7-HARI POST-SESI-1)

### 3.1 Kondisi & approval

- Klaim dalam 7 hari kalender sejak sesi-1 cohort dimulai
- APPROVE — proses dalam 14 hari kerja
- Sesi 1-on-1 (untuk tier ARSITEK PLUS) yang sudah dilaksanakan tidak dapat di-undo, tapi nilai pro-rata tetap di-refund penuh

### 3.2 Email response template

**Subjek:** Refund Cohort A.R.S.I. — Approved

```
Halo {NAMA},

Terima kasih atas pemberitahuan Anda. Refund partisipasi cohort
A.R.S.I. (tier {TIER ARSITEK / ARSITEK PLUS}, transaksi {ID-TRX})
telah saya approve.

Detail proses:
- Pengembalian dana: 100% nilai tier (Rp {NOMINAL})
- Estimasi cair: 7-14 hari kerja via Lynk.id
- Akses cohort: dicabut efektif hari ini (modul, recording, komunitas)
- Sesi 1-on-1 yang sudah berlangsung: tetap valid sebagai sumber belajar
  Anda secara pribadi, namun saya tidak akan menjadwalkan sesi
  selanjutnya
- Status komunitas alumni: hak akses sebagai alumni dicabut

Saya tidak akan ajukan pertanyaan apapun untuk justifikasi keputusan
Anda — itu hak Anda sepenuhnya.

Apakah ada satu masukan untuk format cohort ke depan? Boleh dijawab
boleh tidak — tidak mempengaruhi refund.

Terima kasih atas keputusan dan keterbukaan Anda.

Hormat,
Arif Budiman
the AI Architect
```

### 3.3 Internal action items

1. **Email respons** dalam 24 jam
2. **Lynk.id refund** initiate (lebih besar nominal — verify Lynk.id Pro fee handling)
3. **Update Notion DB** Cohort: status peserta → "refunded D+{N}", note sesi yang sudah diikuti
4. **Cabut akses cohort platform** (Zoom recurring, Google Drive recording, WhatsApp komunitas)
5. **MailerLite tag**: `cohort-arsi-active` → `cohort-arsi-refunded`
6. **Cohort retro log** — tambah ke retrospective template untuk Q1 refresh

### 3.4 Sacred reminder

**Cohort anti-discount selamanya.** Kalau pelanggan minta diskon sebagai alternatif refund: TOLAK halus. Refund full atau lanjut full price — tidak ada middle ground.

---

## 4. SCENARIO C — REFUND CORPORATE AUDIT

### 4.1 Pre-kickoff (BELUM ada sesi pertama)

- Notice ≥7 hari sebelum kickoff: refund 100%
- Notice <7 hari sebelum kickoff: refund 50% (cover allocated calendar/prep cost)

### 4.2 Post-kickoff

- NO refund. Engagement dianggap dimulai. Pembayaran 50% sisa tetap kewajiban kontrak.
- Kalau klien menghentikan engagement: deliverable yang sudah selesai = milik klien. Sisa scope tidak dikerjakan.

### 4.3 Email response template (PRE-KICKOFF, refund 100%)

**Subjek:** Pembatalan Engagement Corporate Audit — Refund 100%

```
Yth. {NAMA-PIC},

Terima kasih atas konfirmasi pembatalan engagement {SCOPE}
({SMALL Rp 25JT / MEDIUM Rp 50JT / LARGE Rp 100JT}) sebelum
jadwal kickoff ({TANGGAL-KICKOFF}).

Karena pemberitahuan diterima ≥7 hari sebelum kickoff, refund
100% akan diproses sesuai kontrak:
- Pengembalian dana: Rp {NOMINAL-50%-PERTAMA}
- Estimasi cair: 14 hari kerja (transfer bank korporat, sesuai
  prosedur compliance)
- Tidak ada biaya pembatalan

Saya akan kirim invoice retur + bukti transfer ke email PIC dalam
2 hari kerja setelah dana ditransfer.

Apakah pembatalan ini berarti ada kebutuhan yang berubah, atau
saya bisa membantu di lain waktu? Boleh dijawab atau tidak.

Saya menghormati keputusan Anda dan tetap terbuka untuk
engagement di masa depan.

Hormat,
Arif Budiman
the AI Architect
```

### 4.4 Email response template (PRE-KICKOFF, notice <7 hari, refund 50%)

**Subjek:** Pembatalan Engagement — Refund 50% sesuai Kontrak

```
Yth. {NAMA-PIC},

Terima kasih atas konfirmasi pembatalan engagement {SCOPE}
yang dijadwalkan kickoff {TANGGAL-KICKOFF}.

Karena pemberitahuan diterima dalam window <7 hari sebelum kickoff,
sesuai pasal kontrak Section 7.3 ToS:
- Refund yang berhak: 50% dari pembayaran 50% pertama
  yaitu Rp {NOMINAL-25%-DARI-FULL}
- Sisa 25% (dari pembayaran pertama) menjadi cancellation fee
  untuk menutup biaya allocated (calendar block, prep
  research, dokumen scoping)
- Estimasi cair: 14 hari kerja

Saya tetap menyiapkan dokumen prep yang sudah selesai (kalau ada)
sebagai goodwill — siap dikirim setelah refund ter-proses.

Hormat,
Arif Budiman
the AI Architect
```

### 4.5 Email response template (POST-KICKOFF, NO refund)

**Subjek:** Konfirmasi Permintaan Penghentian Engagement

```
Yth. {NAMA-PIC},

Terima kasih atas pemberitahuan Anda terkait keinginan menghentikan
engagement {SCOPE} yang sudah dimulai.

Sesuai Section 7.3 ToS dan kontrak yang ditandatangani, engagement
yang sudah kickoff tidak memiliki provisi refund. Berikut yang akan
saya lakukan untuk memastikan transisi yang adil:

1. Deliverable yang sudah selesai/dalam progres saat ini akan saya
   finalisasi dan serahkan ke pihak Anda dalam 7 hari kerja
   ({LIST-DELIVERABLE-SUDAH-SELESAI})
2. Sesi advisory yang sudah dijadwalkan dalam 7 hari ke depan akan
   saya tetap deliverkan kalau diinginkan, atau di-skip kalau tidak
3. Pembayaran 50% sisa yang sesuai kontrak: tetap menjadi kewajiban
   sesuai jadwal yang disepakati

Apakah Anda ingin kita atur sesi closure 30 menit untuk membahas
alasan penghentian + handover deliverable? Tidak wajib, tapi saya
siapkan kalau diperlukan untuk dokumentasi internal pihak Anda.

Hormat,
Arif Budiman
the AI Architect
```

### 4.6 Internal action items (Corporate)

1. **Email respons** dalam 48 jam (slot waktu corporate biasanya lebih lambat)
2. **Update kontrak status** di Notion DB Corporate: pre-cancel / cancelled-with-deliverable
3. **Invoice retur** untuk refund (kalau applicable)
4. **Delivery handover dokumen** sesuai komitmen di email
5. **Update LinkedIn relationship status** PIC: "former engagement, friendly" — tetap warm untuk masa depan

---

## 5. POST-REFUND LEARNING RETRO

### 5.1 Template log (Notion atau Sheets)

| Field | Isi |
|---|---|
| Tanggal refund | {YYYY-MM-DD} |
| Tier produk | Buku Standard/Plus/Premium / Cohort ARSITEK/PLUS / Corporate Small/Medium/Large |
| ID transaksi | {LYNK-ID-TRX} |
| Window day saat klaim | {N hari sejak transaksi/sesi-1} |
| Nominal refund | Rp {N} |
| Alasan (kalau dijawab) | {free text} |
| Kategori alasan | Konten tidak cocok / Format salah / Timing salah / Beli ulang / Tidak ada waktu / Tidak puas / Other |
| Action item produk berikutnya | {kalau ada pelajaran konkret} |
| Status follow-up | Selesai / Pending |

### 5.2 Quarterly review trigger

Setiap akhir Q1 / Q2 / Q3 / Q4, jalankan review:
- **Refund rate per tier** — target sehat <5% buku, <10% cohort
- **Top 3 alasan** — kalau ada pattern, action item ke STRATEGY-REFRESH-PROTOCOL.md
- **Window distribution** — rata-rata refund di hari ke berapa? Awal/tengah/akhir window?
- **Cross-tier signal** — pelanggan refund buku yang juga ada di waitlist cohort: kemungkinan perlu re-segment

Anchor: `STRATEGY-REFRESH-PROTOCOL.md` Section refund analysis + `BULAN-1-TACTICAL-PLAN.md` weekly checkpoint.

---

## 6. PROCESSING CHECKLIST (PRINTABLE)

### Refund buku (per kasus, ~15 menit)

- [ ] Email/WA respons dalam 24 jam pakai template Section 2.2 atau 2.3
- [ ] Lynk.id Dashboard → cari ID-TRX → Initiate Refund
- [ ] Notion DB Funnel update status: refunded
- [ ] MailerLite tag swap: buyer-active → buyer-refunded
- [ ] Cabut akses link buku PDF (kalau pakai protected hosting; kalau native MailerLite delivery, tag swap sudah cukup)
- [ ] Kirim email konfirmasi tracking refund kalau Lynk.id sudah cair
- [ ] Log retro template Section 5.1

### Refund cohort (per kasus, ~30 menit)

- [ ] Email respons dalam 24 jam pakai template Section 3.2
- [ ] Lynk.id Dashboard refund (verify nominal sesuai tier)
- [ ] Cabut akses Zoom recurring + Google Drive recording + WA grup
- [ ] Update Notion DB Cohort: status peserta refunded, log sesi yang sudah diikuti
- [ ] MailerLite tag swap: cohort-active → cohort-refunded
- [ ] Cohort retro log entry
- [ ] Email konfirmasi tracking refund saat cair

### Refund corporate (per kasus, ~60 menit)

- [ ] Email respons dalam 48 jam pakai template Section 4.3-4.5 (sesuai kondisi)
- [ ] Update kontrak status di dokumen kontrak fisik/digital
- [ ] Invoice retur (pakai Notion template kontrak corporate kalau ada)
- [ ] Transfer refund manual via bank (corporate biasanya pakai virtual account, beda dari Lynk.id)
- [ ] Handover dokumen deliverable pre-kickoff (kalau ada)
- [ ] Update Notion DB Corporate: status engagement cancelled
- [ ] LinkedIn relationship maintenance — tetap koneksi warm

---

## 7. ANCHOR & CROSS-REFERENCE

- `LAUNCH-PACK-BUKU.md` Section 4 — Refund policy buku 30-hari (master spec)
- `LAUNCH-PACK-COHORT.md` Section 4 — Refund policy cohort 7-hari post-sesi-1
- `CORPORATE-INBOUND-PLAYBOOK.md` Section 7 — Corporate cancellation terms
- `TERMS-OF-SERVICE-TEMPLATE.md` Section 7 — Legal foundation refund T&C
- `STRATEGY-REFRESH-PROTOCOL.md` — Quarterly refund rate review
- `OPERATIONAL-SETUP.md` — Notion DB Funnel + Cohort + Corporate schema
- `MAILERLITE-AUTOMATION-BRIEF.md` — Tag logic untuk segment refunded

---

*Versi 1.0. Templates di atas adalah starting point — sesuaikan nada dengan konteks specific case. SACRED rule no-question approve TIDAK BOLEH dimodifikasi tanpa quarterly review STRATEGI section refund decision.*
