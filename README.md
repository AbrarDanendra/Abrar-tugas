# =======================================================================
# Sistem Manajemen Perpustakaan Sederhana
# Menggunakan Function – Cocok untuk Pembelajaran Python Dasar
# =======================================================================

# Data awal perpustakaan
perpustakaan = [
    {"judul": "Belajar Python untuk Pemula", "penulis": "Andi", "tahun": 2020, "status": "Tersedia"},
    {"judul": "Algoritma dan Struktur Data", "penulis": "Budi", "tahun": 2019, "status": "Dipinjam"},
    {"judul": "Jaringan Komputer Dasar", "penulis": "Citra", "tahun": 2021, "status": "Tersedia"},
]

# ================================================================
# Function untuk menampilkan seluruh buku
# ================================================================
def tampilkan_buku():
    print("\n=== Daftar Buku di Perpustakaan ===")
    if len(perpustakaan) == 0:
        print("Tidak ada buku dalam perpustakaan.")
        return
    
    for i, buku in enumerate(perpustakaan, start=1):
        print(f"{i}. {buku['judul']} | {buku['penulis']} | {buku['tahun']} | Status: {buku['status']}")
    print("====================================")


# ================================================================
# Function untuk menambah buku baru
# ================================================================
def tambah_buku():
    print("\n=== Tambah Buku Baru ===")
    judul = input("Masukkan judul buku : ")
    penulis = input("Masukkan nama penulis: ")
    tahun = int(input("Masukkan tahun terbit: "))

    buku_baru = {
        "judul": judul,
        "penulis": penulis,
        "tahun": tahun,
        "status": "Tersedia"
    }

    perpustakaan.append(buku_baru)
    print(f"Buku '{judul}' berhasil ditambahkan!")


# ================================================================
# Function untuk menghapus buku
# ================================================================
def hapus_buku():
    tampilkan_buku()
    print("\n=== Hapus Buku ===")
    judul_hapus = input("Masukkan judul buku yang ingin dihapus: ")

    for buku in perpustakaan:
        if buku["judul"].lower() == judul_hapus.lower():
            perpustakaan.remove(buku)
            print(f"Buku '{judul_hapus}' berhasil dihapus!")
            return
    
    print("Buku tidak ditemukan!")


# ================================================================
# Function untuk mencari buku berdasarkan judul
# ================================================================
def cari_buku():
    print("\n=== Cari Buku ===")
    kata_kunci = input("Masukkan judul atau bagian judul: ")

    hasil = []
    for buku in perpustakaan:
        if kata_kunci.lower() in buku["judul"].lower():
            hasil.append(buku)
    
    if len(hasil) == 0:
        print("Tidak ada buku yang cocok dengan pencarian.")
    else:
        print("\nHasil Pencarian:")
        for i, buku in enumerate(hasil, 1):
            print(f"{i}. {buku['judul']} | {buku['penulis']} | {buku['tahun']} | Status: {buku['status']}")


# ================================================================
# Menu utama
# ================================================================
def menu():
    while True:
        print("\n==============================")
        print("   SISTEM PERPUSTAKAAN MINI  ")
        print("==============================")
        print("1. Tampilkan Semua Buku")
        print("2. Tambah Buku")
        print("3. Hapus Buku")
        print("4. Cari Buku")
        print("5. Keluar")
        print("==============================")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            tampilkan_buku()
        elif pilihan == "2":
            tambah_buku()
        elif pilihan == "3":
            hapus_buku()
        elif pilihan == "4":
            cari_buku()
        elif pilihan == "5":
            print("Program selesai. Terima kasih!")
            break
        else:
            print("Pilihan tidak valid, coba lagi!")


# ================================================================
# Jalankan Program
# ================================================================
menu()
