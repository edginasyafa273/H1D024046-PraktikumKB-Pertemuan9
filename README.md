# H1D024046-PraktikumKB-Pertemuan9

- **Nama:** Edgina Syafa Ayu Wicaksono
- **NIM:** H1D024046
- **Shift KRS:** B
- **Shift Baru:** F

---

## Deskripsi
Program ini mengimplementasikan Algoritma Genetika (AG) sebagai pendekatan komputasi evolusioner untuk memecahkan permasalahan optimasi. Studi kasus yang digunakan adalah **Knapsack Problem**, di mana program berusaha menemukan kombinasi barang terbaik yang dapat dimuat ke dalam tas dengan kapasitas terbatas, sekaligus memaksimalkan total nilai barang yang dibawa.

---

## Konsep Dasar
Algoritma Genetika bekerja dengan meniru mekanisme seleksi alam Darwin. Setiap solusi direpresentasikan sebagai **kromosom biner**, di mana nilai `1` berarti barang dipilih dan `0` berarti tidak dipilih. Populasi solusi kemudian "berevolusi" dari generasi ke generasi hingga ditemukan solusi terbaik.

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
## Penjelasan Metode

### Seleksi
- **Roulette Wheel** — Peluang terpilih sebanding dengan nilai fitness individu
- **Tournament** — Beberapa individu dibandingkan, yang terbaik yang menang

### Crossover
- **One-Point** — Kromosom dipotong di satu titik lalu ditukar
- **Two-Point** — Kromosom dipotong di dua titik, bagian tengah ditukar
- **Uniform** — Setiap gen dipilih berdasarkan mask acak

### Mutasi
- **Swap** — Dua posisi gen ditukar
- **Inversion** — Urutan gen dalam segmen tertentu dibalik
- **Uniform** — Gen dibalik nilainya dengan probabilitas tertentu

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
git clone https://github.com/edginasyafa273/H1D024046-PraktikumKB-Pertemuan9.git
3. Install library yang dibutuhkan
pip install matplotlib numpy
5. Jalankan program utama
python main.py
---

## Hasil

Output program terdiri dari dua bagian:
- **Grafik** — Menampilkan perkembangan nilai fitness tertinggi, terendah, dan rata-rata dari setiap generasi
- **Terminal** — Menampilkan barang-barang yang terpilih beserta total nilai dan bobot terbaik

### Grafik Perkembangan Fitness
<img width="1366" height="655" alt="pertemuan 9_prak kb" src="https://github.com/user-attachments/assets/6096a249-22a6-4572-8684-4e734af62a9f" />

- 🔵 **Biru** — Nilai fitness tertinggi per generasi
- 🔴 **Merah** — Nilai fitness rata-rata per generasi  
- 🟡 **Kuning** — Nilai fitness terendah per generasi
- ⚫ **Abu-abu** — Sebaran nilai fitness seluruh individu

### Output Terminal
Nilai Fitness:
Individu 1: Fitness = 0
Individu 2: Fitness = 190
Individu 3: Fitness = 230
Nilai Fitness Terbaik: 334
Total Bobot: 48
Barang Terpilih:
-Barang5
-Barang6
-Barang7
-Barang8

> Setiap run menghasilkan output berbeda karena sifat acak AG. Ini adalah karakteristik alami algoritma evolusioner, bukan kesalahan program.

