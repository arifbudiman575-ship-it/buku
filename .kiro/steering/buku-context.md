---
inclusion: always
---

# Repo Steering — Personal Branding Playbook @arifb.id

> Steering ini di-load otomatis di setiap session Kiro yang buka repo `arifbudiman575-ship-it/buku`. Tujuan: continuity antar-akun + antar-session, supaya tidak perlu re-explain konteks.

---

## 1. CORE IDENTITAS PROJECT

- **Owner:** Arif Budiman, handle `@arifb.id`
- **Core IP:** Buku **THE AI ARCHITECT** (AI Universe Series, Book 0)
- **Positioning:** AI Architect — kategori baru di Indonesia
- **Goal 12 bulan:** 30K followers Threads + Rp 1 miliar revenue
- **Strategi sekarang:** Threads-first Bulan 1, repurpose ke IG + LinkedIn

### 3 Frase Signature (WAJIB di-repeat)

1. **"Sistem, bukan tools."**
2. **"Arsitek, bukan pengguna."**
3. **"Tools berubah. Framework abadi."**

### Karakter Ownable di Buku

- **Riko** = pengguna AI yang stuck di "prompt apa ya?"
- **Citra** = arsitek yang membangun sistem

---

## 2. PAKEM EDITORIAL — TIDAK BOLEH DILANGGAR

### Voice Rules (STRATEGI §5.3)

| OK | HINDARI |
|---|---|
| "Anda" konsisten | "lo / gue / kalian / temen-temen" |
| Kalimat pendek, paragraf 1-2 baris | Paragraf panjang penuh kata sifat |
| Ending pertanyaan / quote | Ending "follow & like ya bro!" |
| Bahasa Indonesia baik (boleh selipkan istilah Inggris untuk konsep teknis) | Indo-English campur acak |
| 1 ide besar per post | Listicle 15 poin tanpa tema |

### Filter 4-Lapis (STRATEGI §0.5) — wajib semua public-facing content

1. **Book-safe** — tidak bocor IP buku (lihat Section 4 di steering ini)
2. **Voice** — tenang, tidak hype, "Anda" konsisten
3. **Frase signature** — minimal 1 kemunculan per post, minimal 2 di pinned/manifesto
4. **Anti-hype** — tidak ada "BURUAN/WAJIB/TINGGAL/RAHASIA"

### Format Kalimat Khas (STRATEGI §5.4)

```
[Pernyataan keras dan pendek].
[Pernyataan kontras yang melawan ekspektasi].
[Pertanyaan retoris yang buka renungan].
[Resolusi singkat — 1 baris quotable].
```

---

## 3. ARSITEKTUR INFORMASI REPO

### File yang Sudah Established (jangan rewrite tanpa diskusi)

| File | Fungsi |
|---|---|
| `STRATEGI-PERSONAL-BRANDING.md` | Source of truth strategi (1.152 baris, 17 sections) |
| `BRAND-JOURNEY-MAP.md` | BJM 5 Q + audit asosiasi |
| `CONTENT-CALENDAR-BULAN-1.md` | Kalender 30 hari final (1.310 baris) |
| `THREADS-LONGFORM-ABC-TEST.md` | 4 long-thread (Opsi A V3, B V2, C V2, D V0) |
| `MANIFESTO-PINNED-V1.md` | Day 1 launch package 3-platform |
| `PERFORMANCE-TRACKER-SETUP.md` | Sheets 4-tab schema |
| `DAY-1-LAUNCH-RUNBOOK.md` | T-7 to T+1 timeline |
| `LEAD-MAGNET-7-DAY-CHALLENGE-SPEC.md` | LP + 8 email full body |
| `NOTION-COMMAND-CENTER-SPEC.md` | 4-database review hub |
| `VISUAL-ASSET-TEMPLATE-LIB.md` | 4 Canva templates |
| `RINGKASAN-SESI.md` | Session log historis |
| `LANJUTKAN-DI-SINI.md` | Status + handover antar-session |
| `analisa_kompetitor.md` | 31 kompetitor benchmark |

