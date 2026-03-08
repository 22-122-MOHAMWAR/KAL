# Operasi Baris Elementer (OBE) -- Eliminasi Gauss

## Sistem Persamaan Linear 5 Variabel

------------------------------------------------------------------------

## 1. Pengertian Sistem Persamaan Linear

Sistem Persamaan Linear (SPL) adalah sekumpulan persamaan yang memiliki
beberapa variabel dan harus diselesaikan secara bersamaan.

Contoh sistem persamaan linear dengan **5 variabel**:

x1 + 2x2 + x3 + x4 + x5 = 7\
2x1 + x2 + 3x3 + x4 + 2x5 = 10\
3x1 + 2x2 + 2x3 + 2x4 + x5 = 13\
x1 + x2 + x3 + 2x4 + 3x5 = 11\
2x1 + 3x2 + x3 + x4 + x5 = 12

Variabel yang dicari:

-   x1
-   x2
-   x3
-   x4
-   x5

------------------------------------------------------------------------

## 2. Metode Eliminasi Gauss

Eliminasi Gauss adalah metode untuk menyelesaikan SPL dengan mengubah
matriks menjadi **bentuk segitiga atas** menggunakan **Operasi Baris
Elementer (OBE)**.

Langkah umum:

1.  Mengubah persamaan ke bentuk **matriks augmented**
2.  Melakukan **operasi baris elementer**
3.  Membuat elemen di bawah diagonal utama menjadi **0**
4.  Menyelesaikan menggunakan **substitusi balik**

------------------------------------------------------------------------

## 3. Bentuk Matriks Augmented

  1   2   1   1   1   7
  --- --- --- --- --- ----
  2   1   3   1   2   10
  3   2   2   2   1   13
  1   1   1   2   3   11
  2   3   1   1   1   12

------------------------------------------------------------------------

$$
\begin{bmatrix}
1 & 2 & 1 & 1 & 1 & | & 7 \\
0 & -3 & 1 & -1 & 0 & | & -4 \\
0 & -4 & -1 & -1 & -2 & | & -8 \\
0 & -1 & 0 & 1 & 2 & | & 4 \\
0 & -1 & -1 & -1 & -1 & | & -2
\end{bmatrix}
$$

## 4. Operasi Baris Elementer (OBE)

Terdapat **3 jenis operasi baris elementer**:

1.  Menukar dua baris\
    Ri ↔ Rj

2.  Mengalikan baris dengan konstanta\
    kRi

3.  Menjumlahkan baris dengan kelipatan baris lain\
    Ri - kRj

------------------------------------------------------------------------

## 5. Langkah Eliminasi Gauss

### Matriks Awal

  1   2   1   1   1   7
  --- --- --- --- --- ----
  2   1   3   1   2   10
  3   2   2   2   1   13
  1   1   1   2   3   11
  2   3   1   1   1   12

### Menghilangkan elemen di bawah pivot pertama

Operasi:

R2 = R2 − 2R1\
R3 = R3 − 3R1\
R4 = R4 − R1\
R5 = R5 − 2R1

Hasil:

  1   2    1    1    1    7
  --- ---- ---- ---- ---- ----
  0   -3   1    -1   0    -4
  0   -4   -1   -1   -2   -8
  0   -1   0    1    2    4
  0   -1   -1   -1   -1   -2

------------------------------------------------------------------------

## 6. Bentuk Segitiga Atas

  1   2   1      1     1    7
  --- --- ------ ----- ---- -----
  0   1   -1/3   1/3   0    4/3
  0   0   1      1     -1   2
  0   0   0      1     2    3
  0   0   0      0     1    1

------------------------------------------------------------------------

## 7. Substitusi Balik

Baris 5\
x5 = 1

Baris 4\
x4 + 2x5 = 3\
x4 = 1

Baris 3\
x3 + x4 − x5 = 2\
x3 = 2

Baris 2\
x2 − 1/3 x3 + 1/3 x4 = 4/3\
x2 = 1

Baris 1\
x1 + 2x2 + x3 + x4 + x5 = 7\
x1 = 1

------------------------------------------------------------------------

## 8. Hasil Akhir

x1 = 1\
x2 = 1\
x3 = 2\
x4 = 1\
x5 = 1

------------------------------------------------------------------------

## 9. Contoh SAGE CELL

![GAMBAR](SAGE.png)

------------------------------------------------------------------------

## 10. Kesimpulan

Metode **Eliminasi Gauss** digunakan untuk menyelesaikan sistem
persamaan linear dengan langkah:

1.  Mengubah persamaan menjadi matriks augmented
2.  Melakukan operasi baris elementer
3.  Mengubah matriks menjadi bentuk segitiga atas
4.  Menentukan nilai variabel dengan substitusi balik

Metode ini efektif untuk menyelesaikan sistem persamaan linear dengan
banyak variabel seperti **5 persamaan dan 5 variabel**.
