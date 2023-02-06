<h1 style="text-align:left">Membuat Dokumen Matematika dengan Markdown di Typora</h1>

**Sahid**

Jurusan Pendidikan Matematika, FMIPA Universitas Negeri Yogyakarta

[sahid@uny.ac.id](), [sahidyk@gmail.com]() 





## LaTeX dan MathJax

Sebagaimana sudah diketahui secara umum, salah satu cara untuk menulis simbol, notasi, dan ekspresi matematika pada dokumen-dokumen ilmiah yang menghasilkan kualitas cetak secara profesional adalah menggunakan LaTeX. LaTeX dapat digunakan juga pada dokumen Markdown. Secara garis besar terdapat dua program yang biasa digunakan untuk memungkinkan pemakaian LaTeX, yaitu **MathJax** dan **KaTeX**. MathJax adalah skrip (program) dalam bahasa Javascript yang memungkinkan kita menampilkan simbol, notasi, dan ekspresi matematika tanpa harus meng-instal software TeX/LaTeX. Dokumen ini bertujuan mengeksplor kemampuan Markdown (dengan editor Typora) dan MathJax dalam memproses perintah-perintah LaTeX. Untuk mengetahui apakah Anda menggunakan MathJax atau KaTeX, Anda harus memeriksa editor Markdown yang Anda gunakan. Sebagian editor Markdown menggunakan MathJax, sebagian yang lain menggunakan KaTeX. Secara umum, keduanya sama-sama mengenal perintah-perintah LaTeX, namun MathJax mengenal lebih banyak perintah LaTeX, namun KaTeX lebih cepat memproses (Akan tetapi mungkin perbedaan kecepatan ini tidak begitu kentara jika Anda hanya menuliskan ekspresi matematika sederhana). 

Typora menggunakan MathJax untuk memproses perintah-perintah LaTeX. Semua contoh teks matematika pada dokumen ini diproses dengan MathJax pada editor Markdown **Typora**. Dokumen ini sekaligus menunjukkan sejauh mana kemampuan Typora dan MathJax dalam memproses perintah-perintah LaTeX. Typora juga dapat menampilkan nomor persamaan secara otomatis untuk ekspresi matematika pada modus *display*. 

```latex
Fungsi Gamma, $\Gamma(z)$ didefinisikan sebagai:
$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$
```

Fungsi Gamma, $\Gamma(z)$ didefinisikan sebagai:
$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

```latex
Fungsi tersebut memenuhi $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$.
```

Fungsi tersebut memenuhi $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$.

Contoh lain:

```latex
Akar/penyelesaian persamaan kuadrat $ax^2+bx+c=0$ adalah:
$$
x = {-b \pm \sqrt{b^2-4ac} \over 2a}.
$$
```
Akar/penyelesaian persamaan kuadrat $ax^2+bx+c=0$ adalah:
$$
x = {-b \pm \sqrt{b^2-4ac} \over 2a}.
$$
### LaTeX untuk Simbol dan Ekspresi Matematika

1. Untuk menuliskan simbol/notasi/ekspresi matematika pada baris teks digunakan pengapit perintah LaTeX `$...$`. Untuk menampilkan simbol/notasi/ekspresi matematika pada baris terpisah digunakan pengapit perintah LaTeX  `$$...$$`.  (Pada beberapa editor, untuk modus *display*, Anda harus menuliskan pengapit `$$` di atas dan di bawah perintah LaTeX-nya. Pada kasus lain, bahkan Anda harus mengawali dan mengakhirinya dengan baris-baris kosong.) Misalnya, `$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$` akan menghasilkan tampilan $\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$ di tengah teks, sedangkan 
  
   ````
   
   $$
   \sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}.
   $$
   
   ````
   
   menampilkan ekspresi pada baris tersendiri.
   $$
   \sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}.
   $$
   Contoh lain, rumus teorema binomial:
   $$
   \left(x+a\right)^n=\sum_{k=0}^{n}{\binom{n}{k}x^ka^{n-k}}.
   $$
   
   
   Banyak ekspresi matematika seperti pecahan, jumlah, limit, dan integral ditampilkan secara berbeda ketika ditulis pada baris teks dan ditampilkan pada baris terpisah. Anda dapat berganti-ganti model penulisan dengan menggunakan `\displaystyle ` dan `\textstyle` untuk mendapatkan tampilan yang diinginkan.
   
   Berikut adalah contoh berganti model penulisan dalam persamaan yang ditampilkan.
   
   ```latex
   $$
   \sum_{n=1}^\infty \frac{1}{n^2} \to
     \textstyle \sum_{n=1}^\infty \frac{1}{n^2} \to
     \displaystyle \sum_{n=1}^\infty \frac{1}{n^2}.
   $$
   ```
   
   $$
   \sum_{n=1}^\infty \frac{1}{n^2} \to
     \textstyle \sum_{n=1}^\infty \frac{1}{n^2} \to
     \displaystyle \sum_{n=1}^\infty \frac{1}{n^2}
   $$
   
   Juga dimungkinkan untuk melakukan pergantian model pada persamaan di baris teks.
   
   ```latex
   Bandingkan tampilan $\displaystyle \lim_{t \to 0} \int_t^1 f(t)\, dt$ dan $\lim_{t \to 0} \int_t^1 f(t)\, dt$.
   ```
   Bandingkan tampilan $\displaystyle \lim_{t \to 0} \int_t^1 f(t)\, dt$ dan $\lim_{t \to 0} \int_t^1 f(t)\, dt$.
   
2. Untuk menuliskan **huruf Yunani**, gunakan `\alpha, \beta, ..., \omega`: $\alpha,\ \beta,\ ...,\ \omega$. Untuk huruf besar, gunakan `\Gamma, \Delta, ..., \Omega`: $\Gamma,\ \Delta,\ ...,\ \Omega$. Beberapa huruf Yunani memiliki bentuk varian: `\epsilon, \varepsilon, \phi, \varphi` $\epsilon,\ \varepsilon,\ \phi,\ \varphi$, dan lain-lain. Secara umum, Anda harus mencari di dalam tabel panjang tentang simbol tertentu yang Anda cari, seperti $Ψ,\ δ,\ ζ,\ ≥,\ ⊆$, …. Dan , ternyata pekerjaan ini dapat memakan waktu dan membuat frustrasi, yang dapat menyebabkan Anda berpikir betapa sulitnya menulis matematika dengan $\LaTeX$, padahal hal ini mungkin hanya terjadi sekali. Setelah Anda terbiasa, maka Anda tidak lagi perlu mencari.

3. Untuk **superskrip** dan **subskrip**, gunakan `^` dan `_`. Contohnya, `x_i^2`: $x_i^2$,  dan`\log_2 x`: $\log_2 x$. Contoh lain tentang indeks tensor: `T^{\alpha\beta}{}_{\gamma\delta}`: $T^{\alpha\beta}{}_{\gamma\delta}$, `T^{\alpha \beta}{}_{\gamma\delta}{}^{\lambda}`: $T^{\alpha \beta}{}_{\gamma\delta}{}^{\lambda}$. Jadi misalnya, tensor (2,2) akan bertindak pada dua kovektor $(\omega, \phi)$ dan dua vektor $(v, w)$ untuk menghasilkan bilangan nyata seperti ini:
   $$
   [T^{\alpha \beta}{}_{\gamma\delta}e_\alpha\otimes e_\beta\otimes e^\gamma \otimes e^\delta](\omega,\varphi,v,w).
   $$
   
4. **Tanda kurung**. Simbol `()[]` digunakan untuk membuat tanda kurung dan tanda kurung biasa $(2+3)[4+4]$. Gunakan perintah `\{` dan `\}` untuk kurung kurawal $\{\}$.

   Ukuran tanda kurung ini tidak menyesuaikan rumus di antaranya, jadi jika Anda menulis `(\frac{\sqrt x}{y^3})` tanda kurung akan terlalu kecil: $(\frac{\sqrt x}{y^3})$. Gunakan perintah `\left( ... \right)` untuk membuat ukuran tanda kurung menyesuaikan secara otomatis dengan rumus yang mereka apit: `\left(\frac{\sqrt x}{y^3}\right)` menghasilkan tampilan $\left(\frac{\sqrt x}{y^3}\right)$.

   Perintah `\left` dan `\right` berlaku untuk semua jenis tanda kurung: `(` dan `)` $\left( x\right)$, `[` dan `]` $\left[x\right]$, `\{` dan `\}` $\left\{x\right\}$, `|` $\left|x\right|$, `\vert` $\left\vert x\right\vert$, `\Vert` $\left\Vert x\right\Vert$, `\langle` dan `\rangle` $⟨x⟩$, `\lceil` dan `\rceil` $⌈x⌉$, dan `\lfloor` dan `\rfloor` $⌊x⌋$. Perintah `\middle` dapat digunakan untuk menambahkan pembagi tambahan. Anda juga dapat menggunakan tanda kurung yang tidak terlihat, ditandai dengan `.`: `\left.\frac12\right\rbrace` hasilnya $\left.\frac12\right\rbrace$. Perhatikan perintah LaTeX bersifat peka perbedaan huruf besar dan huruf kecil.

   Untuk membuat tanda kurung dengan ukuran diatur secara manual dapat digunakan perintah seperti: 

   `\Biggl( \biggl( \Bigl( \bigl( (x) \bigr) \Bigr) \biggr) \Biggr)` 

   yang menghasilkan $\Biggl(\biggl(\Bigl(\bigl((x)\bigr)\Bigr)\biggr)\Biggr)$. Contoh:

   ```latex
   $$
   f \left( \left[ 
   \frac{1+\left\{x,y\right\}}{\left( \frac{x}{y}+\frac{y}{x}\right)\left(u+1\right)}+a
      \right]^{3/2} \right)
   $$
   ```

   $$
   f\left(
      \left[ 
        \frac{
          1+\left\{x,y\right\}
        }{
          \left(
             \frac{x}{y}+\frac{y}{x}
          \right)
          \left(u+1\right)
        }+a
      \right]^{3/2}
   \right)
   $$

   ```latex
   $$
   \begin{aligned}
         a=&\left(1+2+3+  \cdots \right. \\
           & \cdots+ \left. \infty-2+\infty-1+\infty\right)
   \end{aligned}
   $$
   ```

   $$
   \begin{aligned}
        a=&\left(1+2+3+  \cdots \right. \\
          & \cdots+ \left. \infty-2+\infty-1+\infty\right)
   \end{aligned}
   $$

   ```latex
   $$
   \left\langle q \middle\| \frac{\frac{x}{y}}{\frac{u}{v}} \middle| p \right\rangle
   $$
   ```
   $$
   \left\langle q \middle\| \frac{\frac{x}{y}}{\frac{u}{v}}\middle| p 
    \right\rangle
   $$

   Catatan: `\Big( ... \Big)` menghasilkan tanda kurung besar $\Big( ... \Big)$ yang ukurannya tetap dalam semua situasi, tidak seperti `\left( ... \right)` yang menampilkan tanda kurung dengan ukuran bervariasi sesuai dengan isinya. `\Big` dapat berguna dalam berbagai situasi.

5. Notasi **sigma, hasil kali,** dan **integral**: `\sum` dan `\int`; batas bawah ditulis menggunakan subskrip (indeks) dan batas atas ditulis menggunakan superskrip (pangkat), misalnya, `\sum_1^n` $\sum_1^n$, `\int_0^{\pi}\sin x\ dx` $\int_0^{\pi}\sin x\ dx$. Jangan lupa menggunakan kurung kurawal `{...}` apabila batasnya terdiri atas lebih dari satu simbol atau dihasilkan dengan perintah khusus LaTeX.  Contoh lain, `\sum_{i=0}^\infty i^2` $\sum_{i=0}^\infty i^2$. Notasi lain yang sejenis adalah: `\prod` $∏$, `\int` $∫$, `\bigcup` $⋃$, `\bigcap` $⋂$, `\iint` $∬$, `\iiint` $∭$, \`idotsint` $∫⋯∫$.

