# Penyelesaian Sistem Persamaan Linier
## Operasi Baris Elementer
Operasi Baris Elementer (OBE) adalah operasi yang dilakukan pada baris suatu matriks. OBE dapat digunakan untuk menyelesaikan sistem persamaan linear (SPL) dan menentukan invers matriks. 
### Operasi dasar OBE 
Row Scalling: Mengalikan baris matriks dengan konstanta bukan nol
Row Swaping: Menukar urutan baris pada sebuah matriks
Row Replacement: Mengganti baris matriks dengan hasil penjumlahan atau pengurangan baris matriks tersebut dengan baris matriks lainnya
### Tujuan OBE
Tujuan OBE adalah untuk mengubah matriks menjadi bentuk yang paling sederhana agar mudah dipecahkan. Dalam proses perubahan tersebut, terdapat urutan operasi yang bermacam-macam. 
### Cara menyelesaikan SPL dengan OBE
Dalam menyelesaikan SPL dengan OBE, tujuannya adalah untuk membentuk sistem persamaan linear baru yang mempunyai solusi yang sama dengan pemecahan yang lebih mudah. 
### Cara menerapkan OBE
OBE dapat diterapkan dengan dua cara, yaitu eliminasi Gauss dan Gauss-Jordan. 

## Eliminasi Gauss
Metode eliminasi Gauss adalah metode untuk operasi nilai-nilai dalam matriks, untuk membuat matriks lebih sederhana lagi. Metode eliminasi gaus dikembangkan dari metode eliminasi, dengan cara menghilangkan atau mengurangi jumlah variabel, untuk mendapatkan nilai variabel bebas. Metode Eliminasi Gauss dikembangkan oleh Carl Friedrich Gauss (1777-1855). Carl adalah matematikawan berkebangsaan Jerman yang berkontribusi dalam geometri, teori bilangan, fungsi, dan teori probabilitas. Mengutip dari Rpubs.com, eliminasi Gauss yang dikembangkan Carl bermanfaat untuk memecahkan sistem persamaan linear. Eliminasi Gauss mengubah persamaan linear menjadi bentuk matriks, kemudian diubah ke bentuk Eselon Baris melalui Operasi Baris Elementer. Setelah itu bentuk matriks diselesaikan dengan substitusi balik. Eliminasi Gauss ini berasal dari operasi matematika pada baris matriks yang dilanjutkan sampai tersisa satu variabel. Metode eliminasi Gauss dipakai untuk menyelesaikan persamaan dalam bidang astronomi. Berdasarkan Academia.edu, eliminasi Gauss adalah cara mengoperasikan nilai-nilai dalam matriks lebih sederhana. Caranya melakukan operasi baris sehingga matriks tersebut menjadi matriks eselon baris. Cara ini digunakan untuk penyelesaian persamaan linear menggunakan matriks. Persamaan linear masuk ke matriks teraugmentasi dan mengoperasikannya. Kemudian lakukan substitusi balik untuk mendapatkan nilai variabel.

### Contoh Soal 1
Selesaikan dengan menggunakan eleminasi gauss

$
\begin{array}{cc}
x_1+2x_2+3x_3&=6\\
2x_1+4x_2+6x_3&=12\\
x_3+x_2&=2
\end{array}
$

Penyelesaian
Langkah 1: Tulis dalam Bentuk Matriks Augmented
Bentuk matriks augmented dari sistem ini adalah:
$
\begin{bmatrix}
1 & 2 & 3 & | 6 \\
2 & 4 & 6 & | 12 \\
0 & 1 & 1 & | 2
\end{bmatrix}
$

Langkah 2: Eliminasi Baris
Kita akan menghilangkan elemen di bawah elemen utama di kolom pertama. Gunakan operasi:
$
\begin{array}{cc}
R_2 \rightarrow R_2 - 2R_1
\end{array}
$

Sehingga:

$
\begin{bmatrix}
1 & 2 & 3 & | 6 \\
0 & 0 & 0 & | 0 \\
0 & 1 & 1 & | 2
\end{bmatrix}
$

