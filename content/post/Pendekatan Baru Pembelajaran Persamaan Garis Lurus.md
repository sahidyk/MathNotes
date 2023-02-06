---
title:  Pendekatan Baru Pembelajaran Persamaan Garis Lurus
authors:
- admin

type: book
date: 2021-10-06
lastMod: 2023-02-06
math: true
diagram: true
highlight: true
#image:
#  placement: 3
#  caption: 'Image credit: [**John Moeses Bauan**](https://unsplash.com/photos/OGZtQF8iC0g)'
---
**Sahid**<br>
**Jurusan Pendidikan Matematika, FMIPA, UNY**<br>
*[sahid@uny.ac.id](mailto:sahid@uny.ac.id), [sahidyk@gmail.com](mailto:sahidyk@gmail.com)*

{{< toc hide_on="xl" >}}

## Pendahuluan

Bentuk-bentuk persamaan garis lurus adalah:

$$
\begin{align}
ax+by&=c\label{eq:ax+by=c}\\
ax+by+c&=0\label{eq:ax+by+c=0}\\
\frac xa+\frac yb&=1\label{eq:intercept-form}\\
y-b&=m(x-a) \label{eq:y-b=m(x-a)}\\
y&=mx+c\label{eq:y=mx+c}\\
y&=m(x-c).\label{eq:y=m(x-c)}
\end{align}
$$

Secara matematis, masing-masing persamaan tentu dapat diubah ke bentuk-bentuk yang lain. Akan tetapi, secara pedagogis atau di dalam proses pembelajaran Matematika di sekolah, apakah semua persamaan tersebut memiliki makna yang sama dan tingkat kemudahan yang sama untuk dipelajari dan dipahami oleh siswa?

Persamaan $\eqref{eq:ax+by=c}$ dan $\eqref{eq:ax+by+c=0}$ sering disebut sebagai **bentuk umum** atau **bentuk baku** persamaan garis. Bentuk ini tidak secara eksplisit memberikan informasi terkait dengan sifat garis, yakni gradien (kemiringan), titik potong dengan sumbu-$x$, titik potong dengan sumbu-$y$, dan titik-titik lain yang dilalui. Sudah tentu sifat-sifat ini dapat dicari/dihitung, namun harus melalui mengubah persamaannya ke bentuk lain atau menyelesaikan persamaan, bahkan sistem persamaan. Sebagai contoh, dari persamaan  ($\ref{eq:ax+by=c}$) dapat diubah ke bentuk ($\ref{eq:ax+by+c=0}$) menjadi:
$$
ax+by-c=0.
$$
Dari bentuk  ($\ref{eq:ax+by=c}$) dapat diubah ke bentuk ($\ref{eq:intercept-form}$) menjadi:
$$
\frac x{c/a}+\frac y{c/b}=1.
$$
Persamaan garis ($\ref{eq:intercept-form}$) disebut **bentuk titik potong** karena bentuk ini menginformasikan titik potong garis dengan sumbu-$x$ dan sumbu-$y$. Garis yang dinyatakan dengan bentuk ($\ref{eq:intercept-form}$) memotong sumbu-$x$ di $(a,0)$ dan memotong sumbu-$y$ di $(0,b)$. 

Dari bentuk  ($\ref{eq:ax+by=c}$) dapat diubah ke bentuk ($\ref{eq:y=mx+c}$) menjadi:
$$
y=\left(\frac{-a}b\right) x+\frac c b.\label{eq:kan2baku}
$$
Dari bentuk ($\ref{eq:kan2baku}$) dapat diubah ke bentuk ($\ref{eq:y=m(x-c)}$) menjadi:
$$
y=\frac{-a}b\left(x-\frac ca\right).\label{eq:kan2transf}
$$
Langkah-langkah ini bisa jadi merupakan langkah-langkah yang tidak mudah dipahami dan dilakukan oleh siswa SMP, karena melibatkan proses pembagian. Jadi, dari sudut pandang pedagogis, persamaan ($\ref{eq:ax+by=c}$) dan ($\ref{eq:ax+by+c=0}$) berpotensi dapat menimbulkan kesulitan belajar dan memahami persamaan garis serta interpretasinya. Sebagai konsekuensinya, sebaiknya dalam pembelajaran persamaan garis guru tidak memperkenalkan bentuk ($\ref{eq:ax+by=c}$) dan ($\ref{eq:ax+by+c=0}$) ketika hendak membahas tentang persamaan garis lurus. Demikian juga, ketika hendak menjelaskan persamaan garis yang mempunyai sifat-sifat tertentu, misalnya diketahui gradien dan salah satu titik yang dilalui, garis yang melalui dua titik, garis yang memotong sumbu-$x$ dan sumbu-$y$, dan sebagainya, tidak menggunakan kedua bentuk tersebut. Bagaimana dengan bentuk-bentuk persamaan garis yang lain?

