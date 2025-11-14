Berikut contoh *studi kasus* sederhana tentang **Python Function** yang bisa langsung kamu jadikan `README.md` untuk GitHub. Bahasa dibuat jelas dan rapi agar terlihat profesional.

---

# 📘 Studi Kasus: Menggunakan Function di Python

Proyek sederhana ini dibuat untuk mempelajari dasar penggunaan **function (fungsi)** dalam Python dengan contoh studi kasus yang mudah dipahami.

## 🎯 Tujuan

* Memahami cara mendefinisikan dan memanggil fungsi di Python.
* Menggunakan parameter dan *return value*.
* Menerapkan fungsi dalam sebuah studi kasus nyata.

---

# 🧩 Studi Kasus: Program Penghitung Diskon Sederhana

Kita akan membuat fungsi untuk menghitung harga akhir sebuah barang setelah diberikan diskon. Fungsi ini akan menerima:

* `harga`: harga awal barang
* `diskon`: persentase diskon (contoh: 20 untuk 20%)

### 🔍 Flow sederhana:

1. User memasukkan harga barang.
2. User memasukkan diskon yang ingin diberikan.
3. Program memanggil fungsi `hitung_diskon()`.
4. Fungsi mengembalikan harga setelah diskon.

---

# 📄 Contoh Kode

```python
def hitung_diskon(harga, diskon):
    """
    Menghitung harga akhir setelah diskon.

    Parameter:
    - harga (int/float): Harga awal barang.
    - diskon (int/float): Persentase diskon.

    Returns:
    - float: Harga akhir setelah diskon diterapkan.
    """
    potongan = harga * (diskon / 100)
    harga_akhir = harga - potongan
    return harga_akhir


# Contoh penggunaan fungsi
harga_barang = float(input("Masukkan harga barang: "))
persen_diskon = float(input("Masukkan diskon (%): "))

hasil = hitung_diskon(harga_barang, persen_diskon)

print(f"Harga setelah diskon: Rp{hasil:,.2f}")
```

---

# 🧪 Contoh Output

```
Masukkan harga barang: 150000
Masukkan diskon (%): 20
Harga setelah diskon: Rp120,000.00
```

---

# 📦 Apa yang Dipelajari?

✔ Cara membuat fungsi
✔ Cara menerima parameter
✔ Cara mengembalikan nilai dengan `return`
✔ Cara menerapkan fungsi untuk menyelesaikan masalah nyata

---

# 🚀 Pengembangan Selanjutnya

Kamu bisa mengembangkan program ini dengan:

* Menambahkan validasi input
* Membuat menu interaktif
* Menyimpan data barang ke file `.json` atau `.csv`
* Membuat versi GUI dengan `tkinter`

---


