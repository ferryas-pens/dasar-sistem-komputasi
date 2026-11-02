**LAMPIRAN MATERI TAMBAHAN RANGKAIAN LOGIKA**

**Panduan Penilaian untuk Dosen**

*Kunci latihan tingkat A dan B, serta rubrik latihan tingkat C*

**Berkas ini tidak dibagikan kepada mahasiswa.**

Semua kunci pada berkas ini sudah diperiksa dengan menghitung tabel kebenaran lengkap untuk setiap ekspresi, baik ekspresi sebelum maupun sesudah disederhanakan.

**1 Latihan tingkat A**

**Nomor 1.** Tabel NAND berisi 1, 1, 1, 0, sedangkan tabel NOR berisi 1, 0, 0, 0 (urutan AB = 00, 01, 10, 11). Keduanya sama pada baris AB = 00, dengan keluaran 1, dan pada baris AB = 11, dengan keluaran 0.

**Nomor 2.** OR menghasilkan 1 jika salah satu atau kedua masukan bernilai 1. XOR menghasilkan 1 hanya jika tepat satu masukan bernilai 1. Contoh kalimat yang benar adalah kalimat yang tidak mengizinkan kedua pilihan sekaligus, misalnya "Paket hemat ini berisi nasi *atau* kentang", jika memang tidak boleh mengambil keduanya. Terima contoh lain asalkan mahasiswa menjelaskan bahwa kedua pilihan tidak boleh terjadi bersamaan.

**Nomor 3.** NAND cukup untuk membuat NOT, AND, dan OR, sedangkan ketiga gerbang itu cukup untuk membuat fungsi apa pun. NOT dibuat dengan menghubungkan kedua masukan NAND, sehingga (A·A)' = A'.

**Nomor 4.** Urutan kode Gray memastikan dua kotak yang bersebelahan, termasuk kotak di tepi yang berseberangan, hanya berbeda satu variabel. Dengan urutan biner biasa, kolom 01 dan 10 akan bersebelahan, padahal keduanya berbeda dua variabel.

**Nomor 5.** Terima tiga aturan mana pun dari Subbab 7.3, asalkan alasannya benar. Contoh: (a) ukuran kelompok harus pangkat dua karena hanya kelompok seperti itu yang dapat ditulis sebagai satu suku AND; (b) kelompok dibuat sebesar mungkin karena setiap penggandaan ukuran menghilangkan satu variabel; (c) kelompok boleh tumpang tindih karena menurut hukum idempoten, A + A = A, sehingga suku yang dipakai dua kali tidak mengubah fungsi.

**2 Latihan tingkat B: kunci lengkap**

**Nomor 1.** F = A'B + BC'.

| **A** | **B** | **C** | **A'B** | **BC'** | **F** |
|-------|-------|-------|---------|---------|-------|
| 0     | 0     | 0     | 0       | 0       | 0     |
| 0     | 0     | 1     | 0       | 0       | 0     |
| 0     | 1     | 0     | 1       | 1       | 1     |
| 0     | 1     | 1     | 1       | 0       | 1     |
| 1     | 0     | 0     | 0       | 0       | 0     |
| 1     | 0     | 1     | 0       | 0       | 0     |
| 1     | 1     | 0     | 0       | 1       | 1     |
| 1     | 1     | 1     | 0       | 0       | 0     |

Rangkaian yang benar terdiri atas dua gerbang NOT (untuk A' dan C'), dua gerbang AND dua masukan, dan satu gerbang OR dua masukan.

**Kesalahan yang lazim.** Memakai satu NOT untuk hasil AB sehingga menghasilkan (AB)', bukan A'B.

**Nomor 2.** F = AB + A(B + C) + B(B + C).

| **Langkah**              | **Hukum**                     |
|--------------------------|-------------------------------|
| F = AB + AB + AC + BB + BC | Distributif                 |
| F = AB + AC + B + BC     | Idempoten (AB + AB = AB, BB = B) |
| F = B(A + 1 + C) + AC    | Distributif                   |
| F = B·1 + AC             | Dominasi                      |
| F = B + AC               | Identitas                     |

