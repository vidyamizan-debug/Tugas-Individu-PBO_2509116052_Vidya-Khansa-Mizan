# **Sistem Pengelolaan Layanan Perawatan Hewan - Kya's Pet Care**

# Vidya Khansa Mizan |  2509116052 | Sistem Informasi B 2025

## Deskripsi Program
Sistem Pengelolaan Layanan Perawatan Hewan adalah sebuah program berbasis bahasa pemrograman Java yang digunakan untuk mengelola data layanan perawatan hewan secara sederhana. Program ini berfokus pada layanan perawatan kebersihan dan penampilan hewan, yaitu Perawatan (mandi, potong kuku, perawatan bulu) dan Penitipan (jasa menitipkan hewan selama jangka waktu tertentu). Program ini memungkinkan pengguna untuk melakukan CRUD (Create, Read, Update, Delete) sederhana terhadap data layanan tersebut.

## Class yang ada di Program ini
**1. Minpro2PBOKyaPetCare.java**\
Merupakan class utama atau entry point yang digunakan untuk menjalankan program. Class ini menampilkan menu utama, menerima input pilihan dari pengguna, dan memanggil fungsi yang sesuai dari class CRUDLayananKyaPetCare.java.

**2. Layanan.java**\
Merupakan class entitas (superclass) yang menyimpan informasi umum mengenai layanan perawatan hewan, seperti ID layanan, nama layanan, deskripsi, harga, serta data hewan terkait (nama hewan, nama pemilik, jenis hewan, ras hewan, umur hewan). Class ini menerapkan constructor, getter, setter, dan encapsulation.

**3. Perawatan.java**\
Merupakan class entitas (subclass dari Layanan) yang menambahkan atribut khusus jenisPerawatan, digunakan untuk data layanan yang berfokus pada kebersihan dan penampilan hewan.

**4. Penitipan.java**\
Merupakan class entitas (subclass dari Layanan) yang menambahkan atribut khusus lamaPenitipan, digunakan untuk data layanan jasa menitipkan hewan selama jangka waktu tertentu.

**5. CekKyaPetCare.java**\
Merupakan class yang menangani validasi seluruh input dari pengguna, seperti validasi angka, validasi angka harus lebih dari 0, validasi string tidak boleh kosong, validasi pilihan menu, dan validasi jawaban ya atau tidak.

**6. CRUDLayananKyaPetCare.java**\
Merupakan class yang menangani proses CRUD pada program. Class ini menggunakan ArrayList untuk menyimpan data layanan. Class ini menyediakan fungsi untuk menambah, menampilkan, mengubah, dan menghapus data layanan.

**7. Menu.java**
Merupakan class yang menampilkan tampilan menu utama program ke layar.

## Alur Perencanaan Program
Alur program dimulai ketika program dijalankan melalui class Minpro2PBOKyaPetCare.java. Program akan menampilkan menu utama yang berisi lima pilihan, yaitu Tambah Data Layanan, Tampilkan Data Layanan, Update Data Layanan, Hapus Data Layanan, dan Keluar.

Pengguna memilih menu dengan memasukkan angka sesuai pilihan. Program kemudian menggunakan percabangan untuk menentukan proses yang akan dijalankan berdasarkan pilihan pengguna. Pada menu Tambah Data, Tampilkan Data, Hapus Data, dan Update Data. Berbeda dengan pengerjaan sebelumnya yang memisahkan data Pemilik, Hewan, dan Layanan, pada Minpro 2 ini data hewan dan pemilik digabungkan menjadi atribut di dalam data Layanan itu sendiri, sehingga satu data layanan sudah mewakili satu transaksi lengkap untuk satu hewan. Pengguna cukup memilih jenis layanannya (Perawatan atau Penitipan) saat menambah data.

## Penerapan Encapsulation
Encapsulation diterapkan pada seluruh class di package model, yaitu class Layanan, Perawatan, Penitipan.

<img width="207" height="133" alt="image" src="https://github.com/user-attachments/assets/4cc0280c-653f-47b7-83c7-df127387cc68" />

Seperti yang dapt dilihat pada gambar di atas, seluruh atribut yang berada di dalam class Layanan, yang nantinya akan diturunkan ke subclass, dibuat menjadi protected. Sehingga data tidak dapat diakses langsung dari luar class. Untuk atribut id dibuat menjadi private final, sehingga hanya bisa sekali lewat di constructor dan tidak memiliki setter.

<img width="197" height="39" alt="image" src="https://github.com/user-attachments/assets/2da2dd8a-66f9-4905-8c74-412623e2c69d" />


<img width="293" height="41" alt="image" src="https://github.com/user-attachments/assets/e8027d65-d902-427f-816c-925a32c743d0" />

Setiap atribut yang boleh diubah memiliki getter dan setter, sehingga perubahan data hanya bisa dilakukan lewat method yang sudah disediakan. Hal ini berlaku untuk semua atribut kecuali atribut id.

## Penerapan Inheritance
Inheritance diterapkan pada class yang berada di package model.

<img width="619" height="310" alt="image" src="https://github.com/user-attachments/assets/116dd1b4-bb86-4c20-af6c-3b10657240e7" />

Seperti yang dapat dilihat pada gambar di atas, class Layanan merupakan superclass yang menyimpan atribut umum (idLayanan, namaLayanan, deskripsi, harga) beserta data hewan terkait (namaHewan, namaPemilik, jenisHewan, rasHewan, umurHewan).

<img width="685" height="119" alt="image" src="https://github.com/user-attachments/assets/094c72b7-b78b-48ac-b155-92ae59613c92" />

<img width="683" height="121" alt="image" src="https://github.com/user-attachments/assets/6ed64378-fbcd-45e5-8aba-e471bc3c494c" />

