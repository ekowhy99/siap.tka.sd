# Tryout TKA SD (halaman Vercel)

Halaman ini membungkus web app Google Apps Script supaya aplikasi bisa dibuka lewat alamat Vercel.
Data, login, dan soal tetap berjalan di Apps Script dan Google Sheet.

- `index.html` memuat aplikasi Apps Script dalam satu layar penuh.
- Bila web app di-deploy dengan URL baru, ganti nilai `GAS_URL` di `index.html`, lalu commit ke GitHub. Vercel akan memperbarui situs otomatis.

Syarat di Apps Script:
- `doGet()` di `Code.gs` memakai `.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)`.
- Deploy sebagai *Web app*: Execute as **Me**, Who has access **Anyone**.
