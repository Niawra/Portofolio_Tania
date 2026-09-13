# Tania Nurilia Adinda — Portofolio

Website portofolio pribadi yang dibangun dengan HTML, CSS, dan JavaScript murni — tanpa framework, tanpa proses build.

## Cara menjalankan

1. Buka folder ini di VS Code.
2. Install ekstensi **Live Server** jika belum punya.
3. Klik kanan pada `index.html` → **Open with Live Server**.

Selesai — tidak perlu `npm install` atau build tool apa pun.

## Struktur folder

```text
portfolio/
├── index.html          seluruh konten halaman, tersusun per bagian
├── style.css            design token + semua styling
├── script.js             navigasi, efek scroll, animasi reveal, formulir kontak
├── assets/
│   ├── images/           taruh foto-fotomu di sini (lihat di bawah)
│   └── icons/             opsional — untuk favicon atau ikon tambahan
└── README.md
```

## Menambahkan gambar sendiri

Layout tetap terlihat rapi meskipun belum ada gambar — frame kosong akan
otomatis tampil sebagai placeholder bergaris tipis sehingga tidak ada yang
terlihat rusak. Untuk mengganti dengan foto asli, masukkan file ke dalam
`assets/images/` dengan nama persis seperti berikut (atau ubah path `src`
di `index.html`):

| File | Digunakan untuk |
|---|---|
| `profile.jpg` | Potret di bagian hero |
| `project-matchawave.jpg` | Kartu proyek MatchaWave |
| `uiux.jpg` | Kartu proyek UI/UX |
| `project-photography.jpg` | Kartu proyek Fotografi |
| `project-branding-video.jpg` | Kartu proyek Video Personal Branding |
| `project-database.jpg` | Kartu proyek Basis Data |

## Yang perlu diubah sebelum dipublikasikan

Pembuatan situs ini sengaja tidak mengarang pencapaian, pengalaman kerja,
atau testimoni. Cari bagian berikut di `index.html` dan ganti dengan yang
asli:

- **Tautan kontak** — email, Instagram, GitHub, LinkedIn saat ini masih
  memakai alamat placeholder (`hello@example.com`, `#`, dll). Ubah setiap
  `href` di bagian `#contact` dan footer.
- **Tautan proyek** — setiap tombol "Lihat Proyek →" saat ini mengarah ke
  `#`. Arahkan ke demo langsung, repo, atau studi kasus begitu tersedia.
- **Tahun di timeline pengalaman** — ditandai dengan komentar
  `<!-- ubah tahun -->`.
- **Bagian pencapaian** — tiga kartu placeholder dengan teks "Nama
  Pencapaian" / "Deskripsi singkat pencapaian...". Ganti dengan pencapaian
  asli, atau hapus kartu yang tidak diperlukan.
- **Bagian testimoni** — ditandai jelas sebagai kutipan placeholder. Ganti
  dengan testimoni asli begitu tersedia, atau hapus seluruh bagian dengan
  menghapus blok `<section class="testimonials" id="testimonials">…</section>`
  (beserta tautannya di navigasi, jika ditambahkan).

## Catatan tentang formulir kontak

Formulir ini tidak terhubung ke backend — murni frontend, sesuai permintaan.
Saat disubmit, `script.js` akan menampilkan pesan sukses di tempat, bukan
benar-benar mengirim data. Jika ingin formulir ini benar-benar mengirimkan
pesan, hubungkan ke layanan seperti Formspree, EmailJS, atau endpoint
backend milikmu sendiri, lalu sesuaikan handler `submit` di `script.js`.

## Menyesuaikan desain

Semua warna, font, spacing, dan radius didefinisikan sebagai CSS custom
properties di bagian atas `style.css`, di dalam `:root`. Ubah nilainya di
sana dan seluruh tampilan akan ikut berubah — tidak perlu mencari satu per
satu di dalam file.

- `--color-accent` — satu warna aksen (saat ini lavender pudar)
- `--font-display` / `--font-body` / `--font-mono` — tiga jenis huruf yang dipakai
- `--space-*` — skala spacing
