---
title: "Depth-First Search (DFS): Menjelajahi Graf dengan Pendekatan Dalam"
date: 2025-06-08
categories: [Algoritma, Graf]
tags: [dfs, depth-first search, graf, algoritma, pencarian]
---

## Apa Itu Depth-First Search (DFS)?

**Depth-First Search (DFS)** adalah algoritma dasar untuk menjelajahi atau mencari node dalam sebuah graf atau pohon dengan cara menjelajahi **sedalam mungkin** pada satu cabang sebelum kembali dan menjelajahi cabang lain.

---

## Cara Kerja DFS

- DFS dimulai dari **simpul awal (start node)**.
- Algoritma menggunakan **rekursi** atau **stack** untuk melacak node yang sedang dijelajahi.
- Langkah-langkah DFS secara sederhana:
  1. Kunjungi simpul awal dan tandai sebagai sudah dikunjungi.
  2. Dari simpul tersebut, pilih salah satu tetangga yang belum dikunjungi.
  3. Lakukan DFS secara rekursif pada tetangga tersebut.
  4. Jika tidak ada tetangga yang belum dikunjungi, kembali (backtrack) ke simpul sebelumnya.
  5. Ulangi hingga semua node yang terhubung telah dikunjungi.

---

## Contoh Kasus Sederhana

Misal graf berikut:

A -- B -- D
| |
C -- E


Jika DFS dimulai dari node `A`, salah satu urutan kunjungannya bisa:  
`A -> B -> D -> E -> C`

Karena DFS akan mengeksplor cabang sedalam mungkin sebelum pindah ke cabang lain.

---

## Kegunaan DFS

- Menemukan jalur dalam graf.
- Memeriksa apakah graf terhubung.
- Mendeteksi siklus pada graf.
- Topological sorting pada graf terarah.
- Memecahkan teka-teki seperti labirin dan puzzle.

---

## Kompleksitas DFS

- **Waktu:** O(V + E), di mana V adalah jumlah vertex (simpul) dan E adalah jumlah edge (sisi) graf.
- **Ruang:** O(V), untuk menyimpan status visited dan stack rekursi.

---

## Kesimpulan

DFS adalah algoritma pencarian yang mendalam dan efektif untuk banyak masalah graf dan pohon. Memahami DFS membantu dalam memahami konsep rekursi dan backtracking dalam algoritma.

