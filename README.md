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