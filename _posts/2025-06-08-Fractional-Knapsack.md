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

## Implementasi dalam Python

```python
def fractional_knapsack(capacity, weights, values):
    # Hitung value per weight
    items = [(v / w, w, v) for w, v in zip(weights, values)]
    # Urutkan berdasarkan value per weight, descending
    items.sort(key=lambda x: x[0], reverse=True)

    total_value = 0.0
    for ratio, w, v in items:
        if capacity == 0:
            break
        # Ambil sebanyak mungkin
        amount = min(w, capacity)
        total_value += amount * ratio
        capacity -= amount

    return total_value

# Contoh penggunaan
weights = [10, 20, 30]
values = [60, 100, 120]
capacity = 50

max_value = fractional_knapsack(capacity, weights, values)
print(f"Nilai maksimum yang bisa diambil: {max_value}")