Langkah 3: Interpretasi
Baris kedua dirubah menjadi *0 = 0*
$
\begin{aligned}
x_1 + 2x_2 + 3x_3 &= 6 \\
x_2 + x_3 &= 2
\end{aligned}
$
Langkah 4: Substitusi
Dari persamaan kedua:
$
\begin{array}{cc}
x_2 = 2 - x_3
\end{array}
$
Substitusikan ke persamaan pertama:
$
\begin{array}{cc}
x_1 + 2(2 - x_3) + 3x_3& = 6\\
x_1 + 4 - 2x_3 + 3x_3& = 6\\
x_1 + 4 + x_3& = 6\\
x_1 =& 2 - x_3
\end{array}
$
Kesimpulan
Solusi umum dari sistem ini adalah:
$
\begin{aligned}
x_1 &= 2 - x_3 \\
x_2 &= 2 - x_3 \\
x_3 &= x_3
\end{aligned}
$

### Contoh Soal 2 
Selesaikan dengan menggunakan eliminasi gauss
$
\begin{array}{cc}
x_1+x_2+x_3&=3\\
2x_1+x_3&=5\\
x_1+2x_2&=3
\end{array}
$

Penyelesaian 
Langkah 1: Tulis dalam Bentuk Matriks Augmented
$
\begin{bmatrix}
1 & 1 & 1 & | 3 \\
2 & 0 & 1 & | 5 \\
1 & 2 & 0 & | 3
\end{bmatrix}
$
Langkah 2: Eliminasi Baris
Kita akan menghilangkan elemen di bawah elemen utama di kolom pertama.
$
\begin{array}{cc}
R_2 \rightarrow R_2 - 2R_1
\end{array}
$
$
\begin{array}{cc}
R_3 \rightarrow R_3 - R_1
\end{array}
$
Sehingga matriks berubah menjadi:
$
\begin{bmatrix}
1 & 1 & 1 & | 3 \\
0 & -2 & -1 & | -1 \\
0 & 1 & -1 & | 0
\end{bmatrix}
$
Selanjutnya, buat elemen utama di baris kedua menjadi 1 dengan membagi baris kedua dengan -2:
$
\begin{array}{cc}
R_2 \rightarrow \frac{R_2}{-2}
\end{array}
$
Hasilnya:
$
\begin{bmatrix}
1 & 1 & 1 & | 3 \\
0 & 1 & \frac{1}{2} & | \frac{1}{2} \\
0 & 1 & -1 & | 0
\end{bmatrix}
$
Kemudian eliminasi elemen di bawah elemen utama dengan:
$
\begin{array}{cc}
R_3 \rightarrow R_3 - R_2
\end{array}
$
Sehingga diperoleh:
$\begin{bmatrix}
1 & 1 & 1 & | 3 \\
0 & 1 & \frac{1}{2} & | \frac{1}{2} \\
0 & 0 & -\frac{3}{2} & | -\frac{1}{2}
\end{bmatrix}$
Langkah 3: Substitusi Balik*
Dari baris ketiga:
$
\begin{array}{cc}
-\frac{3}{2} x_3 = -\frac{1}{2}
\end{array}

\begin{array}{cc}
x_3 = \frac{1}{3}
\end{array}
$
Dari baris kedua:
$
\begin{array}{cc}
x_2 + \frac{1}{2} x_3 = \frac{1}{2}
\end{array}

\begin{array}{cc}
x_2 + \frac{1}{2} \times \frac{1}{3} = \frac{1}{2}
\end{array}

\begin{array}{cc}
x_2 + \frac{1}{6} = \frac{1}{2}
\end{array}

\begin{array}{cc}
x_2 = \frac{1}{2} - \frac{1}{6} = \frac{3}{6} - \frac{1}{6} = \frac{2}{6} = \frac{1}{3}
\end{array}

Dari baris pertama:
\begin{array}{cc}
x_1 + x_2 + x_3 = 3
\end{array}

\begin{array}{cc}
x_1 + \frac{1}{3} + \frac{1}{3} = 3
\end{array}

