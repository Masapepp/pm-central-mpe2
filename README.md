# PM CENTRAL Enterprise V7.2 – MPE2 Cloudflare Edition

## Identitas aplikasi
- Application: PM CENTRAL Enterprise
- Team: MPE2
- Developer: Masapep / BWK
- Developer / Creator: Masapep / BWK
- Release: V7.2 Cloudflare Edition
- Hosting: Cloudflare Workers
- Source repository: GitHub `Masapepp/pm-central-mpe2`
- Production URL: https://pm-central-enterprise.afifhaidara.workers.dev

Footer aplikasi menampilkan “Developed & Designed by Masapep / BWK” dan “An Internal Digital Maintenance Initiative – MPE2 Team”. Dashboard menampilkan identitas MPE2 dan platform Cloudflare Workers.

## Struktur menu
- Menu utama: PE, NPE, Analyzer & Bagging.
- Analyzer & Bagging: Bagging (PM Ink Jet Printer), BFR, Analyzer (PM Analyzer WTP), Product Warehouse.
- Dokumen pendukung terpisah: PM Compliance dan Daily Schedule MPE2. Keduanya memiliki halaman tersendiri, iframe SharePoint, dan tombol untuk membuka file langsung.
- Dashboard memisahkan tiga workspace tim dari dua dokumen bersama menggunakan jarak, garis pemisah, dan kartu dengan aksen warna berbeda; tema gelap enterprise sebelumnya dipertahankan.
- PE dan NPE adalah halaman awal/placeholder; link form dan sumber data belum diberikan.

## Integrasi link
- PM Ink Jet Printer: Google Apps Script URL terbaru yang diberikan pengguna.
- PM Analyzer WTP: Google Apps Script URL terbaru yang diberikan pengguna.
- PM Compliance: SharePoint link baru milik Dudi Hermansyah yang diberikan pengguna pada pembaruan V7.2.
- Daily Schedule MPE2: SharePoint sharing link yang diberikan pengguna sebelumnya.

## Catatan akses SharePoint
Tampilan iframe bergantung pada kebijakan Microsoft 365/SharePoint dan hak akses file. Jika iframe diblokir atau meminta login, gunakan tombol Buka di SharePoint. Link sharing bukan pengganti autentikasi atau Microsoft Graph API. Kredensial tidak disimpan di frontend.

## Batasan saat ini
- Link Google Apps Script dibuka di dalam iframe dengan tombol fallback tab baru.
- Data equipment, schedule, work order dan upload lokal tetap tersimpan di browser/perangkat sesuai implementasi sebelumnya.
- Belum ada integrasi Microsoft Graph API, upload otomatis ke OneDrive, sinkronisasi lintas perangkat, database terpusat, atau role-based access control.
- PE dan NPE belum memiliki form karena URL modulnya belum diberikan.
- Aplikasi sudah berhasil dimuat pada alamat Cloudflare Workers yang tercantum di atas; perubahan source code berikutnya tetap perlu di-commit dan deploy agar tampil di production.

## Deploy / update melalui GitHub dan Cloudflare
1. Buka repository: https://github.com/Masapepp/pm-central-mpe2
2. Upload/replace file project V7.2 pada branch `main` (pastikan file berada di root project).
3. Commit changes.
4. Buka Cloudflare Dashboard → Workers & Pages → worker `pm-central-enterprise` → Deployments.
5. Jalankan deployment dari repository/branch yang terhubung atau gunakan deployment flow yang sebelumnya berhasil.
6. Buka production URL dan periksa dashboard serta PM Compliance.

Build: `npm run build`
Test: `npm test`
Verify: `npm run verify`

## Catatan penting
- Project masih mempertahankan file `netlify.toml` dari baseline untuk kompatibilitas historis; hosting aktif yang ditampilkan pada versi ini adalah Cloudflare Workers.
- Jangan menyimpan API keys, tokens, password, atau secret di source code publik.
