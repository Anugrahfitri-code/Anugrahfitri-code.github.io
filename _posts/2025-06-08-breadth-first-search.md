---
title: "Breadth-First Search (BFS): Menjelajahi Graf dengan Lebar"
date: 2025-06-08
categories: [Algoritma, Graf]
tags: [bfs, breadth-first search, graf, algoritma, pencarian]
---

## Apa Itu Breadth-First Search (BFS)?

**Breadth-First Search (BFS)** adalah salah satu algoritma dasar untuk menjelajahi atau mencari node dalam sebuah graf atau pohon. BFS bekerja dengan menjelajahi semua node pada **tingkat (level) saat ini** terlebih dahulu sebelum pindah ke tingkat berikutnya.

---

## Cara Kerja BFS

- BFS dimulai dari **simpul awal (start node)**.
- Algoritma menggunakan struktur data **queue** untuk menyimpan node yang akan dikunjungi berikutnya.
- Langkah-langkah BFS secara sederhana:
  1. Masukkan simpul awal ke dalam queue.
  2. Keluarkan simpul dari queue, kunjungi simpul tersebut.
  3. Masukkan semua tetangga (neighbor) yang belum dikunjungi ke dalam queue.
  4. Ulangi langkah 2 dan 3 sampai queue kosong.

---

## Contoh Kasus Sederhana

Misal graf berikut:

A -- B -- D
| |
C -- E


Jika BFS dimulai dari node `A`, urutan kunjungannya adalah:  
`A -> B -> C -> D -> E`

Karena BFS mengeksplor semua tetangga `A` dulu (`B` dan `C`), baru lanjut ke tetangga dari `B` dan `C` (misal `D` dan `E`).

---

## Kegunaan BFS

- Mencari jalur terpendek di graf tak berbobot.
- Menganalisis jaringan sosial.
- Crawling web.
- Pemecahan masalah labirin dan puzzle.
- Memeriksa konektivitas graf.

---

## Kompleksitas BFS

- **Waktu:** O(V + E), di mana V adalah jumlah vertex (simpul) dan E adalah jumlah edge (sisi) graf.
- **Ruang:** O(V), untuk menyimpan visited dan queue.

---

## Kesimpulan

BFS adalah algoritma fundamental yang efisien dan mudah digunakan untuk banyak masalah terkait graf dan pencarian jalur. Memahami BFS sangat penting bagi siapa saja yang belajar algoritma dan struktur data.

