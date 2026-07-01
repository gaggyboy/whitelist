# GitHub Remote Control

Bu dosyalari GitHub reposuna yukle:
`https://github.com/gaggyboy/whitelist` (main branch)

- `setcalma` — HWID whitelist
- `config.json` — uzaktan kill switch / guncelleme

## config.json
Modu uzaktan kapatabilir veya guncelleme zorunlu kilabilirsin.

```json
{
  "enabled": true,
  "kill_switch": false,
  "min_version": "1.0.0",
  "latest_version": "1.1.0",
  "download_url": "https://github.com/.../releases/latest",
  "title": "Guncelleme Gerekli",
  "message": "Yeni surum cikti. Lutfen guncel modu indirin."
}
```

| Alan | Etki |
|------|------|
| `enabled: false` | Mod tamamen kapanir |
| `kill_switch: true` | Acil kapatma |
| `min_version` | Altindaki surumler calismaz, guncelleme ekrani |
| `message` | Ekranda gosterilen metin |
| `download_url` | Indir butonu panoya kopyalar |

## setcalma (whitelist)
```
HWID1234567890ABCD
HWID1234567890ABCD:31-12-2026
```

Tarih formati: `gg-aa-yyyy` (ornek: `31-12-2026`). `/` ve `.` de kabul edilir.
HWID buyuk/kucuk harf fark etmez.

## MinGW Derleme
1. `native\local.env.example` dosyasini `native\local.env` olarak kopyala
2. MSYS2 icin: `MINGW_BIN=C:\msys64\mingw64\bin`
3. `native\build.bat` calistir

## Release
```
build-all.bat
```
