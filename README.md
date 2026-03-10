# 🎨 NUSANTRA — Assets Repository

Repository aset statis untuk game [NUSANTRA](https://pawang.online) — sprite, background, musik, dan efek suara. Di-serve via **GitHub Raw / jsDelivr CDN**.

> Repo utama game: [github.com/username/nusantra](https://github.com/username/nusantra)

---

## Cara Akses Asset (URL CDN)

Asset di repo ini bisa diakses langsung via **jsDelivr** tanpa perlu server sendiri:

```
https://cdn.jsdelivr.net/gh/username/nusantra-assets@main/<path/ke/file>
```

**Contoh:**
```
# Sprite dedemit
https://cdn.jsdelivr.net/gh/username/nusantra-assets@main/dedemit/sprites/kuntilanak.png

# BGM area
https://cdn.jsdelivr.net/gh/username/nusantra-assets@main/audio/bgm/jawa-village.ogg

# Background map
https://cdn.jsdelivr.net/gh/username/nusantra-assets@main/maps/backgrounds/desa-ciawi.webp
```

> Gunakan tag versi (`@1.0.0`) bukan `@main` di production agar tidak terdampak perubahan mendadak:
> `https://cdn.jsdelivr.net/gh/username/nusantra-assets@1.0.0/...`

---

## Struktur Folder

```
nusantra-assets/
│
├── dedemit/
│   ├── sprites/              # Sprite battle (128×128px, PNG)
│   │   ├── kuntilanak.png
│   │   ├── genderuwo.png
│   │   ├── leak.png
│   │   └── ...
│   └── portraits/            # Gambar penuh untuk Dex (256×256px, PNG)
│       ├── kuntilanak.png
│       └── ...
│
├── maps/
│   ├── backgrounds/          # Background area battle (800×600px, WebP)
│   │   ├── desa-ciawi.webp
│   │   ├── hutan-sancang.webp
│   │   └── ...
│   └── thumbnails/           # Thumbnail untuk world map (200×200px, WebP)
│       ├── desa-ciawi.webp
│       └── ...
│
├── items/
│   ├── jimat/                # Icon jimat (64×64px, PNG)
│   │   ├── jimat-rajah.png
│   │   ├── jimat-kemenyan.png
│   │   └── ...
│   └── ramuan/               # Icon ramuan & item lain (64×64px, PNG)
│       ├── air-jampi.png
│       └── ...
│
├── ui/
│   ├── icons/                # Icon UI umum (SVG diutamakan)
│   │   ├── energi.svg
│   │   ├── koin.svg
│   │   └── ...
│   ├── logo/                 # Logo NUSANTRA berbagai ukuran
│   │   ├── logo-full.svg
│   │   ├── logo-icon-192.png
│   │   └── logo-icon-512.png
│   └── frames/               # Frame & dekorasi UI (PNG)
│
└── audio/
    ├── bgm/                  # Background music per area (OGG + MP3)
    │   ├── jawa-village.ogg
    │   ├── jawa-village.mp3  # fallback untuk browser lama
    │   ├── bali-temple.ogg
    │   └── ...
    └── sfx/                  # Sound effects (OGG + MP3)
        ├── battle-hit.ogg
        ├── battle-miss.ogg
        ├── battle-critical.ogg
        ├── catch-shake.ogg
        ├── catch-success.ogg
        ├── catch-fail.ogg
        ├── levelup.ogg
        ├── evolusi.ogg
        └── ...
```

---

## Spesifikasi Asset

### Sprite Dedemit
| Tipe | Ukuran | Format | Maks. Ukuran File |
|------|--------|--------|-------------------|
| Battle sprite | 128×128px | PNG (transparan) | 50KB |
| Portrait (Dex) | 256×256px | PNG (transparan) | 150KB |

### Background Map
| Tipe | Ukuran | Format | Maks. Ukuran File |
|------|--------|--------|-------------------|
| Background battle | 800×600px | WebP | 200KB |
| Thumbnail world map | 200×200px | WebP | 30KB |

### Item & UI Icons
| Tipe | Ukuran | Format | Maks. Ukuran File |
|------|--------|--------|-------------------|
| Item icon | 64×64px | PNG (transparan) | 20KB |
| UI icon | Scalable | SVG diutamakan | 10KB |

### Audio
| Tipe | Format | Bitrate | Maks. Durasi |
|------|--------|---------|--------------|
| BGM | OGG + MP3 | 128kbps | 3 menit (loop) |
| SFX | OGG + MP3 | 96kbps | 3 detik |

> **Kenapa OGG + MP3?** OGG ukurannya lebih kecil dan didukung semua browser modern. MP3 disertakan sebagai fallback. Phaser 3 otomatis memilih format yang didukung browser.

---

## Git LFS

Repo ini menggunakan **Git Large File Storage (LFS)** untuk semua file binary.

## Lisensi

Semua aset di repository ini adalah milik NUSANTRA dan tidak boleh digunakan di luar konteks game tanpa izin.

Folklor dan nama makhluk yang menjadi inspirasi adalah warisan budaya publik Indonesia.
