Berikut adalah tahapan dari mulai autentikasi login menggunakan akun Google hingga aplikasi mendapatkan data profil dan username:

 1. Memulai Proses Login dengan Google
   - Pada aplikasi, pengguna akan melihat tombol untuk "Login with Google" atau serupa.
   - Ketika pengguna menekan tombol ini, aplikasi menginisialisasi permintaan login melalui layanan autentikasi Google. Proses ini biasanya menggunakan pustaka autentikasi atau SDK yang disediakan oleh Google, seperti Firebase Authentication atau Google Sign-In SDK.
   
 2. Pengarahan ke Halaman Login Google
   - Aplikasi mengarahkan pengguna ke halaman login Google melalui URL khusus atau pop-up login.
   - Pengguna diminta untuk memasukkan kredensial Google mereka atau memilih akun yang sudah masuk di perangkat.
   - Pada tahap ini, Google memastikan identitas pengguna dan meminta persetujuan pengguna untuk berbagi data tertentu dengan aplikasi, seperti nama, email, dan gambar profil.

 3. Penerimaan Token Akses (Access Token)
   - Setelah pengguna berhasil login, Google mengembalikan Access Token ke aplikasi. Token ini adalah bukti bahwa pengguna telah terverifikasi dan memberikan izin aplikasi untuk mengakses data profil mereka.
   - Token ini dikirimkan melalui callback atau secara langsung ke aplikasi.

 4. Meminta Data Profil dari Google
   - Dengan menggunakan Access Token, aplikasi melakukan permintaan (request) ke Google API untuk mengambil data profil pengguna.
   - Aplikasi mengirimkan request ke endpoint API Google, seperti `https://www.googleapis.com/oauth2/v3/userinfo`, yang memberikan respons berisi informasi profil pengguna.

 5. Mendapatkan dan Menampilkan Data Pengguna
   - Google API merespons dengan mengirimkan data profil pengguna dalam format JSON, yang umumnya mencakup informasi seperti:
     - Nama pengguna
     - Alamat email
     - Foto profil
   - Aplikasi kemudian menampilkan data ini pada halaman profil atau halaman lain yang sesuai. Pengguna dapat melihat nama, foto, dan informasi lainnya yang diambil langsung dari akun Google mereka.

 6. Penyimpanan dan Penggunaan Data
   - Data yang diperoleh dapat disimpan sementara di aplikasi, seperti di `state` atau `local storage` agar tetap tersedia selama sesi pengguna berlangsung.
   - Aplikasi dapat menggunakan data ini untuk menampilkan nama pengguna di bagian header atau profil dan mempersonalisasi pengalaman pengguna di dalam aplikasi.

Tampilan Halaman:
![Screenshot 2024-11-18 191528](https://github.com/user-attachments/assets/16920fb6-9c2f-475e-a86d-c39043673c7b)

Halaman Login ini memungkinkan pengguna untuk melakukan autentikasi dengan akun Google. Saat pengguna menekan tombol Login with Google, aplikasi memulai proses autentikasi yang diarahkan ke halaman login Google. Setelah berhasil login, aplikasi akan menerima data seperti username, email, dan foto profil.



![Screenshot 2024-11-18 192020](https://github.com/user-attachments/assets/fafd5e8d-8029-47eb-a553-012e18c3c94f)

Pada halaman Home, pengguna akan melihat tampilan utama aplikasi setelah berhasil login. Halaman ini menyajikan informasi dasar serta navigasi menuju halaman lain seperti Profil



![Screenshot 2024-11-18 192034](https://github.com/user-attachments/assets/006f9a3b-c96b-4ffa-b58a-881f52616c5b)

Halaman Profil menampilkan informasi pribadi yang diambil dari akun Google pengguna, termasuk nama, email, dan foto profil. Informasi ini diperoleh setelah autentikasi dan diambil menggunakan token akses dari Google. Pengguna dapat melihat informasi pribadi mereka di sini, yang disinkronkan secara otomatis dengan akun Google.



Tampilan Create

![Screenshot 2024-11-26 202606](https://github.com/user-attachments/assets/2496b378-1ced-44be-9cd9-f098e59bf6a3)

Pada tampilan Create, pengguna dapat menambahkan item baru ke dalam daftar tugas. Pengguna mengisi form dengan informasi seperti judul dan deskripsi tugas, lalu mengklik tombol "Add Todo" untuk menyimpan tugas baru ke Firebase.

Tampilan Read

![Screenshot 2024-11-26 202628](https://github.com/user-attachments/assets/0e75262b-f736-4b5d-b886-62a8eb97e7d2)

Tampilan Read menampilkan daftar tugas yang tersimpan di database Firebase. Setiap tugas memiliki detail seperti judul, deskripsi singkat, dan waktu terakhir diperbarui.

Tampilan Update

![Screenshot 2024-11-26 202658](https://github.com/user-attachments/assets/3fa43a77-6702-44da-bf77-005df7900afb)

Di tampilan Update, pengguna dapat memperbarui informasi tugas yang sudah ada. Saat pengguna memilih tugas, form edit akan terbuka dengan informasi yang bisa diperbarui, seperti judul dan deskripsi.

Tampilan Delete

![Screenshot 2024-11-26 202804](https://github.com/user-attachments/assets/615f192b-085c-4e92-a33e-7e28b5c67d1f)

Untuk menghapus tugas, pengguna dapat melakukan swipe atau klik ikon "Trash". Sistem akan menghapus tugas tersebut dari daftar dan database Firebase.

Cara build apk

``
npx cap open android
``

lalu build di android studio

setelah selesai, buka folder lalu masuk ke android/app/build/output lalu install pada bagian .APK



SS Tampilan APK
![WhatsApp Image 2024-11-26 at 18 45 38_05072688](https://github.com/user-attachments/assets/a10ca9d1-4dcb-4be5-a3ec-847c1c03fbc3)


