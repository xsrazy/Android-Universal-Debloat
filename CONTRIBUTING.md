# Berkontribusi ke Android Universal Debloat (AUD)

Terima kasih sudah mau ikut membangun AUD! 🎉
Proyek ini hidup dari gotong-royong — terutama untuk **melengkapi database bloatware**
berbagai merek HP. Panduan ini menjelaskan cara berkontribusi dengan rapi.

---

## 🧩 Jenis Kontribusi

1. **Menambah / memperbaiki database paket** (paling dibutuhkan!)
2. Memperbaiki bug pada `aud.sh`
3. Menambah fitur baru
4. Memperbaiki dokumentasi / terjemahan

---

## 🗂️ Menambah Paket ke Database

### Format wajib
Setiap baris di file `database/*.txt`:
```
package|nama aplikasi|risk
```

Contoh:
```
com.miui.analytics|MIUI Analytics (pelacak)|recommended
```

### Tingkat risiko
| Risk | Kapan dipakai |
|---|---|
| `safe` | Aman dimatikan, nyaris tanpa efek samping |
| `recommended` | Umumnya aman & disarankan dimatikan |
| `advanced` | Bisa ada efek samping, untuk pengguna paham |
| `dangerous` | Berisiko tinggi, hindari kecuali sangat paham |

### Langkah cepat (pakai fitur bawaan AUD)
1. Jalankan AUD → menu **7) Aplikasi Tak Dikenal**.
2. File hasil tersimpan di `logs/tak-dikenal-*.txt` (format sudah siap salin).
3. Isi nama aplikasi & tentukan tingkat risikonya.
4. Salin baris ke file database merek yang sesuai
   (mis. `database/xiaomi.txt`). Kalau berlaku semua merek → `database/universal.txt`.
5. Buat Pull Request.

### Aturan database
- ❌ **JANGAN** memasukkan paket inti sistem (lihat whitelist di `aud.sh`).
- ❌ Jangan menebak risiko. Kalau ragu, pakai `advanced` dan beri catatan di PR.
- ✅ Urutkan logis (kelompokkan per kategori bila bisa).
- ✅ Pakai nama aplikasi yang ramah orang awam (boleh bahasa Indonesia).
- ✅ Satu paket = satu baris, tanpa duplikat.

---

## 🔧 Mengubah Kode (`aud.sh`)

- Tetap **POSIX/bash** dan kompatibel dengan Termux.
- **JANGAN** menambahkan perintah yang butuh root.
- Default aksi tetap `pm disable-user` (bukan `pm uninstall`).
- Jaga UI tetap **bahasa Indonesia** & ramah awam.
- Selalu sediakan **konfirmasi (y/n)** sebelum aksi yang mengubah HP.
- Uji sintaks sebelum PR:
  ```bash
  bash -n aud.sh
  ```

---

## 🔀 Alur Pull Request

1. **Fork** repo ini.
2. Buat branch deskriptif:
   ```bash
   git checkout -b tambah-database-xiaomi
   ```
3. Commit dengan pesan jelas:
   ```
   db(xiaomi): tambah 5 paket MIUI baru
   ```
4. Push & buka **Pull Request** ke branch `main`.
5. Jelaskan: merek HP, versi Android, dan dari mana kamu tahu paketnya.

### Format pesan commit (disarankan)
```
db(<merek>): ringkasan        # perubahan database
fix: ringkasan                # perbaikan bug
feat: ringkasan               # fitur baru
docs: ringkasan               # dokumentasi
```

---

## ✅ Checklist Sebelum PR

- [ ] Format database `package|nama|risk` benar.
- [ ] Tidak memasukkan paket inti / whitelist.
- [ ] `bash -n aud.sh` lolos (jika mengubah kode).
- [ ] Tidak ada perintah root / `pm uninstall` sebagai default.
- [ ] Sudah diuji di HP sungguhan (sebutkan merek & Android-nya).

---

## 🙏 Kode Etik

Ikuti [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Bersikap sopan & saling membantu.

Terima kasih sudah berkontribusi! ⭐
