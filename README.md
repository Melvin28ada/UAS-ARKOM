# Elevator Control System Using Finite State Machine (FSM)

## Deskripsi Proyek

Proyek ini merupakan simulasi sistem kontrol elevator menggunakan Logisim Evolution yang menerapkan konsep Finite State Machine (FSM). Sistem dapat menerima tujuan lantai dan memindahkan elevator secara bertahap menuju lantai yang dipilih.

## Tujuan Proyek

* Mengimplementasikan konsep FSM.
* Menggunakan D Flip-Flop sebagai penyimpan state.
* Menerapkan logika transisi state menggunakan gerbang logika.
* Menampilkan posisi elevator menggunakan decoder dan LED.

---

## Tampilan Rangkaian

![Rangkaian Elevator](images/elevator-circuit.png)

Gambar 1. Rangkaian utama sistem elevator berbasis FSM.

---

## Komponen yang Digunakan

| Komponen         | Fungsi                                   |
| ---------------- | ---------------------------------------- |
| D Flip-Flop      | Menyimpan state elevator                 |
| AND Gate         | Membentuk persamaan next state           |
| OR Gate          | Menggabungkan hasil logika               |
| Priority Encoder | Mengubah input tujuan menjadi kode biner |
| Decoder          | Mengubah state menjadi output lantai     |
| Clock            | Mengatur perpindahan state               |
| LED              | Menampilkan posisi elevator              |

---

## Cara Kerja Sistem

1. Pengguna memilih lantai tujuan melalui tombol F0, F1, F2, atau F3.
2. Tombol Enable digunakan untuk memasukkan tujuan ke sistem.
3. Tujuan diproses oleh rangkaian logika next state.
4. State elevator disimpan pada empat D Flip-Flop.
5. Setiap satu pulsa clock, elevator berpindah satu lantai menuju tujuan.
6. Decoder menerjemahkan state menjadi output LED.
7. LED menunjukkan posisi elevator saat ini.

---

## Diagram Pergerakan Elevator

Contoh perpindahan dari lantai 0 ke lantai 3:

F0 → F1 → F2 → F3

Setiap perpindahan terjadi setelah satu siklus clock.

---

## Hasil Pengujian

### Kondisi Awal

![Lantai 0](images/fl0.png)

LED FL0 menyala yang menunjukkan elevator berada di lantai 0.

### Pengujian Tujuan F3

![Lantai 1](images/fl1.png)

Clock ke-1: Elevator berada di lantai 1.

![Lantai 2](images/fl2.png)

Clock ke-2: Elevator berada di lantai 2.

![Lantai 3](images/fl3.png)

Clock ke-3: Elevator mencapai lantai tujuan yaitu lantai 3.

---

## Kendala

* Menentukan tabel transisi state FSM.
* Menyusun persamaan D0, D1, D2, dan D3.
* Melakukan debugging pada rangkaian logika.
* Memastikan sinkronisasi antara state dan decoder.

---

## Kesimpulan

Sistem elevator berbasis FSM berhasil diimplementasikan menggunakan Logisim Evolution. Elevator dapat bergerak secara bertahap menuju lantai tujuan berdasarkan input pengguna dan perubahan state yang dikendalikan oleh clock.

---


## File Proyek

* Elevator.circ
* README.md
* Video Demonstrasi.mp4