Terima urutan langkah lain asalkan setiap langkah sah dan hasil akhirnya B + AC.

**Nomor 3.** F(A, B, C) = Σm(0, 1, 2, 5).

Kelompok yang dibentuk: m0 dan m2, yang bersebelahan melalui tepi kiri dan kanan, menghasilkan A'C'. Kelompok m1 dan m5 menghasilkan B'C.

**F = A'C' + B'C.**

Kelompok m0 dan m1 (A'B') sah, tetapi berlebih, karena m0 sudah tercakup oleh A'C' dan m1 sudah tercakup oleh B'C. Jika mahasiswa menulis A'C' + B'C + A'B', jawabannya benar secara fungsi, tetapi tidak paling sederhana.

**Nomor 4.** F(A, B, C, D) = Σm(0, 1, 4, 5, 6, 7, 14, 15).

Kelompok pertama berisi m0, m1, m4, dan m5. Kelompok ini membentuk persegi pada kolom CD = 00 dan 01, baris AB = 00 dan 01, sehingga sukunya A'C'. Kelompok kedua berisi m6, m7, m14, dan m15. Kelompok ini membentuk persegi pada kolom CD = 11 dan 10, baris AB = 01 dan 11, sehingga sukunya BC.

**F = A'C' + BC.**

**Nomor 5.** F(A, B, C, D) = Σm(1, 3, 7, 11, 15) + d(0, 2, 5).

Kelompok CD (m3, m7, m11, m15) wajib ada. Kelompok ini tidak memakai X. Tinggal m1 yang belum tercakup. Ada dua cara yang sama baiknya:

- dengan memakai X pada m0 dan m2, terbentuk kelompok A'B' (m0, m1, m2, m3), sehingga **F = CD + A'B'**;

- dengan memakai X pada m5, terbentuk kelompok A'D (m1, m3, m5, m7), sehingga **F = CD + A'D**.

Kedua jawaban benar, masing-masing terdiri atas dua suku dan empat variabel. Jadi, hasil paling sederhananya tidak tunggal. Beri nilai penuh hanya jika mahasiswa menyadari hal ini atau menuliskan salah satu jawaban dengan pengelompokan yang benar.

**Nomor 6.** Untuk setiap baris, hitung S + MP + MF. Baris yang bernilai 1 adalah baris dengan S = 1 (baris 2, 3, 6, 7, 10, 11, 14, 15), baris dengan M = 1 dan P = 1 (baris 12 sampai 15), atau baris dengan M = 1 dan F = 1 (baris 9, 11, 13, 15). Gabungannya adalah baris 2, 3, 6, 7, 9, 10, 11, 12, 13, 14, dan 15, yang sama persis dengan kolom L pada Tabel 6.

**Kesalahan yang lazim.** Hanya menguji baris yang bernilai 1. Baris bernilai 0, yaitu baris 0, 1, 4, 5, dan 8, juga harus diuji, karena rangkaian yang terlalu sering menyala juga salah.

**3 Latihan tingkat C: rubrik**

**Nomor 1, penyiram otomatis.**

Salah satu tafsiran yang wajar memakai variabel berikut: K (tanah kering), H (sedang hujan), J (jam penyiraman), dan T (tangki berisi). Hasilnya:

Pompa = T·H'·(K + J) = TH'K + TH'J

Tafsiran ini memperlakukan "jangan pernah … kalau tangki kosong" sebagai syarat yang mengalahkan aturan lainnya, dan "kecuali kalau hujan" sebagai syarat yang berlaku pada kedua aturan penyiraman.

