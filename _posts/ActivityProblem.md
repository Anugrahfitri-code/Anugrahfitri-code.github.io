---
layout: post
title: "Greedy Algorithm: Activity Selection Problem"
date: 2025-06-08
categories: [algorithm, greedy]
tags: [greedy, algorithm, activity-selection, coding, cpp]
---

## 📘 Pendahuluan
Activity Selection Problem adalah masalah optimasi klasik di mana kita diberikan sekumpulan aktivitas, masing-masing dengan waktu mulai dan waktu selesai. Tujuan kita adalah memilih sebanyak mungkin aktivitas yang kompatibel (tidak tumpang tindih) satu sama lain dari sekumpulan aktivitas tersebut.

Bayangkan Anda punya banyak rapat yang ingin dihadiri, tapi Anda tidak bisa menghadiri dua rapat yang berlangsung di waktu yang sama. Activity Selection Problem membantu Anda mencari tahu rapat mana saja yang bisa Anda hadiri agar jumlah rapat yang bisa Anda hadiri maksimal.

## 🧠 Masalah

Diberikan `n` aktivitas, masing-masing dengan waktu mulai dan waktu selesai. Tujuannya adalah untuk memilih sebanyak mungkin aktivitas **yang tidak bertabrakan**, hanya satu aktivitas yang bisa dilakukan dalam satu waktu.

## 💡 Prinsip Greedy

Pendekatan **greedy** bekerja dengan strategi berikut:
1. **Urutkan aktivitas berdasarkan waktu selesai (ascending)**.
2. **Pilih aktivitas yang selesai paling awal terlebih dahulu.**
3. Lanjutkan memilih aktivitas berikutnya hanya jika waktu mulainya **≥** waktu selesai dari aktivitas terakhir yang dipilih.

Kenapa greedy berhasil di sini?
> Karena dengan selalu memilih aktivitas yang selesai paling cepat, kita meninggalkan **ruang waktu maksimum** untuk aktivitas selanjutnya.

---

## 📊 Contoh 

```text
input:
Start  = {1, 3, 0, 5, 8, 5}
Finish = {2, 4, 6, 7, 9, 9}

Output:
Aktivitas yang dipilih:
(1, 2)
(3, 4)
(5, 7)
(8, 9)
