# Kebijakan Keamanan

## Versi yang Didukung

Versi terbaru di branch `main` selalu menerima perbaikan keamanan.

| Versi | Didukung |
|------|----------|
| main (terbaru) | ✅ |
| versi lama | ❌ |

## Melaporkan Kerentanan

Jika kamu menemukan masalah keamanan (mis. perintah yang bisa membahayakan perangkat,
penanganan whitelist yang salah, atau potensi kerusakan data), **jangan** membuat
Issue publik terlebih dahulu.

Laporkan secara privat ke:
- 🌐 [www.myrul.dev](https://www.myrul.dev)
- 📘 [facebook.com/myruldev](https://web.facebook.com/myruldev)

Sertakan:
- Deskripsi masalah & dampaknya
- Langkah untuk mereproduksi
- Merek/model HP & versi Android (jika relevan)

Kami akan berusaha merespons secepatnya.

## Catatan Keamanan Penting

AUD **tidak** memakai root dan **tidak** memakai `pm uninstall` sebagai default —
hanya `pm disable-user`, sehingga aksi dapat dibatalkan. Namun menonaktifkan paket
sistem tetap berisiko. Selalu:
- Mulai dari kategori `safe`
- Gunakan **Mode Simulasi** untuk uji coba
- Simpan file **backup** sebelum aksi
