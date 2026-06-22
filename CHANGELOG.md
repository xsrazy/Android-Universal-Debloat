# Changelog

Semua perubahan penting pada proyek ini dicatat di berkas ini.
Format mengikuti [Keep a Changelog](https://keepachangelog.com/id/1.0.0/)
dan proyek ini memakai [Semantic Versioning](https://semver.org/lang/id/).

## [1.1.0] - 2026-06-22
### Ditambahkan
- Banner ASCII "AUD" + identitas (website & Facebook) di setiap layar menu.
- Mode Simulasi (Dry-Run) untuk uji coba tanpa mengubah HP.
- Whitelist kustom via `database/whitelist.txt`.
- Menu **Cari Aplikasi** (pencarian kata kunci).
- Menu **Cek Status Debloat** (aktif vs nonaktif).
- Menu **Aplikasi Tak Dikenal** (deteksi bloatware belum terdaftar + ekspor file).
- Database merek baru: oneplus, honor, huawei, motorola, asus, sony, nokia,
  pixel, zte, nubia, lenovo, meizu, lg, tcl, wiko, sharp, itel.
- Berkas GitHub: README lengkap, LICENSE (MIT), CONTRIBUTING, CODE_OF_CONDUCT,
  SECURITY, CHANGELOG, template issue/PR, banner.

### Diubah
- Deteksi merek otomatis diperluas menjadi 24 merek.
- README dirombak menjadi format dokumentasi GitHub.

## [1.0.0] - 2026-06-22
### Ditambahkan
- Rilis awal `aud.sh`: cek dependency, deteksi device, scan paket,
  Debloat Aman/Disarankan/Manual, Restore, Backup, Log.
- Database awal: universal, xiaomi, samsung, oppo, vivo, realme, infinix, tecno.
- Whitelist pelindung paket inti, backup otomatis, konfirmasi (y/n).