Persamaan garis dalam bentuk titik potong ($\ref{eq:intercept-form}$) biasanya tidak diperkenalkan pada pelajaran Matematika di SMP. Siswa SMP mungkin tidak mudah mengubah bentuk persamaan lain ke bentuk titik potong ini, karena menyangkut pembagian, bahkan boleh jadi pembagian dengan pecahan, sesuatu yang rumit.

## Pendekatan Lama

Pada pembelajaran persamaan garis di SMP, biasanya yang digunakan adalah bentuk  ($\ref{eq:y-b=m(x-a)}$)  dan ($\ref{eq:y=mx+c}$). Persamaan garis bentuk ($\ref{eq:y-b=m(x-a)}$)  disebut **bentuk gradien-titik**, karena persamaan ini menginformasikan gradien garis ($m$) dan titik yang dilalui garis, yakni $(a,b)$. Persamaan ini tidak efisien, karena memuat tiga nilai, yakni $a,\ b, m$, namun informasi yang diberikan hanya dua.

Persamaan garis bentuk ($\ref{eq:y=mx+c}$) disebut **bentuk gradien-titik potong**. Persamaan ini juga hanya memberikan dua informasi, yakni:

* $m$: gradien (kemiringan) garis, dan
* $c$: ordinat titik potong dengan sumbu-$y$.

<center><figure><img src="C:\Users\Sahid\AppData\Roaming\Typora\typora-user-images\image-20211220141754126.png" alt="image-20211220101257101" style="zoom:75%;"/><p>
<figcaption> <b>Gambar 1. </b>Tampilan Media GeoGebra untuk menjelaskan pengertian gradien garis</figcaption></p>
</figure></center>

Jadi persamaan ini hanya menginformasikan gradien dan satu titik yang dilalui oleh garis tersebut, yakni titik $(0,c)$. Tidak terdapat informasi lain yang dapat diperoleh secara langsung dari persamaan tersebut. 

Yang biasanya tidak dibahas secara jelas adalah makna gradien. Biasanya pada buku-buku pelajaran Matematika SMP maupun pada pembelajaran oleh guru hanya disebutkan bahwa gradien adalah **kemiringan** garis. Ini bukanlah penjelasan atau makna gradien, melainkan hanya kata atau istilah lain. Jadi, menjelaskan gradien dengan kata kemiringan, atau juga menggunakan istilah lain ***slope*** itu belum menjelaskan pengertian. **Gambar 1** menunjukkan tampilan suatu media pembelajaran menggunakan **GeoGebra** untuk menjelaskan pengertian gradien garis.

Gradien sebuah garis adalah nilai perubahan $y$​ apabila nilai $x$​ berubah 1 satuan.  Jadi, pada garis dengan persamaan
$$
y=mx, \label{eq:y=mx}
$$
nilai $y$ akan berubah sebesar $m$ satuan apabila nilai $x$ berubah sebesar 1 satuan. Jadi, apabila garis tersebut melalui titik $(p,q)$, maka garis tersebut akan melalui titik-titik 
$$
(p+1, q+m),\ (p-1, q-m),\ (p+2, q+2m),\ (p-2, q-2m), ....
$$
Secara umum, apabila nilai $x$ berubah sebesar $k$, maka nilai $y$ berubah sebesar $k.m$. Dari sini juga dapat dijelaskan bahwa gradien suatu garis adalah **perbandingan perubahan nilai $y$ terhadap perubahan nilai $x$ antar dua titik pada garis tersebut**. Pengertian ini cocok dengan fakta, karena apabila pada persamaan   ($\ref{eq:y=mx}$) nilai $x$ diganti dengan $x+k$, maka 
$$
y=m(x+k)=mx+mk,
$$
yang artinya nilai $y$ berubah menjadi $mx+mk$. Inilah makna sebenarnya kata gradien, kemiringan, atau *slope* suatu garis. Dalam buku-buku Matematika SMP (atau yang dijelaskan guru) biasanya adalah “perbadingan $y$ dan $x$”. Penjelasan ini tentu tidak benar, karena bukan itulah yang dimaksud gradien.

