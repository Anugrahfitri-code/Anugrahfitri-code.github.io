---
title: "Fractional Knapsack Problem: Solusi Optimal dengan Greedy Algorithm"
date: 2025-06-08
categories: [Algoritma, Greedy, Pemrograman]
tags: [knapsack, greedy, algoritma, optimization]
---

## Apa itu Fractional Knapsack?

Fractional Knapsack adalah variasi masalah knapsack di mana kamu diperbolehkan mengambil sebagian dari suatu barang, bukan harus seluruhnya. Tujuannya adalah memaksimalkan nilai total dalam knapsack dengan kapasitas terbatas.

Contohnya, jika kamu hanya punya ruang 50kg, kamu bisa mengambil 30kg dari barang A dan 20kg dari barang B, asalkan total nilai maksimal.

---

## Algoritma Fractional Knapsack

Solusinya menggunakan metode *greedy*, yaitu:

1. Hitung nilai per berat (value/weight) untuk setiap barang.
2. Urutkan barang berdasarkan nilai per berat dari terbesar ke terkecil.
3. Ambil sebanyak mungkin dari barang dengan nilai per berat tertinggi hingga knapsack penuh.
4. Jika barang terakhir tidak muat penuh, ambil sebagian saja.

---

## Kompleksitas Algoritma

- Langkah pengurutan barang berdasarkan rasio nilai per berat memakan waktu sekitar O(n log n), di mana n adalah jumlah barang.
- Setelah itu, pengambilan barang secara berurutan hanya membutuhkan waktu O(n).
- Jadi total waktu eksekusi algoritma ini adalah O(n log n).

---

## Kelebihan dan Kekurangan

**Kelebihan:**

- Algoritma ini sangat efisien dan cepat untuk masalah fractional knapsack.
- Solusinya optimal dan selalu memberikan nilai maksimum.

**Kekurangan:**

- Algoritma ini hanya berlaku jika barang bisa dibagi menjadi bagian-bagian kecil (fractional).  
- Untuk masalah knapsack biasa yang hanya mengizinkan barang utuh (0/1 knapsack), algoritma ini tidak cocok.

---

## Kesimpulan

Fractional Knapsack adalah contoh klasik penerapan algoritma greedy yang menghasilkan solusi optimal dalam waktu efisien. Dengan memanfaatkan rasio nilai per berat, kita bisa menentukan bagian barang mana yang sebaiknya diambil agar nilai total maksimal.

Jika kamu tertarik mempelajari lebih lanjut, kamu bisa mencoba mengimplementasikan algoritma ini sendiri atau mencari tutorial yang dilengkapi kode contoh.

---
