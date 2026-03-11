# PRAKTIKUM: Hands On Function in Python

**Mata Kuliah:** Pemrograman Berorientasi Object
 
**Pertemuan:** 03

---


**Format dasar function:**

```python
def nama_function():
    print("Hello, ini function pertamaku")

#Untuk menjalankan function, cukup panggil namanya
nama_function()
```

**Function dengan Parameter**

Parameter ditentukan setelah nama fungsi, di dalam tanda kurung. Kita dapat menambahkan perintah sebanyak yang kita inginkan, cukup pisahkan dengan koma.

```python
def sapa(nama):
    print(f"Halo, {nama}! Ada yang bisa dibantu?")

sapa("Alicia")
```

**Hands On**

Jika saya ingin membuat nama "***Felda Ramadhan***"
Bagaimana cara untuk melengkapi program dibawah ini ???

```python
def sapa(nama):
    print("Halo, " + nama + "!")

sapa("Felda Ramadhan")
```

**Function dengan Default Parameter**

Kita juga bisa memberikan nilai default pada parameter

```python
def sapa(nama="User"):
    print(f"Halo, {nama}")

sapa()
sapa("Raihan Noval")
```

* Fungsi sapa memiliki satu parameter bernama "nama", yang memiliki nilai default "User".
* print(f"Halo, {nama}") digunakan untuk mencetak teks "Halo, {nama}" dengan nilai nama yang diberikan.

**Function dengan Return Value**

Function bisa mengembalikan nilai dengan *return*

```python
def tambah(a, b):
    return a + b

hasil = tambah(5, 3)
print(hasil)
```

Penjelasan:

*return* diatas bertugas untuk mengembalikan hasilnya ke pemanggil

Kita mendefinisikan fungsi bernama tambah yang menerima dua parameter, a dan b.
* return a + b: Mengembalikan hasil penjumlahan dari a dan b.
* Fungsi tambah(5, 3) dipanggil dengan nilai a = 5 dan b = 3.
* Fungsi tambah mengembalikan hasil 5 + 3 = 8, yang kemudian disimpan dalam variabel hasil.

**Function dengan Banyak Parameter (Arbitrary Arguments)**

Jika jumlah parameter tidak diketahui, kita bisa gunakan *args atau **kwargs

```python
# *args untuk banyak argumen tanpa nama
def jumlahkan(*angka):
    return sum(angka)

print(jumlahkan(1, 2, 3, 4))
```

```python
# **kwargs untuk banyak argumen dengan nama
def Biodata(**data):
    for key, value in data.items():
        print(f"{key}: {value}")

Biodata(nama="Yasin Aprian", umur=19, kota="Batam")
```

1. **data mengumpulkan semua argumen yang dikirim dalam bentuk dictionary.
2. data.items() digunakan untuk mengakses setiap key dan value dalam dictionary tersebut.
3. print(f"{key}: {value}") akan mencetak setiap pasangan key-value dalam format **key** : **value**.

**Hands On**

Buatlah fungsi untuk mencari "***Luas Lingkaran dan Keliling Lingkaran***" dengan jari-jari 15 cm.

1. Luas Lingkaran = 3.14 * jari-jari**2
2. keliling Lingkaran = 2 * 3.14 * jari-jari

```python
# Function untuk menghitung luas lingkaran
def luas_lingkaran(jari_jari):
    pi = 3.14
    return pi * jari_jari ** 2

# Function untuk menghitung keliling lingkaran
def keliling_lingkaran(jari_jari):
    pi = 3.14
    return 2 * pi * jari_jari

print("Luas Lingkaran:", luas_lingkaran(15))
print("Keliling Lingkaran:", keliling_lingkaran(15))
```
