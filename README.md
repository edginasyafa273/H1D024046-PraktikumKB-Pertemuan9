# H1D024046-PraktikumKB-Pertemuan9

- **Nama:** Edgina Syafa Ayu Wicaksono
- **NIM:** H1D024046
- **Shift KRS:** B
- **Shift Baru:** F

---

## Deskripsi
Program ini mengimplementasikan Algoritma Genetika (AG) sebagai pendekatan komputasi evolusioner untuk memecahkan permasalahan optimasi. Studi kasus yang digunakan adalah **Knapsack Problem**, di mana program berusaha menemukan kombinasi barang terbaik yang dapat dimuat ke dalam tas dengan kapasitas terbatas, sekaligus memaksimalkan total nilai barang yang dibawa.

---

## Struktur File
| File | Deskripsi |
|---|---|
| `inisiasipopulasi.py` | Membangkitkan populasi awal berupa kumpulan kromosom biner secara acak |
| `EvaluasiFitness.py` | Mengukur kualitas setiap solusi berdasarkan total nilai barang yang dipilih |
| `selection.py` | Memilih individu yang akan menjadi parent menggunakan Roulette Wheel & Tournament Selection |
| `crossover.py` | Menghasilkan individu baru dari dua parent melalui One-Point, Two-Point, dan Uniform Crossover |
| `mutation.py` | Menjaga keragaman populasi dengan Swap, Inversion, dan Uniform Mutation |
| `main.py` | Mengintegrasikan seluruh proses evolusi dan menampilkan hasil akhir |

---

## Cara Kerja Algoritma Genetika
1. **Inisialisasi** - Populasi awal dibangkitkan secara acak dalam bentuk kromosom biner
2. **Evaluasi Fitness** - Setiap individu dihitung nilainya berdasarkan barang yang dipilih
3. **Seleksi** - Individu dengan fitness lebih tinggi memiliki peluang lebih besar untuk terpilih
4. **Crossover** - Dua parent dikombinasikan untuk menghasilkan keturunan baru
5. **Mutasi** - Beberapa gen diubah secara acak untuk menghindari solusi yang stagnan
6. **Generasi Baru** - Populasi lama digantikan oleh hasil keturunan generasi berikutnya

---

## Parameter yang Digunakan
| Parameter | Nilai |
|---|---|
| Jumlah Generasi | 50 |
| Jumlah Populasi | 20 |
| Probabilitas Crossover | 0.5 |
| Probabilitas Mutasi | 0.1 |
| Kapasitas Tas | 50 |

---

## Data Barang
| Barang | Nilai | Bobot |
|---|---|---|
| Barang1 | 60 | 10 |
| Barang2 | 100 | 20 |
| Barang3 | 120 | 30 |
| Barang4 | 90 | 25 |
| Barang5 | 69 | 11 |
| Barang6 | 70 | 9 |
| Barang7 | 80 | 15 |
| Barang8 | 90 | 10 |
| Barang9 | 25 | 3 |

---

## Cara Menjalankan
1. Clone repositori ini
2. Install library yang dibutuhkan
3. Jalankan program utama
---

## Hasil

Output program terdiri dari dua bagian:
- **Grafik** — Menampilkan perkembangan nilai fitness tertinggi, terendah, dan rata-rata dari setiap generasi
- **Terminal** — Menampilkan barang-barang yang terpilih beserta total nilai dan bobot terbaik

 Karena AG menggunakan proses acak, hasil yang muncul bisa berbeda setiap kali program dijalankan. Hal ini merupakan karakteristik alami dari algoritma evolusioner.