# Stop Slop (Bahasa Indonesia)

> Fork dari [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) karya Hardik Pandya.
> Fork ini menambahkan adaptasi bahasa Indonesia di folder `id/`. Versi bahasa Inggris asli
> tetap ada di root repo tanpa perubahan.

*Indonesian adaptation of stop-slop. The original English skill is kept unchanged at the repo root.*

Skill untuk membuang pola tulisan AI dari prosa berbahasa Indonesia.

## Isi

```
id/
├── SKILL.md              # Aturan inti dan cek cepat
└── references/
    ├── frasa.md          # Frasa yang dibuang
    ├── struktur.md       # Struktur kalimat yang dihindari
    └── contoh.md         # Contoh sebelum/sesudah
```

## Cara pakai

**Claude Code:** pasang folder `id/` sebagai skill.

**Claude Projects:** unggah `id/SKILL.md` dan isi `id/references/` ke project knowledge.

**System prompt / custom instructions:** tempel isi `id/SKILL.md`.

## Beda dari versi asli

- Ditambah pola bahasa terjemahan: "di mana", "yang mana", "melakukan pengecekan", "adalah merupakan".
- Ditambah pembuka dan penutup khas asisten, jargon, istilah Inggris, serta aturan format.
- Kalimat pasif tidak dilarang, karena pasif di- adalah bentuk wajar bahasa Indonesia.
- Larangan semua kata keterangan diganti larangan kata pengisi.
- Larangan kalimat berawalan What/Why/How dihapus; padanannya, pola "Yang ... adalah ...", masuk ke struktur.

## Kredit

- Versi asli: [Hardik Pandya](https://hvpandya.com), [stop-slop](https://github.com/hardikpandya/stop-slop)
- Adaptasi bahasa Indonesia: [Riyogarta Pratikto](https://github.com/riyogarta)

## Lisensi

MIT, mengikuti versi asli. Lihat [LICENSE](LICENSE).