Selanjutnya, yang kurang mendapat perhatian di dalam pembelajaran garis di sekolah adalah makna $c$ pada persamaan ($\ref{eq:y=mx+c}$). Di atas sudah disebutkan makna nilai $c$ tersebut. Secara geometris, nilai $c$ mempunyai makna yang sangat penting, dan apabila guru dapat menjelaskan dengan benar, siswa akan belajar dua hal sekaligus ketika mempelajari persamaan garis lurus, yakni geometri transformasi. Harus dijelaskan bahwa garis $y=mx+c$ sangat berhubungan dengan garis $y=mx$. Pertama, kedua garis memiliki gradien yang sama, yakni $m$. Kedua, garis $y=mx$ melalui titik $(0,0)$, sedangkan garis $y=mx+c$ melalui titik $(0, c)$. Dengan demikian, garis $y=mx+c$ dapat diperoleh dengan menggeser searah sumbu-$y$ sejauh $c$. Sayang, karena guru kurang dapat menjelaskan keterkaitan demikian, pembelajaran persamaan garis dan geometri transformasi dilakukan secara terpisah dan tidak saling dikaitkan satu sama lain, maka siswa mengalami beban belajar (*cognitive load*) yang berlebih dan kebingungan serta kesulitan belajar matematika.

<center><figure><img src="C:\Users\Sahid\AppData\Roaming\Typora\typora-user-images\image-20211221055852245.png" alt="image-20211220101257101" style="zoom:75%;"/><p>
<figcaption> <b>Gambar 2. </b>Tampilan Media GeoGebra untuk menjelaskan hubungan garis y=mx+c dan y=mx</figcaption></p>
</figure></center>

## Pendekatan Baru

Perhatikan contoh terakhir yang diperlihatkan pada **Gambar 2**. Persamaan garisnya adalah $y=2x+3$. Pada gambar tersebut diperlihatkan bahwa menggeser garis $y=2x$ ke atas sejauh $+3$ satuan sama saja menggeser garis $y=2x$ ke kiri sejauh $-\frac32$ satuan. Tanda plus menunjukkan translasi ke kanan atau ke atas, tanda minus menunjukkan translasi ke kiri atau ke bawah. Menggeser ke kiri garis $y=mx$ sama saja menggeser ke kanan sumbu-$y$, sehingga nilai-nilai $x$ pada persamaan $y=2x$ bertambah dengan $\frac32$, sehingga persamaannya dapat ditulis sebagai
$$
y=2(x+\frac 32)\notag.
$$
Ini tidak lain adalah persamaan $y=2x+3$.

<center><figure><img src="C:\Users\Sahid\AppData\Roaming\Typora\typora-user-images\image-20211221114123125.png" alt="image-20211220101257101" style="zoom:70%;"/><p>
<figcaption> <b>Gambar 3. </b>Tampilan Media GeoGebra untuk menjelaskan hubungan garis y=m(x-c) dan y=mx</figcaption></p>
</figure></center>

Sekarang perhatikan persamaan garis ($\ref{eq:y=m(x-c)}$),
$$
y=m(x-c). \notag
$$
Apakah keuntungan penyajian persamaan garis dalam bentuk ($\ref{eq:y=m(x-c)}$)? Bentuk ini disebut **bentuk gradien-titik potong 2**, untuk membedakan dengan bentuk gradien-titik potong ($\ref{eq:y=mx+c}$).  Persamaan tersebut menginformasi beberapa hal, yakni:

1. $m$ merupakan gradien garis,
2. $c$ adalah absis titik potong garis dengan sumbu-$x$,
3. $-mc$ menyatakan ordinat titik potong garis dengan sumbu-$y$,
4. garis tersebut melalui dua titik, yakni: $(c,0)$ dan $(0,-mc)$.

