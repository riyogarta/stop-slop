# Stop Slop (Bahasa Indonesia)

> Fork dari [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) karya Hardik Pandya.
> Fork ini menambahkan adaptasi bahasa Indonesia sebagai plugin Claude di folder `plugins/stop-slop-id/`.
> Versi bahasa Inggris asli tetap ada di root repo tanpa perubahan.

*Indonesian adaptation of stop-slop, packaged as a Claude plugin. The original English skill is kept unchanged at the repo root.*

Skill untuk membuang pola tulisan AI dari prosa berbahasa Indonesia.

## Cara pasang

### Claude.ai atau aplikasi desktop (disarankan)

1. Buka **Customize > Plugins**
2. Pilih **Add > Add marketplace**, isi `riyogarta/stop-slop`
3. Pasang plugin **stop-slop-id**

Cara ini membuat plugin ikut terbarui saat repo ini diperbarui.

### Unggah manual

Unduh dari halaman [Releases](https://github.com/riyogarta/stop-slop/releases/latest):

- [`stop-slop-id-plugin.zip`](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id-plugin.zip): unggah lewat **Customize > Plugins > Add > Upload plugin**
- [`stop-slop-id.zip`](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id.zip): unggah lewat **Customize > Skills > + > Upload a skill**

Jangan unggah zip dari tombol **Code > Download ZIP**. Isinya dua `SKILL.md` (Inggris dan Indonesia), jadi akan ditolak.

### Claude Code

```
/plugin marketplace add riyogarta/stop-slop
/plugin install stop-slop-id@riyogarta
```

### System prompt atau custom instructions

Tempel isi [`plugins/stop-slop-id/skills/stop-slop-id/SKILL.md`](plugins/stop-slop-id/skills/stop-slop-id/SKILL.md).

## Cara pakai

Minta Claude menulis atau menyunting teks bahasa Indonesia, dan skill ini dipakai otomatis. Untuk memanggilnya sendiri, ketik `/` di kotak pesan lalu pilih `stop-slop-id`.

## Isi

```
.claude-plugin/marketplace.json        # katalog plugin
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
