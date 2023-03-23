# Tugas 2 Pemrograman Jaringan
- Nama: Kurnia Cahya Febryanto
- NRP: 5025201073
- Kelas: Pemrograman Jaringan A

## Daftar Isi
- [Deskripsi](#deskripsi)
- [Implementasi Client dan Server](#implementasi-client-dan-server)

## Deskripsi
Buatlah program client untuk Tugas 2 dengan mengimplementasikan ketentuan di tugas 2 dengan metode
### 1. Thread
- Membuat file `client_thread.py` untuk implementasi thread dalam client.
- Import library yang diperlukan seperti sys, socket, logging, dan threading. </br>
<img src="https://user-images.githubusercontent.com/70510279/227042491-93c4c85d-3889-471c-97a5-942515547c0c.png" width="100"/>

- Buat fungsi `kirim_data()` yang digunakan untuk membuat socket, mengirimkan pesan ke server, dan menerima respons dari server. </br>
<img src="https://user-images.githubusercontent.com/70510279/227042770-80c53593-2f78-4ba3-a645-b8b90df91dff.png" width="300"/>

- Buat fungsi `create_thread()` untuk menjalankan fungsi `kirim_data()`.  </br>
<img src="https://user-images.githubusercontent.com/70510279/227043559-6a1fa97c-0e07-445b-8fc9-f30bc90c5ed3.png" width="300"/>
- Pada bagian `main`, koda akan menjalankan thread sebanyak yang diinginkan menggunakan iterasi. </br>
<img src="https://user-images.githubusercontent.com/70510279/227044087-268f8513-0698-46ce-8755-6a95be5b7586.png" width="300"/>

### 2. Threadpool
- Membuat file `client_threadpool.py` untuk implementasi threadpool dalam client.
- Import library yang diperlukan seperti sys, socket, logging, dan ThreadPoolExecutor. </br>
<img src="https://user-images.githubusercontent.com/70510279/227099297-9a528792-d0a5-463f-81b0-33896aede8aa.png" width="300"/>

- Buat fungsi `kirim_data()` yang digunakan untuk membuat socket, mengirimkan pesan ke server, dan menerima respons dari server dan mencetaknya dengan logging. </br>
<img src="https://user-images.githubusercontent.com/70510279/227099474-0dac194a-36d6-4bfc-93eb-053845da4292.png" width="300"/>

- Pada bagian `main`, menjalankan ThreadPoolExecutor menggunakan iterasi for loop sehingga bisa menjalankan fungsi kirim_data dengan sesuai banyak iterasi yang diinginkan. </br>
<img src="https://user-images.githubusercontent.com/70510279/227105760-85b2b18b-a29e-410a-b108-092dcb421b57.png" width="300"/>

### 3. Process
- Membuat file `client_process.py` untuk implementasi Process dalam client.
- Import library yang diperlukan seperti sys, socket, logginng, dan process. </br>
<img src="https://user-images.githubusercontent.com/70510279/227106023-59bb6449-de68-4d80-9f90-63df76d9944a.png" width="300"/>

- Buat fungsi `kirim_data()` untuk melakukan pembuatan socket, mengirim pesan, dan menerima respons dari server. </br>
<img src="https://user-images.githubusercontent.com/70510279/227106070-1c0cf587-8c1d-4803-b0e9-8a152527ba83.png" width="300"/>

- Buat fungsi `create_process()` untuk menjalakan fungsi `kirim_data()`. Fungsi `create_process` berguna untuk membuat objek `Process` serta memulai prosess. </br>
<img src="https://user-images.githubusercontent.com/70510279/227106175-6861fbf4-7c73-467e-8955-f55f7cd20c6a.png" width="300"/>

- Pada bagian `main`, menjalankan fungsi `create_process()` dan akan dijalankan secara iterasi sesuai yang diinginkan. </br>
<img src="https://user-images.githubusercontent.com/70510279/227106229-c0cfd9e8-51e8-4fb2-b33f-30c0e3ac5599.png" width="300"/>

## Implementasi Client dan Server
Jalankan server pada tugas 2, lalu, untuk setiap metode pada nomor 1, jalankan tugas 3 nomor 1 dan amatilah jumlah maksimum thread yang dapat dijalankan di lingkungan eksekusi anda. </br>

Pada bagian file server, saya tambahkan perhitungan untuk menghitung berapa banyak respons yang diterima server. Bisa dilihat pada potongan kode berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227106367-7df193cc-4761-4983-87a9-6d1be98cf9a2.png" width="500"/>

### 1. Thread
- Untuk melakukan perbandingan dengan metode lain, maka `client_thread.py` dijalankan dengan waktu yang ditentukan.
- Selain itu, juga simpan jumlah thread yang terkoneksi dengan server selama waktu tersebut.
- Implementasi tambahan kode pada file `client_thread.py` bisa dilihat sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227106581-d9a56544-63e4-4807-8e41-d22a91bee951.png" width="500"/>

- Bisa dilihat pada pada file client_thread.py, program akan dijalankan selama <b>30 detik</b> dan mencetak total jummlah threads. 
- Ketika dijalankan dengan command `python3 client_thread.py`, maka hasilnya sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227106822-cfe7b110-0e00-4e0f-a25e-4de373e28ee6.png" width="300"/>

- Pada terminal server, keluar output sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227109799-5a63835d-e5ae-4937-b568-ab2efe787df3.png" width="300"/>

### 2. Threadpool
- Untuk melakukan perbandingan dengan metode lain, maka `client_threadpool.py` dijalankan dengan waktu yang ditentukan.
- Selain itu, juga simpan jumlah thread yang terkoneksi dengan server selama waktu tersebut.
- Implementasi tambahan kode pada file `client_threadpool.py` bisa dilihat sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227113533-51a43a62-aca2-4384-87a8-227f524ee286.png" width="500"/>

- Bisa dilihat pada pada file `client_threadpool.py`, program akan dijalankan selama <b>30 detik</b> dan mencetak total jummlah threads. 
- Ketika dijalankan dengan command `python3 client_threadpool.py`, maka hasilnya sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227113714-aaf7dc51-1585-46f8-9fac-8d9bd31b121d.png" width="300"/>

- Pada terminal server, keluar output sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227113897-e15ff817-867c-4d3e-aebd-d2f02b76d153.png" width="300"/>

### 3. Process
- Untuk melakukan perbandingan dengan metode lain, maka `client_process.py` dijalankan dengan waktu yang ditentukan.
- Selain itu, juga simpan jumlah thread yang terkoneksi dengan server selama waktu tersebut.
- Implementasi tambahan kode pada file `client_process.py` bisa dilihat sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227114928-244227e5-f5dc-4321-b7c9-d4d0723e2a81.png" width="500"/>

- Bisa dilihat pada pada file client_process.py, program akan dijalankan selama <b>30 detik</b> dan mencetak total jummlah threads. 
- Ketika dijalankan dengan command `python3 client_process.py`, maka hasilnya sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227115058-93c61675-2eae-4edd-956d-8cdcf225208c.png" width="300"/>

- Pada terminal server, keluar output sebagai berikut: </br>
<img src="https://user-images.githubusercontent.com/70510279/227115140-b66b3eae-4291-4094-bc3a-c008fe31af6c.png" width="300"/>

## Kesimpulan
Setiap process metode client yang dijalankan selama 30 detik sehingga pengukurang yang dilakukan berdasarkan request dan response yang dikirim dan diterima selama waktu 30 detik. Adapun kesimpulan hasilnya sebagai berikut: </br>

| Jenis Metode Client | Request yang dikirimkan    | Response yang dikirimkan server    | Request yang tidak diterima | Persentase |
| :---:   | :---: | :---: | :---: | :---: |
| Client Thread | 6250   | 6250   | 0   | 100%   |
| Client Threadpool | 908   | 11501   | 10593   | 7.89%   |
| Client Process | 2730   | 2730   | 0   | 100%   |

</br>
Bisa dilihat pada hasil di atas bahwa dalam 30 detik, client thread mengirimkan 6250 request dan server mengirimkan dengan hasil yang sama. Sedangkan, client process mengirimkan 2730 request dan server  mengirimkan dengan hasil yang sama. Hal yang berbeda adalah pada client threadpool bisa dilihat bahwa request hanya mengirimkan 908, sedangkan response mengirimkan 11501. Hal tersebut kemungkinan bisa terjadi bottlenect pada server saat proses dengan client threadpool atau juga terjadi timeout sehingga request membutuhkan waktu yang lebih lama daripada yang ditentukan. Dari hasil juga dilihat bahwa metode client thread dan client process memiliki kinerja yang baik. 