Informasi yang diperoleh menjadi dua kalinya dibandingkan dengan informasi pada persamaan ($\ref{eq:y=mx+c}$). Apakah hanya itu informasi yang diperoleh dari persamaan terakhir? Tidak!

* Persamaan ($\ref{eq:y=m(x-c)}$) juga menginformasikan bahwa garis tersebut dapat diperoleh dengan menggeser (atau men-translasi-kan) garis $y=mx$ searah  sumbu-$x$ sejauh $c$. Hal ini dapat dilihat dari nilai $x$ yang dikurangi dengan $c$. Apabila nilai $c$ positif, maka translasinya ke kanan, dan apabila nilai $c$ negatif, maka translasinya ke kiri.
* Secara ekuivalen, translasi garis ke searah sumbu-$x$ juga dapat dipandang sebagai translasi garis searah sumbu-$y$ sejauh $-mc$. Ingat, makna gradien yang sudah dijelaskan di atas. Karena gradien garisnya adalah $m$, maka jika nilai $x$ berubah sebesar $-c$, maka nilai $y$ berubah sebesar $-mc$. Ini cocok dengan persamaan ($\ref{eq:y=m(x-c)}$).

Jadi, sebenarnya persamaan setiap garis dapat dengan mudah didapat jika kita sudah tahu titik potong garis tersebut dengan sumbu-$x$ dan sumbu-$y$. Mengapa demikian? Karena kedua titik potong tersebut secara otomatis menginformasinya gradien garisnya, yakni perbandingan ordinat titik potong garis dengan sumbu-$y$ dengan absis titik potong garis dengan sumbu-$x$. 

Persamaan garis dalam bentuk gradien-titik potong 2 merupakan persamaan yang paling efisien dibandingkan dengan bentuk-bentuk lain, karena bentuk gradien-titik potong hanya memuat dua nilai, namun informasi yang diberikan lebih dari dua. Selain itu, secara umum bentuk persamaannya tidak memuat pembagian. Bentuk ini sangat cocok untuk diperkenalkan pada pelajaran persamaan garis di SMP.

Bentuk gradien-titik potong 2 juga dapat digunakan untuk menyatakan semua persamaan garis dengan informasi atau sifat-sifat garis yang diketahui:

1. gradien dan titik potong garis dengan sumbu-$x$,
2. gradien dan titik potong garis dengan sumbu-$y$,
3. titik potong garis dengan sumbu-$x$ dan sumbu-$y$,
4. gradien dan titik yang dilalui, dan
5. dua titik yang dilalui garis.

### Kasus 1: Garis melalui titik pangkal koordinat

Persamaan garis yang melalui titik asal $(0,0)$ adalah ($\ref{eq:y=mx}$):
$$
y=m(x-0)=mx,\notag
$$
 untuk semua nilai $m$ bilangan riil. 

### Kasus 2: Diketahui gradien dan titik potong garis dengan sumbu-$x$

Tentukan persamaan garis dengan gradien $m$ dan melalui titik $a,0$.

Berdasarkan sifat nomor 2 pada penjelasan persamaan ($\ref{eq:y=m(x-c)}$), persamaan garis dimaksud adalah
$$
y=m(x-a).\label{eq:y=m(x-a)}
$$

| Gradien<br> (Diketahui) | Titik potong dengan<br/> sumbu-$x$  (Diketahui) | Persamaan garis   |
| ----------------------- | ----------------------------------------------- | ----------------- |
| $-2$                    | $(3,0)$                                         | $y=-2(x-3)$       |
| $2$                     | $(-1,0)$                                        | $y=2(x+1)$        |
| $1/2$                   | $(-4,0)$                                        | $y=\frac12(x+4)$  |
| $-2/3$                  | $(3,0)$                                         | $y=-\frac23(x-3)$ |

### Kasus 3: Diketahui gradien dan titik potong garis dengan sumbu-$y$

Tentukan persamaan garis dengan gradien $m$ dan melalui titik $(0,c)$.

Menurut sifat nomor 3 pada penjelasan persamaan ($\ref{eq:y=m(x-c)}$) di atas, persamaan garisnya adalah:
$$
y=m\left(x-(-\frac cm)\right)\quad\text{atau}\quad y=m(x+\frac cm).
$$

