# PRAKTIKUM: OOP Paradigm Concepts

**Mata Kuliah:** Pemrograman Berorientasi Object
 
**Pertemuan:** 03

---


## Object Oriented Programming (OOP) di Python

Dalam paradigma OOP, sebuah code pemograman akan dibagi-bagi menjadi beberapa kelas-kelas. Kelas-Kelas tersebut kemudian akan dibungkus menjadi beberapa objek. Nah, objek-objek inilah yang kemudian akan saling berinteraksi dan membangun pemograman kita.

Objek adalah sesuatu yang memiliki identitas berupa atribut dan dapat memiliki behaviour (prilaku) berdasarkan suatu aksi.

Contoh:
Misalkan kita sedang membangun sebuah objek yang dinamakan "MOBIL"
- Mobil memiliki atribut berupa jenis mobil (sedan, jeep, truk), merek, warna, setir, pedal, rem, ban, dll.
- Mobil memiliki prilaku atau aksi berupa berjalan cepat, berjalan rambat, mengerem, membunyikan klakson dll.

### Mendefinisikan Class dalam OOP

Semua hal dalam python sebenarnya dapat kita pandang sebagai objek. Objek tersebut dibangun dari kelas. Jadi, kita dapat memandang bahwa kelas adalah suatu rancangan atau suatu *blueprint* untuk membangun suatu objek.

Untuk membuat class dalam python, dapat menggunakan keyword **class** diikuti dengan tanda petik dua (:)

```python
# mendefinisikan kelas untuk membangun objek untuk mobil
class car :
    car_type = '...'
    color = '...'

print(...)
```

#### Membuat Objek dari Suatu Kelas

Kita tahu bahwa kelas merupakan suatu konstruktor atau rancangan dari suatu objek. Untuk membuat suatu objek, kita dapat meng-assign kelas yang telah kita buat sebelumnya dalam suatu objek.

```python
# Buat objek berupa "mobil_ayah" dari kelas mobil
mobil_ayah = ...()

# print untuk melihat spesifikasi mobil_ayah
print("--- Informasi Mobil Ayah ---")
print("Jenis mobil ayah :",...)
print("Warna mobil ayah :",...)
```

Dari output diatas bisa dilihat bahwa mobil ayah dan mobil adik merupakan dua objek yang berbeda atau tidak sama, walaupun berasal dari kelas yang sama

#### Fungsi `__init__`

Di bagian sebelumnya, kita sudah mendefinisikan class secara sederhana. Namun, hal itu belum cukup dan belum ada manfaatnya untuk aplikasi atau program yang kompleks. Untuk dapat memahami class lebih jauh, kita perlu mengetahui fungsi bawaan python yaitu `__init__`. Fungsi `__init__` digunakan untuk menginisiasi class yang akan membentuk objek. Biasanya fungsi ini berisikan nilai atau data yang akan mendeskripsikan properti suatu objek. Di fungsi ini juga dapat berisi operasi lain yang dilakukan ketika suatu objek diinisiasi.

Fungsi `__init___` didefinisikan seperti kita mendefinisikan suatu fungsi python.

**Default Constructor**

```python
class Mobil:
    def __init__(self):
        self.jenis_mobil = "Sedan"
        self.warna_mobil = "Hitam"
        self.dapat_menyala = False

mobil_baru = Mobil()
print(mobil_baru.jenis_mobil)
```

Di default Contructor, setiap objek **Mobil** yang dibuat akan memiliki jenis mobil "Sedan", warna "Hitam".

**Parameterized Constructor**

```python
class Mobil:
    def __init__(self, jenis, warna, ada_aki):
        self.jenis_mobil = jenis
        self.warna_mobil = warna
        self.dapat_menyala = self.starter(ada_aki)

    def starter(self, aki):
        if aki:
            return True
        else:
            return False

# Membuat objek mobil_ayah dan mobil_adik dari konstruktor kelas
mobil_ayah = Mobil("sedan", "merah", True)
mobil_adik = Mobil("jeep", "hijau", False)
```

```python
print(f"""
--- Informasi Mobil Ayah ---
Jenis mobil: {mobil_ayah.jenis_mobil}
Warna mobil: {mobil_ayah.warna_mobil}
Apakah menyala? {mobil_ayah.dapat_menyala}
""")

print(f"""
--- Informasi Mobil Adik ---
Jenis mobil: {mobil_adik.jenis_mobil}
Warna mobil: {mobil_adik.warna_mobil}
Apakah menyala? {mobil_adik.dapat_menyala}
""")
```