### Layered IP Hierarchy (STRATEGI §0.1)

1. Buku THE AI ARCHITECT (sacred core IP)
2. Strategi pak Bi (private playbook, internal)
3. Brand Journey Map (BJM)
4. STRATEGI-PERSONAL-BRANDING (consolidated)
5. Public content (Threads, IG, LinkedIn)

**Aturan resolusi konflik:** higher layer wins. Buku tidak bisa di-override oleh strategi.

---

## 4. SACRED — TIDAK BOLEH MASUK PUBLIC CONTENT

> Detail Prolog buku yang sengaja di-gate sampai buku rilis publik:

- Scene Februari 2024 jam 2 pagi
- **Saldo Rp 847.000** (saldo real rekening) — DETAIL ANGKA DAN KONTEKS spesifik (boleh menyebut "kondisi finansial sulit" tanpa angka)
- 347 prompt + breakdown 5 kategori
- Recovery arc 340%
- Metafora resep masakan

> Konteks penting: angka `Rp 847.000` muncul di file repo (legit untuk planning), tapi **tidak boleh** muncul di sosmed sebelum buku rilis. Kalau menulis konten, **periksa angka spesifik ini absent**.

---

## 5. DECISIONS LOCKED (per 30 Mei 2026)

| Keputusan | Lock value | File reference |
|---|---|---|
| Day 1 launch date | **Senin 15 Juni 2026** | Tracker Tab 1 + Runbook |
| Aksen warna Manifesto | `#1F3A5F` (biru tua) | Manifesto §2 + Visual Asset Lib §1 |
| Email tool | **MailerLite free** | Lead Magnet §0 |
| Domain LP | Link bio aggregator (MVP Day 7-10) | Lead Magnet §0 |
| Triple publish slot | **19:30 WIB** Threads, **19:32** IG, **19:35** LinkedIn | Runbook §9 |
| Repurpose hard cap | 3 ide/minggu, Reels 2/minggu max | CONTENT-REPURPOSING-PLAYBOOK |

---

## 6. CONSTRAINTS YANG TIDAK BOLEH DILANGGAR

### Hard No Bulan 1

1. Bank konten 12 bulan ahead (Bulan 1 dulu, baseline data dulu, baru Bulan 2)
2. Tools berbayar selain yang sudah listed (Canva free + MailerLite free + Sheets + Notion)
3. Pop-up exit-intent / countdown timer / urgency hype di LP
4. A/B testing Bulan 1 (volume belum cukup)
5. CRM / dashboard tools selain Sheets
6. YouTube long-form Bulan 1 (Bulan 3+)
7. Outsource visual ke designer (Bulan 1 produksi sendiri — friction = data)
8. Detail Prolog buku di sosmed (lihat Section 4)
9. Force push ke main, langsung commit ke main, atau merge tanpa review user
10. Buat PR otomatis tanpa user request

### Standard Workflow

1. **Drafting:** di chat dulu (code fence markdown), bukan langsung file
2. **File creation:** ke `_kiro_drafts/` di workspace dulu (sandbox), bukan langsung repo
3. **Commit:** branch baru dari `main`, prefix `add-` / `update-` / `lock-` / `docs-`
4. **Push:** pakai `mcp_tool_server_github_push_to_remote`, bukan `git push`
5. **PR:** **JANGAN buat otomatis.** User yang buat manual via GitHub UI.
6. **Verification numerik:** WAJIB derive dari `wc -l` / `grep -c` aktual sebelum tulis target di commit message atau spec brief. JANGAN estimasi mental (lihat learning history).

---

## 7. SESSION HANDOVER — STATE per 30 Mei 2026

### Branches Outstanding (siap PR, BELUM merged)

