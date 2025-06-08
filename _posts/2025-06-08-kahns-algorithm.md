---
title: "Kahn’s Algorithm: Topological Sorting dengan Pendekatan BFS"
date: 2025-06-08
categories: [Algoritma, Graf, Topological Sorting]
tags: [kahns algorithm, topological sorting, graf, algoritma, bfs]
---

## Apa Itu Kahn’s Algorithm?

**Kahn’s Algorithm** adalah algoritma yang digunakan untuk melakukan **topological sorting** pada graf berarah tanpa siklus (DAG). Algoritma ini memanfaatkan pendekatan **BFS (Breadth-First Search)** dengan mengeliminasi simpul yang tidak memiliki sisi masuk (indegree = 0) secara bertahap.

---

## Tujuan Topological Sorting

Topological sorting menghasilkan urutan linear dari simpul graf sehingga untuk setiap sisi (u → v), simpul u muncul sebelum simpul v dalam urutan tersebut. Berguna untuk penjadwalan tugas, pengurutan dependensi, dan lain-lain.

---

## Cara Kerja Kahn’s Algorithm

1. Hitung **indegree** (jumlah sisi masuk) untuk setiap simpul.
2. Masukkan semua simpul dengan indegree 0 ke dalam antrian (queue).
3. Selama queue tidak kosong:
   - Keluarkan simpul dari queue dan tambahkan ke hasil topological sorting.
   - Kurangi indegree dari semua tetangga simpul tersebut sebanyak 1.
   - Jika ada tetangga yang indegree-nya menjadi 0, masukkan tetangga tersebut ke queue.
4. Jika semua simpul sudah diproses, hasilnya adalah topological order.
5. Jika ada simpul yang belum diproses (graf memiliki siklus), maka topological sorting tidak mungkin dilakukan.

---

## Contoh Kasus

Misal graf berarah:

5 → 0
5 → 2
4 → 0
4 → 1
2 → 3
3 → 1


Langkah Kahn’s Algorithm:

- Hitung indegree:
  - 0: 2
  - 1: 2
  - 2: 1
  - 3: 1
  - 4: 0
  - 5: 0
- Masukkan simpul dengan indegree 0 ke queue: `[4, 5]`
- Proses queue dan update:
  - Ambil `4`, output: `4`, kurangi indegree tetangga 0 dan 1
  - Ambil `5`, output: `5`, kurangi indegree tetangga 0 dan 2
  - Ketika indegree 0 atau 1 menjadi 0, masukkan ke queue
- Hasil topological order bisa jadi: `4 5 0 2 3 1`

---

## Kompleksitas

- Waktu: O(V + E) — memproses semua simpul dan sisi sekali saja.
- Ruang: O(V) untuk menyimpan indegree dan queue.

---

## Kesimpulan

Kahn’s Algorithm adalah metode efisien dan mudah dipahami untuk melakukan topological sorting menggunakan BFS. Sangat berguna untuk mengurutkan tugas yang memiliki dependensi dan memeriksa apakah graf berarah mengandung siklus.

