---
title: 'market research: AI video editors that match your editing style'
type: 'market'
topic: 'AI video editors that match your editing style'
decision: 'Where a SaaS built on this codebase has a defensible wedge, and at what price, before the product brief is written'
source: 'native run — harness web search + direct fetch, 2026-11-11'
status: complete
preset: 'standard'
validation: 'normal'
created: '2026-11-11'
updated: '2026-11-11'
claims: 'verified 17, unverified 1, disputed 1 (tally); 1 claim overturned during verification'
---

# market research: AI video editors that match your editing style

**Decision this research serves:** Di mana wedge SaaS yang dibangun di atas kode ini, dan pada harga berapa — sebelum brief ditulis.

> Catatan bahasa: narasi dalam Bahasa Indonesia; kutipan pengguna dan tabel sumber dibiarkan verbatim dalam bahasa aslinya.
> Catatan verifikasi: satu temuan D2 **dibatalkan** dan satu dikoreksi setelah pemeriksaan ulang. Rinciannya di `digests/verification-r1.md`, dan di bagian [Koreksi verifikasi](#koreksi-verifikasi).

## Executive summary

**Fitur yang jadi rencana utama SaaS-mu sudah bukan pembeda.** "Belajar gaya editing dari beberapa video referensi" sudah dikirim oleh minimal enam produk pada November 2026, termasuk satu proyek MIT yang bisa dipakai gratis [1][3][4][6][7][8]. Yang paling matang secara klaim: **Cutprint**, yang mengukur pacing, hook, struktur, komposisi shot, caption, audio dan warna, lalu menyajikannya sebagai aturan berbahasa manusia dengan bukti per aturan [1] — tapi masih invite-only [2]. **Lua** menjualnya di $30/$79/$199 per bulan, khusus Mac Apple silicon, Instagram-first [4]. Dan **cutai** memberi `style-learn` dari banyak referensi video secara gratis, MIT [6].

Artinya: kalau rencanamu adalah "cooked. tapi sebagai SaaS, dengan style learning sebagai headline", kamu masuk pasar sebagai pemain ketujuh dengan fitur yang sama, tanpa merek.

**Tiga temuan yang mengarahkan jawaban:**

1. **Tidak ada satu pun yang menggabungkan seluruh kemampuan cooked.** Yang paling dekat adalah Lua, dan Lua hanya Mac, hanya Instagram, dan belum rilis umum [4][5]. Pemain besar justru menyelesaikan "konsistensi" dengan cara yang jauh lebih dangkal — Descript pakai Brand Studio dan layout pack [9], Submagic pakai Brand Kit dan preset [11], OpusClip pakai brand template [21]. Tidak ada pemain besar yang belajar gaya dari video referensi.

2. **Permintaan pasar terhadap style-matching tidak terbukti; yang terbukti adalah permintaan akan kendali.** Dari review berbayar yang bisa saya verifikasi ulang, tidak ada yang meminta AI yang lebih pintar meniru gaya mereka. Yang mereka tulis adalah keluhan bahwa alatnya memaksa framing, caption, dan narator yang tidak diminta [25][27], dan bahwa watermark baru muncul setelah kerja selesai [26][27]. Ini ketegangan paling penting di laporan ini: fitur yang paling sulit kamu bangun bukan fitur yang paling mereka keluhkan.

3. **Model bisnis kategori ini dibangun di atas hal yang paling dibenci pelanggannya — dan harganya sudah tidak bergerak.** Margin datang dari kredit tak terpakai, sementara keluhan terpadat dalam 12 bulan terakhir adalah kredit hangus saat render gagal [26][27]. Di sisi lain, harga OpusClip dan Descript **tidak berubah selama 18 bulan** [12][13][14][15] — tidak ada perang harga untuk ditakuti, dan tidak ada ruang untuk menang dengan harga lebih murah.

**Kaveat terbesar:** dua sumber terkuat untuk "style learning sudah ada" adalah halaman marketing vendor tanpa liputan independen. Cutwords dan Clypmint mengklaim hal yang sama tanpa perusahaan, harga, atau bukti apa pun [7][8] — keduanya saya turunkan ke `unverified`. **Fidelitas gaya yang dipelajari tidak dibuktikan siapa pun**, termasuk oleh Cutprint. Jadi "sudah dikomoditisasi" benar pada tingkat fitur, belum terbukti pada tingkat mutu.

## D1 — Lanskap & kecocokan fitur

Delapan kemampuan cooked. diuji satu per satu terhadap produk yang halaman resminya benar-benar dibuka. ✅ ya · ◐ sebagian · ✗ tidak.

| Produk | Hapus retake | Belajar gaya dari referensi | Caption per kata | Visual di kata yang diucapkan | Panjang→shorts | URL→video | Profil→gaya | Lokal/OSS/agent |
|---|---|---|---|---|---|---|---|---|
| OpusClip | ✅ [21] | ✗ template merek [21] | ✅ | ◐ stok/AI [22] | ✅ | ✗ | ✗ | ◐ MCP |
| Descript | ✅ [10] | ✗ Brand Studio [9] | ✅ | ◐ layout | ✅ | ✗ | ✗ | ✗ |
| Submagic | ✅ [11] | ✗ preset [11] | ✅ | ◐ b-roll | ? | ✗ | ✗ | ◐ API |
| Klap | ? | ✗ | ✅ | ◐ b-roll | ✅ | ✗ | ✗ | ◐ MCP |
| Pictory | ? | ✗ | ✅ | ◐ stok | ◐ | ✅ [23] | ✗ | ✗ |
| **Cutprint** | ✅ [1] | ✅ **[1]** | ✅ | ◐ | ✅ | ✗ | ◐ | ✗ invite-only [2] |
| **Ponder** | ◐ | ✅ **[3]** | ✅ | ◐ | ? | ✗ | ◐ | ✗ |
| **Lua** | ✅ [4] | ✅ **[4]** | ✅ | ✅ **[5]** | ◐ IG saja | ✗ | ✗ | ✗ Mac saja [4] |
| **cutai** | ✅ [6] | ✅ **[6]** | ✅ | ✗ | ✅ | ✗ | ✗ | ✅ MIT [6] |

**Yang menjawab pertanyaanmu langsung:** ya, ada aplikasi dengan fitur yang sama — dan lebih dari satu. Yang membedakan mereka bukan keberadaan fiturnya, melainkan **seberapa jauh mereka melangkah dari short-form**. Cutprint dan Ponder bergerak di sekitar studio short-form [1][3]. Lua membangun seluruh aplikasi Mac dengan b-roll yang direkam dari situs produk [4][5]. cutai adalah CLI/desktop alpha, MIT, satu maintainer, dan belum merilis versi sejak 0.2.0 pada 2 April 2026 [6].

**Yang belum ada di mana pun:** tidak ada produk stok-b-roll yang menangkap halaman web asli dan logo per kalimat — Lua satu-satunya yang terkonfirmasi, dan itu terkunci di Mac [5]. Tidak ada pemain yang menggabungkan URL→video [23][24] dengan gaya yang dipelajari. Pemisahan itu nyata, dan itu satu-satunya celah yang saya bisa verifikasi.

## D2 — Pricing & packaging

Harga dibaca langsung dari halaman vendor pada 2026-11-11.

| Produk | Gratis | Masuk | Menengah | Atas | Meteran | Sumber |
|---|---|---|---|---|---|---|
| OpusClip | 60 kredit, watermark | $15/bln | $29/bln atau $14,5/bln tahunan ($174/thn) | custom | 1 kredit = 1 menit proses | [12] |
| Descript | 60 menit media | $16 (tahunan) | $24 | $50 | Jam media + kredit AI | [14] |
| Submagic | trial | $12 | $23 | $41 | Kredit; **cap 2/5/30 menit** | [16] |
| VEED | ada | $10/user | $21/user | custom | Kredit + user | [17] |
| Kapwing | 10 kredit | $16 | $50 | custom | Kredit + cap ekspor 4/120 menit | [18] |
| Klap | — | $14,50 (100 klip) | $39,50 | $94,50 | **Klip**, bukan menit | [19] |
| Vizard | 60 kredit | $29 (atau $174/thn) | $39 | — | **1 kredit = 1 menit upload** [20] | [20] |

**Pola:** kredit mendominasi (6 dari 7). Tidak ada yang menjual "unlimited" di tier masuk. Yang dikunci, berurutan: watermark → resolusi → **cap durasi per video** → cap panjang ekspor → jumlah template → seat → menit API. Cap durasi adalah dinding paling tajam dan paling tidak dipromosikan: Submagic membatasi 2/5/30 menit per tier, jadi file 60 menit **melewati semua tier yang dipublikasikan** [16].

**Biaya satu jam footage mentah:** $0,80–$6 tergantung produk. Vizard $1,45/jam [20]; Descript $0,80–1,60/jam [14]; OpusClip $2,90/jam di Pro tahunan sampai $6,00/jam di Starter, dihitung dari definisi resmi 1 kredit = 1 menit [12]. Itu 1–7% dari tarif satu jam editor.

**Arah perubahan — tidak ada.** OpusClip: $29 bulanan, $14,50 bulanan tahunan, $174/tahun, 3.600 kredit/tahun, **identik** pada snapshot Juni 2025 [13] dan hari ini [12]. Descript identik sejak Mei 2025 [14][15]. Kesimpulan: **harga dan meteran kategori stabil 18 bulan.** Yang bergeser bukan harga, melainkan **batas pakai** — dan itu tidak dinaikkan, hanya dijual lebih mahal.

## D3 — Keluhan pelanggan

Basis bukti: feed review publik Apple untuk tiga aplikasi, dibaca 2026-11-11 [25][26][27]. Hanya kutipan yang bisa saya baca langsung yang dipakai; kutipan di luar halaman pertama feed dibuang, bukan diulang. Trustpilot OpusClip **tidak** dipakai karena vendor mengundang reviewernya sendiri [30].

| # | Pola | Bukti terverifikasi | Kutipan | Tanggal |
|---|---|---|---|---|
| 1 | **Kredit hangus saat render gagal; coba lagi harus bayar lagi** | VEED ×2, CapCut ×1 | *"it got to 99% and failed. when i went to retry… it wants another 190 credits. what did i even pay for?"* | 2026-09-24 |
| 2 | **Harga di checkout ≠ harga yang diiklankan; trial diam-diam menagih** | VEED ×2, OpusClip ×1 | *"It'll tell you that it's $14 a month but it really charges you $32 a month."* | 2026-10-13 |
| 3 | **Watermark/paywall baru muncul saat ekspor, atau tetap ada walau sudah bayar** | VEED ×2, CapCut ×1 | *"I spent 30 min on a video ONLY TO FIND OUT AT THE END I HAVE TO PAY FOR NO WATERMARK"* | 2026-09-02 |
| 4 | **Alat memaksakan gayanya sendiri, tanpa saklar mati** | OpusClip ×2, CapCut ×1 | *"Sucks even in pro it zooms in to far or zooms in and out messing up the ratio."* | 2026-10-04 |
| 5 | **Cap durasi memblokir pekerjaan nyata** *(temuan baru)* | CapCut ×1 | *"I dont like the 'video must be under 10 min' that is way too low for youtube"* | 2026-11-09 |
| 6 | **Caption meleset waktunya setelah update** | VEED ×3 | *"Captions are not timed right. Only last a fraction of a second"* | 2026-08-27 |
| 7 | **Dukungan berupa bot; tanpa manusia dan tanpa refund** | OpusClip ×1, VEED ×1 | *"Customers service is low grade AI and won't hand reviews over to a human. Then it will just flat out ignore you."* | 2026-10-20 |

**Bukti sekunder yang tidak diverifikasi ulang:** dua thread Reddit dirujuk oleh peneliti D3 tetapi tidak dibuka kembali saat verifikasi — seorang editor profesional yang menolak kategori ini karena kurang kendali editorial [28], dan satu keluhan podcaster bahwa AI memilih momen yang salah [29]. Keduanya masih masuk akal dan sejalan dengan pola 4 dan 6, tetapi kepercayaannya saya turunkan dan **tidak ada rekomendasi yang bergantung padanya**.

**Yang mereka lakukan sebagai gantinya:** turun ke alat gratis, atau pindah tanpa rencana. *"Going to switch tools because this one obviously doesn't have the upkeep I would expect for a video editing tool I am paying for"* [27]. Pesaingmu yang sebenarnya adalah "gratis" dan "tidak melakukan apa-apa", bukan Opus.

**Yang mereka bilang mau dibayar:** hanya satu yang terbukti — **kendali**: saklar mati per perilaku otomatis, dan watermark yang tidak muncul setelah kerja selesai. Tidak ada bukti siapa pun mau membayar untuk gaya yang lebih mirip dirinya. Perlakukan "orang mau bayar untuk style-matching" sebagai **belum terbukti**.

## Insight lintas dimensi

- **D1 × D3 — fitur yang paling sulit dibangun bukan yang paling diminta.** Pasar sudah punya enam cara belajar gaya, sementara pelanggan yang membayar menulis tentang saklar mati, bukan tentang fidelity. Membangun "AI yang lebih pintar meniru" berarti berkompetisi di sumbu yang tidak dipedulikan pembeli; membangun "AI yang patuh dan bisa dimatikan per bagian" menyerang keluhan yang berulang tiga tahun.
- **D2 × D3 — model bisnis kategori bertabrakan dengan keluhan terbesarnya.** Margin berasal dari kredit tak terpakai; keluhan terpadat adalah kredit hangus saat gagal. Meteran jujur (refund saat gagal, tanpa cap durasi, menit upload yang terlihat) memenangkan kepercayaan **dan** mengorbankan margin. Itu harus diputuskan di PRD, bukan ditemukan saat billing.
- **D2 × D3, temuan baru — cap durasi adalah titik sakit yang tidak disadari pesaingnya.** D2 menunjukkan cap durasi sebagai dinding paket yang paling tajam [16]; D3 menemukan pelanggan menyebutnya sendiri sebagai penghalang pekerjaan [27]. Ini satu-satunya keluhan di seluruh riset yang **belum** dijawab siapa pun dengan produk, dan yang bisa kamu hapus hanya dengan keputusan desain.
- **D1 × D2 × D3 — "URL→video produk" adalah pembeli yang berbeda, bukan fitur tambahan.** Yang memakainya adalah tim marketing SaaS, yang anchor harganya bukan $15/bulan alat klip. Pelanggan yang terdokumentasi di D3 semuanya kreator solo. Jadi ini keputusan segmen, dan sebaiknya tidak dicampur dengan wedge kreator.

## Koreksi verifikasi

Tiga hal berubah setelah pemeriksaan ulang. Rincian dan buktinya di `digests/verification-r1.md`.

1. **DIBATALKAN — "OpusClip memotong harga tahunan 21%".** Angka $11,5/$138 itu harga untuk negara TIER2 (non-AS/UK/DE/AU/CA/FR/ES/SEPA), bukan AS. Harga AS hari ini **[12] dan Juni 2025 [13] identik**: $29 bulanan, $14,50 tahunan, $174/tahun, 3.600 kredit/tahun. Kesimpulan "meteran makin ketat" juga gugur.
2. **DIKOREKSI — OpusClip mendefinisikan kreditnya.** Halaman harga memuat tooltip "1 credit = 1 minute of video processing" [12]. Biaya per jam footage jadi terhitung, bukan asumsi.
3. **DIKONFIRMASI — kutipan review App Store asli.** Auditor semantik awalnya menyatakan tidak ada dukungan, karena hanya melihat 10 review yang dirender di HTML. Di feed RSS Apple, kutipannya **verbatim dan tanggalnya cocok** [25][26][27]. Satu parafrase diperbaiki (reviewer VEED menulis "very important, high-profile", bukan "very high-profile"). Kutipan di luar halaman pertama feed dibuang, bukan diulang.

## Rekomendasi

1. **Jangan memimpin dengan "kami belajar gayamu".** Itu sudah meja taruhan sebelum kamu rilis. Kalau tetap dipakai, posisikan sebagai syarat masuk, bukan pembeda. — *Dasar: kepercayaan tinggi, enam produk terverifikasi [1][3][4][6].*

   **Koreksi dari pemilik produk (2026-11-11):** klaim yang lebih tepat adalah **"kami belajar gaya creator yang Anda sukai"**, bukan gaya pengguna sendiri. Ini diterima — dan ia mengubah tiga hal. Lihat catatan di bawah.
2. **Pimpin dengan bundel yang belum ada: talking-head panjang → gaya yang kamu ukur → visual produk asli (screenshot/logo/halaman) di kata yang tepat.** Celah itu terverifikasi: tidak ada pemain yang menggabungkan gaya terukur dengan tangkapan halaman asli, kecuali Lua yang Mac-only dan IG-only [4][5][23][24]. — *Kepercayaan sedang: kecocokan fitur tinggi, kemauan-bayar belum teruji.*
3. **Serang kegagalan kepercayaan, bukan celah kecerdasan.** Tanpa cap durasi per video, menit upload yang eksplisit, kredit dikembalikan saat render gagal, dan watermark yang tidak pernah mengejutkan. — *Kepercayaan tinggi pada keluhannya [26][27], sedang pada kesediaan membayar premi.*
4. **Harga: $19–24 per seat masuk, meteran menit upload, sekitar $1–3 per jam footage.** Di bawah anchor $29 OpusClip [12], di atas $10–16 VEED/Kapwing [17][18], jauh di bawah $30 Lua [4]. Karena harga kategori stabil 18 bulan [12][13][14][15], **kamu tidak perlu takut perang harga — dan tidak bisa menang dengan harga lebih murah.** Menanglah lewat packaging. — *Kepercayaan tinggi untuk rentang, sedang untuk titik persisnya.*
5. **Pilih satu segmen sebelum PRD.** Kreator solo (pasar terbukti, harga tertekan) atau tim marketing produk (harga lebih longgar, belum ada bukti keluhan). Jangan keduanya di v1. — *Kepercayaan sedang: segmen agensi/editor tidak berhasil didokumentasikan sama sekali.*

### Konsekuensi klaim "gaya creator yang Anda sukai"

Klaim ini **lebih jujur** dan **lebih menjawab keluhan D3** daripada "gaya kamu sendiri". Tapi ia mengubah tiga hal yang harus masuk PRD:

1. **Pesaing langsungnya berganti.** Bukan Cutprint atau Ponder — keduanya belajar dari arsip milikmu sendiri [1][3]. Yang pitchnya nyaris identik adalah **Lua**: *"Show Lua the reels you love. It learns the pace, the caption look and the b-roll"* [4]. Kalau ini headline-mu, kamu berhadapan langsung dengan aplikasi yang sudah punya harga, tim, dan produk jalan — meski masih Mac-only dan waitlist.
2. **Pembelinya berganti.** "Gaya kamu" adalah janji konsistensi untuk kreator yang **sudah** punya arsip. "Gaya creator yang kamu sukai" adalah janji untuk orang yang **belum** punya gaya — kreator baru, pemilik bisnis kecil. Pasarnya jauh lebih besar, tapi nilai jualnya berubah dari "jaga gayamu" menjadi "boleh tampil seperti ini".
3. **Pembeda harus pindah.** Gaya yang dipelajari dari video publik bukan milikmu dan tidak bisa jadi moat — Cutprint dan cutai sudah melakukannya. Yang tersisa: **fidelitas** hasilnya, **bundel** (tangkapan halaman asli per kalimat), dan **kendali** (bisa dimatikan per bagian). Ketiganya, bukan "kami belajar gaya".

Satu batasan desain yang perlu kamu salin dari Cutprint: mereka menyatakan bahwa dari kreator lain ia **hanya** mempelajari sifat editing abstrak — bukan klip, branding, suara, atau musiknya [1]. Meniru "gaya" seorang kreator bernama menyentuh kebijakan konten tidak-orisinal platform dan hak identitas orang itu. Itu bukan nasihat hukum dari saya, tapi itu keputusan produk yang harus diambil sebelum copy ditulis.

## Pertanyaan terbuka

- **Apakah siapa pun membayar untuk style-matching?** Tidak ada bukti di sampel ini. Cara menjawab: uji Cutprint (invite) atau Ponder langsung, dan bandingkan hasilnya dengan 3 video referensi yang sama — fidelitas, bukan fitur.
- **Seberapa bagus gaya yang dipelajari, sebenarnya?** Tidak ada vendor yang mempublikasikan evaluasi. Ini pertanyaan termahal dan paling menentukan.
- **Segmen agensi/editor.** Nol suara terkumpul. Butuh wawancara langsung, bukan riset web.
- **Harga CapCut Pro** tidak terbaca (locale-gated); **harga bulanan Submagic** tidak terkonfirmasi [16].

## Lampiran sumber

| # | Menopang | Penerbit | Terbit | Diakses | Kepercayaan |
|---|---|---|---|---|---|
| [1] | Cutprint mengukur gaya jadi aturan ber-evidence | [Cutprint](https://cutprint.app/features/style-learning) | undated | 2026-11-11 | tinggi |
| [2] | Cutprint invite-only, 4 tier berbayar | [Cutprint](https://cutprint.app/) | ©2026 | 2026-11-11 | tinggi |
| [3] | Ponder belajar dari video/channel referensi | [Ponder](https://ponder.ai/docs/using-ponder/reference-videos-and-briefs) | undated | 2026-11-11 | tinggi |
| [4] | Lua belajar gaya reels, $30–199, Mac saja | [Lua](https://www.trylua.com/) | undated | 2026-11-11 | tinggi |
| [5] | Lua merekam b-roll dari situs produk, bukan stok | [Lua](https://www.trylua.com/product/b-roll) | undated | 2026-11-11 | tinggi |
| [6] | cutai MIT: style-learn, EDITSTYLE.md, MCP | [PyPI](https://pypi.org/project/cutai/) | 2026-04-02 | 2026-11-11 | tinggi |
| [7] | Cutwords klaim style card dari referensi | [Cutwords](https://cutwords.com/edit-styles) | undated | 2026-11-11 | rendah |
| [8] | Clypmint klaim clone dari link | [Clypmint](https://clypmint.com/clone-video-editing-style) | undated | 2026-11-11 | rendah |
| [9] | Descript: konsistensi = Brand Studio | [Descript](https://help.descript.com/branding/brand-studio) | undated | 2026-11-11 | tinggi |
| [10] | Descript punya Remove Retakes | [Descript](https://help.descript.com/descript-terms-and-concepts) | undated | 2026-11-11 | tinggi |
| [11] | Submagic: konsistensi = Brand Kit + preset | [Submagic](https://docs.submagic.co/llms-full.txt) | 2026-10-28 | 2026-11-11 | tinggi |
| [12] | Harga OpusClip hari ini + definisi kredit | [OpusClip](https://www.opus.pro/pricing) | live | 2026-11-11 | tinggi |
| [13] | Harga OpusClip Juni 2025 (identik) | [Internet Archive](https://web.archive.org/web/20250603012036/https://www.opus.pro/pricing) | 2025-06-03 | 2026-11-11 | tinggi |
| [14] | Harga Descript + meteran ganda | [Descript](https://www.descript.com/pricing) | live | 2026-11-11 | tinggi |
| [15] | Harga Descript Mei 2025 (identik) | [Internet Archive](https://web.archive.org/web/20250529120751/https://www.descript.com/pricing) | 2025-05-29 | 2026-11-11 | tinggi |
| [16] | Submagic: cap durasi 2/5/30 menit | [Submagic](https://www.submagic.co/pricing) | live | 2026-11-11 | tinggi |
| [17] | VEED harga per user + kredit | [VEED](https://www.veed.io/pricing) | live | 2026-11-11 | sedang |
| [18] | Kapwing kredit + cap ekspor | [Kapwing](https://www.kapwing.com/pricing) | live | 2026-11-11 | tinggi |
| [19] | Klap meteran per klip | [Klap](https://klap.app/pricing) | live | 2026-11-11 | tinggi |
| [20] | Vizard: 1 kredit = 1 menit | [Vizard](https://vizard.ai/pricing) | live | 2026-11-11 | tinggi |
| [21] | OpusClip API/MCP: brand template, bukan timeline | [OpusClip](https://www.opus.pro/tools/video-editing-api) | undated | 2026-11-11 | tinggi |
| [22] | OpusClip b-roll = stok atau AI | [OpusClip](https://www.opus.pro/blog/three-hacks-to-create-engaging-shorts-faster-with-opus-clip) | undated | 2026-11-11 | tinggi |
| [23] | Pictory: URL/blog → video | [Pictory](https://pictory.ai/url-to-video) | undated | 2026-11-11 | tinggi |
| [24] | Revid: screenshot dan logo asli | [Revid](https://www.revid.ai/tools/website-to-video) | undated | 2026-11-11 | sedang |
| [25] | Review OpusClip (feed RSS, hal. 1) | [App Store RSS](https://itunes.apple.com/us/rss/customerreviews/id=6743615403/sortBy=mostRecent/json) | 2026-09→2026-11 | 2026-11-11 | tinggi |
| [26] | Review VEED Lite (feed RSS, hal. 1) | [App Store RSS](https://itunes.apple.com/us/rss/customerreviews/id=1634439688/sortBy=mostRecent/json) | 2026-04→2026-11 | 2026-11-11 | tinggi |
| [27] | Review CapCut (feed RSS, hal. 1) | [App Store RSS](https://itunes.apple.com/us/rss/customerreviews/id=1500855883/sortBy=mostRecent/json) | 2026-11 | 2026-11-11 | tinggi |
| [28] | Editor profesional menolak kategori | [r/editors](https://www.reddit.com/r/editors/comments/1ukn4aq/) | 2026-07-01 | 2026-11-11 | sedang — tidak diverifikasi ulang |
| [29] | AI memilih momen yang salah, 2023→2026 | [r/podcasting](https://www.reddit.com/r/podcasting/comments/14zzbpk/) | 2023 | 2026-11-11 | rendah — tidak diverifikasi ulang |
| [30] | Skor Trustpilot OpusClip bersifat solicited | [Trustpilot](https://www.trustpilot.com/review/opus.pro) | live | 2026-11-11 | tinggi |

## Peta kedaluwarsa

Dihitung dengan `recon_kit.py staleness`, jendela per kelas: fitur & harga & packaging 3 bulan, sentimen 12 bulan. Hasilnya: **2 klaim sudah lewat jendela**, 17 belum.

- **`cutai` (recheck 2026-07-01, lewat).** Bukan karena halamannya basi — saya buka hari ini — tapi karena rilis terakhirnya 0.2.0 pada 2 April 2026: tujuh bulan tanpa rilis dari satu maintainer. Kesimpulan "ada alternatif MIT gratis" tetap benar, tapi **ancamannya lebih kecil daripada yang terlihat**: proyeknya tidak bergerak.
- **Perbandingan harga OpusClip Juni 2025 (recheck 2025-09-01, lewat).** Ini wajar dan **tidak perlu diperbarui**: klaimnya adalah fakta historis (harga pada tanggal tertentu), bukan keadaan hari ini. Yang perlu dicek berkala adalah harga hari ini [12], dan itu sudah berstatus segar.
- Klaim fitur, harga, dan packaging lain: recheck 2027-01-01 sampai 2027-02-01.
- Sentimen: recheck 2027-07-01 sampai 2027-10-01.
- **Recheck paling awal yang bermakna: 2027-02-01** untuk seluruh tabel fitur dan harga. Kalau Cutprint membuka pendaftaran umum, atau Lua keluar dari Mac, ulangi D1 lebih cepat.

Refresh/Deepen menangani ini tanpa mengulang seluruh riset.
