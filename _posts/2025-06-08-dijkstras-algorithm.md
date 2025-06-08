---
title: "Dijkstra’s Algorithm: Mencari Jalur Terpendek pada Graf Berbobot"
date: 2025-06-08
categories: [Algoritma, Graf]
tags: [dijkstra, algoritma, jalur terpendek, graf berbobot]
---

## Apa Itu Dijkstra’s Algorithm?

**Dijkstra’s Algorithm** adalah algoritma yang digunakan untuk menemukan **jalur terpendek** dari sebuah simpul sumber (source) ke semua simpul lain dalam graf berbobot dengan bobot sisi yang bernilai positif.

---

## Cara Kerja Dijkstra’s Algorithm

- Mulai dari simpul sumber, atur jarak awal ke 0 dan jarak ke simpul lain sebagai tak hingga (infinity).
- Gunakan struktur data **priority queue (min-heap)** untuk memilih simpul dengan jarak terkecil yang belum diproses.
- Pada setiap langkah:
  1. Ambil simpul dengan jarak minimum dari priority queue.
  2. Update jarak tetangga simpul tersebut jika ditemukan jalur yang lebih pendek melalui simpul itu.
- Ulangi sampai semua simpul telah diproses.

---

## Contoh Kasus Sederhana

Misal graf berbobot:

Simpul Tetangga (Berat)
A B(4), C(2)
B C(5), D(10)
C E(3)
D F(11)
E D(4)
F -


- Mulai dari A, jarak A = 0, lainnya tak hingga.
- Pilih simpul dengan jarak terkecil (A).
- Update jarak B = 4, C = 2.
- Pilih simpul berikutnya C (jarak 2).
- Update jarak E = 5 (2 + 3).
- Pilih simpul B (jarak 4).
- Update jarak D = 14 (4 + 10), tapi kemudian diperbarui ke 9 (5 + 4) dari jalur lewat E.
- Dan seterusnya sampai semua simpul ter-update.

---

## Kegunaan Dijkstra’s Algorithm

- Navigasi dan peta digital (GPS).
- Jaringan komputer untuk routing paket.
- Sistem rekomendasi jalur.
- Analisis graf berbobot.

---

## Kompleksitas

- Waktu:  
  - O(V²) untuk implementasi sederhana menggunakan matriks jarak.  
  - O((V + E) log V) dengan priority queue dan adjacency list (V = jumlah simpul, E = jumlah sisi).
- Ruang: O(V) untuk menyimpan jarak dan status simpul.

---

## Kesimpulan

Dijkstra’s Algorithm adalah algoritma penting untuk menemukan jalur terpendek dalam graf berbobot positif. Memahami algoritma ini krusial untuk aplikasi praktis di banyak bidang, terutama yang melibatkan pencarian rute dan jaringan.