| Branch | File | Status |
|---|---|---|
| `add-manifesto-pinned-v1` | MANIFESTO-PINNED-V1.md | Standalone (442 lines) |
| `add-performance-tracker-setup` | PERFORMANCE-TRACKER-SETUP.md | Standalone (227 lines) |
| `add-day1-launch-runbook` | DAY-1-LAUNCH-RUNBOOK.md | Standalone (254 lines) |
| `add-lead-magnet-spec` | LEAD-MAGNET-7-DAY-CHALLENGE-SPEC.md | Standalone (576 lines) |
| `add-arsi-7-hari-draft` | THREADS-LONGFORM-ABC-TEST.md +152 | Append Opsi D V0 |
| `add-notion-command-center` | NOTION-COMMAND-CENTER-SPEC.md | Standalone (189 lines) |
| `add-visual-asset-library` | VISUAL-ASSET-TEMPLATE-LIB.md | Standalone (169 lines) |
| **`lock-day1-decisions`** | 4 file modified | **Superset** — sudah include 4 branch awal + decisions lock |

### Recommended Merge Strategy

**Opsi simpel:** Merge **`lock-day1-decisions`** ke main = 1 PR. Otomatis include Manifesto + Tracker + Runbook + Lead Magnet + decisions. Lalu merge 3 branch sisa: `add-arsi-7-hari-draft`, `add-notion-command-center`, `add-visual-asset-library`. Total 4 PR.

**Opsi granular:** Merge 7 branch awal individual untuk history rapi (1 file per PR), lalu merge `lock-day1-decisions` sebagai patch — total 8 PR.

### Pending Work (Opsi B sisa, untuk Kiro Desktop session)

| # | Task | Estimasi | Prioritas |
|---|---|---|---|
| 3 | Hari 1 Worksheet PDF design (Lead Magnet attachment) | 1-2 jam | Sebelum Day 7 |
| 4 | Polish A.R.S.I. 7-Hari Opsi D V0 → V1 | 1 jam | Sebelum Day 18 |
| 5 | Bulan 2 outline (high-level only) | 1-2 jam | Bulan 1 minggu 4 |

### Pending Decisions (belum locked)

- Profile picture final (foto Anda, bukan AI generated)
- Bio Threads/IG/LinkedIn final wording (template ada di STRATEGI §9)
- Apakah bikin domain `arifb.id/start` atau stay di link bio aggregator setelah Day 14

---

## 8. STARTER PROMPT — UNTUK KIRO DESKTOP NEW SESSION

Copy-paste prompt ini ke Kiro Desktop session baru:

```
Saya lanjut kerja playbook personal branding @arifb.id di repo
arifbudiman575-ship-it/buku.

Steering file .kiro/steering/buku-context.md berisi state lengkap.
Tolong baca dulu, lalu konfirmasi 3 hal:
1. Decisions locked yang Anda baca dari Section 5
2. Branches outstanding yang belum di-merge
3. Pending work yang perlu saya prioritas

Setelah itu, tugas saya: [pilih salah satu]
- Hari 1 Worksheet PDF design untuk Lead Magnet
- Polish A.R.S.I. 7-Hari V0 ke V1
- Bulan 2 outline high-level

Mulai dari yang mana?
```

---

## 9. ANTI-PATTERN YANG SUDAH TERJADI — JANGAN ULANGI

### Insiden 30 Mei 2026: Phantom Delete Dialog

Saat ChatGPT (via GitHub Contents API) mau commit file yang berisi angka format Rupiah (mis. "Rp 847.000"), UI ChatGPT auto-flag angka tersebut sebagai PII di sharing-data confirmation dialog dengan label "BankAccount" — false positive PII classifier, BUKAN connector finansial bocor.

Di insiden 30 Mei, dialog "Delete file" muncul setelah PROMPT 2 (CREATE) dengan commit message palsu "remove accidental test file". User correctly DENY. Pattern ini hijack — tidak normal. Mitigation:

1. Saat eksekusi via Claude di sandbox langsung (bukan via ChatGPT), risiko ini tidak ada.
2. Kalau tetap pakai ChatGPT untuk commit: WARN user tentang false-positive PII flag sebelum mereka paste prompt.
3. Kalau dialog "Delete" muncul setelah prompt CREATE → INSTRUKSI user untuk DENY dan stop sesi ChatGPT itu.

---

> Steering ini = handover bridge antar-session. Update Section 5, 7, 8 setiap kali ada keputusan baru atau session selesai.