6. **Pengelompokan**. Superskrip, subskrip, dan operasi lainnya hanya berlaku untuk "kelompok" berikutnya. "Kelompok" adalah simbol tunggal, atau rumus apa pun yang dikelilingi oleh kurung kurawal `{...}`. Jika Anda mengetik `10^10`, hasilnya akan mengejutkan Anda: $10^10$. Akan tetapi, `10^{10}` menghasilkan seperti yang mungkin Anda harapkan: $10^{10}$. Menggunakan kurung kurawal untuk membatasi superskrip (batas atas atau pangkat) dan subskrip (batas bawah atau indeks: `x^5^6` akan salah karena ambigu; `{x^y}^z` adalah ${x^y}^z$, dan `x^{y^z}` adalah$x^{y^z}$. Perhatikan perbedaan antara `x_i^2` $x_i^2$ dan `x_{i^2}` $x_{i^2}$.

7. **Pecahan**. Ada tiga cara untuk membuat ini. `\frac ab` berlaku untuk dua kelompok berikutnya, dan menghasilkan $\frac ab$; untuk pembilang dan penyebut yang lebih rumit gunakan kurung kurawal `{...}`: `\frac{a+1}{b+1}` untuk $\frac{a+1}{b+1}$. Jika pembilang dan penyebut rumit, Anda mungkin lebih suka menggunakan '\over', yang memisahkan pembilang dan penyebut di dalam tanda kurung kurawal: `{a+1\over b+1}` adalah ${a+1\over b+1}$. Perintah `\cfrac{a}{b}` berguna untuk menampilkan pecahan berlanjut $\cfrac{a}{b}$.

8. **Jenis Huruf**

   + Gunakan perintah `\mathbb` atau `\Bbb` untuk huruf tebal "blackboard":

     $\Bbb{CHNQRZ}$.

   + Gunakan perintah `\mathbf` untuk huruf tebal **boldface**: 

     $\mathbf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$  $\mathbf{abcdefghijklmnopqrstuvwxyz}$.

   + Untuk karakter berbasis ekspresi, gunakan `\boldsymbol` sebagai gantinya: $α$

   + Gunakan `\mathit` untuk huruf miring: 

     $\mathit{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathit{abcdefghijklmnopqrstuvwxyz}$.

   + Gunakan `\pmb` untuk huruf tebal miring: 

     $\pmb{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\pmb{abcdefghijklmnopqrstuvwxyz}$.

   + Gunakan `\mathtt` untuk huruf mesin ketik: 

     $\mathtt{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathtt{abcdefghijklmnopqrstuvwxyz}$.

   + Gunakan `\mathrm` untuk huruf Roman: 

     $\mathrm{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathrm{abcdefghijklmnopqrstuvwxyz}$.

   + Gunakan `\mathsf` untuk huruf sans-serif: 

     $\mathsf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathsf{abcdefghijklmnopqrstuvwxyz}$.

   + Gunakan `$\verb|. . .|$` untuk menghasilkan huruf-huruf:

     $\verb|A, B, C, D, E, ..., X, Y, Z, a, b, c, d, ..., x, y, z|$

   + Gunakan `\mathcal` untuk huruf kaligrafis: 

     $\mathcal{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$

   + Gunakan `\mathscr` untuk huruf tulisan tangan: 

     $\mathscr{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$.

   + Gunakan `\mathfrak` untuk huruf "Fraktur" (huruf Jerman lama): 

     $\mathfrak{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathfrak{abcdefghijklmnopqrstuvwxyz}$.

9. **Tanda akar.** Untuk menuliskan tanda akar gunakan perintah  `\sqrt`, yang otomatis menyesuaikan dengan ukuran argumennya: `\sqrt{x^3}` $\sqrt{x^3}$; `\sqrt[3]{\frac xy}` $\sqrt[3]{\frac xy}$. Untuk ekspresi yang rumit, sebaiknya pergunakan  tanda pangkat $\frac 12$:  `{...}^{1/2}`.

10. **Fungsi-fungsi khusus** seperti "lim", "sin", "max", "ln", dan sejenisnya biasanya dicetak dalam huruf tegak, bukan dengan huruf miring. Gunakan perintah-perintah seperti `\lim`, `\sin`, dan sebagainya, bukan `sin x,  sinx`. Gunakan  subskrip untuk menuliskan nilai variabel pada `\lim`: `\lim_{x\to 0}`: $\displaystyle\lim_{x\to 0} $. 

    Untuk menulis limit fungsi (seperti $\lim \limits_{x \to 1} \frac{x^2-1}{x-1}$), gunakan sintaks ini:

    + Pertama, mulailah dengan `\lim`. Ini akan menghasilkan tulisan $\lim$, bukan $lim$. 

    + Kedua, tambahkan `\limits_{x \to 1}` di belakangnya. Perintah selengkapnya adalah `\lim \limits_{x \to 1}` dan hasilnya $\lim \limits_{x \to 1}$. 

    + Terakhir, tambahkan fungsi yang ingin Anda hitung limitnya. Jadi, secara lengkap Anda menuliskan `\lim\limits_{x \to 1} \frac{x^2-1}{x-1}`   untuk menghasilkan $\lim\limits_{x \to 1} \frac{x^2-1}{x-1}$ (Sudah tentu jangan lupa pengapit dolarnya).

    Mengapa Anda harus menuliskan  `\lim \limits_{x \to 1}` dan bukannya  `\lim_{x \to 1}`? Inilah bedanya: $\lim_{x \to 1}$, jika Anda menggunakan yang terakhir.
    Nama fungsi non-standar dapat ditulis dengan sintaks: `\operatorname{fungsi}(x)`: $\operatorname{fungsi}(x)$. Sintaks `\operatorname{arsinh}(x)` menghasilkan $ \operatorname{arsinh}(x)$.    Untuk operator yang memerlukan batasan di atas dan di bawah operator, gunakan `\operatorname*{...}`, seperti `\operatorname*{Res}_{z=1}\left(\frac1{z^2-z}\right)=1`: $\operatorname*{Res}_{z=1}\left(\frac1{z^2-z}\right)=1$.

11. Terdapat sejumlah besar **simbol dan notasi khusus**, terlalu banyak untuk didaftar di sini. Berikut adalah daftar sebagian kecil simbol dan notasi dalam matematika.

    + Notasi ketaksamaan: `\lt, \gt, \le, \leq, \leqq, \leqslant, \ge, \geq, \geqq, \geqslant, \neq`:$\lt,\ \gt,\ \le,\ \leq,\ \leqq,\ \leqslant,\ \ge,\ \geq,\ \geqq, \ \geqslant,\ \neq$. Gunakan  `\not` untuk mencoret simbol-simbol tersebut, misalnya $\not\lt$, meskipun terkadang terlihat tidak bagus. Simbol lain: $x \gvertneqq y,\ x \lvertneqq y,\ \gtrless,\ \lessgtr,\ \gtreqless,\ \lesseqgtr,\ \gtreqqless,\ \lesseqgtr$

    + Simbol operasi: `\times, \div, \pm, \mp` $\times,\ \div,\ \pm,\ \mp$. `\cdot` menghasilkan tanda titik di tengah: $x⋅y$. Perhatikan perbedaan perintah `\ldots`, seperti pada  $a_1,\ a_2,\ \ldots,\ a_n$, dan  `\cdots`, seperti pada $a_1+a_2+\cdots+a_n$.

    + Simbol-simbol terkait himpunan: `\cup, \cap, \setminus, \subset, \subseteq, \subsetneq, \supset, \in, \notin, \emptyset, \varnothing`: $\cup,\ \cap,\ \setminus,\ \subset,\ \subseteq,\ \subsetneq,\ \supset,\ \in,\ \notin,\ \emptyset,\ \varnothing$.

    + Notasi binomial: `{n+1 \choose 2k}` atau `\binom{n+1}{2k}`: $\binom{n+1}{2k}$.

    + Simbol aneka panah: `\to, \rightarrow, \leftarrow, \Rightarrow, \Leftarrow, \mapsto`:  $\to, \ \rightarrow,\ \leftarrow,\ \Rightarrow,\ \Leftarrow,\ \mapsto$. 

    + Untuk simbol implikasi, `\implies` ($\implies$) adalah alternatif yang lebih disukai sebagai pengganti `\Rightarrow` ($\Rightarrow$). Terdapat juga `\iff` $\iff$ dan `\impliedby` ($\impliedby$).

    + Perintah `\to` ($\to$) lebih baik daripada `\rightarrow` atau `\longrightarrow` untuk menuliskan definisi fungsi, seperti $f:A\to B$. Kebalikannya adalah `\gets` ($\gets$). Perhatikan perbedaan antara `\to` dan `\mapsto`, seperti  `T:\mathbb R\to \mathbb R,\; x\mapsto x+1`: $T:\mathbb R\to \mathbb R,\; x\mapsto x+1$, `p\land((q\lor r)\to s)`: $p\land((q\lor r)\to s)$, `x+2=4-x\implies x=1`: $x+2=4-x\implies x=1$, `\overset{3.1415}{\underset{26535}{\implies}}`: $\overset{3.1415}{\underset{26535}{\implies}}$.

    + Simbol-simbol dalam logika: `\land, \lor, \lnot, \forall, \exists, \top, \bot, \vdash, \vDash` $\land,\ \lor,\ \lnot,\ \forall,\ \exists,\ \top,\ \bot,\ \vdash,\ \vDash$.

    + Simbol-simbol operator abstrak: `\star, \ast, \oplus, \circ, \bullet` $\star,\ \ast,\ \oplus,\ \circ,\ \bullet$∙

    + Simbol hampiran, kesebangunan, konkruensi, ekuivalensi, dan kesimpulan: `\approx, \thickapprox, \sim, \thicksim, \backsim, \simeq, \cong, \equiv, \prec, \lhd, \therefore` $\approx,\ \thickapprox,\ \sim,\ \thicksim,\ \backsim,\ \simeq,\ \cong,\ \equiv,\ \prec,\ \lhd,\ \therefore$.

    + Untuk ekuivalensi modulo, gunakan  `\pmod` seperti: `a\equiv b\pmod n` $a\equiv b\pmod n$, sedangkan untuk operator biner modulo, gunakan  `\bmod` seperti: `a\bmod 17` $a\bmod 17$. Hindari penggunaan `\mod`, karena perintah ini akan menghasilkan spasi berlebihan: `a\mod 17` $a\mod 17$.

    + Simbol ketak-hingga-an: `\infty, \aleph_0` $\infty,\ \aleph_0$, nabla dan diferensial parsial:`\nabla, \partial` $\nabla,\ \partial$, komponen bilangan kompleks: `\Im, \Re` $\Im,\ \Re$.

    + Huruf kecil l seperti tulisan tangan dihasilkan dengan perintah `\ell` $\ell$.

    + Untuk menyatukan dua simbol dapat digunakan spasi negatif `\!` atau `\rlap`: `\mathbin{\rlap{\,\wedge}\bigcirc}`: $\mathbin{\rlap{\,\wedge}\bigcirc}$, `\mathbin{\rlap{\,\pm}\bigcirc}`: $\mathbin{\rlap{\,\pm}\bigcirc}$, `\mathbin{\rlap{\, \, \}}\div}`: $\mathbin{\rlap{\, \, \}}\div}$, `I\!P`: $I\!P$.

    + **Contoh**: Akan dibuktikan
      $$
      \forall m, n \in \mathbb{N}\cup \{0\}, \ n^{2m + 1} \equiv -1 \pmod {n + 1}. \notag
      $$
      Itu dapat dibuktikan dengan menunjukkan bahwa
      $$
      n^{2m + 1} + 1 = n^{2m + 1} - (-1) = n^{2m + 1} - (-1)^{2m + 1}.\notag
      $$
      Karena
      $$
      a^k - b^k = (a - b)\sum_{i = 1}^k a^{k - i}b^{i - 1}\notag
      $$
      maka
      $$
      n + 1 \mid n^{2m + 1} + 1\notag
      $$
      atau
      $$
      n^{2m + 1} \equiv -1 \pmod {n + 1}.\notag
      $$
    
12. **Simbol derajat**
    MathJax aslinya belum mendukung simbol khusus derajat, jadi berikut adalah beberapa cara untuk menghasilkan simbol derajat. Perhatikan perbedaan simbol derajat yang dihasilkan.
    $$
    \begin{align*} 
    \verb*45^\text{o}   * & \text{ menghasilkan} & 45^\text{o} & \\
    \verb*45^o   * & \text{ menghasilkan} & 45^o & \\
    \verb*45^\circ   * & \text{ menghasilkan} & 45^\circ & \\
    \verb*45^{\large\circ}   * & \text{ menghasilkan} & 45^{\large\circ}&\\
    \verb*45\unicode{xB0}   * & \text{ menghasilkan} & 45\unicode{xB0} & \text{ (karakter Unicode)}\\
    \verb*90°   * & \text{ menghasilkan} & 90° & \text{ (menggunakan keyboard)}\notag
    \end{align*}
    $$
    Simbol derajat untuk sudut bukan `^\circ`. Meskipun banyak orang menggunakan notasi ini, hasilnya terlihat sangat berbeda dari simbol derajat yang dihasilkan dengan *font*, seperti yang terlihat di atas.
    
    Jika *keyboard* Anda tidak memiliki tombol `°`, apabila *keyboard* Anda memiliki tombol-tombol numerik, gunakan kombinasi `Alt`+`0176` atau `Alt`+`248`, (angka diketik dengan tombol numerik), hasilnya seperti °.
    
13. **Masalah Spasi**. MathJax biasanya menggunakan spasi yang sesuai pada rumus secara otomatis, dengan menggunakan sekumpulan aturan yang kompleks. Penggunaan spasi ekstra antar huruf di dalam penulisan rumus tidak akan mengubah lebar tempat yang digunakan MathJax dalam menampilkan rumus tersebut: `a␣b` dan `a␣␣␣␣b` hasilnya sama, $ab$. Jika menginginkan spasi ekstra, gunakan  `\,` atau `\␣` untuk spasi yang agak sempit, seperti $a\,b$, $a\ b$, `\;` untuk spasi yang agak lebar, seperti  $a\; b$, atau `\quad` dan `\qquad` untuk spasi yang lebih lebar lagi, seperti $a\quad b$, $a\qquad b$.

14. **Teks**. Untuk menuliskan teks di dalam rumus matematika, gunakan perintah  `\text{...}`, seperti: $A=\{x∈\Bbb R∣x \text{ bilangan desimal dengan banyak digit genap}\}$.

15. **Tanda aksen dan diakritik**. Gunakan  `\hat` simbol tunggal, seperti $\hat x$, `\widehat` untuk rumus yang lebih lebar, seperti $\widehat{xy}$. Jika Anda membuatnya terlalu lebar, itu akan terlihat agak aneh. Demikian pula, terdapat perintah `\bar` ($\bar x$) dan `\overline` ($\overline{xyz}$), dan `\vec` ($\vec  x$) dan `\overrightarrow` ($\overrightarrow{xy}$) dan `\overleftrightarrow` ($\overleftrightarrow{xy}$). Untuk tanda titik, seperti $\frac d{dx}x\dot x =  \dot x^2 +  x\ddot x$, gunakan  `\dot` dan `\ddot`. 

    Aksen satu karakter yang lain: `\check`: $\check I$, `\acute`: $\acute J$, `\grave`: $\grave K$, `\vec`: $\vec u,\  \vec{AB}$ (lihat juga `\overrightarrow`), `\bar`: $\bar z$, `\hat`: $\hat x$, `\tilde`: $\tilde x$, `\dot \ddot \dddot`: $\dot x,\ \ddot x,\ \dddot x$, `\mathring`: $\mathring A$.

16. Untuk menampilkan **karakter khusus** yang digunakan LaTeX di dalam rumus, seperti `$`, `{`,`}`, `_`,  gunakan `\`: `\$` $\$$, `\{` $\{$, `\_` $\_$, dan lain-lain. Untuk menampilkan tanda `\` di dalam rumus,, gunakan perintah  `\backslash` (simbol) atau`\setminus` (operator biner)  $\setminus$, karena   `\\` digunakan untuk berganti baris.

17. **Tanda busur** di atas simbol

    `\overset{\huge\frown}{PQ}`: $\overset{ \huge\frown}{PQ}$ menunjukkan busur di atas titik $P$ dan $Q$. `\overset{\frown}{AB}\overset{\large\frown}{CD}\overset{\Large\frown}{EF}\overset{ \huge\frown}{GH}\overset{\Huge\frown}{ABC}`: $\overset{\frown}{AB}\overset{\large\frown}{CD}\overset{\Large\frown}{EF}\overset{ \huge\frown}{GH}\overset{\Huge\frown}{ABC}$.

18. **Penumpukan simbol**

    Jika Anda tidak dapat menemukan simbol Anda, ingat bahwa Anda dapat menumpuk berbagai simbol menggunakan perintah seperti di bawah ini.

    `\overset{bagian atas}{baris}`: $\overset{@}{ABC}\ \overset{x^2}{\longmapsto}\ \overset{\bullet\circ\circ\bullet}{T}$.

    `\underset{bagian bawah}{baris}`: $\underset{@}{ABC}\ \underset{x^2}{\longmapsto}\ \underset{\bullet\circ\circ\bullet}{T}$.

    Anda dapat menggunakan keduanya bersamaan,`X\overset{a}{\underset{b}{\to}}Y`: $X\overset{a}{\underset{b}{\to}}Y$.

19. **Harga mutlak dan *norm***

    Harga mutlak dapat ditandai dengan `\lvert ... \rvert` atau, secara umum, dengan`\left\lvert ... \right\rvert` dan hasilnya seperti $\left\lvert x \right\rvert$.

    *Norm* vektor (atau matriks) dituliskan dengan `\lVert ... \rVert` atau, secara umum, dengan`\left\lVert ... \right\rVert` dan hasilnya seperti $\left\lVert x \right\rVert$. (Anda juga dapat menggunakan `\left\| ... \right\|` atau `\| ... \|`  sebagai alternatif.)

    Ketiga perintah tersebut menghasilkan tampilan yang lebih baik daripada `|x|` atau `||v||`, yang menghasilkan garis tegak yang tidak turun cukup rendah dan spasi yang kurang optimal. 

    Perhatikan perbedaan tanda harga mutlak dan *norm* di bawah ini: 
    $$
    |x|, ||v|| \quad\overset{\text{diubah menjadi}}{\longmapsto}\quad \lvert x\rvert, \lVert v\rVert
    $$
    yang dihasilkan dengan perintah:

    ```latex
    $$
    |x|, ||v|| \quad\overset{\text{diubah menjadi}}{\longmapsto}\quad \lvert x\rvert, \lVert v\rVert.
    $$
    ```
    Contoh lain:
    $$
    \rm{\bf Petunjuk\!:}\ (p\!-\!1)^2\! \mid p^q\!-1 \!\iff\! p\!-\!1\ \bigg|\ \dfrac{p^q\!-1}{p\!-\!1} = p^{q-1}\! +\cdots\!+p\! +\! 1.
    $$

20. **Simbol-simbol kartu**. Jika Anda mengajukan (atau menjawab) pertanyaan kombinatorik tentang kartu, Anda dapat menampilkan simbol-simbol kartu dengan perintah-perintah LaTeX `\spadesuit`, `\heartsuit`, `\diamondsuit`, `\clubsuit` pada ekspresi matematika: $\spadesuit\quad\heartsuit\quad\diamondsuit\quad\clubsuit$. Contoh unik: $\mathop{\large\spadesuit}\limits_{i = 0}^n k^i$. 

    Anda juga dapat menampilkan simbol-simbol tersebut dengan warna: `\color{red}{\heartsuit}`, `\color{red}{\diamondsuit}`, seperti: $\color{red}{\heartsuit}\quad\color{red}{\diamondsuit}$ $\color{yellow}♥\!\!\!\color{blue}♡$, bahkan dengan ukuran diperbesar: 
    $$
    \Huge \color{green}\Huge \color{green}♥\!\!\!\!\!\!\!\!\!\!\,\color{red}♡\notag
    $$
    Anda juga dapat menggunakan karakter ***Unicode*** standar (`U+2660 BLACK SPADE SUIT`, dll.) seperti di bawah ini.
    $$
    \spadesuit\quad\heartsuit\quad\diamondsuit\quad\clubsuit\notag\\
    ♤\quad♥\quad♦\quad♧\notag
    $$
### Menuliskan Matriks dengan LaTeX di Markdown

1. Untuk menuliskan matriks, gunakan `$$\begin{matrix}...\end{matrix}$$` elemen-elemen matriks dituliskan di antara `\begin` dan `\end`, pisahkan antar elemen dalam satu baris dengan `&` dan pisahkan antar baris dengan `\\`. Contoh:

   ```latex
   $$\begin{matrix}
       1 & x & x^2 \\
       1 & y & y^2 \\
       1 & z & z^2 \\
   \end{matrix}$$
   ```

   menampilkan:

   $$
   \begin{matrix}
       1 & x & x^2 \\
       1 & y & y^2 \\
       1 & z & z^2 \\
   \end{matrix}
   $$

   MathJax akan mengatur secara otomatis lebar kolom dan baris sehingga segalanya terlihat rapi.
   
2. Untuk menambahkan tanda kurung, gunakan `\left ... \right` atau ganti perintah `matrix` dengan `pmatrix`: $\begin{pmatrix}1&2\\3&4\\ \end{pmatrix}$, `bmatrix`: $\begin{bmatrix}1&2\\3&4\\ \end{bmatrix}$, `Bmatrix`: $\begin{Bmatrix}1&2\\3&4\\ \end{Bmatrix}$, `vmatrix`: $\begin{vmatrix}1&2\\3&4\\ \end{vmatrix}$, atau `Vmatrix`: $\begin{Vmatrix}1&2\\3&4\\ \end{Vmatrix}$.

3. Gunakan perintah  `\cdots` ($\cdots$) `\ddots` ($\ddots$) `\vdots` ($\vdots$) untuk mengganti elemen-elemen matriks yang tidak ditulis:
   $$
   \begin{pmatrix}
    1 & a_1 & a_1^2 & \cdots & a_1^n \\
    1 & a_2 & a_2^2 & \cdots & a_2^n \\
    \vdots  & \vdots& \vdots & \ddots & \vdots \\
    1 & a_m & a_m^2 & \cdots & a_m^n  
    \end{pmatrix}
   $$
   
3. Untuk menampilkan matriks "gabungan" horizontal, gunakan `array`, seperti untuk membuat tabel (lihat di bagian bawah), dan tanda kurung. Berikut adalah contohnya:
   $$
   \left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
    \right]
   $$
   yang dihasilkan dari:
   
    ```latex
    $$ 
    \left[\begin{array}{cc|c} 1&2&3\\ 4&5&6 \end{array}\right] 
    $$
    ```
   
   Format `cc|c` digunakan untuk mengatur format setiap kolom dan memberi tanda garis tegak antara kolom kedua dan ketiga.
   
2. Pada matriks gabungan vertikal, gunakan `\hline` untuk menampilkan garis pembatas horisontal. Matriks 
    $$
    \begin{pmatrix}
        a & b\\
        c & d\\
      \hline
        1 & 0\\
        0 & 1
      \end{pmatrix}
    $$
	dihasilkan dengan perintah-perintah:
	```latex
	$$
	\begin{pmatrix} a & b\\ c & d\\ \hline 1 & 0\\ 0 & 1 \end{pmatrix}
	$$.
	```
	
6.  Untuk menampilkan matriks berukuran kecil pada baris teks dapat digunakan  `\bigl(\begin{smallmatrix} ... \end{smallmatrix}\bigr)`, seperti $\bigl( \begin{smallmatrix} a & b \\ c & d \end{smallmatrix} \bigr)$ diperoleh dengan perintah `$\bigl( \begin{smallmatrix} a & b \\ c & d \end{smallmatrix} \bigr)$`.

7.  Untuk menuliskan matriks berukuran besar secara langsung menggunakan LaTeX tentu sangat membosankan. Salah satu cara yang mudah untuk menghasilkan matriks besar adalah menggunakan aplikasi matematika seperti Octave, kemudian matriks yang dihasilkan Octave diubah ke format LaTeX. Untuk mengubah format matriks $A$ di Octave menjadi kode LaTeX dapat digunakan perintah, misalnya:

    ```octave
    strcat("\\begin{pmatrix}\n",strrep(strrep(mat2str(A)," "," & "), ...
    ";"," \\\\\n")(2:end-1),"\n\\end{pmatrix}\n")
    ```

    Jika diketahui

    ```
    A = [1 2 2; 2 3 4; 4 4 2]
    A =
    
       1   2   2
       2   3   4
       4   4   2
    ```

    maka Octave akan mengubah tampilan matriks $A$ menjadi

    ```
    \begin{pmatrix}
    1 & 2 & 2 \\
    2 & 3 & 4 \\
    4 & 4 & 2
    \end{pmatrix}
    ```

    sehingga apabila ditempel di LaTeX atau Markdown hasilnya:
    $$
    \begin{pmatrix}
    1 & 2 & 2 \\
    2 & 3 & 4 \\
    4 & 4 & 2
    \end{pmatrix}.\notag
    $$
    
8.  Contoh penulisan matriks jarang:
    $$
    \begin{pmatrix} 
    1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 0 \\
    1/2 & 0   & 0   & 0   & 0   & 0   & 0   & 0 \\
    0   & 1/2 & 0   & 0   & 0   & 0   & 0   & 0 \\
    0   & 0   & 1/2 & 0   & 0   & 0   & 0   & 0 \\
    0   & 0   & 0   & 1/2 & 0   & 0   & 0   & 0 \\
    0   & 0   & 0   & 0   & 1/2 & 0   & 0   & 0 \\
    0   & 0   & 0   & 0   & 0   & 1/2 & 0   & 0 \\
    0   & 0   & 0   & 0   & 0   & 0   & 1/2 & 1 
    \end{pmatrix}
    $$

Matriks di atas dapat dihasilkan menggunakan Octave sebagai berikut.

```octave
>>A=zeros(8);
>>A(1,1:7)=1/2;
>>A(8,8)=1;
>>B=1/2*ones(1,7);
>>C=diag(B,7,8);
>>D=[zeros(1,8);C];
>>A=A+D;
>>strcat("\\begin{pmatrix}\n",strrep(strrep(strrep(mat2str(A),"0.5","1/2"),...
" "," & "),";"," \\\\\n")(2:end-1),"\n\\end{pmatrix}\n")

ans = \begin{pmatrix}
1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 0 \\
1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 1
\end{pmatrix}
```

Selanjutnya, hasil dari `strcat` tersebut disalin ke Typora, hasilnya adalah sebagai berikut.
$$
\begin{pmatrix}
1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 0 \\
1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 1
\end{pmatrix}
$$
Contoh matriks jarang serupa yang lebih besar (dihasilkan menggunakan program Octave):
$$
\begin{pmatrix}
1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1/2 & 1
/2 & 0 \\
1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1/2 & 1
\end{pmatrix}
$$

### Penyelarasan Persamaan

Seringkali serangkaian persamaan harus ditulis menjadi satu baris demi baris, ruas kiri hanya dituliskan pada baris pertama, dan baris-baris selanjutnya hanya dituliskan ruas kanan dan tanda sama dengan. Dalam ini biasanya tanda sama dengan harus ditulis selaras (segaris) sehingga rangkaian persamaan mudah dibaca. Hal ini juga berlaku untuk menampilkan persamaan panjang yang harus ditampilkan dalam beberapa baris. Untuk melakukan hal ini, gunakan `\begin{aligned}...\end{aligned}` atau `\begin{align}...\end{align}`. Yang pertama mengakibatkan persamaan tidak diberi nomor, sedangkan yang kedua menyebabkan setiap baris diberi nomor otomatis. Setiap baris harus diakhiri dengan tanda `\\`, dan karakter sebagai titik penyelarasan diawali dengan tanda `&`. Misalnya,

$$
\begin{aligned}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{aligned}
$$

diperoleh dari perintah-perintah $\LaTeX$:

```latex
$$
\begin{aligned}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{aligned}
$$
```

Contoh lain,

```latex
$$
\begin{aligned} 
f(x)&=(x^3)+(x^3+x^2+x)+(x^3+x^2),\\ 
f'(x)&=(3x^2)+(3x^2+2x+1)+(3x^2+2x),\\ 
f''(x)&=(18x+4).\\ 
\end{aligned}
$$
```

menghasilkan tampilan:
$$
\begin{aligned} 
f(x)&=(x^3)+(x^3+x^2+x)+(x^3+x^2),\\ 
f'(x)&=(3x^2)+(3x^2+2x+1)+(3x^2+2x),\\ 
f''(x)&=(18x+4).\\ 
\end{aligned}
$$
```latex
$$
\begin{align}
f(x:xs) &= \sum_{i:\ 0 \leq i < \#(x:xs)} (x:xs).i * (i + 1)\\
&=\sum_{i:\ i =0} (x:xs).i * (i + 1)+\sum_{i:\ 1\le i<\#xs+1}(x:xs).i * (i + 1)\\
&=x + \sum_{i:\ 1 \leq i \le \#xs} xs.(i-1) * (i + 1)\\
&=x + \sum_{j:\ 0 \leq j < \#xs} xs.j * (j + 2)\quad\quad(\text{Here }j=i-1\text{ dan }i\text{ is replaced with }j+1)\\
&=x + \sum_{j:\ 0 \leq j < \#xs} xs.j + \sum_{j:\ 0 \leq j < \#xs} xs.j * (j+1)\\
&=x + t(xs) + f(xs)\\
\end{align}
$$
```

menghasilkan tampilan:
$$
\begin{align}
f(x:xs) &= \sum_{i:\ 0 \leq i < \#(x:xs)} (x:xs).i * (i + 1)\\
&=\sum_{i:\ i =0} (x:xs).i * (i + 1)+\sum_{i:\ 1\le i<\#xs+1}(x:xs).i * (i + 1)\\
&=x + \sum_{i:\ 1 \leq i \le \#xs} xs.(i-1) * (i + 1)\\
&=x + \sum_{j:\ 0 \leq j < \#xs} xs.j * (j + 2)\quad\quad(\text{Ganti }j=i-1\text{ dan }i\text{ dengan }j+1)\\
&=x + \sum_{j:\ 0 \leq j < \#xs} xs.j + \sum_{j:\ 0 \leq j < \#xs} xs.j * (j+1)\\
&=x + t(xs) + f(xs)\\
\end{align}
$$
Berikut adalah tampilan persamaan multi-baris tanpa menggunakan penyelarasan.

$$
\lim_{x \to\infty} \dfrac{\ln(x^2+4)}{\ln(x+\sqrt{1+x^2})} = \lim_{x \to\infty} \dfrac{\ln(x^2) + \ln(1+4/x^2)}{\ln(x) + \ln(1+\sqrt{1+1/x^2})}\\
 = \lim_{x \to \infty} \dfrac{\ln(x^2)}{\ln(x)} \dfrac{\left(1+\dfrac{\ln(1+4/x^2)}{\ln(x^2)} \right)}{\left(1 + \dfrac{\ln(1+\sqrt{1+1/x^2})}{\ln(x)} \right)}\\
 = \lim_{x \to \infty} 2 \dfrac{\ln(x)}{\ln(x)} \lim_{x \to \infty} \dfrac{\left(1+\dfrac{\ln(1+4/x^2)}{\ln(x^2)} \right)}{\left(1 + \dfrac{\ln(1+\sqrt{1+1/x^2})}{\ln(x)} \right)}\\
 = 2 \lim_{x \to \infty} \dfrac{\left(1+\dfrac{\ln(1+4/x^2)}{\ln(x^2)} \right)}{\left(1 + \dfrac{\ln(1+\sqrt{1+1/x^2})}{\ln(x)} \right)} =2.
$$

Untuk menuliskan alasan pada setiap langkah (baris persamaan) gunakan trik seperti contoh berikut ini.

```latex
$$
\begin{align}
  ax^2+bx+c & = 0  &&\text{PK yang diketahui dengan } a\ne 0 \tag{P1}\\
  x^2+\frac ba x+\frac ca  & =  0 && \text{Kedua ruas dibagi }a \tag{P2}\\
  \left(x+\frac{b}{2a}\right)^2+\frac ca-\left(\frac{b}{2a}\right)^2& = 0 && \text{Ruas kiri (P2) sbg kuadrat sempurna}\tag{P3}\\
  \left(x+\frac{b}{2a}\right)^2&=-\frac ca+\left(\frac{b}{2a}\right)^2 && \text{Ruas kiri (P2) sbg kuadrat sempurna}\tag{P4}\\
\left(x+\frac{b}{2a}\right)^2&=\frac{-4ac+b^2}{4a^2} && \text{Ruas kanan (P4) disederhanakan}\tag{P5}\\
   x+\frac{b}{2a}&=\frac{\pm\sqrt{b^2-4ac}}{2a} && \text{Kedua ruas (P5) ditarik akar kuadratnya}\tag{P6}\\
   x&=\frac{-b\pm\sqrt{b^2-4ac}}{2a} && \text{Diperoleh rumus abc untuk akar (P1).}\tag{P7}\\
\end{align}
$$
```

$$
{\small
\begin{align}
  ax^2+bx+c & = 0  &&\text{PK yang diketahui dengan } a\ne 0 \tag{P1}\\
  x^2+\frac ba x+\frac ca  & =  0 && \text{Kedua ruas dibagi }a \tag{P2}\\
  \left(x+\frac{b}{2a}\right)^2+\frac ca-\left(\frac{b}{2a}\right)^2& = 0 && \text{Ruas kiri (P2) sbg kuadrat sempurna}\tag{P3}\\
  \left(x+\frac{b}{2a}\right)^2&=-\frac ca+\left(\frac{b}{2a}\right)^2 && \text{Sifat persamaan}\tag{P4}\\
\left(x+\frac{b}{2a}\right)^2&=\frac{-4ac+b^2}{4a^2} && \text{Ruas kanan (P4) disederhanakan}\tag{P5}\\
   x+\frac{b}{2a}&=\frac{\pm\sqrt{b^2-4ac}}{2a} && \text{Kedua ruas (P5) ditarik akar kuadratnya}\tag{P6}\\
   x&=\frac{-b\pm\sqrt{b^2-4ac}}{2a} && \text{Diperoleh rumus abc untuk akar (P1).}\tag{P7}\\
\end{align}}
$$



### Definisi per kasus (Fungsi sepotong-sepotong)

Untuk menuliskan definisi per kasus atau fungsi sepotong-sepotong, gunakan  `\begin{cases}...\end{cases}` atau `\begin{array}...\end{array}`. Setiap kasus diakhiri dengan `\\`, gunakan `&`  di depan bagian yang harus ditulis selaras. Sebagai contoh:
$$
f(n) = \begin{cases}
n/2,  & \text{jika $n$ genap} \\
3n+1, & \text{jika $n$ ganjil}
\end{cases}
$$
diperoleh dengan menuliskan perintah-perintah:
```latex
$$
f(n) = \begin{cases}
n/2,  & \text{jika $n$ genap} \\
3n+1, & \text{jika $n$ ganjil}
\end{cases}
$$
```
Tanda kurung kurawal dapat ditaruh di sebalah kanan:
$$
\left.
\begin{array}{l}
\text{Jika $n$ genap:}&n/2\\
\text{Jika $n$ ganjil:}&3n+1
\end{array}
\right\}
=f(n)
$$
dengan menuliskan:
```latex
$$
\left. \begin{array}{l}
\text{Jika $n$ genap:}&n/2\\
\text{Jika $n$ ganjil:}&3n+1
\end{array} \right\} =f(n)
$$
```
Jika menginginkan spasi antar baris yang lebih longgar, gunakan  `\\[1ex]` sebagai pengganti `\\`. Misalnya:
$$
f(n) = \begin{cases}
n/2,  & \text{jika $n$ genap} \\[1ex]
3n+1, & \text{jika $n$ ganjil}
\end{cases}
$$
diperoleh dengan menuliskan:
```latex
$$
f(n) = \begin{cases}
n/2,  & \text{jika $n$ genap} \\
3n+1, & \text{jika $n$ ganjil}
\end{cases}
$$
```
(Satuan ‘ex’ adalah tinggi huruf `x` yang dicetak terakhir kali; `1ex` artinya setinggi huruf `x` yang dicetak terakhir.)

### Tabel

Seringkali lebih mudah untuk membaca tabel yang diformat dalam MathJax daripada tabel yang dihasilkan dengan sintaks Markdown. *Array* dan tabel dibuat dengan lingkungan LaTeX 'array'. Tepat setelah `\begin{array}` dituliskan format setiap kolom, huruf `c` untuk kolom rata tengah, `r` untuk rata kanan, `l` untuk rata kiri dan `|` untuk garis tegak. Sama seperti matriks, sel dipisahkan dengan `&` dan baris-baris dipisahkan `\\`. Untuk membuat garis mendatar digunakan perintah `\hline`.

Misalnya,

```
$$
\begin{array}{c|lcr}
n & \text{Kiri} & \text{Tengah} & \text{Kanan} \\ \hline
1 & 0.24 & 1 & 125 \\ 2 & -1 & 189 & -8 \\ 3 & -20 & 2000 & 1+10i
\end{array}
$$
```

menghasilkan tabel:

$$
\begin{array}{c|lcr}
n & \text{Kiri} & \text{Tengah} & \text{Kanan}  \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i
\end{array}\notag
$$

Contoh lain adalah tabel data tabungan.

```latex
$$
\begin{array}{c|r|r|r}
 \style{font-family:inherit}{\text{Hari ke-}} & \style{font-family:inherit}{\text{Keluar}}
& \style{font-family:inherit}{\text{Masuk}} & \style{font-family:inherit}{\text{Saldo}}\\\hline
 0                                       & 0    & 0   & 10000 \\\hline
 1                                       & 100  & 500 & 9600 \\\hline
 2                                       & 0    & 400 & 10000 \\\hline
 3                                       & 1000 & 500 & 10500
\end{array}
$$
```

$$
\begin{array}{c|r|r|r}
 \style{font-family:inherit}{\text{Hari ke-}} & \style{font-family:inherit}{\text{Keluar}}
& \style{font-family:inherit}{\text{Masuk}} & \style{font-family:inherit}{\text{Saldo}}\\\hline
 0                                       & 0    & 0   & 10000 \\\hline
 1                                       & 100  & 500 & 9600 \\\hline
 2                                       & 0    & 400 & 10000 \\\hline
 3                                       & 1000 & 500 & 10500
\end{array}\notag
$$

Contoh tabel dengan judul kolom berupa ekspresi matematika:
$$
\begin{array}{| r | r | r |}
  \hline                       
  N & \frac{1}{\sqrt{N-2^{1/2}}} & \frac{1}{c_4(N)\sqrt{N-1}} \\
  \hline                       
  3 & 0,7941 & 0,7979 \\
  4 & 0,6219 \notag& 0,6267 \\
  5 & 0,5281 & 0,5319 \\
  \hline  
\end{array}\notag
$$
Berikut adalah contoh tabel yang memuat ekspresi matematika terkait rumus banyaknya permutasi dan kombinasi.

```latex
\begin{array}{l}
 \begin{array}{c|c}
  \hskip43.5pt & \hskip42.5pt\style{font-family:inherit}{\text{Dengan urutan}}
 \end{array} \\[-7pt]\hline\hskip-5.5pt
 \begin{array}{c|c|c}
  \style{font-family:inherit}{\text{Pengulangan}} & \style{font-family:inherit}{\text{Ya}}
& \style{font-family:inherit}{\text{Tidak}} \\\hline
  \style{font-family:inherit}{\text{Ya}}         & P_r^n=n^r
& C_r^n=\left(\!\binom{n}{r}\!\right) =\binom{ n+r-1}{r}\\[0pt]\hline
  \style{font-family:inherit}{\text{Tidak}}        & nPr=\frac{n!}{(n-r)!}
& nCr=\binom n r =\frac{n!}{r!(n-r)!}
 \end{array}\hskip-5.5pt
\end{array}}
$$
```

$$
\begin{array}{l}
 \begin{array}{c|c}
  \hskip43.5pt & \hskip42.5pt\style{font-family:inherit}{\text{Dengan urutan}}
 \end{array} \\[-7pt]\hline\hskip-5.5pt
 \begin{array}{c|c|c}
  \style{font-family:inherit}{\text{Pengulangan}} & \style{font-family:inherit}{\text{Ya}}
& \style{font-family:inherit}{\text{Tidak}} \\\hline
  \style{font-family:inherit}{\text{Ya}}         & P_r^n=n^r
& C_r^n=\left(\!\binom{n}{r}\!\right) =\binom{ n+r-1}{r}\\[0pt]\hline
  \style{font-family:inherit}{\text{Tidak}}        & nPr=\frac{n!}{(n-r)!}
& nCr=\binom n r =\frac{n!}{r!(n-r)!}
 \end{array}\hskip-5.5pt
\end{array}\notag
$$

Contoh aplikasi tabel:
$$
{\small
\begin{array}{r|l}                                                                                                                                       
(\forall  L\subseteq \Sigma^*)  
  & \text{Untuk setiap bahasa $L$ atas alfabet $\Sigma$} \\
(\mbox{reguler}(L)
  & \text{kita katakan $L$ “reguler”} \\
\Rightarrow
  & \text{jika: }\\                                                                                                           
\quad     ((\exists p\geq 1)
  & \text{terdapat bilangan  $p$ lebih besar atau sama dengan $1$} \\
( (\forall w\in L) ((|w|\geq p) \Rightarrow
  & \text{sdm hgg. untuk setiap kata $w$ di dalam $L$, dengan panjang minimal $p$,} \\                                                                    
\quad ((\exists x,y,z \in \Sigma^*)(w=xyz
  & \text{Kita selalu dapat memisahkan $w$ menjadi tiga string, $x,y,$ dan $z$}  \\
\qquad\land (|y|\geq 1 \land |xy|\leq p 
  & \text{dengan $y$ tidak kosong dan panjang $xy$ tidak lebih dari $p$,} \\
\land (\forall n\geq 0)(xy^nz\in L)                                                                                                                   
  & \text{shg. $xy^nz$ juga di dalam $L$ untuk setiap bilangan non-netaif $n$.} \\
   )))))))
  & \text{(Pasangan tanda kurungnya harus cocok.)}
\end{array}}\notag
$$


Tabel juga dapat berisi tabel (tabel tersarang), seperti contoh di bawah ini.

```latex
$$
\begin{array}{|c|}
\hline
\begin{array}{cc}
\begin{array}{c|cccc}
\text{min} & 0 & 1 & 2 & 3\\ \hline
0 & 0 & 0 & 0 & 0\\ 1 & 0 & 1 & 1 & 1\\ 2 & 0 & 1 & 2 & 2\\ 3 & 0 & 1 & 2 & 3
\end{array}
&
\begin{array}{c|cccc}
\text{maks}&0&1&2&3\\ \hline
0 & 0 & 1 & 2 & 3\\ 1 & 1 & 1 & 2 & 3\\ 2 & 2 & 2 & 2 & 3\\ 3 & 3 & 3 & 3 & 3
\end{array}
\end{array}
\\\hline
\begin{array}{c|cccc}
\Delta&0&1&2&3\\ \hline
0 & 0 & 1 & 2 & 3\\ 1 & 1 & 0 & 1 & 2\\ 2 & 2 & 1 & 0 & 1\\ 3 & 3 & 2 & 1 & 0
\end{array}\\\hline
\end{array}
$$
```

menghasilkan tabel yang berisi tabel di bawah ini.

$$
\begin{array}{|c|}
\hline
\begin{array}{cc}
\begin{array}{c|cccc}
\text{min} & 0 & 1 & 2 & 3\\ \hline
0 & 0 & 0 & 0 & 0\\ 1 & 0 & 1 & 1 & 1\\ 2 & 0 & 1 & 2 & 2\\ 3 & 0 & 1 & 2 & 3
\end{array}
&
\begin{array}{c|cccc}
\text{maks}&0&1&2&3\\ \hline
0 & 0 & 1 & 2 & 3\\ 1 & 1 & 1 & 2 & 3\\ 2 & 2 & 2 & 2 & 3\\ 3 & 3 & 3 & 3 & 3
\end{array}
\end{array}
\\\hline
\begin{array}{c|cccc}
\Delta&0&1&2&3\\ \hline
0 & 0 & 1 & 2 & 3\\ 1 & 1 & 0 & 1 & 2\\ 2 & 2 & 1 & 0 & 1\\ 3 & 3 & 2 & 1 & 0
\end{array}\\\hline
\end{array}\notag
$$

#### Masalah spasi pada ekspresi matematika

Berikut adalah saran-saran yang perlu dipertimbangkan dalam penulisan ekspresi matematika. Ini adalah masalah yang tidak akan mempengaruhi kebenaran ekspresi, namun mungkin membuat ekspresi matematika terlihat jauh lebih baik atau bahkan lebih buruk. Anda bebas untuk mengabaikan hal ini, namun tidak sia-sia jika Anda tetap memperhatikan hal ini.

+ Jangan menggunakan `\frac` pada pangkat atau batas integral, karena akan terlihat tidak bagus dan dapat membingungkan. Hal ini jarang dilakukan dalam penulisan matematika profesional. Tulis pecahan secara horizontal, dengan garis miring.

    $$
    \begin{array}{cc}
    \text{Tidak bagus} & \text{Lebih baik} \\
    \hline \\
    e^{i\frac{\pi}2} \quad e^{\frac{i\pi}2}& e^{i\pi/2} \\
    \int_{-\frac\pi2}^\frac\pi2 \sin x\,dx & \int_{-\pi/2}^{\pi/2}\sin x\,dx \\
    \end{array}\notag
    $$

+ Simbol `|` menghasilkan spasi yang salah ketika digunakan sebagai pembatas, misalnya pada definisi himpunan. Gunakan `\mid` sebagai gantinya. Contoh: $\left\{x\middle | \frac{x^2}{2} \in \mathbb{z}\right\}$ dan $\left\{\,x\in\Bbb R\,\middle|\, \frac{x^2}{2}\in\Bbb Z\,\right\}$.

    $$
    \begin{array}{cc}
    \text{Tidak bagus} & \text{Lebih baik}\\
    \hline \\
    \{x|x^2\in\Bbb Z\} & \{x\mid x^2\in\Bbb Z\} \\
    \end{array}\notag
    $$

+ Pada saat menggunakan pembatas yang dapat diregangkan (yaitu dengan `\left` dan `\right`, mungkin lebih baik menggunakan `\,\middle|\,`. Ini menghasilkan garis tegak yang ukurannya disesuaikan secara otomatis. Alternatif lain adalah menggunakan titik dua sebagai gantinya.

    $$
    \begin{array}{cc}
    \text{Tidak bagus} & \text{Lebih baik} \\
    \hline \\
    \left\{\dfrac{m}{n} \mid m,n\in\Bbb Z\right\} & \left\{\dfrac{m}{n} \,\middle|\, m,n\in\Bbb Z\right\} \\
    \end{array}\notag
    $$

+ Untuk integral lipat jangan menggunakan `\int\int` atau `\int\int\int`. Sebagai gantinya, gunakan perintah khusus untuk integral lipat `\iint` atau `\iiint`.

    $$
    \begin{array}{cc}
    \text{Tidak bagus} & \text{Lebih baik} \\
    \hline \\
    \int\int_S f(x)\,dy\,dx & \iint_S f(x)\,dy\,dx \\
    \int\int\int_V f(x)\,dz\,dy\,dx & \iiint_V f(x)\,dz\,dy\,dx
    \end{array}\notag
    $$

+ Gunakan `\,` untuk menyisipkan spasi tipis sebelum diferensial, tanpa ini $\TeX$ ini akan menuliskan mereka berdempetan.

    $$
    \begin{array}{cc}
    \text{Tidak bagus} & \text{Lebih baik}\\
    \hline \\
    \iiint_V f(x)dz dy dx & \iiint_V f(x)\,dz\,dy\,dx
    \end{array}\notag
    $$

### Mencoret ekspresi matematika

+ Untuk mencoret bagian dari suatu ekspresi matematika gunakan `\require{cancel}` pada ekspresi pertama yang ingin Anda coret. Anda hanya perlu menuliskan perintah tersebut sekali setiap halaman. Selanjutnya gunakan perintah-perintah sebagai berikut.

    $$
    {\small
    \require{cancel}
    \begin{array}{|l|l|}\hline
    \text{Penulisan} & \text{Hasil/Tampilan}\\\hline
    \verb|y+\cancel{x}| & y+\cancel{x}\\
    \verb|\cancel{y+x}| & \cancel{y+x}\\
    \verb|y+\bcancel{x}| & y+\bcancel{x}\\
    \verb|y+\xcancel{x}| & y+\xcancel{x}\\
    \verb|y+\cancelto{0}{x}| & y+\cancelto{0}{x}\\
    \verb|\frac{1\cancel9}{\cancel95} = \frac15|& \frac{1\cancel9}{\cancel95} = \frac15 \\ 
    \verb|\cancelto{\cancelto{\cancelto{x^{2+x}}{\cancelto{x^2}{x}+4}}4}0|& \cancelto{\cancelto{\cancelto{x^{2+x}}{\cancelto{x^2}{x}+4}}4}0 \\ 
    \verb|\require{cancel}\cancelto{1}{\dfrac{\sqrt{7x^7-y^9}}{8x^3+1}}
    |&\cancelto{1}{\dfrac{\sqrt{7x^7-y^9}}{8x^3+1}}\\
    \hline
    \end{array}}\notag
    $$

+ Gunakan `\require{enclose}` untuk kasus-kasus sebagai berikut.

    $$
    \require{enclose}
    \begin{array}{|l|l|}\hline
    \text{Penulisan} & \text{Hasil/Tampilan}\\\hline
    \verb|\enclose{horizontalstrike}{x+y}| & \enclose{horizontalstrike}{x+y}\\
    \verb|\enclose{verticalstrike}{\frac xy}| & \enclose{verticalstrike}{\frac xy}\\
    \verb|\enclose{updiagonalstrike}{x+y}| & \enclose{updiagonalstrike}{x+y}\\
    \verb|\enclose{downdiagonalstrike}{x+y}| & \enclose{downdiagonalstrike}{x+y}\\
    \verb|\enclose{horizontalstrike,updiagonalstrike}{x+y}| & \enclose{horizontalstrike,updiagonalstrike}{x+y}\\\hline
    \end{array}\notag
    $$
    
    Perintah `\enclose` juga dapat menghasilkan kotak tertutup, lingkaran/oval, dan notasi lainnya: $\enclose{box}{x+y},\ \enclose{circle}{x+y},\ \enclose{box,circle}{x+y},\ \enclose{roundedbox}{x+y}$.

### Sistem persamaan

Untuk menuliskan sistem persamaan gunakan  `\begin{array}...\end{array}` dan `\left\{...\right.`. Berikut adalah contoh pertama.

$$
\left\{
\begin{array}{c}
a_1x+b_1y+c_1z=d_1 \\
a_2x+b_2y+c_2z=d_2 \\
a_3x+b_3y+c_3z=d_3
\end{array}
\right.
$$

Alternatif lain adalah menggunakan `\begin{cases}...\end{cases}`. Sistem yang sama dengan sistem di atas.

$$
\begin{cases}
a_1x+b_1y+c_1z=d_1 \\
a_2x+b_2y+c_2z=d_2 \\
a_3x+b_3y+c_3z=d_3
\end{cases}
$$

Untuk meluruskan tanda `=` gunakan  `\begin{aligned}...\end{aligned}` dan `\left\{...\right`.

$$
\left\{
\begin{aligned}
a_1x+b_1y+c_1z &=d_1+e_1 \\
a_2x+b_2y&=d_2 \\
a_3x+b_3y+c_3z &=d_3
\end{aligned}
\right.
$$

Untuk meruluskan tanda `=` dan susku-suku gunakan `array` dengan format perataan yang sesuai.

$$
\left\{
\begin{array}{ll}
a_1x+b_1y+c_1z &=d_1+e_1 \\
a_2x+b_2y &=d_2 \\
a_3x+b_3y+c_3z &=d_3
\end{array}
\right.
$$

Spasi tegak antar persamaan dapat dihasilkan dengan, misalnya, `\\[2ex]`, tergantung seberapa lebar spasi yang diinginkan.

$$
\begin{cases}
a_1x+b_1y+c_1z=d_1 \\[2ex]
a_2x+b_2y+c_2z=d_2 \\[2ex]
a_3x+b_3y+c_3z=d_3
\end{cases}
$$

$$
\left\{ \begin{array}{l}
0 = c_x-a_{x0}-d_{x0}\dfrac{(c_x-a_{x0})\cdot d_{x0}}{\|d_{x0}\|^2} + c_x-a_{x1}-d_{x1}\dfrac{(c_x-a_{x1})\cdot d_{x1}}{\|d_{x1}\|^2} \\[2ex]
0 = c_y-a_{y0}-d_{y0}\dfrac{(c_y-a_{y0})\cdot d_{y0}}{\|d_{y0}\|^2} + c_y-a_{y1}-d_{y1}\dfrac{(c_y-a_{y1})\cdot d_{y1}}{\|d_{y1}\|^2} \end{array} \right.
$$
Bandingkan dengan yang tanpa penambahan spasi di bawah ini.

$$
\begin{cases}
a_1x+b_1y+c_1z=\frac{p_1}{q_1} \\
a_2x+b_2y+c_2z=\frac{p_2}{q_2} \\
a_3x+b_3y+c_3z=\frac{p_3}{q_3}
\end{cases}
$$

### Warna

Nama warna tergantung pada browser, jika browser tidak mengetahui nama warna tertentu, ia akan menampilkan teks dengan warna hitam. Warna berikut adalah standar dalam HTML4 dan CSS2 yang dimengerti oleh sebagian besar browser.
$$
\begin{array}{|rc|}
\hline
\verb+\color{black}{Teks}+ & \color{black}{Teks} \\
\verb+\color{gray}{Teks}+ & \color{gray}{Teks} \\
\verb+\color{silver}{Teks}+ & \color{silver}{Teks} \\
\verb+\color{white}{Teks}+ & \color{white}{Teks} \\
\hline
\verb+\color{maroon}{Teks}+ & \color{maroon}{Teks} \\
\verb+\color{red}{Teks}+ & \color{red}{Teks} \\
\verb+\color{yellow}{Teks}+ & \color{yellow}{Teks} \\
\verb+\color{lime}{Teks}+ & \color{lime}{Teks} \\
\verb+\color{olive}{Teks}+ & \color{olive}{Teks} \\
\verb+\color{green}{Teks}+ & \color{green}{Teks} \\
\verb+\color{teal}{Teks}+ & \color{teal}{Teks} \\
\verb+\color{aqua}{Teks}+ & \color{aqua}{Teks} \\
\verb+\color{blue}{Teks}+ & \color{blue}{Teks} \\
\verb+\color{navy}{Teks}+ & \color{navy}{Teks} \\
\verb+\color{purple}{Teks}+ & \color{purple}{Teks} \\
\verb+\color{fuchsia}{Teks}+ & \color{magenta}{Teks} \\
\hline
\end{array}\notag
$$

HTML5 dan CSS3 mendefinisikan 124 nama warna tambahan yang dimengerti oleh sebagian besar browser.

Warna dapat dinyatakan dengan format `#rgb` dengan $r,\ g,\ b$ bernilai  $0\ – 9$, $a - f$  ($a=10$, $b=11$, ..., $f=15$) yang menyatakan intensitas warna merah, hijau, dan biru pada skala $0\ –15$. Berikut adalah tabel contoh-contoh warna.
$$
\begin{array}{|rrrrrrrr|}\hline
\verb+#000+ & \color{#000}{Teks} & & &
\verb+#00F+ & \color{#00F}{Teks} & & \\
& & \verb+#0F0+ & \color{#0F0}{Teks} &
& & \verb+#0FF+ & \color{#0FF}{Teks}\\
\verb+#F00+ & \color{#F00}{Teks} & & &
\verb+#F0F+ & \color{#F0F}{Teks} & & \\
& & \verb+#FF0+ & \color{#FF0}{Teks} &
& & \verb+#FFF+ & \color{#FFF}{Teks}\\
\hline
\end{array}
$$

$$
\begin{array}{|rrrrrrrr|}
\hline
\verb+#000+ & \color{#000}{Teks} & \verb+#005+ & \color{#005}{Teks} & \verb+#00A+ & \color{#00A}{Teks} & \verb+#00F+ & \color{#00F}{Teks}  \\
\verb+#500+ & \color{#500}{Teks} & \verb+#505+ & \color{#505}{Teks} & \verb+#50A+ & \color{#50A}{Teks} & \verb+#50F+ & \color{#50F}{Teks}  \\
\verb+#A00+ & \color{#A00}{Teks} & \verb+#A05+ & \color{#A05}{Teks} & \verb+#A0A+ & \color{#A0A}{Teks} & \verb+#A0F+ & \color{#A0F}{Teks}  \\
\verb+#F00+ & \color{#F00}{Teks} & \verb+#F05+ & \color{#F05}{Teks} & \verb+#F0A+ & \color{#F0A}{Teks} & \verb+#F0F+ & \color{#F0F}{Teks}  \\
\hline
\verb+#080+ & \color{#080}{Teks} & \verb+#085+ & \color{#085}{Teks} & \verb+#08A+ & \color{#08A}{Teks} & \verb+#08F+ & \color{#08F}{Teks}  \\
\verb+#580+ & \color{#580}{Teks} & \verb+#585+ & \color{#585}{Teks} & \verb+#58A+ & \color{#58A}{Teks} & \verb+#58F+ & \color{#58F}{Teks}  \\
\verb+#A80+ & \color{#A80}{Teks} & \verb+#A85+ & \color{#A85}{Teks} & \verb+#A8A+ & \color{#A8A}{Teks} & \verb+#A8F+ & \color{#A8F}{Teks}  \\
\verb+#F80+ & \color{#F80}{Teks} & \verb+#F85+ & \color{#F85}{Teks} & \verb+#F8A+ & \color{#F8A}{Teks} & \verb+#F8F+ & \color{#F8F}{Teks}  \\
\hline
\verb+#0F0+ & \color{#0F0}{Teks} & \verb+#0F5+ & \color{#0F5}{Teks} & \verb+#0FA+ & \color{#0FA}{Teks} & \verb+#0FF+ & \color{#0FF}{Teks}  \\
\verb+#5F0+ & \color{#5F0}{Teks} & \verb+#5F5+ & \color{#5F5}{Teks} & \verb+#5FA+ & \color{#5FA}{Teks} & \verb+#5FF+ & \color{#5FF}{Teks}  \\
\verb+#AF0+ & \color{#AF0}{Teks} & \verb+#AF5+ & \color{#AF5}{Teks} & \verb+#AFA+ & \color{#AFA}{Teks} & \verb+#AFF+ & \color{#AFF}{Teks}  \\
\verb+#FF0+ & \color{#FF0}{Teks} & \verb+#FF5+ & \color{#FF5}{Teks} & \verb+#FFA+ & \color{#FFA}{Teks} & \verb+#FFF+ & \color{#FFF}{Teks}  \\
\hline
\end{array}\notag
$$

### Dekorasi tambahan

$\newcommand{\demo}[2]{#1{#2}\ #1{#2#2}\ #1{#2#2#2}}$
`\overline`: $\demo \overline A$

`\underline`: $\demo\underline B$

`\widetilde`: $\demo\widetilde C$

`\widehat`: $\demo\widehat D$

`\fbox`: $\demo\fbox E$

`\underleftarrow`: varian: `\xleftarrow{}`: $\xleftarrow{abc}$

`\underrightarrow`: $\demo\underrightarrow G$ varian: `\xrightarrow{}`: $\xrightarrow{abc}$

`\underleftrightarrow`: $\demo\underleftrightarrow H$

`\overrightarrow`: $\demo\overrightarrow {AB}$

`\overbrace`: $\overbrace{(n - 2) + \overbrace{(n - 1) + n + (n + 1)} + (n + 2)}$

`\underbrace`: $\underbrace{(n - 2) + \underbrace{(n - 1) + n + (n + 1)} + (n + 2)}$

`\overbrace` dan `\underbrace` masing-masing menerima superskrip atau subskrip, untuk membuat anotasi kurung kurawal. Misalnya, `$\underbrace{a\cdot a\cdots a}_{b\text{ times}}$` menghasilkan $\underbrace{a\cdot a\cdots a}_{b\text{ times}}$.

Catatan: `\varliminf`: $\varliminf$ dan `\varlimsup`:$\varlimsup$ memiliki simbol khusus untuk mereka.

### Diagram komutatif

Untuk membuat diagram komutatif dengan LaTEX dapat digunakan paket **AMScd** dengan perintah `require{AMScd}`. Perintah ini cukup ditulis sekali.
Untuk pertama kali menggambar diagram komutatif, Anda dapat menuliskan:

```latex
$$
\require{AMScd}
\begin{CD}
A @>a>> B\\
@V b V V= @VV c V\\
C @>>d> D
\end{CD}
$$
```

dan hasilnya adalah diagram:
$\require{AMScd}$
$$
\require{AMScd}
\begin{CD}
A @>a>> B\\
@V b V V= @VV c V\\
C @>>d> D
\end{CD}\notag
$$

`@>label>>` untuk membuat panah ke kanan

`@<label<<` untuk membuat panah ke kiri

`@V label VV` untuk membuat panah ke bawah

`@A label AA` untuk membuat panah ke atas

`@=` untuk membuat garis mendatar dobel

`@|` untuk membuat garis tegak dobel

`@.` untuk tidak ada garis/panah.

Contoh lain:

```latex
$$
\begin{CD}
    A @>>> B @>{\text{label panjang}}>> C \\
    @. @AAA @| \\
    D @= E @<<< F
\end{CD}
$$
```

akan menghasilkan gambar:

$$
\begin{CD}
    A @>>> B @>{\text{label panjang}}>> C \\
    @. @AAA @| \\
    D @= E @<<< F
\end{CD}\notag
$$



Diagram:
$$
\begin{CD}
    H \otimes M @>{\rho}>> M @>{\delta}>> H \otimes M \\
    @V{\Delta^2 \otimes \delta}VV @. @AA{m^2 \otimes \rho}A \\
    H^{\otimes 4} \otimes M @>>{\mathbb{1} \otimes T \otimes \mathbb{1}}> H^{\otimes 4} \otimes M @>>{\mathbb{1}\otimes\mathbb{1}\otimes S \otimes\mathbb{1}\otimes\mathbb{1}}> H^{\otimes 4} \otimes M
\end{CD}\notag
$$
digambar dengan perintah LaTeX:

```latex
$$
\begin{CD}
    H \otimes M @>{\rho}>> M @>{\delta}>> H \otimes M \\
    @V{\Delta^2 \otimes \delta}VV @. @AA{m^2 \otimes \rho}A \\
    H^{\otimes 4} \otimes M @>>{\mathbb{1} \otimes T \otimes \mathbb{1}}> H^{\otimes 4} \otimes M @>>{\mathbb{1}\otimes\mathbb{1}\otimes S \otimes\mathbb{1}\otimes\mathbb{1}}> H^{\otimes 4} \otimes M
\end{CD}
$$
```

Label yang panjang otomatis meningkatkan panjang anak-anak panah yang sesuai. Berikut adalah contoh penggunaan diagram komutatif untuk menuliskan reaksi kimia.

```latex
$$
\begin{CD}
  \text{RCOHR$'SO_3$Na} @>{\text{Hydrolysis},\Delta, \text{Dil.HCl}}>> (RCOR')+NaCl+SO_2+ H_2O
\end{CD}
$$
```

$\require{AMScd}$

$$
\begin{CD}
  \text{RCOHR$'SO_3$Na} @>{\text{Hydrolysis},\Delta, \text{Dil.HCl}}>> (RCOR')+NaCl+SO_2+ H_2O
\end{CD}
$$
### Pecahan berlanjut

- Pecahan berlanjut adalah pecahan yang setiap penyebutnya memuat pecahan demikian seterusnya, mungkin sampai tak hingga. Untuk menuliskan pecahan berlanjut, gunakan `\cfrac`, yang bekerja sama seperti `\frac` tetapi tampilan yang berbeda.

$$
x = a_0 + \cfrac{1^2}{a_1
          + \cfrac{2^2}{a_2
          + \cfrac{3^2}{a_3 + \cfrac{4^4}{a_4 + \cdots}}}}
$$

- Jangan menggunakan perintah pecahan sederhana`\frac` atau `\over`, hasilnya akan semakin mengecil dan tidak bagus dilihat.

$$
x = a_0 + \frac{1^2}{a_1
          + \frac{2^2}{a_2
          + \frac{3^2}{a_3 + \frac{4^4}{a_4 + \cdots}}}}
$$

- Perintah `\frac` dapat digunakan untuk notasi pecahan berlanjut dalam bentuk mendatar.

$$
x = a_0 + \frac{1^2}{a_1+}
          \frac{2^2}{a_2+}
          \frac{3^2}{a_3 +} \frac{4^4}{a_4 +} \cdots
$$

- Pecahan berlanjut tidak sesuai ditampilkan pada baris teks, dan apabila ingin ditampilkan pada baris teks maka sebaiknya digunakan notasi pecahan berlanjut dalam bentuk ringkas, misalnya seperti $[a_0;\ a_1,\ a_2,\ a_3,\ ...]$.
- Ruas kanan pada pecahan berlanjut

$$
\cfrac{a_{1}}{b_{1}+\cfrac{a_{2}}{b_{2}+\cfrac{a_{3}}{b_{3}+\ddots }}}=   {\genfrac{}{}{}{}{a_1}{b_1}}   {\genfrac{}{}{0pt}{}{}{+}}   {\genfrac{}{}{}{}{a_2}{b_2}}   {\genfrac{}{}{0pt}{}{}{+}}   {\genfrac{}{}{}{}{a_3}{b_3}}   {\genfrac{}{}{0pt}{}{}{+\dots}}
$$

 	dapat ditampilkan dengan perintah `\genfrac`:

+   ```latex
    $$
      {\genfrac{}{}{}{}{a_1}{b_1}} {\genfrac{}{}{0pt}{}{}{+}} {\genfrac{}{}{}{}{a_2}{b_2}} {\genfrac{}{}{0pt}{}{}{+}} {\genfrac{}{}{}{}{a_3}{b_3}} {\genfrac{}{}{0pt}{}{}{+\dots}}. 
    $$
    ```

​	Cara yang lebih sederhana adalah seperti $\frac12{\vphantom{1}\atop+}\frac34$ dengan menggunakan perintah:	 	`\frac12{\vphantom{1}\atop+}\frac34`.

- Perintah 

  ```latex
  $$
  \underset{j=1}{\overset{\infty}{\LARGE\mathrm K}}\frac{a_j}{b_j}= \cfrac{a_1}{b_1+\cfrac{a_2}{b_2+\cfrac{a_3}{b_3+\ddots}}}
  $$
  ```
  
  akan menghasilkan tampilan:

$$
\underset{j=1}{\overset{\infty}{\LARGE\mathrm K}}\frac{a_j}{b_j}=\cfrac{a_1}{b_1+\cfrac{a_2}{b_2+\cfrac{a_3}{b_3+\ddots}}}.
$$

​	Dapat juga menggunakan  `\mathop` sebagai pengganti `\overset` dan `\underset`:

​	`\mathop{\LARGE\mathrm K}_{i=1}^\infty \frac{a_i}{b_i}` akan menghasilkan:
$$
\mathop{\LARGE\mathrm K}_{i=1}^\infty \frac{a_i}{b_i}.
$$

### Mendefinisikan perintah baru dengan \newcommand

MathJax memungkinkan untuk mendefinisikan perintah baru LaTeX seperti yang diakukan dalam file TeX biasa. Perhatikan contoh berikut dan penggunaannya. Misalkan Anda menuliskan definisi perintah `\SSE` sebagai berikut (lengkap dengan pengapit `$ ...$`).
`$\newcommand{\SES}[3]{ 0 \to #1 \to #2 \to #3 \to 0 }$`
$\newcommand{\SES}[3]{ 0 \to #1 \to #2 \to #3 \to 0 }$
Setelah Anda menuliskan definisi tersebut, Anda dapat menggunakan perintah `\SSE`, misalnya  `$$\SES{A}{B}{C} $$` akan menampilkan:
$$
\SES{A}{B}{C}
$$

Anda juga dapat menggunakan perintah `\def` untuk mendefinisikan perintah baru.
`$\def\ses#1#2#3{0 \to #1 \to #2 \to #3 \to 0}$`.
$\def\ses#1#2#3{0 \to #1 \to #2 \to #3 \to 0}$
Selanjutnya, perintah `$\ses{A}{B}{C}$` akan menghasilkan tampilan yang sama.

### Tag dan Referensi

Untuk perhitungan yang lebih panjang (atau merujuk ke bagian lain dari dokumen) lebih mudah untuk menggunakan sistem penandaan/pelabelan/referensi. Untuk menandai suatu persamaan gunakan `\tag{tanda}` (dengan kurung) atau `\tag*{tanda}` (tanpa kurung), dan jika Anda ingin merujuk ke tag tersebut kemudian, tambahkan `\label{label}` setelah/di belakang perintah `\tag` tersebut. Tidak ada keharusan `tanda` dan `label` sama, namun biasanya akan lebih mudah jika keduanya sama.
`$$a = x^2-y^3 \tag{\*}\label{\*}$$`

$$
a = x^2-y^3 \tag{*}\label{*}
$$

Penanda dapat berupa simbol khusus, misalnya berupa kotak, simbol kartu, huruf Yunani, dll. seperti:  
$$
a^2+b^2=c^2 \tag{$\Box$}
$$
atau
$$
a^2+b^2=c^2 \tag*{$\heartsuit$}.
$$
Untuk merujuk ke suatu persamaan gunakan  `\eqref{label}` atau  `\ref{label}`.

`$$ a+y^3 \stackrel{\eqref{*}}= x^2 $$`
$$
a+y^3 \stackrel{\eqref{*}}= x^2
$$

Perintah `\eqref{label}` akan menghasilkan rujukan persamaan $\eqref{*}$, sedangkan  perintah  `\ref{label}`  menghasilkan rujukan persamaan $\ref{*}$.

Untuk penomoran persamaan multi-baris, yang sebenarnya hanya satu persamaan, perintah LaTeX yang benar adalah menggunakan lingkungan `aligned` bukan `align`, sehingga jika diberi nomor atau tanda hanya satu nomor/tanda, tidak setiap baris.

$$
\begin{aligned}
a &= b + c \\
  &= d + e + f + g \\
  &= h + i
\end{aligned}\tag{$\clubsuit$}\label{eq2}
$$
Persamaan $\eqref{eq2}$ adalah persamaan multi-baris. Kode untuk menghasilkan persamaan $\eqref{eq2}$ adalah:

```latex
$$
\begin{aligned}
a &= b + c \\
  &= d + e + f + g \\
  &= h + i
\end{aligned}\tag{$\clubsuit$}\label{eq2}.
$$
```

Untuk beberapa persamaan (kumpulan) yang diselaraskan lebih baik digunakan lingkungan `align` dan setiap baris baris persamaan dapat diberi nomor rujukan.
$$
\begin{align}
a &= b + c \tag{$\pi_1$}\label{eq3} \\
x &= yz \tag{$\pi_2$}\label{eq4}\\
l &= m - n \tag{$\pi_3$}\label{eq5}
\end{align}
$$
Persamaan $\eqref{eq3},\ \eqref{eq4},\ \eqref{eq5}$ merupakan tiga persamaan yang diselaraskan, dihasilkan dengan perintah:

```latex
$$
\begin{align}
a &= b + c \tag{$\pi_1$}\label{eq3} \\
x &= yz \tag{$\pi_2$}\label{eq4}\\
l &= m - n \tag{$\pi_3$}\label{eq5}
\end{align}.
$$
```

Seperti yang Anda lihat, referensi bahkan diubah menjadi *hiperlink*, yang dapat Anda gunakan secara eksternal juga. Perhatikan bahwa Anda juga dapat merujuk label di dokumen lain selama berada di folder yang sama. Hal ini sangat bermanfaat pada saat merujuk ke suatu pertanyaan dengan beberapa persamaan. 

Untuk mengaktifkan penandaan persamaan secara otomatis dengan *tag* berupa nomor urut, tambahkan

```html
<script type="text/x-mathjax-config"> MathJax.Hub.Config({TeX: {equationNumbers: {autoNumber: "all"}}}); </script>
```

di bagian awal dokumen Markdown.

### Menyorot Persamaan

Untuk menyorot persamaan dapat digunakan perintah `\bbox` misalnya,

```latex
$$
\bbox[yellow]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}
$$
```

menghasilkan

$$
\bbox[yellow]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}.
$$

Perhatikan penggunaan tanda kurung kurawal untuk mengapit persamaan yang akan disorot.

Aslinya, kotak penyorot "mepet", sehingga tidak melewati rumus. Anda dapat menambahkan sedikit spasi di sekitar persamaan dengan menambahkan ukuran spasi setelah warna. Misalnya,

```latex
$$ 
\bbox[pink,5px]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}
$$
```

akan menghasilkan

$$
\bbox[pink,5px]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}.
$$

Untuk memberi kotak pada persamaan Anda dapat menggunakan, sperti: 

```latex
$$ 
\bbox[5px,border:2px solid blue]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}
$$
```

dan hasilnya 

$$
\bbox[5px,border:2px solid blue]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}.
$$

Jika menginginkan kotak persamaan dengan warna penyorot, gunakan seperti:

```latex
$$
\bbox[yellow,5px,border:2px solid red]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}.
$$
```

yang menghasilkan

$$
\bbox[yellow,5px,border:2px solid red]
{e^x=\lim_{n\to\infty}
\left( 1+\frac{x}{n} \right)^n}.
$$

### Pembagian Bersusun dan Pembagian Sintetik

Berikut adalah beberapa contoh penulisan pembagian bersusun dan pembagian polinomial (pembagian sintentik) dengan LaTeX di Markdown.
$$
\require{enclose}
\begin{array}{r}
                13  \\[-3pt]
4 \enclose{longdiv}{52} \\[-3pt]
     \underline{4}\phantom{2} \\[-3pt]
                12  \\[-3pt]
     \underline{12}
\end{array}
$$

```latex
$$
\require{enclose}
\begin{array}{r}
                13  \\[-3pt]
4 \enclose{longdiv}{52} \\[-3pt]
     \underline{4}\phantom{2} \\[-3pt]
                12  \\[-3pt]
     \underline{12}
\end{array}
$$
```


$$
\require{enclose}
\begin{array}{rll}
    125 && \hbox{(Keterangan)} \\[-3pt]
   4 \enclose{longdiv}{500}\kern-.2ex \\[-3pt]
      \underline{4\phantom{00}} && \hbox{($4 \times 1 = 4$)} \\[-3pt]
      10\phantom{0} && \hbox{($5 - 4 = 1$)} \\[-3pt]
      \underline{\phantom{0}8\phantom{0}} && \hbox{($4 \times 2 = 8$)} \\[-3pt]
      \phantom{0}20 && \hbox{($10 - 8 = 2$)} \\[-3pt]
      \underline{\phantom{0}20} && \hbox{($4 \times 5 = 20$)} \\[-3pt]
      \phantom{00}0
  \end{array}
$$

```latex
$$
\require{enclose}
\begin{array}{rll}
    125 && \hbox{(Keterangan)} \\[-3pt]
   4 \enclose{longdiv}{500}\kern-.2ex \\[-3pt]
      \underline{4\phantom{00}} && \hbox{($4 \times 1 = 4$)} \\[-3pt]
      10\phantom{0} && \hbox{($5 - 4 = 1$)} \\[-3pt]
      \underline{\phantom{0}8\phantom{0}} && \hbox{($4 \times 2 = 8$)} \\[-3pt]
      \phantom{0}20 && \hbox{($10 - 8 = 2$)} \\[-3pt]
      \underline{\phantom{0}20} && \hbox{($4 \times 5 = 20$)} \\[-3pt]
      \phantom{00}0
  \end{array}
  $$
```


$$
\begin{array}{rl}
    \underline{125} & \hbox{(Keterangan)} \\[-5pt]
    4 | 500 \\
      \underline{4\phantom{00}} & \hbox{($4 \times 1 = 4$)} \\
      10\phantom{0} & \hbox{($5 - 4 = 1$)} \\
      \underline{\phantom{0}8\phantom{0}} & \hbox{($4 \times 2 = 8$)} \\
      \phantom{0}20 & \hbox{($10 - 8 = 2$)} \\
      \underline{\phantom{0}20} & \hbox{($4 \times 5 = 20$)} \\
      \phantom{00}0
\end{array}
$$

```latex
$$
\begin{array}{rl}
    \underline{125} & \hbox{(Keterangan)} \\[-5pt]
    4 | 500 \\
      \underline{4\phantom{00}} & \hbox{($4 \times 1 = 4$)} \\
      10\phantom{0} & \hbox{($5 - 4 = 1$)} \\
      \underline{\phantom{0}8\phantom{0}} & \hbox{($4 \times 2 = 8$)} \\
      \phantom{0}20 & \hbox{($10 - 8 = 2$)} \\
      \underline{\phantom{0}20} & \hbox{($4 \times 5 = 20$)} \\
      \phantom{00}0
\end{array}
$$
```


$$
\begin{array}{c|rrrr}& x^3 & x^2 & x^1 &  x^0\\ & 1 & -6 & 11 & -6\\ {\color{red}1} & \downarrow & 1 & -5 & 6\\ \hline & 1 & -5 & 6 & |\phantom{-} {\color{blue}0} \end{array}
$$

```latex
$$
\begin{array}{c|rrrr}& x^3 & x^2 & x^1 &  x^0\\ & 1 & -6 & 11 & -6\\ {\color{red}1} & \downarrow & 1 & -5 & 6\\ \hline & 1 & -5 & 6 & |\phantom{-} {\color{blue}0} \end{array}
$$
```


$$
\begin{array}{rrrr|ll} x^3 & -6x^2 & +11x & -6   & x  -  1  \\   -x^3 & +x^2 &  &  &   x^2-5x+6 \\ \hline     & -5x^2 & +11x & -6\\ & \phantom{-}5x^2 & -5x & & & & \\ \hline  & & +6x & -6 \\ & & -6x & +6 \\ \hline & &  0 & 0 \end{array}
$$

```latex
$$
\begin{array}{rrrr|ll} x^3 & -6x^2 & +11x & -6   & x  -  1  \\   -x^3 & +x^2 &  &  &   x^2-5x+6 \\ \hline     & -5x^2 & +11x & -6\\ & \phantom{-}5x^2 & -5x & & & & \\ \hline  & & +6x & -6 \\ & & -6x & +6 \\ \hline & &  0 & 0 \end{array}
$$
```

### Pemrograman Linier

Suatu program linier secara teoritis dapat dinyatakan sebagai

```latex
$$
\begin{array}{ll}
\text{Maksimumkan}  & c^T x \\
\text{dengan syarat}& d^T x = \alpha \\
&0 \le x \le 1.
\end{array}
$$
```

$$
\begin{array}{ll}
\text{Maksimumkan}  & c^T x \\
\text{dengan syarat}& d^T x = \alpha \\
&0 \le x \le 1.
\end{array}
$$

Untuk menuliskan suatu masalah program linier khusus, yang diketahui koefisien-koefisien fungsi objektif dan fungsi-fungsi kendala, gunakan `alignat` bukan `align` untuk memperoleh perataan tanda, variabel dan koefisien secara lebih selaras.

```latex
$$
\begin{alignat}{5}
  \max \quad        & z = &   x_1  & + & 12 x_2  &   &       &         && \\
  \mbox{d.s.} \quad &     & 13 x_1 & + & x_2     & + & 12x_3 & \geq 5  && \tag{kendala 1} \\
                    &     & x_1    &   &         & + & x_3   & \leq 16 && \tag{kendala 2} \\
                    &     & 15 x_1 & + & 201 x_2 &   &       & =    14 && \tag{kendala 3} \\
                    &     & \rlap{x_i \ge 0,\quad i = 1, 2, 3} &&& \tag{kendala 4}
\end{alignat}
$$
```


$$
\begin{alignat}{5}
  \max \quad        & z = &   x_1  & + & 12 x_2  &   &       &         && \\
  \mbox{d.s.} \quad &     & 13 x_1 & + & x_2     & + & 12x_3 & \geq 5  && \tag{kendala 1} \\
                    &     & x_1    &   &         & + & x_3   & \leq 16 && \tag{kendala 2} \\
                    &     & 15 x_1 & + & 201 x_2 &   &       & =    14 && \tag{kendala 3} \\
                    &     & \rlap{x_i \ge 0,\quad i = 1, 2, 3} &&& \tag{kendala 4}
\end{alignat}
$$
Untuk mendapatkan tampilan yang selaras tersebut, masing-masing dari **max**, **$z$**,  setiap variabel, tanda +/-, dan ruas kanan dituliska pada kolom terpisah, dan menambahkan kolom kosong di sebelah kanan.  Selanjutnya, kita hitung banyaknya pemisah kolom (`&`), hasilnya ditambah satu kemudian dibagi dua. (misalnya (9 + 1) ÷ 2 = 5).

Perintah `\rlap` digunakan untuk menggabungkan beberapa kolom. 

Perintah (opsional) `\tag` digunakan untuk menandai (memberi label) setiap kendala.

**Tabel Simplex**

Karena koefisien fungsi objektif $z$ tidak pernah berubah, biasanya kolom $z$ tidak perlu ditulis pada tabel simplex. 

**Tabel simplex normal**

```latex
$$
\begin{array}{rrrrrr|r}
               & x_1 & x_2 & s_1 & s_2 & s_3 &    \\ \hline
           s_1 &   0 &   1 &   1 &   0 &   0 &  8 \\
           s_2 &   1 &  -1 &   0 &   1 &   0 &  4 \\
           s_3 &   1 &   1 &   0 &   0 &   1 & 12 \\ \hline
               &  -1 &  -1 &   0 &   0 &   0 &  0
\end{array}
$$
```

$$
\begin{array}{rrrrrr|r}
               & x_1 & x_2 & s_1 & s_2 & s_3 &    \\ \hline
           s_1 &   0 &   1 &   1 &   0 &   0 &  8 \\
           s_2 &   1 &  -1 &   0 &   1 &   0 &  4 \\
           s_3 &   1 &   1 &   0 &   0 &   1 & 12 \\ \hline
              \notag &  -1 &  -1 &   0 &   0 &   0 &  0
\end{array}\notag
$$



Tabel simplex dapat ditumpuk/digabung untuk memberikan ilustrasi memasukkan variabel pada tahap yang berbeda.

```latex
$$
\begin{array}{rrrrrrr|rr}
      & x_1 & x_2 & s_1 & s_2 & s_3 &  w &    & \text{rasio} \\ \hline
  s_1 &   0 &   1 &   1 &   0 &   0 &  0 &  8 &            - \\
    w & 1^* &  -1 &   0 &  -1 &   0 &  1 &  4 &            4 \\
  s_3 &   1 &   1 &   0 &   0 &   1 &  0 & 12 &           12 \\ \hdashline
      &   1 &  -1 &   0 &  -1 &   0 &  0 &  4 &              \\ \hline
  s_1 &   0 &   1 &   1 &   0 &   0 &  0 &  8 &              \\
  x_1 &   1 &  -1 &   0 &  -1 &   0 &  1 &  4 &              \\
  s_3 &   0 &   2 &   0 &   2 &   1 & -1 &  8 &              \\ \hdashline
      &   0 &   0 &   0 &   0 &   0 & -1 &  0 &
\end{array}
$$
```

$$
\begin{array}{rrrrrrr|rr}
      & x_1 & x_2 & s_1 & s_2 & s_3 &  w &    & \text{rasio} \\ \hline
  s_1 &   0 &   1 &   1 &   0 &   0 &  0 &  8 &            - \\
    w & 1^* &  -1 &   0 &  -1 &   0 &  1 &  4 &            4 \\
  s_3 &   1 &   1 &   0 &   0 &   1 &  0 & 12 &           12 \\ \hdashline
      &   1 &  -1 &   0 &  -1 &   0 &  0 &  4 &              \\ \hline
  s_1 &   0 &   1 &   1 &   0 &   0 &  0 &  8 &              \\
  x_1 &   1 &  -1 &   0 &  -1 &   0 &  1 &  4 &              \\
  s_3 &   0 &   2 &   0 &   2 &   1 & -1 &  8 &              \\ \hdashline
      &   0 &   0 &   0 &   0 &   0 & -1 &  0 &
\end{array}\notag
$$

**Tabel Simplex Dual**

```
$$
\begin{array}{rrrrrrrr|r}
             & x_1 & x_2 & x_3 & x_4 & x_5 & x_6 &  x_7 &        \\ \hline
         x_4 &   0 &  -3 &   7 &   1 &   0 &   0 &    2 & 2M  -4 \\
         x_5 &   0 &  -9 &   0 &   0 &   1 &   0 &   -1 & -M  -3 \\
         x_6 &   0 &   6 &  -1 &   0 &   0 &   1 & -4^* & -4M +8 \\
         x_1 &   1 &   0 &   1 &   0 &   0 &   0 &    1 &      M \\ \hline
             &   0 &   1 &   1 &   0 &   0 &   0 &    2 &     2M \\
\text{rasio} &     &     &   1 &     &     &     &  1/2 &
\end{array}
$$
```

$$
\begin{array}{rrrrrrrr|r}
             & x_1 & x_2 & x_3 & x_4 & x_5 & x_6 &  x_7 &        \\ \hline
         x_4 &   0 &  -3 &   7 &   1 &   0 &   0 &    2 & 2M  -4 \\
         x_5 &   0 &  -9 &   0 &   0 &   1 &   0 &   -1 & -M  -3 \\
         x_6 &   0 &   6 &  -1 &   0 &   0 &   1 & -4^* & -4M +8 \\
         x_1 &   1 &   0 &   1 &   0 &   0 &   0 &    1 &      M \\ \hline
             &   0 &   1 &   1 &   0 &   0 &   0 &    2 &     2M \\
\text{rasio} &     &     &   1 &     &     &     &  1/2 &
\end{array}\notag
$$

Tabel dapat ditumpuk/digabung untuk memberikan ilustrasi teoritis tentang apa yang terjadi di langkah-langkah mendatang.
$$
\begin{array}{rrrrrrr|r}
         &  x_1 &  x_2 &  x_3 &  s_1 &    s_2 &  s_3 &       \\     \hline
     s_1 &   -2 &    0 &   -2 &    1 &      0 &    0 &   -60 \\
     s_2 &   -2 & -4^* &   -5 &    0 &      1 &    0 &   -70 \\
     s_3 &    0 &   -3 &   -1 &    0 &      0 &    1 &   -27 \\ \hdashline
         &    8 &   10 &   25 &    0 &      0 &    0 &     0 \\
\text{rasio} &   -4 & -5/2 &   -5 &      &        &      &       \\     \hline
     s_1 & -2^* &    0 &   -2 &    1 &      0 &    0 &   -60 \\
     x_2 &  1/2 &    1 &  5/4 &    0 &   -1/4 &    0 &  35/2 \\
     s_3 &  \notag3/2 &    0 & 11/4 &    0 &   -3/4 &    1 &  51/2 \\ \hdashline
         &    3 &    0 & 25/2 &    0 &    5/2 &    0 &  -175 \\
\text{rasio} & -3/2 &      & 25/4 &      &        &      &       \\     \hline
     x_1 &    1 &    0 &    1 & -1/2 &      0 &    0 &    30 \\
     x_2 &    0 &    1 &  3/4 &  1/4 &   -1/4 &    0 &   5/2 \\
     s_3 &    0 &    0 &  5/4 &  3/4 & -3/4^* &    1 & -39/2 \\ \hdashline
         &    0 &    0 & 19/2 &  3/2 &    5/2 &    0 &  -265 \\
\text{rasio} &      &      &      &      &  \dots &      &       \\     \hline
     x_1 &    1 &    0 &    1 & -1/2 &      0 &    0 &    30 \\
     x_2 &    0 &    1 &  1/3 &    0 &      0 & -1/3 &     9 \\
     s_2 &    0 &    0 & -5/3 &   -1 &      1 & -4/3 &    26 \\ \hdashline
         &    0 &    0 & 41/3 &    4 &      0 & 10/3 &  -330
\end{array}
$$

**Dualitas**

Satu gambar bernilai [seribu kata](https://math.stackexchange.com/q/2572928/290189). Berikut adalah ilustrasi hubungan antara suatu program linier dan dualnya.
$$
\require{extpfeil} % produce extensible horizontal arrows
\begin{array}{ccc} % arrange LPPs
% first row
% first LPP
\bbox[yellow,5px,border:2px solid red]
{\begin{array}{ll}
\max & z = c^T x \\
\text{d.s.} & A x \le b \\
& x \ge 0
\end{array}}
& \xtofrom{\text{dualitas}} &
% second LPP
\bbox[yellow,5px,border:2px solid red]
{\begin{array}{ll}
\min & v = b^T y \\
\text{d.s.} & A^T y \ge c \\
& y \ge 0
\end{array}} \\
({\cal PC}) & & ({\cal DC}) \\
\text{ditambah } {\Large \downarrow} \text{variabel slak} &  & \text{dikurangi } {\Large \downarrow} \text{vaiabel surplus}\\ % Change to your favorite arrow style
%
% second row
% third LPP
\bbox[cyan,5px,border:2px solid red]
{\begin{array}{ll}
\max & z = c^T x \\
\text{d.s.} & A x + s = b \\
& x,s \ge 0
\end{array}}
& \xtofrom[\text{beberapa langkah dilewati}]{\text{dualitas}} &
% fourth LPP
\bbox[cyan,5px,border:2px solid red]
{\begin{array}{ll}
\min & v = b^T y \\
\text{d.s.} & A^T y - t = c \\
& y,t \ge 0
\end{array}} \\
({\cal PS}) & & ({\cal DS})
%
\end{array}\notag
$$

### Satuan

Meskipun LaTeX memiliki paket khusus untuk mengatur tampilan satuan, namun MathJax tidak. Untuk konsistensi visual, Anda harus mengatur tampilan satuan pada kode MathJax dengan nilai yang sesuai, memisahkan nilai dan satuan dengan `\` (spasi-*backslash*-spasi) untuk menghasilkan spasi kecil antara nilai dan satuan. Selain itu, ikuti konvensi di bawah ini untuk mengatur tampilan nilai dan satuan.

+ **Pemisah Desimal & Pemisahan Digit**

  Mengikuti konvensi dunia berbahasa Inggris, sebuah titik `.` harus digunakan untuk memisahkan bagian desimal dan bagian bulat suatu bilangan, bukan menggunakan koma `,` seperti yang umum dipakai dalam beberapa bahasa. Ini karena koma sudah disediakan untuk memisahkan notasi matematika seperti argumen fungsi multivariabel, anggota-anggota suatu himpunan, dan *tupel* berurutan untuk koordinat.

  Tidak ada tanda baca yang harus digunakan untuk memisahkan setiap tiga digit di kedua sisi pemisah desimal — sebagai gantinya, spasi kecil yang dihasilkan oleh  `\, ` harus digunakan pada kedua sisi penanda desimal ketika *string* digit terdiri atas lebih dari empat atau lima digit. Misalnya,

  + `4321.1234` $4321.1234$
  + `54\,321.123\,45` $54\,321.123\,45$
  + `0.56789` $0.56789$
  + `0.567\,89` $0.567\,89$

  Jika Anda menggunakan pemisah desimal, Anda harus menyertakan digit di kedua sisi pemisah, bahkan jika digitnya hanya 00.

+ **Perpangkatan 10**

  Karena kita bukan kalkulator, lebih baik kita menulis sepenuhnya tanpa singkatan `\times10^{n}` $\times10^{n}$ ketika notasi ilmiah atau teknik sangat membantu atau diperlukan. Anda tidak perlu menambah atau mengurangi spasi karena `\times` akan mengatur spasi sendiri.

  Namun demikian, jika perlu, gunakan variasi penulisan notasi ilmiah dengan  huruf 'E' atau 'e' tegak sebagai pengganti $\times10^{n}$, seperti

  + `\mathrm{E}\,6` $\mathrm{E}\,6$, 
  + `\scriptsize{\mathrm{E}}\,\normalsize{6}` $\scriptsize{\mathrm{E}}\,\normalsize{6}$, dan
  + `\mathrm{e}\,6` $\mathrm{e}\,6$.

+ **Satuan Tunggal**

  Penulisan simbol satuan apa pun, terutama satuan sistem internasional (SI), harus mengikuti bentuk `\mathrm{nama_satuan`. Misalnya,

  + `\mathrm{m}`  $\mathrm{m}$
  + `\mathrm{kg}` $\mathrm{kg}$
  + `\mathrm{cm.}` $\mathrm{cm.}$

  Jangan menggunakan titik pada simbol satuan, melainkan gunakan titik pada simbol satuan yang disingkat.

+ **Satuan dengan titik pengali**

  Satuan-satuan yang dikalikan dengan tanda titik harus dituliskan dengan mengikuti bentuk `\mathrm{u}\!\cdot\!\mathrm{v}` $\mathrm{u}\!\cdot\!\mathrm{v}$. Karena `\cdot` dirancang untuk memisahkan angka, spasi negatif kecil `\!` pada kedua sisi mempertahankan spasi seragam pada semua kombinasi satuan. Misalnya,

  + `\mathrm{N}\!\cdot\!\mathrm{m}` $\mathrm{N}\!\cdot\!\mathrm{m}$
  + `\mathrm{s}\!\cdot\!\mathrm{A}` $\mathrm{s}\!\cdot\!\mathrm{A}$.

  Jangan menggunakan `\times` $\times$ sebagai pengali satuan.

+ **Satuan dengan garis miring pembagi**

  Satuan yang dibagi dengan menggunakan garis miring pembagi harus ditulis mengikuti bentuk`\left.\mathrm{u}\middle/\mathrm{v}\right.` $\left.\mathrm{u}\middle/\mathrm{v}\right.$. Perhatikan garis miringnya dicetak agak panjang untuk memastikan sesuai dengan tinggi huruf satuan, terutama apabila terkait pangkat. Misalnya,

  + `\left.\mathrm{J}\middle/\mathrm{s}\right.` $\left.\mathrm{J}\middle/\mathrm{s}\right.$
  + `\left.\mathrm{m}\middle/\mathrm{s}^2\right.` $\left.\mathrm{m}\middle/\mathrm{s}^2\right.$.

  Jika mau, Anda dapat menambahkan spasi negatif `\!` di kedua sisi.

+ **Pangkat**

  Pangkat pada satuan dapat dituliskan dengan cara biasa. Tanda pangkat (`^`) dan angka harus segera mengikuti tanda kurung penutup pada `\mathrm{}`. Misalnya,

  + `\mathrm{m}^2` $\mathrm{m}^2$
  + `\left.\mathrm{m}\middle/\mathrm{s}^2\right.` $\left.\mathrm{m}\middle/\mathrm{s}^2\right.$.

+ **Tanda kurung**

  Tanda kurung dapat ditulis dengan cara seperti biasanya, yakni menggunakan perintah `\left(` dan `\right)` di luar perintah `\mathrm`. Misalnya,

  + `\left.\mathrm{kg}\!\cdot\!\mathrm{m}^2\middle/\left(\mathrm{C}\!\cdot\!\mathrm{s}\right)\right.` $\left.\mathrm{kg}\!\cdot\!\mathrm{m}^2\middle/\left(\mathrm{C}\!\cdot\!\mathrm{s}\right)\right.$.

+ **Pangkat pada satuan yang digabung**

  Jika Anda lebih menyukai untuk tidak menggunakan pemisah satuan dan hanya menggunakan pangkat, pisahkan setiap `\mathrm{}` dengan spasi sempit `\,` dan gunakan pangkat sebagaimana diperlukan. Misalnya,

  + `\mathrm{m}\,\mathrm{s}^{-2}` $\mathrm{m}\,\mathrm{s}^{-2}$
  + `\mathrm{s}^{-1}\,\mathrm{mol}` $\mathrm{s}^{-1}\,\mathrm{mol}$.

+ **Contoh dalam konteks**

  ```latex
  $$
  + \mu_0=4\pi\times10^{-7} \ \left.\mathrm{\mathrm{T}\!\cdot\!\mathrm{m}}\middle/\mathrm{A}\right.
  $$
  ```

  $$
  + \mu_0=4\pi\times10^{-7} \ \left.\mathrm{\mathrm{T}\!\cdot\!\mathrm{m}}\middle/\mathrm{A}\right..
  $$

  

  ```latex
  $$
  180^\circ=\pi \ \mathrm{rad}
  $$
  ```

  $$
  180^\circ=\pi \ \mathrm{rad}.
  $$

  

  ```latex
  $$
  N_A = 6.022\times10^{23} \ \mathrm{mol}^{-1}
  $$
  ```

  $$
  N_A = 6.022\times10^{23} \ \mathrm{mol}^{-1}.
  $$

### Menggunakan MathJax pada Penulisan Kode Semu (Pseudocode)

Berikut adalah contoh penggabungan MathJax di dalam kode semu (*pseudocode*) atau penulisan algoritma:

==============================================================================================================

**Input:** bilangan bulat positif $n$
**Output:** Bilangan-bilagan $T_1,\ T_2,\ T_3,\ \ldots,T_n$
$T_1\gets1$
`untuk` $k$ `dari` $2$ `sampai` $n$
	$T_k\gets (k−1)T_{k−1}$
`untuk` $k$ `dari` $2$ `sampai` $n$
	`untuk` $j$ `dari` $k$ `sampai` $n$
			$T_j\gets(j−k)T_{j−1}+(j−k+2)T_j$
`hasilnya` $T_1,\ T_2,\ T_3,\ \ldots,T_n$.

==============================================================================================================

Pada contoh di atas, indentasi (pemunduran teks) dilakukan dengan menggunakan spasi kosong atau `tab` dan terkadang hal ini akan berbeda ketika dokumen Markdown diproses menjadi dokumen lain.

Berikut adalah versi penulisan algoritma di atas menggunakan `\phantom` untuk menghasilkan indentasi dan mengubah jarak antara kode dan ekspresi MathJax dengan `\;`. Mungkin Anda tidak menyadari perbedaan kedua penulisan tersebut, karena tampilannya memang sama hanya cara yang digunakan berbeda!

==============================================================================================================

**Input:** bilangan bulat positif$\; n$
**Output:** Bilangan-bilagan$\; T_1,\ T_2,\ T_3,\ \ldots,T_n$
$T_1\gets1$
`untuk`$\; k$ `dari`$\; 2$ `sampai`$\; n$
$\phantom{{}++{}}T_k\gets (k−1)T_{k−1}$
`untuk`$\; k$ `dari`$\; 2$ `sampai`$\; n$
$\phantom{{}++{}}$`untuk`$\; j$ `dari`$\; k$ `sampai`$\; n$
$\phantom{{}++{}}\phantom{{}++{}}\phantom{{}++{}}T_j\gets(j−k)T_{j−1}+(j−k+2)T_j$
`hasilnya`$\; T_1,\ T_2,\ T_3,\ \ldots,T_n$.

==============================================================================================================

### Menampilkan persamaan secara interaktif

MathJax dapat digunakan untuk menampikan persamaan multibaris secara interaktif. Hal ini sangat menarik untuk presentasi proses pembuktian. Berikut adalah beberapa contoh persamaan matematika interaktif. Untuk berinteraksi dengan persamaan matematis Anda harus menampilkan file Markdown ini pada program pratinjau (*previewer*). Kebanyakan editor Markdown (termasuk Typora) sudah dapat melihat hasil tampilan ketika Anda mengedit file Markdown. Anda juga dapat menampilkan file Markdown dengan browser favorit Anda (Google Chrome, Mozilla Firefork, MS IE, atau MS Edge) setelah Anda memasang ekstensi **Markdown preview**. Setelah Anda memasang ekstensi tersebut, buka file Markdown dengan browser Anda tersebut. 

```latex
$\require{action}
\require{enclose}$
$$
\toggle{
x\cdot 0 = 0\quad\enclose{roundedbox}{\text{Klik untuk melihat buktinya}}
}{
\begin{array}{rll}
x\cdot 0
&= \mathtip{x\cdot 0 + 0}{0 \text{ adalah elemen identitas penjumlahan}} \\
&= \mathtip{x\cdot 0 + (x\cdot 0 + -(x\cdot 0))}{ -(x\cdot 0) \text{ adalah invers penjumlahan } x\cdot 0}\\
&= \mathtip{(x\cdot 0 + x\cdot 0) + -(x\cdot 0)}{ \text{ sifat asosiatif penjumlahan }\;}\\
&= \mathtip{x\cdot(0 + 0) + -(x\cdot 0) }{ \text{ sifat distributif perkalian terhadap penjumlahan }\;}\\
&= \mathtip{x\cdot 0 + -(x\cdot 0) }{ 0 \text{ adalah elemen identitas penjumlahan}} \\
&= \mathtip{0.}{ -(x\cdot 0) \text{ adalah invers penjumlahanf } x\cdot 0}
\end{array}
\quad\quad
\bbox[4pt,border: 1px solid red]{
\begin{array}{l}
\text{Jika Anda masih bingung pada setiap langkah}\\
\text{geser panah mouse Anda ke ruas kanan}\\
\text{baris tersebut untuk klu/penjelasan.}
\end{array}}
}\endtoggle
$$
```

akan menghasilkan tampilan

$\require{action}\require{enclose}$
$$
\toggle{
x\cdot 0 = 0\quad\enclose{roundedbox}{\text{Klik untuk melihat buktinya}}
}{
\begin{array}{rll}
x\cdot 0
&= \mathtip{x\cdot 0 + 0}{0 \text{ adalah elemen identitas penjumlahan}} \\
&= \mathtip{x\cdot 0 + (x\cdot 0 + -(x\cdot 0))}{ -(x\cdot 0) \text{ adalah invers penjumlahan } x\cdot 0}\\
&= \mathtip{(x\cdot 0 + x\cdot 0) + -(x\cdot 0)}{ \text{ sifat asosiatif penjumlahan }\;}\\
&= \mathtip{x\cdot(0 + 0) + -(x\cdot 0) }{ \text{ sifat distributif perkalian terhadap penjumlahan }\;}\\
&= \mathtip{x\cdot 0 + -(x\cdot 0) }{ 0 \text{ adalah elemen identitas penjumlahan}} \\
&= \mathtip{0.}{ -(x\cdot 0) \text{ adalah invers penjumlahanf } x\cdot 0}
\end{array}
\quad\quad
\bbox[4pt,border: 1px solid red]{
\begin{array}{l}
\text{Jika Anda masih bingung pada setiap langkah}\\
\text{geser panah mouse Anda ke ruas kanan}\\
\text{baris tersebut untuk klu/penjelasan.}
\end{array}}
}\endtoggle
$$

Pada contoh di atas MathJax menggunakan ekstensi `Action`, `Enclose` dan `BBox`.  BBox otomatis akan dimuat, sehingga untuk menggunakan  `Action` dan `Enclose`, gunakan perintah `\require{action}` dan `\require{enclose}` di dalam `$ ... $`.

- Perintah `\enclose{roundedbox}{...}` menggambar kotak teks pesan.
- Perintah `\texttip{ekspresi}{info}` dan `\mathtip{ekspresi}{info}` menambahkan informasi yang akan muncul apabila ekspresi matematika ditunjuk. Perbedaan keduanya ada teks informasinya apakah hanya teks biasa atau dapat memuat ekspresi matematika juga.
- Perintah `\bbox[4pt,border: 1px outset red]{...}` menggambar kotak teks dengan spesifikasi yang diberikan.

**Hasil**:

- Perintah `toggle` berhasil dengan benar.
- Meskipun `tooltip` berhasil, terkadang hasilya tidak sesuai keinginan.
- Kehilangan cara yang baik untuk menuliskan teks multibaris di dalam modus matematika. 
- Perintah `\parbox` tidak berhasil???

Contoh lain, ekspansi kuadrat suku dua:

```latex
$$
\require{action}
\def\rhsa{(x+1)(x+1)}
\def\rhsb{x(x+1) + 1(x+1)}
\def\rhsc{(x^2+x) + (x+1)}
\def\rhsd{x^2 + (x + x) + 1}
\def\rhse{x^2 + 2x + 1}
\def\click{\rlap{\enclose{roundedbox}{\small\text{langkah berikutnya}}}\hphantom{\rhsb}}
\def\={\phantom{{}={}}}
(x+1)^2
\toggle
  {\begin{aligned}[t]& = \click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\[3px]& = \rhsc\\[3px]&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\[3px]& = \rhsc\\[3px]& = \rhsd\\[3px]&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\[3px]& = \rhsc\\[3px]& = \rhsd\\[3px]& = \rhse\end{aligned}}
\endtoggle
$$
```

$$
\require{action}
\def\rhsa{(x+1)(x+1)}
\def\rhsb{x(x+1) + 1(x+1)}
\def\rhsc{(x^2+x) + (x+1)}
\def\rhsd{x^2 + (x + x) + 1}
\def\rhse{x^2 + 2x + 1}
\def\click{\rlap{\enclose{roundedbox}{\small\text{langkah berikutnya}}}\hphantom{\rhsb}}
\def\={\phantom{{}={}}}
(x+1)^2
\toggle
  {\begin{aligned}[t]& = \click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\[3px]& = \rhsc\\[3px]&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\[3px]& = \rhsc\\[3px]& = \rhsd\\[3px]&\=\click\end{aligned}}
  {\begin{aligned}[t]& = \rhsa\\[3px]& = \rhsb\\[3px]& = \rhsc\\[3px]& = \rhsd\\[3px]& = \rhse\end{aligned}}
\endtoggle
$$

Berikut adalah contoh proses perhitungan limit.

$$
\def\click{\rlap{\enclose{roundedbox}{\small\text{langkah berikutnya}}}\hphantom{\RHSc}}
\def\={\phantom{{}={}}}

\def\LHS{\lim_{x \rightarrow \infty} \dfrac{\ln(x^2+4)}{\ln(x+\sqrt{1+x^2})}}

\def\RHSa{\lim_{x \rightarrow \infty} \dfrac{\ln(x^2) + \ln(1+4/x^2)}{\ln(x) + \ln(1+\sqrt{1+1/x^2})}}

\def\RHSb{\lim_{x \rightarrow \infty} \dfrac{\ln(x^2)}{\ln(x)} \dfrac{\left(1+\dfrac{\ln(1+4/x^2)}{\ln(x^2)} \right)}{\left(1 + \dfrac{\ln(1+\sqrt{1+1/x^2})}{\ln(x)} \right)}}

\def\RHSc{\lim_{x \rightarrow \infty} 2 \dfrac{\ln(x)}{\ln(x)} \lim_{x \rightarrow \infty} \dfrac{\left(1+\dfrac{\ln(1+4/x^2)}{\ln(x^2)} \right)}{\left(1 + \dfrac{\ln(1+\sqrt{1+1/x^2})}{\ln(x)} \right)}}

\def\RHSd{2 \lim_{x \rightarrow \infty} \dfrac{\left(1+\dfrac{\ln(1+4/x^2)}{\ln(x^2)} \right)}{\left(1 + \dfrac{\ln(1+\sqrt{1+1/x^2})}{\ln(x)} \right)}}

\def\tipa{
\begin{array}{l}
\text{Keluarkan $x^2$ dan $x$,}\\\text{gunakan sifat logaritma hasilkali}
\end{array}
}

\def\tipb{\text{Keluarkan $\ln (x^2)$ dan $\ln (x)$}}
\def\tipc{\text{Sifat logaritma perpangkatan}}
\def\tipd{\text{Karena $x\ne1,\ \ln (x)\ne 0, \text{ dan } \frac{\ln (x)}{\ln (x)}=1$}}
\def\tipe{\text{Nilai limit di ruas kanan sama dengan 1}}
\LHS
\toggle
{\begin{aligned}[t]& = \click\end{aligned}}

{\begin{aligned}[t]& = 
\mathtip{\RHSa}{\tipa}\\[3px]&\=\click\end{aligned}}

{\begin{aligned}[t]& = 
\mathtip{\RHSa}{\tipa}\\[3px]& =
\mathtip{\RHSb}{\tipb}\\[3px]&\=\click\end{aligned}}

{\begin{aligned}[t]& = 
\mathtip{\RHSa}{\tipa}\\[3px]& =
\mathtip{\RHSb}{\tipb}\\[3px]& = 
\mathtip{\RHSc}{\tipc}\\[3px]&\=\click\end{aligned}}

{\begin{aligned}[t]& = 
\mathtip{\RHSa}{\tipa}\\[3px]& =
\mathtip{\RHSb}{\tipb}\\[3px]& = 
\mathtip{\RHSc}{\tipc}\\[3px]& = 
\mathtip{\RHSd}{\tipd}\\[3px]&\=\click\end{aligned}}

{\begin{aligned}[t]& = 
\mathtip{\RHSa}{\tipa}\\[3px]& =
\mathtip{\RHSb}{\tipb}\\[3px]& = 
\mathtip{\RHSc}{\tipc}\\[3px]& = 
\mathtip{\RHSd}{\tipd}\\[3px]& = 
\mathtip{2.}{\tipe}\end{aligned}}
\endtoggle
$$

Berikut ini adalah contoh menyembunyikan tulisan.
$$
\toggle{ 
\quad\enclose{roundedbox}{\text{ Paragraf ini tersemunyi. Klik untuk melihat.}}
}{
\quad\quad
\bbox[4pt,border: 1px solid red]{
\begin{array}{l}
\text{Untuk setiap bilangan asli }N>1\text{ kita memiliki beberapa bilangan prima }\\
p_1,\ p_2,\ \ldots,\ p_k\leq N. \\
\text{Kita juga tahu bahwa untuk }x\in A\setminus\{1\},\\
x= p_1^{l_1}p_2^{l_2}\ldots p_k^{l_k} ,\quad l_i\geq 0.\\
\text{Jadi, untuk suatu pasangan bilangan asli }(m,n),\ m,\ n>1\text{ kita peroleh:}\\
m=p_1^{s_1} p_2^{s_2}\ldots p_k^{s_k},\ s_i\geq 0\qquad n=p_1^{t_1} p_2^{t_2}\ldots p_k^{t_k}, t_i\geq 0 \\
\text{Kita mulai menghitung pangkat-pangkat}\\
\left (\begin{array}{}s_1 & s_2 &\ldots & s_k\\t_1 & t_2 &\ldots &t_k \end{array}\right )\\
\text{Baik $m$ maupun $n$ tidak mungkin semua faktor primanya}\\
\text{berpangkat $\ge1$, karena hal itu berakibat}\\ \text{salah satu bilangan sama dengan $1$, yang tidak kita gunakan.}
\end{array}}
}\endtoggle
$$



### Contoh aplikasi overlaping dan `\mathtip`

Berikut adalah menggambar bendera Indonesia. Kita tahu bendera Indonesia mempunyai perbandingan panjang dan lebar 3 banding 2. Gambar berikut diperoleh dengan menggunakan perintah `\Rule`, `\rlap`, dan `\lower`.

```latex
$$
\rlap{{\color{red}{\Rule{9em}{3em}{0em}}}}\\
\vspace{0em}\rlap{\color{white}{\Rule{9em}{3em}{0em}}}\notag
$$
```
$$
\rlap{{\color{red}{\Rule{9em}{3em}{0em}}}}\\
\rlap{\color{white}{\Rule{9em}{3em}{0em}}}\notag
$$



Contoh lain aplikasi `\mathtip`:

```latex
$$
\require{action}
{
\overset{\color{red}\overset{\Rule{0.9em}{0.3em}{0.05em}} {\color{black}\Huge\heartsuit}}

{\overset{\Rule{2em}{0.5em}{0.05em}}
{\overset{\Rule{5em}{0.05em}{0.05em}}
{\overset{\Rule{9em}{0.05em}{0.05em}}
{\overset{\Rule{14em}{0.05em}{0.05em}}

{\overline{\left\rfloor\left\rfloor\overset{\underline{{\displaystyle \Huge {\scr F\sf o\tt n\cal t\frak s}} }}

{\underline{\underline{\underline{\underline{\underline{\underline{\left[\overline{\begin{matrix}
\mathtip{\overset{\infty}{\underset{j=0}{\LARGE\rm B}}}{\text{\rm}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\cal C}}}{\text{\cal}} \,\overset{\displaystyle f(c)}{}&\qquad
  \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\sf E}}}{\text{\sf}}\,\overset{\displaystyle f(c)}{} \\
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\tt G}}}{\text{\tt}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{ \ \ \, \infty}{\underset{j=0}{\LARGE\it K}}}{\text{\it}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\quad\infty}{\underset{j=0}{\LARGE\scr M}}}{\text{\scr}}\,\overset{\displaystyle f(c)}{} \\
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\bf S}}}{\text{\bf}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\frak T}}}{\text{\frak}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\Bbb W}}}{\text{\Bbb}}\,\overset{\displaystyle f(c)}{}  \\\end{matrix}}\right]
}}}}}}}
\right\lfloor\right\lfloor}}}}}}}\\\text{Tunjuk huruf untuk melihat jenisnya}
$$
```



$$
\require{action}
{
\overset{\color{red}\overset{\Rule{0.9em}{0.3em}{0.05em}} {\color{black}\Huge\heartsuit}}

{\overset{\Rule{2em}{0.5em}{0.05em}}
{\overset{\Rule{5em}{0.05em}{0.05em}}
{\overset{\Rule{9em}{0.05em}{0.05em}}
{\overset{\Rule{14em}{0.05em}{0.05em}}

{\overline{\left\rfloor\left\rfloor\overset{\underline{{\displaystyle \Huge {\scr F\sf o\tt n\cal t\frak s}} }}

{\underline{\underline{\underline{\underline{\underline{\underline{\left[\overline{\begin{matrix}
\mathtip{\overset{\infty}{\underset{j=0}{\LARGE\rm B}}}{\text{\rm}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\cal C}}}{\text{\cal}} \,\overset{\displaystyle f(c)}{}&\qquad
  \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\sf E}}}{\text{\sf}}\,\overset{\displaystyle f(c)}{} \\
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\tt G}}}{\text{\tt}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{ \ \ \, \infty}{\underset{j=0}{\LARGE\it K}}}{\text{\it}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\quad\infty}{\underset{j=0}{\LARGE\scr M}}}{\text{\scr}}\,\overset{\displaystyle f(c)}{} \\
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\bf S}}}{\text{\bf}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\frak T}}}{\text{\frak}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\Bbb W}}{\verb*\Bbb*}\,\overset{\displaystyle f(c)}{}  \\ \end{matrix}}\right]
}}}}}}}
\right\lfloor\right\lfloor}}}}}}}\\\text{Tunjuk huruf untuk melihat jenisnya}\notag
$$

$$
\require{action}
\overset{\rlap{\overset{\,{\rlap{\overset{\overset{\overset{\color{red}{\rlap{\color{\green}{\,\,\star}}{\Rule{1em}{0.5em}{0.25em}}}}{}}{}}{}}{\Huge|}}}{}}{\Rule{0.5em}{0.25em}{0.05em}}}{\overset{\Rule{2em}{0.05em}{0.05em}}{\overset{\Rule{5em}{0.05em}{0.05em}}{\overset{\Rule{9em}{0.05em}{0.05em}}{\overset{\Rule{14em}{0.05em}{0.05em}}
{\overline{\left\rfloor\left\rfloor\overset{\underline{{\displaystyle \Huge {\scr F\sf o\rm n\cal t\frak s}} }}{\underline{\underline{\underline{\underline{\underline{\underline{\left[\overline{\begin{matrix}
\mathtip{\overset{\infty}{\underset{j=0}{\LARGE\rm A}}}{\text{\rm}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\cal B}}}{\text{\cal}} \,\overset{\displaystyle f(c)}{}&\qquad
  \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\sf C}}}{\text{\sf}}\,\overset{\displaystyle f(c)}{} \\
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\tt D}}}{\text{\tt}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{ \ \ \, \infty}{\underset{j=0}{\LARGE\it E}}}{\text{\it}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\quad\infty}{\underset{j=0}{\LARGE\scr H}}}{\text{\scr}}\,\overset{\displaystyle f(c)}{} \\
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\bf K}}}{\text{\bf}}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\frak M}}}{\verb*\frak*}\,\overset{\displaystyle f(c)}{} &\qquad
 \mathtip{\overset{\infty}{\underset{j=0}{\LARGE\Bbb N}}}{\verb*\Bbb*}\,\overset{\displaystyle f(c)}{}  \\\end{matrix}}\right]}}}}}}}\right\lfloor\right\lfloor}}}}}}\notag
 \\\text{Tunjuk huruf untuk melihat jenisnya}
$$



## Referensi

Mathematics Meta Stack Exchange. (2017). *[MathJax basic tutorial dan quick reference](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)*. diakses 27-4-2021.

Dr. Carol JVF Burns. (2011). *TeX Commands available in MathJax*. https://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm. diakses 5-5-2021
