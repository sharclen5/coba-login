# PrakPemmobMinggu8

Cara Kerja Login :

1. Proses di Database: User memasukkan username dan password yang kemudian dicek ke database dengan password disimpan dalam format MD5. Jika benar, user bisa masuk, jika salah, maka user harus mengulang.

2. Alur di Backend (PHP): File koneksi.php menghubungkan aplikasi ke database dengan  (Cross-Origin Resource Sharing) supaya bisa diakses dari aplikasi Ionic, dan login.php memproses login. Kemudian akan dicocokkan dengan database. Jika sesuai, sistem mengirimkan token dan status login berhasil.

3. Alur di Ionic (Frontend): Service authentication.service.ts mengatur penyimpanan token dan username menggunakan Preferences. Guard memastikan akses hanya untuk pengguna yang sudah login. Halaman login memvalidasi input dan menampilkan pesan jika ada kesalahan atau masalah koneksi.

4. Penyimpanan Data: Data login disimpan dalam Preferences dengan key auth-login (untuk token) dan auth-user (untuk username) hingga user melakukan logout, setelah itu data dihapus.

5. Keamanan: Password disimpan dalam MD5, login divalidasi dengan token, route dilindungi dengan Guard, dan API menggunakan CORS.


## Screenshot
<img src="src/assets/image/login.png">
<img src="src/assets/image/sukses.png">
