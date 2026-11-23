# Stop Slop (Bahasa Indonesia)

> Fork dari [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) karya Hardik Pandya.
> Fork ini menambahkan adaptasi bahasa Indonesia sebagai plugin Claude di folder `plugins/stop-slop-id/`.
> Versi bahasa Inggris asli tetap ada di root repo tanpa perubahan.

*Indonesian adaptation of stop-slop, packaged as a Claude plugin. The original English skill is kept unchanged at the repo root.*

Skill untuk membuang pola tulisan AI dari prosa berbahasa Indonesia. Formatnya `SKILL.md` standar, jadi bisa dipakai di Claude, ChatGPT, dan Gemini.

## Cara pasang

### Claude.ai atau aplikasi desktop (disarankan)

1. Buka **Customize > Plugins**
2. Pilih **Add > Add marketplace**, isi `riyogarta/stop-slop`
3. Pasang plugin **stop-slop-id**

Cara ini membuat plugin ikut terbarui saat repo ini diperbarui.

### Unggah manual ke Claude

Unduh dari halaman [Releases](https://github.com/riyogarta/stop-slop/releases/latest):

- [`stop-slop-id-plugin.zip`](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id-plugin.zip): unggah lewat **Customize > Plugins > Add > Upload plugin**
- [`stop-slop-id.zip`](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id.zip): unggah lewat **Customize > Skills > + > Upload a skill**

Jangan unggah zip dari tombol **Code > Download ZIP**. Isinya dua `SKILL.md` (Inggris dan Indonesia), jadi akan ditolak.

### Claude Code

```
/plugin marketplace add riyogarta/stop-slop
/plugin install stop-slop-id@riyogarta
```

### ChatGPT

Skills di ChatGPT tersedia untuk akun Business, Enterprise, Healthcare, dan Edu.

1. Unduh [`stop-slop-id.zip`](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id.zip)
2. Di sidebar, pilih **Plugins**, lalu buka tab **Skills**
3. Pilih **Create > Upload from your computer**, lalu pilih zip tadi

ChatGPT memindai skill yang diunggah. Kalau ditandai **Needs Review**, periksa dulu sebelum dipakai.

### Gemini

Skills di Gemini tersedia untuk akun Google pribadi usia 18 tahun ke atas. Akun Workspace menyusul. Unggah skill hanya bisa di [gemini.google.com](https://gemini.google.com) atau aplikasi Gemini di Mac.

1. Unduh [`stop-slop-id.zip`](https://github.com/riyogarta/stop-slop/releases/latest/download/stop-slop-id.zip), lalu ekstrak. Hasilnya folder `stop-slop-id`.
2. Buka **Customize > Skills** di sidebar. Kalau "Customize" tidak terlihat, klik **More** dulu.
3. Unggah folder `stop-slop-id`. Nama folder harus sama dengan nama skill, jadi jangan diganti.

### System prompt atau custom instructions

Tempel isi [`plugins/stop-slop-id/skills/stop-slop-id/SKILL.md`](plugins/stop-slop-id/skills/stop-slop-id/SKILL.md).

## Cara pakai

Minta asisten menulis atau menyunting teks bahasa Indonesia, dan skill ini dipakai otomatis. Untuk memanggilnya sendiri:

| Platform | Cara panggil |
|---|---|
| Claude | ketik `/` lalu pilih `stop-slop-id` |
| Claude Code | `/stop-slop-id:stop-slop-id` |
| ChatGPT | `@stop-slop-id` |
| Gemini | `/stop-slop-id` |

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