Hands On!
Buat suatu kelas bernama User

```python
# Membuat kelas User
class User:
    def __init__(self, username, email, umur):
        ...
        ...
        ...

    def info_user(self):
        return f"Username: {self....}, Email: {self....}, Umur: {self...}"

# Membuat objek dari kelas User
...

# Menampilkan informasi pengguna
...
```

#### Instance Variable

Selain memiliki atribut, sebuah objek juga dapat memiliki method (atau biasa kita juga mengenalnya sebagai fungsi). Method ini akan dilaksanakan ketika kita memanggil objek kita beserta method yang akan dilakukan.

```python
# Membuat class Mobil

# Mobil tersebut akan menghabiskan 5 liter bensin setiap kilometernya

class Mobil:
    def __init__(self,jenis,warna,bensin = 100) :
        self.jenis_mobil = jenis
        self.warna_mobil = warna
        self.liter_bensin = bensin
        self.kilometer = 0

    def jalan_maju(self,jumlah_km) :
      # aksi apabila ada bensin (bensin tidak kurang dari sama dengan nol)
      if self.liter_bensin > 0 :
        # menghitung bensin yang masih tersisa untuk melakukan aksi
        sisa_bensin = self.liter_bensin - jumlah_km*5

        # apabila sisa bensin lebih dari nol
        if sisa_bensin > 0 :
            self.kilometer += jumlah_km
            self.liter_bensin = sisa_bensin
            print(f"mobil maju {jumlah_km} km, sekarang mobil berada di posisi {self.kilometer} km dari titik awal. Bensin tersisa tinggal {self.liter_bensin}")
        # apabila sisa bensin kurang dari nol
        else :
            self.kilometer += self.liter_bensin/5
            print(f"Bensin tidak cukup! Mobil hanya maju {self.liter_bensin/5} km. Sekarang mobil di posisi {self.kilometer} dari posisi awal. Bensin sudah habis!")
            self.liter_bensin -= jumlah_km*5

      # apabila bensin tidak ada (minus atau sama dengan nol, maka mobil tidak bisa melakukan aksi apa-apa)
      else :
            print(f"mobil tidak ada bensin, jadi tidak bisa maju!")

    def jalan_mundur(self,jumlah_km) :
      # aksi apabila ada bensin (bensin tidak kurang dari sama dengan nol)
        if self.liter_bensin > 0 :
            # menghitung bensin yang masih tersisa untuk melakukan aksi
                sisa_bensin = self.liter_bensin - jumlah_km*5

                # apabila sisa bensin lebih dari nol
                if sisa_bensin > 0 :
                    self.kilometer -= jumlah_km
                    self.liter_bensin = sisa_bensin
                    print(f"mobil maju {jumlah_km} km, sekarang mobil berada di posisi {self.kilometer} km dari titik awal. Bensin tersisa tinggal {self.liter_bensin}")
                # apabila sisa bensin kurang dari nol
                else :
                    self.kilometer -= self.liter_bensin/5
                    print(f"Bensin tidak cukup! Mobil hanya mundur {self.liter_bensin/5} km. Sekarang mobil di posisi {self.kilometer} dari posisi awal. Bensin sudah habis!")
                    self.liter_bensin -= jumlah_km*5

          # apabila bensin tidak ada (minus atau sama dengan nol,
          # maka mobil tidak bisa melakukan aksi apa-apa)
        else :
            print(f"mobil tidak ada bensin, jadi tidak bisa maju!")

    def isi_bensin(self):
        self.liter_bensin = 100
        print("bensin mobil sudah terisi penuh!")

mobil_ayah = Mobil("jeep", "merah")
mobil_ayah.jalan_maju(10)
mobil_ayah.jalan_mundur(30)
mobil_ayah.jalan_maju(5)
mobil_ayah.isi_bensin()
mobil_ayah.jalan_maju(2)
```

Thank you :)

# Hands On

Buatlah class Lingkaran yang memiliki atribut : jari-jari 10 cm, pi = 3.14159
dengan method Luas Lingkaran dan Keliling Lingkaran

```python
class Lingkaran:
    ...
```
