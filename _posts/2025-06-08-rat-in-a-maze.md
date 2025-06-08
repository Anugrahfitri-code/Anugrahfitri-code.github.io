---
title: "Rat in a Maze: Menemukan Jalur Bebas dari Labirin"
date: 2025-06-08
categories: [Algoritma, Backtracking]
tags: [rat in a maze, backtracking, algoritma, maze]
---

## Apa Itu Rat in a Maze?

**Rat in a Maze** adalah salah satu masalah klasik dalam algoritma **backtracking**, di mana seekor tikus harus menemukan jalur dari **titik awal (biasanya kiri atas)** menuju **tujuan (biasanya kanan bawah)** di dalam **labirin 2D** yang terdiri dari blok yang bisa dilewati dan blok yang terhalang.

Tantangannya adalah **menemukan jalur** (atau semua jalur) dari awal ke akhir **tanpa melewati dinding** dan **tanpa keluar dari batas labirin**.

---

## Representasi Masalah

Labirin biasanya direpresentasikan sebagai **matriks 2 dimensi**:

- `1` artinya bisa dilewati (jalan)
- `0` artinya tidak bisa dilewati (tembok)

Contoh labirin 4×4:
1 0 0 0
1 1 0 1
0 1 0 0
1 1 1 1

Tujuan: cari jalur dari kiri atas `(0,0)` ke kanan bawah `(3,3)` dengan hanya bergerak **maju (kanan)** atau **turun (bawah)** — atau dalam versi lanjutan, juga boleh ke **atas** dan **kiri**.

---

## Pendekatan Penyelesaian

Masalah ini diselesaikan dengan **backtracking**, yaitu:

1. Mulai dari titik awal.
2. Cek apakah posisi saat ini valid dan belum dikunjungi.
3. Coba gerak ke salah satu arah: kanan, bawah, kiri, atau atas.
4. Tandai jalur yang sedang dicoba.
5. Jika mentok (tidak bisa lanjut), **mundur ke langkah sebelumnya** dan coba arah lain.
6. Jika mencapai tujuan, **catat solusi**.

---

## Output

Output bisa berupa:
- **Satu solusi** (jalur tunggal dari awal ke akhir)
- **Semua solusi** (jika lebih dari satu jalur mungkin)
- Representasi jalur yang dilewati, misalnya menggunakan huruf `'R'`, `'D'`, `'L'`, `'U'` (Right, Down, Left, Up)

---

## Kompleksitas

- Waktu: O(4^(N×N)) di kasus terburuk, karena bisa ada banyak cabang
- Ruang: O(N×N) untuk menyimpan jalur dan visited

---

## Kegunaan dalam Dunia Nyata

- Navigasi otomatis
- Pemrograman robot
- Game AI (pathfinding)
- Simulasi rute

---

## Penutup

Masalah **Rat in a Maze** membantu kita memahami cara kerja **rekursi dan backtracking** dalam memecahkan masalah eksplorasi jalur. Walaupun terlihat sederhana, konsep ini menjadi dasar bagi banyak algoritma pencarian rute yang digunakan di dunia nyata.