| Gradien<br/> (Diketahui) | Titik potong dengan <br/>sumbu-$y$ (Diketahui) | Persamaan garis                             |
| ------------------------ | ---------------------------------------------- | ------------------------------------------- |
| $-2$                     | $(0,3)$                                        | $y=-2(x-\frac32)$                           |
| $2$                      | $(0,-1)$                                       | $y=2(x-\frac12)$                            |
| $1/2$                    | $(0,-4)$                                       | $y=\frac12(x-\frac4{\frac12})=\frac12(x-8)$ |
| $-2/3$                   | $(0,3)$                                        | $y=-\frac23(x-3)$                           |

### Kasus 4: Diketahui titik potong garis dengan sumbu-$x$ dan sumbu-$y$

Berdasarkan sifat nomor 4 pada penjelasan persamaan ($\ref{eq:y=m(x-c)}$), persamaan garis yang melalui titik $(p,0)$ dan $(0,q)$ adalah:
$$
y=-\frac qp(x-p).\label{eq:garisx2y}
$$
Perhatikan, apabila $x=p$, maka pada persamaan ($\ref{eq:garisx2y}$) nilai $y=0$ dan jika $y=0$, maka nilai $x=q$. Beberapa contoh kasus disajikan pada tabel di bawah ini.

| Titik potong dengan sumbu-$x$ <br/>dan sumbu-$y$ (Diketahui) | Persamaan garis                        |
| ------------------------------------------------------------ | -------------------------------------- |
| $(3,0)$ dan $(0, 5)$                                         | $y=-\frac53(x-5)$                      |
| $(3,0 )$ dan $(0, -6)$                                       | $y=-\frac{-6}3(x-3)=2(x-3)$            |
| $(-2,0)$ dan $(0,6)$                                         | $y=-\frac 6{-2}(x+2)=3(x+2)$           |
| $(-3,0)$ dan $(0,-5)$                                        | $y=-\frac{-5}{-3}(x+3)=-\frac 53(x+3)$ |

### Kasus 5: Diketahui gradien dan titik yang dilalui garis

Tentukan persamaan garis dengan gradien $m$ dan melalui titik $(p,q)$.

Sesuai bentuk ($\ref{eq:y-b=m(x-a)}$), maka persamaan garisnya adalah:
$$
y-q=m(x-p).\notag
$$
Apabila bentuk terakhir dinyatakan ke bentuk ($\ref{eq:y=m(x-c)}$), maka diperoleh:
$$
y=m(x-p+\frac qm).\notag
$$
Bentuk tersebut juga dapat diperoleh secara langsung dengan cara mencari titik potong garis dengan sumbu-$x$, misalnya $(a,0)$. Dari titik $(p,q)$ ke titik $(a,0)$, besar perubahan nilai $x$ adalah $a-p$ dan perubahan nilai $y$ adalah $-q$, sehingga berlaku
$$
m=\frac{-q}{a-p}\quad\text{atau}\quad a=p-\frac qm.\notag
$$
Jadi persamaan garisnya adalah
$$
y=m(x-(p-\frac qm))=m(x-p+\frac qm),\notag
$$
yakni, hasil yang sama dengan sebelumnya. Keuntungan pendekatan ini adalah siswa akan menggunakan pengetahuan tentang gradien garis untuk menentukan titik potong garis dengan sumbu-$x$.

| Gradien Garis<br/> (Diketahui) | Titik yang dilalui<br/> (Diketahui) | Titik potong dengan sumbu-$x$ | Persamaan garis   |
| ------------------------------ | ----------------------------------- | ----------------------------- | ----------------- |
| $3$                            | $(3,6)$                             | $(1,0)$                       | $y=3(x-1)$        |
| $2/3$                          | $(-1,4)$                            | $(-7,0)$                      | $y=\frac23(x+7)$  |
| $-2$                           | $(4,-2)$                            | $(3,0)$                       | $y=-2(x-3)$       |
| $-1/2$                         | $(-3,-2)$                           | $(-7,0)$                      | $y=-\frac12(x+7)$ |

### Kasus 6: Garis melalui dua titik berbeda

Tentukan persamaan garis yang melalui titik $(1,1)$ dan $(5,6)$. Dapatkah kita menentukan persamaan garisnya dengan menggunakan pendekatan titik potong garis tersebut dengan sumbu-$x$ dan sumbu-$y$?

