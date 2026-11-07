Panduan Pemasangan E-Folio Melalui Google Apps Script

Sistem ini menggunakan Google Sheets sebagai pangkalan data dan Google Drive sebagai storan fail. Setiap jabatan boleh menyalin (Copy) sistem ini secara berasingan.

Langkah 1: Sediakan Pangkalan Data (Google Sheet)

Buka Google Sheets.

Klik + Blank (helaian kosong) untuk mencipta dokumen baharu.

Namakan fail tersebut mengikut jabatan (contoh: DB E-FOLIO UNIT KOKURIKULUM).

PENTING: Anda tidak perlu mencipta tab atau memasukkan tajuk lajur secara manual. Sistem akan menjana tab APP_USERS, APP_RECORDS, dan lain-lain secara automatik pada Langkah 5.

Langkah 2: Buka Google Apps Script

Di dalam Google Sheet yang anda buka tadi, klik menu Extensions (Sambungan) > Apps Script.

Satu tetingkap baharu akan terbuka.

Langkah 3: Masukkan Kod Backend (Code.gs)

Di dalam editor Apps Script, cari fail bernama Code.gs di panel kiri.

Padam semua kod sedia ada di dalamnya.

Salin (Copy) keseluruhan kod dari Fail 1 (Code.gs) di atas dan tampal (Paste) ke dalam editor.

Klik ikon Save (💾).

Langkah 4: Masukkan Kod Frontend (Index.html)

Di editor Apps Script, klik ikon + (Tambah fail) di sebelah kiri, pilih HTML.

Namakan fail tersebut sebagai Index (huruf besar 'I', tanpa .html).

Padam semua kod sedia ada.

Salin keseluruhan kod dari Fail 2 (Index.html) di atas dan tampal.

Klik ikon Save (💾).

Langkah 5: Deploy Web App (Kali Pertama)

Di penjuru atas kanan, klik butang Deploy > New deployment.

Klik ikon gear (⚙️) di sebelah Select type dan pilih Web app.

Isikan butiran:

Description: E-Folio App v1

Execute as: Me (Akaun anda)

Who has access: Anyone (Sesiapa sahaja yang mempunyai pautan)

Klik Deploy.

Tetingkap kebenaran (Authorize) akan muncul. Klik Authorize access.

Pilih akaun Google anda, klik Advanced > Go to [Nama Projek] (unsafe), dan klik Allow.

Salin (Copy) Web app URL yang diberikan.

Langkah 6: Kemas Kini URL Web App (Penting)

Kembali ke editor Apps Script.

Buka fail Code.gs.

Cari baris ini (di bahagian atas):
const WEB_APP_URL = 'https://script.google.com/...';

Gantikan URL lama dengan Web app URL yang anda salin pada Langkah 5 tadi.

Klik Save (💾).

Langkah 7: Deploy Versi Baharu

Klik Deploy > Manage deployments.

Klik ikon Pensel (Edit).

Pada bahagian Version, pilih New version.

Klik Deploy. (Ini penting supaya URL baharu digunakan untuk fungsi e-mel).

Langkah 8: Ujian & Log Masuk Admin

Buka Web app URL di pelayar anda.

Log masuk menggunakan akaun Admin lalai (sila ubah di dalam kod jika perlu):

Emel: admin@ipgm.edu.my

Kata Laluan: 987654321

Sistem kini bersedia digunakan. Akaun Admin akan melihat menu Panel Pemantau dan Senarai Semak EOMS.