Kedua gambar di atas menunjukkan bahwa class  Perawatan dan Penitipan merupakan subclass yang menggunakan extends Layanan, sehingga mewarisi seluruh atribut dan method dari Layanan, ditambah atribut khusus masing-masing (jenisPerawatan untuk Perawatan, lamaPenitipan untuk Penitipan). Kedua subclass tersebut memanggil constructor superclass menggunakan super(...) untuk mengisi atribut umum sebelum mengisi atribut khususnya sendiri.

## Penerapan Nilai Tambah

**1. Tampilan Menu Utama**

<img width="178" height="141" alt="image" src="https://github.com/user-attachments/assets/a28c81b8-86ac-4cf1-92ed-22fe2d7c5c20" />

gambar di atas merupakan tampilan awal atau yang biasa disebut menu utama dari program yang telah saya rancang dan jalankan. Dapat dilihat bahwa menu utamanya memiliki 5 pilihan utama, yaitu menambah data, menampilkan data, menghapus data, mengupdate data, dan menu keluar. 

**2. Tambah Data**

<img width="178" height="101" alt="image" src="https://github.com/user-attachments/assets/63b2f7b5-1066-4567-bf9b-7994004d5810" />

Setelah memilih menu nomor pertama, maka kita akan dialihkan ke pilihan menu untuk menambahkan data pemilik hewan, hewan yang akan dilayani, ataupun pelayanan yang ingin ditambahkan datanya.

- Tambah Data Pemilik

<img width="191" height="116" alt="image" src="https://github.com/user-attachments/assets/0ffcb981-24b2-48c9-8bc5-b15857b5da3d" />

Jika memilih untuk menambahkan data pemilik, maka kita akan diminta untuk mengisi formulir data seperti pada gambar di atas.

- Tambah Data Hewan

<img width="185" height="128" alt="image" src="https://github.com/user-attachments/assets/e5ad43aa-d34f-49db-852f-78ea8d5d6c39" />

Jika memilih untuk menambahkan data hewan, maka kita akan diminta untuk mengisi formulir data seperti pada gambar di atas.

- Tambah Data Layanan

<img width="237" height="115" alt="image" src="https://github.com/user-attachments/assets/b52eed40-6917-42c7-a06e-48dbddffa4c2" />

Jika memilih untuk menambahkan data layanan, maka kita akan diminta untuk mengisi formulir data seperti pada gambar di atas.

**3. Tampilkan Data**

<img width="181" height="101" alt="image" src="https://github.com/user-attachments/assets/d1fe2dd3-1d15-42af-8c98-bb9a43e51a9d" />

Setelah memilih menu nomor kedua, maka kita akan dialihkan ke pilihan menu untuk menampilkan seluruh data pemilik hewan, hewan yang akan dilayani, ataupun pelayanan yang ingin ditampilkan datanya.

- Tambah Data Pemilik

<img width="183" height="116" alt="image" src="https://github.com/user-attachments/assets/1273ca9d-d6a8-4ec3-bac6-7a50ec52e659" />

Jika memilih untuk menampilkan data pemilik yang telah dibuat, maka sistem akan menampilkan data pemilik yang tersimpan seperti pada gambar di atas.

- Tambah Data Hewan

<img width="184" height="128" alt="image" src="https://github.com/user-attachments/assets/3926684c-ca45-4375-bf17-9b89068ee0c0" />

Jika memilih untuk menampilkan data hewan yang telah dibuat, maka sistem akan menampilkan data pemilik yang tersimpan seperti pada gambar di atas.

- Tambah Data Layanan

<img width="232" height="113" alt="image" src="https://github.com/user-attachments/assets/5a186067-721a-4351-96e9-70e10260b790" />

Jika memilih untuk menampilkan data layanan yang telah dibuat, maka sistem akan menampilkan data pemilik yang tersimpan seperti pada gambar di atas.

**4. Hapus Data**

<img width="179" height="100" alt="image" src="https://github.com/user-attachments/assets/ab9d3220-76fc-4bc3-8f91-7a7546b14e45" />

Setelah memilih menu nomor ketiga, maka kita akan dialihkan ke pilihan menu untuk menghapus data dari pemilik hewan, hewan yang akan dilayani, ataupun pelayanan yang ingin dihapus datanya.

<img width="175" height="178" alt="image" src="https://github.com/user-attachments/assets/be80175b-c062-4661-ab45-ea7714e213dd" />

Disini, saya memilih untuk menghapus data yang tersimpan di dalam data layanan. Dan dapat dilihat bahwa data berhasil untuk dihapus.

**5. Update Data**

<img width="179" height="100" alt="image" src="https://github.com/user-attachments/assets/a751ae90-c17d-4640-8c24-6760f8b6a4d1" />

Setelah memilih menu nomor keempat, maka kita akan dialihkan ke pilihan menu untuk mengupdate data yang telah tersimpan di daya pemilik hewan, hewan yang akan dilayani, ataupun pelayanan yang ingin diupdate datanya.

<img width="181" height="229" alt="image" src="https://github.com/user-attachments/assets/e7aae0d6-e793-4926-958f-8c082b9dbff4" />

Disini, saya memilih untuk mengupdate data ynag telah tersimpan di dalam data hewan. Saya mengupdate jenis ras nya yang awalnya ialah ras 'anggora', menjadi ras 'himalayan'.

**6. Keluar**

<img width="185" height="168" alt="image" src="https://github.com/user-attachments/assets/0d77035a-d627-4f05-abc9-7c0ba4c1c314" />

Jika jita memilih menu nomor kelima, maka kita akan dikeluarkan dari sistem.