Pertama, kita cari tahu berapakah gradien garis tersebut? Perhatikan perubahan $x$ dan perubahan $y$ dari kedua titik tersebut. Perubahan nilai $x$ adalah sebesar $5-1=4$ dan perubahan nilai $y$ adalah sebesar $6-1=5$. Jadi gradien garis tersebut adalah $m=5/4$. Selanjutnya, kita cukup mencari titik potong garisnya dengan sumbu-$x$. Kita gunakan titik $(1,1)$ sebagai pangkal menuju titik potong dengan sumbu-$x$, misalnya $(a,0)$. Dari $(1,1)$ ke $(a,0)$ besar perubahan $x$ adalah $a-1$ dan besar perubahan $y$ adalah -1, Jadi 
$$
\frac54=\frac{-1}{a-1}\quad \text{atau }\quad a=1-\frac 45(1)=\frac 15.\notag
$$
Jadi, garis tersebut memotong sumbu-$x$ di $(\frac15,0)$.  Dengan demikian, berdasarkan sifat 2 pada penjelasan persamaan ($\ref{eq:y=m(x-c)}$) di atas, persamaan garisnya adalah
$$
y=\frac54(x-\frac15).
$$
Karena gradiennya $m=\frac54$, maka garis tersebut memotong sumbu-$y$ di $(0,-\frac14)$. 

Secara umum, untuk mencari persamaan garis yang melalui titik $(x_1,y_1)$ dan $(x_2,y_2)$ dapat dilakukan dengan tiga langkah, yakni:

1. menghitung gradien garis tersebut, yakni:
   
   $$
   m=\frac{y_2-y_1}{x_2-x_1},
   $$

2. mencari absis titik potong dengan sumbu-$x$ sebagai berikut:
   
   Dengan menggunakan titik $(x_1,y_1)$ sebagai pangkal, jika titik potong dengan sumbu-$x$ adalah $(a,0)$, maka
   
   $$
   \begin{align}
\frac{y_2-y_1}{x_2-x_1}&=\frac{-y_1}{a-x_1}\notag\\
a&=x_1-y_1\left(\frac{x_2-x_1}{y_2-y_1} \right).
\end{align}
   $$

3. menggunakan persamaan ($\ref{eq:y=m(x-c)}$) untuk mendapatkan persamaan garis yang diminta, yakni:

$$
y=\frac{y_2-y_1}{x_2-x_1}\left(x-x_1+y_1(\frac{x_2-x_1}{y_2-y_1}) \right).\label{eq:garis2titik}
$$

Perhatikan, persamaan ($\ref{eq:garis2titik}$) ekuivalen dengan
$$
(x_2-x_1)(y-y_1)=(y_2-y_1)(x-x_1),
$$
yang merupakan persamaan garis melalui $(x_1,y_1)$ dan $(x_2,y_2)$, namun persamaan terakhir tidak memberikan informasi langsung sifat garisnya. Persamaan yang sama (ekuivalen) tentu dapat juga diperoleh apabila titik pangkal yang digunakan pada langkah 2 di atas adalah titik kedua.

| Dua titik yang dilalui garis<br/> (Diketahui) | Gradien                | Titik potong garis <br> dengan sumbu-$x$                                             | Persamaan Garis         |
| --------------------------------------------- | ---------------------- | ------------------------------------------------------------------------------------ | ----------------------- |
| $(0,0)$ & $(2,4)$                             | $2$                    | $(0,0)$                                                                              | $y=2(x-0)=2x$           |
| $(1,2)$ & $(4,5)$                             | $1$                    | $(-1,0)$                                                                             | $y=1(x+1)=x+1$          |
| $(-3,4)$ & $(5,-2)$                           | $\frac 6{-8}=-\frac34$ | $(\frac73,0)$ Keterangan:<br>$-\frac34=\frac{-4}{a+3}$<br> $a=-3+\frac{16}3=\frac73$ | $y=-\frac34(x-\frac73)$ |
| $(-2,4)$ & $(1,-2)$                           | $-3$                   | $(-\frac23,0)$ Keterangan:<br> $-3=\frac{-4}{a+2}$<br> $a=-2+\frac43=-\frac23$       | $y=-3(x+\frac23)$       |

## Kesimpulan