\begin{array}{cc}
x_1 = 3 - \frac{2}{3} = \frac{9}{3} - \frac{2}{3} = \frac{7}{3}
\end{array}
$
Kesimpulan
Jadi, solusi dari sistem persamaan adalah:
$\begin{aligned}
x_1 &= \frac{7}{3} \\
x_2 &= \frac{1}{3} \\
x_3 &= \frac{1}{3}
\end{aligned}$

<iframe scrolling="no" title="Lab11 System of Equations - Multivariable" src="https://www.geogebra.org/material/iframe/id/dmIAq6KX/width/1164/height/816/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/true/ld/false/sdz/true/ctl/false" width="1164px" height="816px" style="border:0px;"> </iframe>

### Contoh Soal 3 
Selesaikan dengan menggunakan eliminasi gauss
$
\begin{array}{cc}
2x_1+2x_2&=4\\
x_1+x_2&=2
\end{array}
$

Penyelesaian 
Langkah 1 : Menyelesaikan ke bentuk matriks augmented 
$
\begin{bmatrix} 
2 & 2 & | 4 \\ 
1 & 1 & | 2 
\end{bmatrix}
$
Langkah 2 : membuat elemen di bawah pivot menjadi nol. 
$
\begin{array}{cc}
R_1 \leftarrow R_1 - 2R_2
\end{array}
$
Setelah melakukan perhitungan kita mendapatkan :

$
\begin{array}{cc}
R_1: 2 - 2 \cdot 1 = 0\\
2 - 2 \cdot 1 = 0\\
4 - 2 \cdot 2 = 0
\end{array}
$

Sehingga matriks augmented menjadi : 
$
\begin{bmatrix} 
1 & 1 & | 2 \\
0 & 0 & | 0 
\end{bmatrix}$

Dari baris kedua, kita dapat mengekspresikan (x_1) dalam bentuk (x_2): 
$
\begin{array}{cc}
x_1 + x_2 = 2 \Rightarrow x_1 = 2 - x_2
\end{array}$


Karena kita memiliki satu persamaan dengan dua variabel, kita dapat menyatakan solusi dalam bentuk parameter. Misalkan (x_2 = t), maka:
$
\begin{array}{cc}
x_1 = 2 - t
\end{array}$

Jadi, solusi umum dari sistem persamaan ini adalah:
$
\begin{cases} 
x_1 = 2 - t\\
x_2 = t
\end{cases}$

di mana (t) adalah parameter bebas.

### Contoh Soal 4 
Selesaikan dengan menggunakan eliminasi gauss
$
\begin{array}{cc}
x_1+x_2&=5\\
x_1+2x_3&=6\\
\end{array}
$

Penyelesaian : 

1. Tulis sistem persamaan dalam bentuk matriks augmented:
$
\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
1 & 0 & 2 & | & 4
\end{bmatrix}$


2. Lakukan operasi baris untuk mendapatkan bentuk eselon baris:

$
\begin{array}{cc}
R_2 \rightarrow R_2 
\end{array}$

Hasilnya : 
$
\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & -1 & 2 & | & -1
\end{bmatrix}

\begin{array}{cc}
R_2 \rightarrow \frac{R_2}{-1}
\end{array}$

Hasilnya : 
$
\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & 1 & -2 & | & 1
\end{bmatrix}$

3. Lakukan substitusi mundur untuk menemukan solusi:

- Dari baris 2:
$
\begin{array}{cc}
x_1 + x_2 = 2 \Rightarrow x_1 = 2 - x_2
\end{array}$

- Dari baris 1:
$
\begin{array}{cc}
x_1 + x_2 = 5 \implies x_1 + (1 + 2x_3) = 5 \implies x_1 = 4 - 2x_3
\end{array}$

4. Solusi Akhir:
$
\begin{aligned}
x_1 &= 4 - 2x_3 \\
x_2 &= 1 + 2x_3 \\
x_3 &= x_3
\end{aligned}$

Jadi, solusi dari sistem persamaan adalah:
$
\begin{array}{cc}
\left(x_1, x_2, x_3\right) = \left(4 - 2t, 1 + 2t, t\right), \quad t \in \mathbb{R}
\end{array}$

Sistem ini memiliki banyak solusi karena terdapat parameter bebas $( t )$.