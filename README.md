# Tugas PBP | Aliyah Nahisa Sugiana | 2306275405

A new Flutter project.

## Tugas Individu 7
1. **Stateless Widget vs Stateful Widget**:  
   Stateless widget adalah widget yang tidak memiliki state internal dan tetap sama setelah dibuat. Contohnya adalah teks atau ikon yang tidak berubah. Sebaliknya, stateful widget memiliki state yang dapat berubah selama siklus hidup widget. Misalnya, tombol yang mengubah tampilan ketika ditekan. Perbedaan utama adalah bahwa stateful widget dapat berubah secara dinamis, sedangkan stateless widget tetap statik.

2. **Widget yang Digunakan**:  
   Beberapa widget yang digunakan dalam proyek ini adalah:
   - `Scaffold`: Struktur dasar halaman yang menyediakan layout standar seperti `AppBar` dan `body`.
   - `AppBar`: Menampilkan header di bagian atas halaman.
   - `Card`: Menampilkan konten dalam kotak dengan efek bayangan.
   - `GridView.builder`: Menampilkan item dalam bentuk grid.
   - `Icon` dan `Text`: Menampilkan ikon dan teks di dalam `ItemCard`.
   - `InkWell`: Menangani interaksi pengguna, seperti tap pada kartu.

3. **Fungsi `setState()`**:  
   Fungsi `setState()` digunakan untuk memperbarui state dalam stateful widget. Fungsi ini memberi tahu Flutter untuk merender ulang widget dengan perubahan terbaru. Variabel yang didefinisikan di dalam kelas yang menggunakan state (di dalam `_MyHomePageState`, misalnya) akan terdampak oleh `setState()`.

4. **Perbedaan `const` dan `final`**:  
   `const` digunakan untuk nilai konstan yang tidak akan pernah berubah dan harus ditentukan pada waktu kompilasi. `final` digunakan untuk nilai yang hanya diinisialisasi sekali dan bisa ditentukan saat runtime. `const` lebih ketat dibandingkan `final`, sedangkan `final` memungkinkan penentuan nilai yang dinamis.

5. **Implementasi Checklist**:  
   Untuk implementasi checklist di atas, saya menambahkan widget sesuai fungsi masing-masing, misalnya `AppBar` untuk header, `Card` dan `GridView.builder` untuk layout grid, dan menggunakan `setState()` saat ingin memperbarui tampilan berdasarkan interaksi pengguna.

## Tugas Individu 8
1. **Kegunaan `const` di Flutter**:  
   `const` digunakan untuk mendeklarasikan nilai yang tidak berubah sepanjang aplikasi berjalan. Keuntungannya adalah peningkatan performa karena objek `const` diinisialisasi sekali dan dapat digunakan berulang kali. Sebaiknya gunakan `const` pada widget statis, sementara pada data yang bersifat dinamis jangan digunakan.

2. **Penggunaan `Column` dan `Row` di Flutter**:  
   `Column` menyusun widget secara vertikal, cocok untuk tempat letak seperti daftar atau formulir. Sementara itu, `Row` menyusun widget secara horizontal dan sesuai untuk baris ikon atau teks. Keduanya memungkinkan pengaturan alignment sesuai kebutuhan tempat letak.

3. **Elemen Input pada Halaman Form**:  
   Pada halaman form yang saya buat kali ini, elemen input yang digunakan adalah:
      a. TextFormField untuk input Game: Digunakan untuk memasukkan nama game. Memiliki validasi agar tidak kosong.
      b. TextFormField untuk input Price: Digunakan untuk memasukkan harga game. Memiliki validasi agar hanya menerima angka.
      c. TextFormField untuk input Description: Digunakan untuk memasukkan deskripsi game. Juga memiliki validasi agar tidak kosong.

4. **Mengatur Tema (Theme) dalam Aplikasi Flutter**:  
   Tema diatur dengan `ThemeData` pada `MaterialApp` untuk menciptakan tampilan yang konsisten dalam aplikasi. Tema ini memungkinkan kontrol penuh atas warna, font, dan style di seluruh aplikasi. Tema dasar telah diterapkan dalam proyek ini.

5. **Menangani Navigasi dalam Aplikasi Flutter**:  
   Navigasi antarhalaman diatur menggunakan `Navigator` dan `MaterialPageRoute`. `Navigator.push` digunakan untuk membuka halaman baru, sedangkan `Navigator.pop` untuk kembali. Metode ini memastikan alur navigasi berjalan dengan baik pada aplikasi yang memiliki banyak halaman.

## Tugas Individu 9
1. **Mengapa perlu model untuk JSON?**  
   Model diperlukan untuk mempermudah konversi data JSON menjadi objek Dart, sehingga data dapat diolah lebih efisien. Jika tidak membuat model, aplikasi tetap bisa berfungsi, tetapi penanganan data menjadi lebih sulit, rawan error, dan kurang terstruktur.

2. **Fungsi library `http`**  
   Library `http` digunakan untuk melakukan komunikasi antara aplikasi Flutter dengan server, seperti pengambilan data menggunakan GET atau pengiriman data menggunakan POST. Library ini membantu menangani permintaan HTTP dengan mudah.

3. **Fungsi dan pentingnya `CookieRequest`**  
   `CookieRequest` digunakan untuk menangani sesi pengguna dengan menyimpan cookie. Instance-nya dibagikan ke seluruh komponen agar data sesi tetap konsisten di semua halaman, memungkinkan pengguna tetap login tanpa perlu autentikasi ulang.

4. **Mekanisme pengiriman data**  
   Data yang diinput pengguna dikirim melalui permintaan HTTP (biasanya POST) ke server. Server memproses data, menyimpan ke basis data, lalu merespons dengan data baru yang dikirim kembali ke aplikasi untuk ditampilkan.

5. **Mekanisme autentikasi**  
   Pada login, data pengguna dikirim dari Flutter ke Django menggunakan POST. Django memverifikasi data, lalu mengembalikan token atau cookie sesi jika valid. Pada register, data pengguna baru dikirim, disimpan di basis data, lalu pengguna diarahkan ke halaman login. Saat logout, sesi pengguna dihapus, baik di Flutter maupun Django.

6. **Implementasi checklist secara step-by-step**  
   - Membuat model untuk memetakan data JSON ke objek Dart.  
   - Menggunakan library `http` untuk mengirim atau menerima data dari API Django.  
   - Mengatur instance `CookieRequest` untuk manajemen sesi.  
   - Menambahkan logika login, register, dan logout dengan endpoint API.  
   - Membuat halaman untuk input dan menampilkan data dengan menghubungkannya ke fungsi-fungsi API.  