Setiap garis dapat ditentukan oleh dua hal, misalnya: (1) gradien dan titik potong garis dengan sumbu-$x$, (2) gradien dan titik potong garis dengan sumbu-$y$, (3) titik potong garis dengan sumbu-$x$ dan sumbu-$y$, (4) gradien dan titik yang dilalui, atau (5) dua titik yang dilalui garis. Sementara itu, persamaan garis lurus dapat dinyatakan dalam berbagai bentuk, di antaranya bentuk umum atau baku, bentuk titik potong, bentuk gradien–titik, bentuk gradien titik potong, dan bentuk gradien titik potong 2. Bentuk baku (umum) persamaan garis tidak memuat informasi secara langsung sifat-sifat garis. Bentuk titik potong menginformasikan secara langsung absis titik potong garis dengan sumbu-$x$ dan ordinat titik potong garis dengan sumbu-$y$. Mengubah persamaan garis ke bentuk titik potong tidaklah sederhana bagai siswa SMP. Bentuk baku dan bentuk titik potong biasanya tidak diajarkan di SMP. 

Pada pembelajaran persamaan garis di SMP biasanya yang dibahas adalah bentuk gradien-titik dan bentuk gradien-titik potong. Bentuk gradien-titik merupakan bentuk persamaan garis yang tidak efisien, karena memuat tiga parameter, namun informasi yang diberikan secara langsung hanya dua hal, yakni gradien garis dan titik yang dilalui. Bentuk gradien-titik potong memuat dua parameter dan dua informasi langsung, yakni gradien garis dan ordinat titik potong garis dengan sumbu-$y$. 

Bentuk persamaan garis yang paling efisien adalah bentuk gradien-titik potong 2, yakni ($\ref{eq:y=m(x-c)}$). Bentuk ini hanya memuat dua parameter, namun memuat informasi langsung yang lengkap, yakni gradien garis, absis titik potong dengan sumbu-$x$, ordinat titik potong dengan sumbu-$y$, sekaligus dua titik yang dilalui oleh garis tersebut. Selain itu, persamaan ini juga menginformasikan hal yang tidak diinformasikan oleh semua bentuk persamaan lain, yakni bentuk ini menunjukkan secara langsung transformasi (translasi) garis yang melalui titik pangkal koordinat searah sumbu-$x$ atau secara ekuivalen translasi searah sumbu-$y$. Translasi searah sumbu-$x$ merupakan sifat yang penting dan dapat diterapkan pada persamaan-persamaan kurva lain secara umum.

Bentuk gradien – titik potong 2 dapat digunakan untuk menyatakan secara langsung persamaan garis yang diketahui informasinya dalam bentuk apapun, di antara lima kemungkinan yang disebutkan di atas. Kuncinya adalah pengertian gradien garis. Oleh karena di dalam pembelajaran persamaan garis, pengertian gradien garis harus dibahas secara mendalam dan siswa harus memahami secara komprehensif konsep gradien garis. Dengan pemahaman gradien garis, untuk garis yang diketahui dua titik (di luar sumbu-sumbu koordinat) yang dilalui, maka harus ditentukan titik potong garis dengan sumbu-$x$. Selanjutnya persamaan garis dalam bentuk gradien – titik potong 2 dapat dengan mudah ditentukan.

Pembelajaran persamaan garis lurus dengan menggunakan pendekatan (bentuk) gradien – titik potong 2, siswa dipaksa untuk memahami konsep gradien sekaligus belajar konsep transformasi (translasi) kurva, yang dapat diterapkan untuk belajar kurva-kurva atau grafik fungsi yang lain, seperti fungsi kuadratik, fungsi trigonometri, dan sebagainya. 

## Daftar Referensi

Butler, Douglas (2015). “ax + b” is dead, long live “a(x – b)”. Douglas Butler on transformations of polynomial and trigonometric functions. *MATHEMATICS TEACHING* Issue 248 (September 2015), pages 5-6. available at https://www.tsm-resources.com/pubs/atm/MT-248/pdf/ax+b.pdf.

Wikipedia contributors. (2021, November 18). “Linear equation”. In *Wikipedia, The Free Encyclopedia*. Retrieved 13:19, December 21, 2021, from https://en.wikipedia.org/w/index.php?title=Linear_equation&oldid=1055950543
