---
title: "N-Queens Problem: Menempatkan Ratu Tanpa Saling Serang"
date: 2025-06-08
categories: [Algoritma, Backtracking]
tags: [n-queens, backtracking, algoritma, rekursi]
---

## Apa Itu N-Queens Problem?

**N-Queens Problem** adalah tantangan klasik dalam algoritma dan rekayasa perangkat lunak: menempatkan **N buah ratu** di papan catur berukuran **N×N** sedemikian rupa sehingga **tidak ada dua ratu** yang saling menyerang.

Artinya, tidak boleh ada dua ratu yang berada di **baris**, **kolom**, atau **diagonal** yang sama.

---

## Contoh Kasus: 4-Queens

Tujuannya: Letakkan 4 ratu di papan 4×4 tanpa saling menyerang.

Salah satu solusi:


Keterangan:  
`Q` = posisi ratu  
`.` = posisi kosong  

- Ratu di baris 1, kolom 2  
- Ratu di baris 2, kolom 4  
- Ratu di baris 3, kolom 1  
- Ratu di baris 4, kolom 3  

Semua ratu aman: tidak ada yang berada di baris, kolom, atau diagonal yang sama.

---

## Pendekatan Penyelesaian

Masalah ini diselesaikan secara efisien dengan **backtracking**. Inti dari pendekatan ini adalah mencoba satu per satu kemungkinan penempatan ratu di setiap baris, lalu:

1. **Cek validitas** posisi: apakah ratu tidak diserang dari kolom atau diagonal.
2. **Jika valid**, lanjut ke baris berikutnya.
3. **Jika tidak valid**, mundur (backtrack) dan coba posisi lain.
4. Ulangi hingga semua ratu berhasil ditempatkan.

---

## Kompleksitas dan Tantangan

- Kompleksitas waktu: tergantung pada nilai N, dalam kasus terburuk sekitar **O(N!)**
- Semakin besar nilai N, jumlah kemungkinan penempatan bertambah drastis.
- Tidak semua N memiliki solusi:
  - N = 2 dan N = 3 **tidak punya solusi**
  - N = 1, 4, 5, 6, 7, ... **punya solusi**

---

## Aplikasi Dunia Nyata

Walaupun ini masalah papan catur, konsep N-Queens sering digunakan dalam:

- **Penjadwalan (scheduling)**
- **Pengujian constraint pada AI**
- **Masalah optimasi ruang dan sumber daya**

Karena menekankan **pengambilan keputusan bertahap dan validasi dinamis**, N-Queens adalah latihan ideal untuk memahami **algoritma rekursif dan backtracking**.

---

## Kesimpulan

N-Queens bukan sekadar teka-teki, tapi juga contoh konkret bagaimana komputer "mencoba dan mundur" untuk menemukan solusi yang valid. Ini adalah dasar penting dalam pemrograman logika, pemecahan constraint, dan pemikiran algoritmik secara umum.

---


