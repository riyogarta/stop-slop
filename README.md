# Stop Slop (Bahasa Indonesia)

> Fork dari [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) karya Hardik Pandya.
> Fork ini menambahkan adaptasi bahasa Indonesia yang dikemas sebagai plugin Claude di folder
> `plugins/stop-slop-id/`. Versi bahasa Inggris asli tetap ada di root repo tanpa perubahan.

*Indonesian adaptation of stop-slop, packaged as a Claude plugin. The original English skill is kept unchanged at the repo root.*

Skill untuk membuang pola tulisan AI dari prosa berbahasa Indonesia.

## Pasang

Plugin dan skill membutuhkan **Create and edit files** (dulu bernama *Code execution and file creation*) dalam keadaan aktif di **Settings > Capabilities**.

### Claude.ai dan aplikasi desktop

**Cara 1: langsung dari GitHub**

1. Buka **Customize > Plugins**.
2. Klik **Add > Add marketplace**, isi `riyogarta/stop-slop`.
3. Pilih plugin **stop-slop-id**, lalu klik **Add**.

**Cara 2: unggah zip**

1. Unduh [stop-slop-id-plugin.zip](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id-plugin.zip).
2. Buka **Customize > Plugins**, klik **Add > Upload plugin**, lalu pilih file tadi.

Jangan unggah zip dari tombol **Code > Download ZIP** di GitHub. Zip itu berisi dua `SKILL.md` (Inggris dan Indonesia) sehingga ditolak.

### Claude Code

```
/plugin marketplace add riyogarta/stop-slop
/plugin install stop-slop-id@stop-slop-id
```

### Alat lain

Untuk system prompt atau alat lain yang mengikuti standar Agent Skills, pakai isi
[`SKILL.md`](plugins/stop-slop-id/skills/stop-slop-id/SKILL.md). Versi skill saja (tanpa kemasan plugin) tersedia di
[Releases](https://github.com/riyogarta/stop-slop/releases/latest) sebagai `stop-slop-id.zip`.

## Cara pakai

Minta Claude menulis atau menyunting teks bahasa Indonesia, dan skill ini dipakai otomatis. Untuk memanggilnya sendiri, ketik `/` di kotak pesan lalu pilih `stop-slop-id`.

## Isi

```
.claude-plugin/marketplace.json        # katalog marketplace
plugins/stop-slop-id/
├── .claude-plugin/plugin.json         # manifest plugin
└── skills/stop-slop-id/
    ├── SKILL.md                       # aturan inti dan cek cepat
    └── references/
        ├── frasa.md                   # frasa yang dibuang
        ├── struktur.md                # struktur kalimat yang dihindari
        └── contoh.md                  # contoh sebelum/sesudah
```

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
