
---

# 📘 Studi Kasus: Fungsi Python — *calculate_discount()*

## 🎯 Tujuan Fungsi

Fungsi ini digunakan untuk menghitung harga akhir sebuah produk setelah diberikan diskon. Fungsi menerima:

* **harga awal**
* **persentase diskon**
* **opsional: batas maksimum diskon (jika ada)**

## 📝 Deskripsi Singkat

Fungsi akan:

1. Menghitung jumlah diskon berdasarkan persentase.
2. Memastikan diskon tidak melebihi batas maksimum (jika ditentukan).
3. Menghasilkan harga final setelah diskon diterapkan.
4. Mengembalikan data berupa detail perhitungan.

---

# 📂 Contoh Studi Kasus & Output

## **Studi Kasus 1:** Diskon Tanpa Batas Maks

**Input:**

* Harga awal: `100000`
* Diskon: `20%`

**Output (contoh):**

```
Harga awal      : 100000
Persentase diskon: 20%
Jumlah diskon    : 20000
Harga akhir      : 80000
```

---

## **Studi Kasus 2:** Diskon Dengan Batas Maksimum

**Input:**

* Harga awal: `250000`
* Diskon: `50%`
* Maksimal diskon: `80000`

**Output (contoh):**

```
Harga awal         : 250000
Persentase diskon  : 50%
Hitungan diskon     : 125000
Batas diskon maksimal: 80000
Diskon diterapkan   : 80000
Harga akhir         : 170000
```

---

## **Studi Kasus 3:** Diskon Sangat Kecil

**Input:**

* Harga awal: `50000`
* Diskon: `2%`

**Output (contoh):**

```
Harga awal      : 50000
Persentase diskon: 2%
Jumlah diskon    : 1000
Harga akhir      : 49000
```

---

## **Studi Kasus 4:** Diskon 100%

**Input:**

* Harga awal: `75000`
* Diskon: `100%`

**Output (contoh):**

```
Harga awal      : 75000
Persentase diskon: 100%
Jumlah diskon    : 75000
Harga akhir      : 0
```

---

