---
title: "Subset Sum Problem: Menemukan Kombinasi Angka yang Tepat"
date: 2025-06-08
categories: [Algoritma, Backtracking, Dynamic Programming]
tags: [subset sum, backtracking, dp, algoritma]
---

## Apa Itu Subset Sum Problem?

**Subset Sum Problem** adalah masalah klasik dalam ilmu komputer:  
> Diberikan sebuah himpunan bilangan bulat dan sebuah target, apakah ada **subset** dari bilangan tersebut yang jumlahnya **sama dengan target**?

Masalah ini berkaitan erat dengan optimasi dan teori himpunan, dan sering menjadi dasar untuk pemahaman awal algoritma **backtracking** dan **dynamic programming**.

---

## Contoh Kasus

Misalkan kita punya:

- Himpunan: {3, 34, 4, 12, 5, 2}  
- Target: 9

Pertanyaannya:  
> Apakah ada subset dari himpunan tersebut yang jika dijumlahkan hasilnya 9?

### Jawaban:
Ya, karena:
- 4 + 5 = 9  
- atau 3 + 4 + 2 = 9

---

## Pendekatan Penyelesaian

Ada beberapa cara untuk menyelesaikan masalah ini:

### 1. **Backtracking (Brute Force)**

- Periksa semua kemungkinan subset dari himpunan.
- Cek apakah jumlahnya sama dengan target.
- Cocok untuk himpunan kecil, tapi sangat lambat jika jumlah elemen besar (kompleksitas eksponensial).

### 2. **Dynamic Programming (DP)**

- Gunakan tabel 2D untuk menyimpan informasi:  
  `dp[i][j] = true` jika subset dari elemen ke-1 sampai ke-i bisa menghasilkan jumlah j.
- DP jauh lebih efisien dibanding backtracking untuk jumlah data besar.
- Kompleksitas waktu: **O(n × target)**

---

## Visualisasi Tabel DP

Misal kita punya himpunan {2, 3, 7, 8, 10}, target = 11.  
Kita buat tabel dengan baris = elemen, kolom = nilai dari 0 sampai 11.

Kita isi tabel berdasarkan:
- Apakah elemen tersebut bisa digunakan untuk mencapai jumlah tertentu?
- Apakah mungkin mencapai jumlah itu tanpa elemen tersebut?

Hasil akhirnya akan menunjukkan apakah target bisa dibentuk dari subset atau tidak.

---

## Kasus yang Lebih Sulit

Masalah ini juga bisa dikembangkan menjadi:

- **Count of Subset Sum**: Berapa banyak subset yang memenuhi target?
- **Subset Sum Closest**: Subset dengan jumlah mendekati target.
- **Partition Problem**: Bisakah array dibagi dua dengan jumlah yang sama?  
  → Ini variasi dari subset sum dengan target = total/2.

---

## Aplikasi Dunia Nyata

Subset Sum bukan sekadar teka-teki matematika. Ia digunakan dalam:

- **Kriptografi**
- **Pemrograman keuangan (alokasi anggaran)**
- **Pemecahan masalah kombinatorial**
- **Pengujian sistem keamanan berdasarkan kompleksitas subset**

---

## Kesimpulan

Subset Sum Problem adalah latihan penting dalam memahami algoritma eksploratif dan strategi optimasi. Dari brute force hingga dynamic programming, masalah ini menuntut pemahaman struktur data dan efisiensi solusi.

Apakah kamu bisa menantang dirimu untuk menyelesaikan Subset Sum dengan dataset besar?

---

