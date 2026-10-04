# Proyek Algoritma: Binary Search (Pencarian Biner)

---

## Penjelasan Singkat
Algoritma **Binary Search** digunakan untuk mencari posisi nilai target pada array yang sudah terurut (*sorted array*). Algoritma ini bekerja dengan membagi rentang pencarian menjadi dua bagian secara berulang hingga data ditemukan.

* **Kompleksitas Waktu (*Time Complexity*)**: $\mathcal{O}(\log N)$
* **Kompleksitas Ruang (*Space Complexity*)**: $\mathcal{O}(1)$

---

##  Struktur Repositori

```text
.
├── README.md
└── main.py
```

---

##  Kode Program (`main.py`)

```python
# main.py - Program Pencarian Biner (Binary Search)

def binary_search(data, target):
    kiri = 0
    kanan = len(data) - 1
    
    while kiri <= kanan:
        tengah = (kiri + kanan) // 2
        if data[tengah] == target:
            return tengah  # Ditemukan
        elif data[tengah] < target:
            kiri = tengah + 1
        else:
            kanan = tengah - 1
            
    return -1  # Tidak ditemukan

if __name__ == "__main__":
    angka = [2, 5, 8, 12, 16, 23, 38, 56, 72, 91]
    target = 23

    hasil = binary_search(angka, target)

    print("=== PROGRAM BINARY SEARCH ===")
    print(f"Data Terurut : {angka}")
    print(f"Cari Angka   : {target}")

    if hasil != -1:
        print(f"Hasil        : Angka ditemukan pada indeks ke-{hasil}")
    else:
        print("Hasil        : Angka tidak ditemukan")
```

---
