KALITIRTO - ANDROID APK BUILD STARTER

Isi proyek:
- www/: aplikasi web KALITIRTO yang sudah ada, dibundel secara lokal.
- capacitor.config.json: identitas aplikasi Android.
- .github/workflows/build-apk.yml: workflow untuk membangun APK debug melalui GitHub Actions.

CARA BUILD DARI HP:
1. Upload seluruh isi ZIP ini ke root repository GitHub kalitirto (termasuk folder .github).
2. Commit perubahan ke branch main.
3. Buka tab Actions pada repository.
4. Pilih workflow "Build KALITIRTO APK".
5. Tekan Run workflow dan konfirmasi Run workflow.
6. Tunggu job selesai dengan tanda hijau.
7. Buka hasil run, bagian Artifacts, unduh KALITIRTO-debug-apk.
8. Ekstrak ZIP artifact dan instal app-debug.apk di Android.

CATATAN PENTING:
- Ini menghasilkan APK debug untuk uji coba, bukan APK rilis bertanda tangan untuk distribusi publik.
- Database aplikasi di APK terpisah dari database browser website. Pengguna menyatakan belum ada data penting, sehingga pengujian dapat dimulai dari data kosong.
- Aplikasi web dibundel lokal sehingga konten inti tidak membutuhkan internet saat dijalankan.
- PDF saat ini memakai window.open()/window.print() dari browser. Fitur ini perlu diuji di Android WebView; mungkin memerlukan penyesuaian native print bila tidak bekerja.
- Unduh file CSV/JSON melalui Blob juga perlu diuji pada WebView Android. Jangan anggap fungsi cetak/unduh sudah lolos uji sebelum dites pada HP.
- APK debug saat ini belum ditandatangani sebagai release build.