| **Skor** | **Ciri jawaban**                                                                                                                                                                                                                  |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4        | Variabel didefinisikan dengan arti nilai 1 dan 0. Tabel kebenaran 16 baris lengkap. Hasil sederhana sesuai dengan tafsiran yang dinyatakan. Paragraf menyebut minimal satu ambiguitas nyata dan merumuskan pertanyaan yang dapat dijawab "ya" atau "tidak" oleh petugas kebun. |
| 3        | Seperti skor 4, tetapi paragraf hanya menyebut ambiguitas tanpa pertanyaan konfirmasi, atau ada satu kesalahan kecil pada tabel yang tidak mengubah hasil akhir.                                                                     |
| 2        | Fungsi dan rangkaian benar, tetapi tafsiran tidak dinyatakan. Mahasiswa menganggap pesan itu jelas.                                                                                                                                |
| 1        | Ada kesalahan logika yang mengubah perilaku, misalnya pompa dapat menyala saat tangki kosong.                                                                                                                                      |

Contoh ambiguitas yang dapat diterima:

1.  Apakah pada jam penyiraman pompa tetap menyala walaupun tanah masih basah? Jika ya, ada risiko pemborosan air.

2.  Apakah "kecuali kalau hujan" juga berlaku pada aturan pertama? Dalam pesan itu, aturan pertama sudah menyebut syarat tidak hujan, tetapi petugas dapat saja bermaksud lain.

3.  Apa arti "tangki kosong" dalam praktik, misalnya di bawah batas tertentu?

Tafsiran lain boleh diterima asalkan dinyatakan dan konsisten dengan fungsi yang dihasilkan.

**Nomor 2.** Keduanya benar, karena kedua ekspresi menghasilkan tabel kebenaran yang sama. Namun, jawaban kedua lebih sederhana. Pada peta tiga variabel, suku BC mencakup m3 dan m7. Kotak m3 sudah tercakup oleh A'C, sedangkan m7 sudah tercakup oleh AB. Jadi, kelompok BC tidak memiliki satu pun angka 1 milik sendiri dan termasuk kelompok berlebih. Secara aljabar, bentuk XY + X'Z + YZ = XY + X'Z dikenal sebagai teorema konsensus. Mahasiswa tidak wajib menyebut nama teorema ini.

| **Skor** | **Ciri jawaban**                                                                                                                |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| 4        | Menyatakan keduanya benar secara fungsi, membuktikannya dengan tabel kebenaran, dan menunjukkan di peta mengapa BC berlebih.      |
| 3        | Menyatakan keduanya benar dengan bukti tabel, tetapi penjelasan peta tidak lengkap.                                             |
| 2        | Menyatakan hanya jawaban kedua yang benar karena lebih pendek. Ini menunjukkan mahasiswa mencampuradukkan "benar" dan "paling sederhana". |
| 1        | Menyatakan jawaban pertama salah tanpa bukti, atau menyatakan kedua ekspresi berbeda fungsinya.                                  |

**Nomor 3.** Pendapat teman itu keliru. Soal Tingkat B nomor 5 punya dua jawaban paling sederhana yang sama-sama sah, yaitu CD + A'B' dan CD + A'D. Jawaban yang berbeda dari kunci harus diperiksa dengan tabel kebenaran, bukan langsung dianggap salah. Mahasiswa yang baik juga menyebutkan batasnya: walaupun hasil paling sederhana dapat lebih dari satu, jumlah suku dan jumlah variabel pada hasil-hasil itu sama. Jika jawaban mahasiswa memakai lebih banyak suku, jawabannya mungkin benar secara fungsi tetapi belum paling sederhana.

| **Skor** | **Ciri jawaban**                                                                                                   |
|----------|--------------------------------------------------------------------------------------------------------------------|
| 4        | Membantah dengan contoh dari soal B5, menyebut cara memeriksa dengan tabel kebenaran, dan membedakan "benar" dari "paling sederhana". |
| 3        | Membantah dengan contoh, tetapi tidak menyebut cara memeriksa atau tidak membedakan kedua pengertian itu.          |
| 2        | Membantah tanpa contoh konkret.                                                                                    |
| 1        | Setuju dengan pendapat teman itu.                                                                                  |
