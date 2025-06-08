---
title: "Huffman Coding: Kompresi Teks Optimal dengan Pendekatan Greedy"
date: 2025-06-08
categories: [Algoritma, Greedy, Struktur Data]
tags: [huffman, greedy, algoritma, kompresi]
---

## Apa Itu Huffman Coding?

Huffman Coding adalah algoritma kompresi lossless yang digunakan untuk mengurangi ukuran data dengan mengubah karakter-karakter dalam teks menjadi kode biner yang panjangnya bervariasi. Karakter yang sering muncul diberi kode yang lebih pendek, sedangkan karakter yang jarang muncul diberi kode yang lebih panjang.
Algoritma ini ditemukan oleh David A. Huffman dan merupakan salah satu contoh algoritma *greedy* paling terkenal di bidang pengolahan data dan komunikasi.

---

## Langkah-langkah Algoritma Huffman Coding

1. Hitung frekuensi kemunculan setiap karakter dalam teks.
2. Buat simpul (node) untuk setiap karakter beserta frekuensinya.
3. Gabungkan dua simpul dengan frekuensi terendah menjadi satu simpul baru.
4. Ulangi langkah 3 hingga hanya tersisa satu simpul (pohon Huffman lengkap).
5. Dari pohon tersebut, buat kode biner untuk tiap karakter:
   - Kiri diberi angka 0
   - Kanan diberi angka 1

---

## Contoh Perhitungan Huffman Coding

Misalkan kita ingin mengompres string berikut:


### 1. Hitung Frekuensi

| Karakter | Frekuensi |
|----------|-----------|
| A        | 5         |
| B        | 2         |
| R        | 2         |
| C        | 1         |
| D        | 1         |

### 2. Buat Daftar Node dan Gabungkan

Kita gabungkan node dengan frekuensi terkecil berulang kali:

- Gabung C (1) + D (1) → CD (2)
- Gabung B (2) + R (2) → BR (4)
- Gabung CD (2) + BR (4) → CD-BR (6)
- Gabung A (5) + CD-BR (6) → A-CD-BR (11)

Pohon selesai dibuat.

### 3. Buat Kode Biner

Dari pohon di atas, kita tetapkan:

- A → 0  
- C → 100  
- D → 101  
- B → 110  
- R → 111

*Catatan: kode bisa bervariasi tergantung arah kiri/kanan, tapi tetap valid asal prefix-free.*

---

## 4. Kompresi

Kata **ABRACADABRA** jika dikodekan:

- A → 0  
- B → 110  
- R → 111  
- C → 100  
- D → 101  

Maka hasil encoding:  
0 110 111 0 100 0 101 0 110 111 0

Total bit: **27 bit**

Jika setiap huruf awalnya 3-bit (karena ada 5 karakter unik → perlu 3 bit tetap), maka:

- Panjang asli: 11 huruf × 3 bit = 33 bit  
- Setelah dikompres: 27 bit

**Penghematan: 6 bit (~18%)**

---

## Kesimpulan

Huffman Coding adalah solusi optimal untuk kompresi teks berbasis frekuensi. Algoritma ini efisien karena memanfaatkan sifat greedy, di mana karakter dengan frekuensi tinggi dikodekan lebih pendek. Cocok digunakan dalam sistem kompresi file, transmisi data, hingga algoritma dasar dalam file ZIP dan JPEG.

---
