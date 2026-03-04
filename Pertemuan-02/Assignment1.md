
# PRAKTIKUM: Object Oriented Programming (OOP) 

**Mata Kuliah:** Pemrograman Berorientasi Object
 
**Pertemuan:** 02

**Assinment:** 01
---


## Soal - Soal : 

---

- 1. Sebuah kendaraan sedang melakukan perjalanan di dalam kota dan harus melewati enam lampu lalu lintas secara berurutan. Setiap kali melewati satu lampu, pengemudi harus menyesuaikan kecepatan kendaraan sesuai dengan kondisi lampu yang dihadapi. Jika lampu berwarna hijau, kendaraan dapat berjalan lebih cepat dengan menambah kecepatan sebesar 20 km/jam. Jika lampu berwarna kuning, kendaraan harus melambat sehingga kecepatan berkurang 10 km/jam. Namun, jika lampu berwarna merah, kendaraan harus berhenti dan kecepatan menjadi 0 km/jam. Kecepatan kendaraan tidak boleh melebihi 100 km/jam dan tidak boleh kurang dari 0 km/jam.  
Buatlah sebuah program Python yang mensimulasikan kondisi tersebut dengan menggunakan perulangan for untuk memproses enam lampu lalu lintas, serta menggunakan percabangan if-elif-else untuk menentukan perubahan kecepatan berdasarkan warna lampu yang dimasukkan oleh pengguna. Di akhir simulasi, tampilkan kecepatan akhir kendaraan setelah melewati seluruh lampu lalu lintas.

----
- 2. Sebuah kendaraan memiliki tiga mode berkendara, yaitu Mode Santai, Mode Normal, dan Mode Sport. Kecepatan awal kendaraan adalah 0 km/jam. Mode Santai menambah kecepatan 10 km/jam, Mode Normal menambah 20 km/jam, dan Mode Sport menambah 30 km/jam. Kendaraan juga dapat melambat dengan mengurangi kecepatan sesuai input pengguna. Program harus terus berjalan sampai pengguna memilih keluar 
Buatlah program Python menggunakan while loop untuk menampilkan menu secara berulang. Menu yang ditampilkan adalah:
1 untuk memilih Mode Santai,
2 untuk memilih Mode Normal,
3 untuk memilih Mode Sport,
4 untuk mengurangi kecepatan,
5 untuk melihat status kendaraan,
6 untuk keluar.
Gunakan percabangan if-elif-else untuk menentukan perubahan kecepatan. Kecepatan maksimal adalah 150 km/jam dan tidak boleh kurang dari 0 km/jam. Jika kecepatan mencapai batas maksimal, tampilkan pesan "Kecepatan maksimal tercapai". Jika kecepatan 0, tampilkan "Kendaraan berhenti".
---
- 3. Sebuah kendaraan memiliki kecepatan awal 0 km/jam dan dapat berjalan atau melambat sesuai perintah pengguna. Program simulasi akan terus berjalan sampai pengguna memilih keluar. Selain menambah dan mengurangi kecepatan, sistem juga memiliki fitur peringatan jika kendaraan melaju terlalu cepat.Buatlah program Python menggunakan while loop agar program berjalan terus sampai pengguna memilih keluar. Tampilkan menu:
1 untuk menambah kecepatan,
2 untuk mengurangi kecepatan,
3 untuk melihat status kendaraan,
4 untuk keluar.
Gunakan percabangan if-elif-else untuk memproses pilihan pengguna. Ketentuan program adalah kecepatan maksimal 120 km/jam dan tidak boleh kurang dari 0 km/jam. Jika kecepatan lebih dari 80 km/jam, tampilkan pesan "Hati-hati, kecepatan tinggi!". Jika kecepatan sama dengan 0, tampilkan "Kendaraan berhenti". Jika kecepatan lebih dari 0, tampilkan "Kendaraan berjalan".
---
- 4. Sebuah kendaraan memiliki kecepatan awal 0 km/jam. Kendaraan tersebut dapat berjalan dengan menambah kecepatan, melambat dengan mengurangi kecepatan, dan berhenti apabila kecepatannya mencapai 0 km/jam. Program simulasi kendaraan ini harus berjalan terus-menerus hingga pengguna memilih untuk keluar dari program. Pengguna akan diberikan beberapa pilihan menu untuk mengontrol kendaraan, seperti menambah kecepatan, mengurangi kecepatan, melihat status kendaraan, atau keluar dari program.
Buatlah sebuah program Python untuk mensimulasikan kondisi tersebut dengan menggunakan while loop agar program terus berjalan sampai pengguna memilih menu keluar. Tampilkan menu pilihan sebagai berikut:
1 untuk menambah kecepatan,
2 untuk mengurangi kecepatan,
3 untuk melihat status kendaraan, dan
4 untuk keluar dari program.
Gunakan percabangan if-elif-else untuk memproses pilihan yang dimasukkan pengguna. Ketentuan dalam program adalah kecepatan maksimal kendaraan sebesar 120 km/jam dan kecepatan tidak boleh kurang dari 0 km/jam. Jika kecepatan sama dengan 0, tampilkan pesan "Kendaraan berhenti", sedangkan jika kecepatan lebih dari 0, tampilkan pesan "Kendaraan berjalan".
---

- 5. Sebuah kendaraan memiliki kecepatan awal 0 km/jam dan bahan bakar awal sebanyak 50 liter. Kendaraan dapat berjalan dengan menambah kecepatan, melambat dengan mengurangi kecepatan, atau berhenti jika kecepatan menjadi 0 km/jam. Setiap kali kendaraan berjalan (kecepatan > 0), bahan bakar akan berkurang 5 liter setiap putaran menu. Program harus terus berjalan sampai pengguna memilih keluar atau bahan bakar habis.
Buatlah program Python menggunakan while loop agar menu terus muncul sampai pengguna memilih keluar. Tampilkan menu pilihan:
1 untuk menambah kecepatan,
2 untuk mengurangi kecepatan,
3 untuk melihat status kendaraan dan sisa bahan bakar,
4 untuk keluar dari program.
Gunakan percabangan if-elif-else untuk memproses pilihan pengguna. Kecepatan maksimal adalah 120 km/jam dan tidak boleh kurang dari 0 km/jam. Jika bahan bakar habis, tampilkan pesan "Bahan bakar habis, kendaraan berhenti" dan program otomatis berhenti.