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

#### Soal 1 :
**Selesaikan menggunakan eliminasi gauss**
$$
\begin{array}{cc}
x_1+2x_2+3x_3z&=6\\
2x_1+4x_2+6x_3&=12\\
x_3+x_2&=2
\end{array}
$$

Penyelesaian :
$$
\begin{bmatrix}
1&2&3&|6\\
0&0&0&|0\\
0&1&1&|2
\end{bmatrix}
$$

- Tukar baris kedua dan ketiga untuk mendapatkan pivot lebih baik : 

$$
\begin{bmatrix}
1&2&3&|6\\
0&1&1&|2\\
0&0&0&|0
\end{bmatrix}
$$

- Solusi Akhir
$$
\begin{aligned}
x_1&=2-t\\
x_2&=2-t\\
x_3&=t
\end{aligned}
$$

- Jadi, solusi umum dari sistem persamaan adalah:
$$
(x_1,x_2,x_3)=(2-t,2-t,t), \quad t \in \mathbb{R}
$$
- Karena ada parameter bebas 𝑡, sistem ini memiliki banyak solusi.

#### Soal 2:
**Selesaikan menggunakan eliminasi Gauss**


\begin{array}{cc}
x_1 + x_2 + x_3 &= 3 \\
2x_1 + x_3 &= 5 \\
x_1 + 2x_2 &= 3
\end{array}


**Penyelesaian:**
**Matriks Augmented:**

**Tulis sistem persamaan dalam bentuk matriks augmented:**


\begin{bmatrix}
1 & 1 & 1 & | & 3 \\
2 & 0 & 1 & | & 5 \\
1 & 2 & 0 & | & 3
\end{bmatrix}


**Eliminasi Gauss:**

- Langkah 1: Gunakan baris pertama untuk mengeliminasi elemen di bawah pivot pertama (1 pada baris pertama).
- Baris 2: $( R_2 <- R_2 - 2R_1 )$
- Baris 3: $( R_3 <- R_3 - R_1 )$

**Hasilnya:**


\begin{bmatrix}
1 & 1 & 1 & | & 3 \\
0 & -2 & -1 & | & -1 \\
0 & 1 & -1 & | & 0
\end{bmatrix}


- Langkah 2: Gunakan baris kedua untuk mengeliminasi elemen di bawah pivot kedua (-2 pada baris kedua).

- Baris 3: $( R_3 <- R_3 + \frac{1}{2}R_2 )$

Hasilnya:


\begin{bmatrix}
1 & 1 & 1 & | & 3 \\
0 & -2 & -1 & | & -1 \\
0 & 0 & -\frac{3}{2} & | & -\frac{1}{2}
\end{bmatrix}

**Substitusi Mundur:**

   - Dari baris 3: $( -\frac{3}{2}x_3 = -\frac{1}{2} \Rightarrow x_3 = \frac{1}{3} )$
   - Dari baris 2:$( -2x_2 - x_3 = -1 \Rightarrow -2x_2 - \frac{1}{3} = -1 \Rightarrow x_2 = \frac{1}{3} )$
   - Dari baris 1: $( x_1 + x_2 + x_3 = 3 \Rightarrow x_1 + \frac{1}{3} + \frac{1}{3} = 3 \Rightarrow x_1 = \frac{7}{3} )$

**Solusi Akhir:**
\
\begin{aligned}
x_1 &= \frac{7}{3} \\
x_2 &= \frac{1}{3} \\
x_3 &= \frac{1}{3}
\end{aligned}


#### Soal 3 :
**Selesaikan menggunakan eliminasi gauss**
$$
\begin{array}{cc}
2x_1+2x_2&=4\\
x_1+x_2&=2
\end{array}
$$
{Penyelesaian:}

1. **Tulis sistem persamaan dalam bentuk matriks augmented:**

\[
\begin{bmatrix}
2 & 2 & | & 4 \\
1 & 1 & | & 2
\end{bmatrix}
\]

2. **Lakukan operasi baris untuk mendapatkan bentuk eselon baris:**

   - **Baris 1 = Baris 1 / 2:**

\[
\begin{bmatrix}
1 & 1 & | & 2 \\
1 & 1 & | & 2
\end{bmatrix}
\]

   - **Baris 2 = Baris 2 - Baris 1:**

\[
\begin{bmatrix}
1 & 1 & | & 2 \\
0 & 0 & | & 0
\end{bmatrix}
\]

3. **Analisis hasil eliminasi:**

   - Baris kedua menunjukkan $( 0x_1 + 0x_2 = 0 )$, yang selalu benar. Ini berarti sistem persamaan memiliki banyak solusi (tergantung pada parameter bebas).

4. **Tentukan solusi umum:**

   - Dari baris pertama:

        $[
        x_1 + x_2 = 2 \implies x_1 = 2 - x_2
        ]$

   - Misalkan $( x_2 = t )$, di mana $( t )$ adalah parameter bebas, maka:
        $$
        [
        x_1 = 2 - t
        ]$$

5. **Solusi Akhir:**


\begin{aligned}
x_1 &= 2 - t \\
x_2 &= t
\end{aligned}


Jadi, solusi umum dari sistem persamaan adalah:

$[
\left(x_1, x_2\right) = \left(2 - t, t\right), \quad t \in \mathbb{R}
]$

Sistem ini memiliki banyak solusi karena terdapat parameter bebas $( t )$.


#### Soal 4 :
Selesaikan menggunakan eliminasi gauss
$$
\begin{array}{cc}
x_1+x_2&=5\\
x_1+2x_3&=4
\end{array}
$$

{Penyelesaian:}

1. **Tulis sistem persamaan dalam bentuk matriks augmented:**


\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
1 & 0 & 2 & | & 4
\end{bmatrix}


2. **Lakukan operasi baris untuk mendapatkan bentuk eselon baris:**

   - **Baris 2 = Baris 2 - Baris 1:**


\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & -1 & 2 & | & -1
\end{bmatrix}


   - **Baris 2 = Baris 2 / (-1):**


\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & 1 & -2 & | & 1
\end{bmatrix}


3. **Lakukan substitusi mundur untuk menemukan solusi:**

   - Dari baris 2:

$[
x_2 - 2x_3 = 1 \implies x_2 = 1 + 2x_3
]$

   - Dari baris 1:

$[
x_1 + x_2 = 5 \implies x_1 + (1 + 2x_3) = 5 \implies x_1 = 4 - 2x_3
]$

4. **Solusi Akhir:**

$[
\begin{aligned}
x_1 &= 4 - 2x_3 \\
x_2 &= 1 + 2x_3 \\
x_3 &= x_3
\end{aligned}
]$

Jadi, solusi dari sistem persamaan adalah:

$[
\left(x_1, x_2, x_3\right) = \left(4 - 2t, 1 + 2t, t\right), \quad t \in \mathbb{R}
]$

Sistem ini memiliki banyak solusi karena terdapat parameter bebas $( t )$.