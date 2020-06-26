# Metode Bagi-Dua (Bisection Method)

**Metode Bagi-Dua** adalah algoritma pencarian akar pada sebuah interval. Interval tersebut membagi dua bagian, lalu memilih dari dua bagian ini dipilih bagian mana yang mengandung akar dan bagian yang tidak mengandung akar dibuang. Hal ini dilakukan berulang-ulang hingga diperoleh akar persamaan atau mendekati akar persamaan. Metode ini berlaku ketika ingin memecahkan persamaan ![f(x)=0](https://s0.wp.com/latex.php?latex=f%28x%29%3D0&bg=ffffff&fg=666666&s=0) dengan ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=666666&s=0) merupakan fungsi kontinyu.



[![Photobucket](https://i2.wp.com/i1172.photobucket.com/albums/r578/aimprof08/MetodeBagiDua.jpg)](http://s1172.photobucket.com/albums/r578/aimprof08/?action=view&current=MetodeBagiDua.jpg)

Prosedur Metode Bagi-Dua :



Misal dijamin bahwa ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=666666&s=0) adalah fungsi kontinyu pada interval ![[a, b]](https://s0.wp.com/latex.php?latex=%5Ba%2C+b%5D&bg=ffffff&fg=666666&s=0) dan ![f(a)f(b) < 0](https://s0.wp.com/latex.php?latex=f%28a%29f%28b%29+%3C+0&bg=ffffff&fg=666666&s=0). Ini artinya bahwa ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=666666&s=0) paling tidak harus memiliki akar pada interval ![[a, b]](https://s0.wp.com/latex.php?latex=%5Ba%2C+b%5D&bg=ffffff&fg=666666&s=0). Kemudian definisikan titik tengah pada interval ![[a, b]](https://s0.wp.com/latex.php?latex=%5Ba%2C+b%5D&bg=ffffff&fg=666666&s=0) yaitu ![c = \dfrac{a+b}{2}](https://s0.wp.com/latex.php?latex=c+%3D+%5Cdfrac%7Ba%2Bb%7D%7B2%7D&bg=ffffff&fg=666666&s=0). Dari sini kita memperoleh dua subinterval yaitu ![[a, c]](https://s0.wp.com/latex.php?latex=%5Ba%2C+c%5D&bg=ffffff&fg=666666&s=0) dan ![[c, b]](https://s0.wp.com/latex.php?latex=%5Bc%2C+b%5D&bg=ffffff&fg=666666&s=0). Setelah itu, cek apakah ![f(a)f(c) < 0 ](https://s0.wp.com/latex.php?latex=f%28a%29f%28c%29+%3C+0+&bg=ffffff&fg=666666&s=0) atau ![f(b)f(c) < 0](https://s0.wp.com/latex.php?latex=f%28b%29f%28c%29+%3C+0&bg=ffffff&fg=666666&s=0) ? Jika ![f(a)f(c) < 0](https://s0.wp.com/latex.php?latex=f%28a%29f%28c%29+%3C+0&bg=ffffff&fg=666666&s=0)maka ![b = c ](https://s0.wp.com/latex.php?latex=b+%3D+c+&bg=ffffff&fg=666666&s=0) (artinya titik ![b](https://s0.wp.com/latex.php?latex=b&bg=ffffff&fg=666666&s=0) digantikan oleh titik ![c](https://s0.wp.com/latex.php?latex=c&bg=ffffff&fg=666666&s=0) yang berfungsi sebagai titik ![b](https://s0.wp.com/latex.php?latex=b&bg=ffffff&fg=666666&s=0) pada iterasi berikutnya), jika tidak maka ![a = c](https://s0.wp.com/latex.php?latex=a+%3D+c&bg=ffffff&fg=666666&s=0). Dari iterasi pertama kita memperoleh interval ![[a, b]](https://s0.wp.com/latex.php?latex=%5Ba%2C+b%5D&bg=ffffff&fg=666666&s=0) yang baru dan titik tengah ![c](https://s0.wp.com/latex.php?latex=c&bg=ffffff&fg=666666&s=0) yang baru. Kemudian lakukan pengecekan lagi seperti sebelumnya sampai memperoleh error yang cukup kecil.

**Contoh :
**

Carilah akar dari ![x^3 + 4x^2 -10 = 0](https://s0.wp.com/latex.php?latex=x%5E3+%2B+4x%5E2+-10+%3D+0&bg=ffffff&fg=666666&s=0) pada interval ![[1, 2]](https://s0.wp.com/latex.php?latex=%5B1%2C+2%5D&bg=ffffff&fg=666666&s=0).

**Penyelesaian :
**

Dalam penyelesaian ini saya akan menggunakan sampai iterasi ke-10 dan menggunakan 5 angka dibelakang koma.



f(x) = x3 + 4x2 – 10



f(1) = (1)3 + 4(1)2 – 10 = -5



f(2) = (2)3 + 4(2)2 – 10 = 14



f(1.5) = (1.5)3 + 4(1.5)2 – 10 = 2.375



f(1.25) = (1.25)3 + 4(1.25)2 – 10 = -1.79687



f(1.375) = (1.375)3 + 4(1.375)2 – 10 = 0.16210



f(1.3125) = (1.3125)3 + 4(1.3125)2 – 10 = -0.84838



f(1.34375) = (1.34375)3 + 4(1.34375)2 – 10 = -0.35098



f(1.35938) = (1.35938)3 + 4(1.35938)2 – 10 = -0.09632



f(1.36719) = (1.36719)3 + 4(1.36719)2 – 10 = 0.03239



f(1.36329) = (1.36329)3 + 4(1.36329)2 – 10 = -0.03200



f(1.36524) = (1.36524)3 + 4(1.36524)2 – 10 = 0.000016



f(1.36426) = (1.36426)3 + 4(1.36426)2 – 10 = -0.01601



f(1.36329) = (1.36329)3 + 4(1.36329)2 – 10 = -0.00784





| ![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=666666&s=0) | ![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=666666&s=0) | ![b](https://s0.wp.com/latex.php?latex=b&bg=ffffff&fg=666666&s=0) | ![c = \dfrac{a + b}{2}](https://s0.wp.com/latex.php?latex=c+%3D+%5Cdfrac%7Ba+%2B+b%7D%7B2%7D&bg=ffffff&fg=666666&s=0) | ![f(a)](https://s0.wp.com/latex.php?latex=f%28a%29&bg=ffffff&fg=666666&s=0) | ![f(b)](https://s0.wp.com/latex.php?latex=f%28b%29&bg=ffffff&fg=666666&s=0) | ![f(c)](https://s0.wp.com/latex.php?latex=f%28c%29&bg=ffffff&fg=666666&s=0) | ![f(a)f(c)](https://s0.wp.com/latex.php?latex=f%28a%29f%28c%29&bg=ffffff&fg=666666&s=0) | ![f(b)f(c)](https://s0.wp.com/latex.php?latex=f%28b%29f%28c%29&bg=ffffff&fg=666666&s=0) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 12345678910                                                  | 111.251.251.31251.343751.359381.359381.363291.36329          | 21.51.51.3751.3751.3751.3751.367191.367191.36524             | 1.51.251.3751.31251.343751.359381.367191.363291.365241.36426 | ––––––––––                                                   | ++++++++++                                                   | +–+–––+–+–                                                   | –+–+++–+–+                                                   | +–+–––+–+–                                                   |

Jadi akar yang diperoleh dari ![f(x) = x^3 + 4x^2 -10](https://s0.wp.com/latex.php?latex=f%28x%29+%3D+x%5E3+%2B+4x%5E2+-10&bg=ffffff&fg=666666&s=0) menggunakan 10 iterasi adalah 1.36426 



Program Kode

    
    # Regula-Falsi 
    def  Regfal ( a , b , n ): 
        e  =  0,001 
        fa  =  a ** 2 - 5 * a + 6 
        fb  =  b ** 2 - 5 * b + 6 
        jika  fa * fb < 0 : 
            n + = 1 
            cetak ( "iterasi kem" + str ( n )) 
            x  =  (( a* abs ( fb )) + ( b * abs ( fa ))) / ( abs ( fa ) + abs ( fb )) 
            fx  =  x ** 2 - 5 * x + 6 
            jika  fa * fx < 0 : 
                b  =  x 
            lain : 
                a  =  x 
            jika  abs ( a - b ) < e: 
                cetak ( x ) 
            lain : 
                Regfal ( a , b , n ) 
        lain : 
            jika  fa < fb : 
                a - = 0,1 
            lainnya : 
                b + = 0,1 
            Regfal ( a , b , n )
    
    a  =  float ( input ( "Masukkan interval a:" )) 
    b  =  float ( input ( "Masukkan interval b:" )) 
    Regfal ( a , b , 0 )
```python
`Masukkan interval a: 1`
`Masukkan interval b: 2.1`
`iterasi ke-1`
`iterasi ke-2`
`iterasi ke-3`
`iterasi ke-4`
`iterasi ke-5`
`iterasi ke-6`
`iterasi ke-7`
`iterasi ke-8`
`iterasi ke-9`
`iterasi ke-10`
`iterasi ke-11`
`iterasi ke-12`
`iterasi ke-13`
`iterasi ke-14`
`iterasi ke-15`
`iterasi ke-16`
`iterasi ke-17`
`iterasi ke-18`
`iterasi ke-19`
`iterasi ke-20`
`iterasi ke-21`
`iterasi ke-22`
`iterasi ke-23`
`iterasi ke-24`
`iterasi ke-25`
`iterasi ke-26`
`iterasi ke-27`
`iterasi ke-28`
`iterasi ke-29`
`iterasi ke-30`
`iterasi ke-31`
`iterasi ke-32`
`iterasi ke-33`
`iterasi ke-34`
`iterasi ke-35`
`iterasi ke-36`
`iterasi ke-37`
`iterasi ke-38`
`iterasi ke-39`
`iterasi ke-40`
`iterasi ke-41`
`iterasi ke-42`
`iterasi ke-43`
`iterasi ke-44`
`iterasi ke-45`
`iterasi ke-46`
`iterasi ke-47`
`2.0000000000000004
```

# Metode Regula Falsi (Regula Falsi Method)

 

**Metode Regular Falsi** adalah panduan konsep [**Metode Bagi-Dua**](https://aimprof08.wordpress.com/2012/08/30/metode-bagi-dua-bisection-method/) dan [**Metode Secant**](https://aimprof08.wordpress.com/2012/09/01/metode-secant-secant-method/). Menggunakan konsep [**Metode Bagi-Dua**](https://aimprof08.wordpress.com/2012/08/30/metode-bagi-dua-bisection-method/) karena dimulai dengan pemilihan dua titik awal ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=666666&s=0) dan ![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0) sedemikian sehingga ![f(x_0)](https://s0.wp.com/latex.php?latex=f%28x_0%29&bg=ffffff&fg=666666&s=0) dan ![f(x_1)](https://s0.wp.com/latex.php?latex=f%28x_1%29&bg=ffffff&fg=666666&s=0) berlawanan tanda atau ![f(x_0) f(x_1) < 0](https://s0.wp.com/latex.php?latex=f%28x_0%29+f%28x_1%29+%3C+0&bg=ffffff&fg=666666&s=0). Kemudian menggunakan konsep [**Metode Secant**](https://aimprof08.wordpress.com/2012/09/01/metode-secant-secant-method/) yaitu dengan menarik garis ![l](https://s0.wp.com/latex.php?latex=l&bg=ffffff&fg=666666&s=0) dari titik ![f(x_0)](https://s0.wp.com/latex.php?latex=f%28x_0%29&bg=ffffff&fg=666666&s=0) dan ![f(x_1)](https://s0.wp.com/latex.php?latex=f%28x_1%29&bg=ffffff&fg=666666&s=0) sedemikian sehingga garis ![l](https://s0.wp.com/latex.php?latex=l&bg=ffffff&fg=666666&s=0)berpotongan pada sumbu – ![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=666666&s=0) dan memotong kurva / grafik fungsi pada titik ![f(x_0)](https://s0.wp.com/latex.php?latex=f%28x_0%29&bg=ffffff&fg=666666&s=0) dan ![f(x_1)](https://s0.wp.com/latex.php?latex=f%28x_1%29&bg=ffffff&fg=666666&s=0). Sehingga **Metode Regular Falsi** ini akan menghasilkan titik potong pada sumbu-![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=666666&s=0) yaitu ![x_2](https://s0.wp.com/latex.php?latex=x_2&bg=ffffff&fg=666666&s=0) yang merupakan calon akar dan tetap berada dalam interval ![[x_0, x_1]](https://s0.wp.com/latex.php?latex=%5Bx_0%2C+x_1%5D&bg=ffffff&fg=666666&s=0). Metode ini kemudian berlanjut dengan menghasilkan berturut-turut interval ![[x_{n-1}, x_n]](https://s0.wp.com/latex.php?latex=%5Bx_%7Bn-1%7D%2C+x_n%5D&bg=ffffff&fg=666666&s=0) yang semuanya berisi akar ![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=666666&s=0).

[![Photobucket](https://i2.wp.com/i1172.photobucket.com/albums/r578/aimprof08/MetodeRegularFalsi-1.jpg)](http://s1172.photobucket.com/albums/r578/aimprof08/?action=view&current=MetodeRegularFalsi-1.jpg)

Prosedur **Metode Regular Falsi**

Menentukan interval titik awal x0 dan x1 sedemikian sehingga ![f(x_0) f(x_1) < 0](https://s0.wp.com/latex.php?latex=f%28x_0%29+f%28x_1%29+%3C+0&bg=ffffff&fg=666666&s=0). Setelah itu menghitung ![x_2 = x_1- \dfrac{f(x_1)[x_1-x_0]}{f(x_1)-f(x_0)}](https://s0.wp.com/latex.php?latex=x_2+%3D+x_1-+%5Cdfrac%7Bf%28x_1%29%5Bx_1-x_0%5D%7D%7Bf%28x_1%29-f%28x_0%29%7D&bg=ffffff&fg=666666&s=0). Kemudian periksa apakah ![f(x_0) f(x_2) < 0](https://s0.wp.com/latex.php?latex=f%28x_0%29+f%28x_2%29+%3C+0&bg=ffffff&fg=666666&s=0) atau ![f(x_1) f(x_2) < 0](https://s0.wp.com/latex.php?latex=f%28x_1%29+f%28x_2%29+%3C+0&bg=ffffff&fg=666666&s=0), jika ![f(x_0) f(x_2) < 0](https://s0.wp.com/latex.php?latex=f%28x_0%29+f%28x_2%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ![x_0 = x_0](https://s0.wp.com/latex.php?latex=x_0+%3D+x_0&bg=ffffff&fg=666666&s=0) atau ![x_2 = x_1](https://s0.wp.com/latex.php?latex=x_2+%3D+x_1&bg=ffffff&fg=666666&s=0), jika tidak maka ![x_1 = x_1](https://s0.wp.com/latex.php?latex=x_1+%3D+x_1&bg=ffffff&fg=666666&s=0) atau ![x_2 = x_0](https://s0.wp.com/latex.php?latex=x_2+%3D+x_0&bg=ffffff&fg=666666&s=0). Kemudian ulangi terus langkah-langkah tersebut sampai ketemu ‘akar’ yang paling mendekati ‘akar yang sebenarnya’ atau mempunyai error yang cukup kecil.

Secara umum, rumus untuk **Metode Regular Falsi** ini adalah sebagai berikut

![x_{n+1} = x_n -\dfrac{f(x_n)[x_n-x_{n-1}]}{f(x_n)-f(x_{n-1})}](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D+%3D+x_n+-%5Cdfrac%7Bf%28x_n%29%5Bx_n-x_%7Bn-1%7D%5D%7D%7Bf%28x_n%29-f%28x_%7Bn-1%7D%29%7D&bg=ffffff&fg=666666&s=0)

Untuk mendapatkan rumus tersebut, perhatikan gambar diatas.

syarat : ![f(x_0) f(x_1) < 0](https://s0.wp.com/latex.php?latex=f%28x_0%29+f%28x_1%29+%3C+0&bg=ffffff&fg=666666&s=0)

pandang garis *l* yang melalui ![(x_0, f(x_0))](https://s0.wp.com/latex.php?latex=%28x_0%2C+f%28x_0%29%29&bg=ffffff&fg=666666&s=0) dan ![(x_1, f(x_1))](https://s0.wp.com/latex.php?latex=%28x_1%2C+f%28x_1%29%29&bg=ffffff&fg=666666&s=0) sebagai gradien garis, sehingga diperoleh persamaan gradient sebagai berikut

![\dfrac{f(x_1)-f(x_0)}{x_1-x_0} = \dfrac{f(x_1)-y}{x_1-x_2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bf%28x_1%29-f%28x_0%29%7D%7Bx_1-x_0%7D+%3D+%5Cdfrac%7Bf%28x_1%29-y%7D%7Bx_1-x_2%7D&bg=ffffff&fg=666666&s=0)

karena ![x_2](https://s0.wp.com/latex.php?latex=x_2&bg=ffffff&fg=666666&s=0) merupakan titik potong pada sumbu-![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=666666&s=0) maka ![f(x_2)=0=y](https://s0.wp.com/latex.php?latex=f%28x_2%29%3D0%3Dy&bg=ffffff&fg=666666&s=0), sehingga diperoleh

![\dfrac{f(x_1)-f(x_0)}{x_1-x_0} = \dfrac{f(x_1)-0}{x_1-x_2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bf%28x_1%29-f%28x_0%29%7D%7Bx_1-x_0%7D+%3D+%5Cdfrac%7Bf%28x_1%29-0%7D%7Bx_1-x_2%7D&bg=ffffff&fg=666666&s=0)

![x_1-x_2 = \dfrac{f(x_1)[x_1-x_0]}{f(x_1)-f(x_0)}](https://s0.wp.com/latex.php?latex=x_1-x_2+%3D+%5Cdfrac%7Bf%28x_1%29%5Bx_1-x_0%5D%7D%7Bf%28x_1%29-f%28x_0%29%7D&bg=ffffff&fg=666666&s=0)

![x_2 = x_1- \dfrac{f(x_1)(x_1-x_0)}{f(x_1)-f(x_0)}](https://s0.wp.com/latex.php?latex=x_2+%3D+x_1-+%5Cdfrac%7Bf%28x_1%29%28x_1-x_0%29%7D%7Bf%28x_1%29-f%28x_0%29%7D&bg=ffffff&fg=666666&s=0)

atau jika ditulis secara umum menjadi

![x_{n+1} = x_n -\dfrac{f(x_n)[x_n-x_{n-1}]}{f(x_n)-f(x_{n-1})}](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D+%3D+x_n+-%5Cdfrac%7Bf%28x_n%29%5Bx_n-x_%7Bn-1%7D%5D%7D%7Bf%28x_n%29-f%28x_%7Bn-1%7D%29%7D&bg=ffffff&fg=666666&s=0)

**Contoh :**

Tentukan akar dari ![4x^3-15x2 + 17x-6 = 0](https://s0.wp.com/latex.php?latex=4x%5E3-15x2+%2B+17x-6+%3D+0&bg=ffffff&fg=666666&s=0) menggunakan **Metode Regular Falsi**sampai 9 iterasi.

**Penyelesaian :**

6![f(x) = 4x^3-15x2 + 17x-6](https://s0.wp.com/latex.php?latex=f%28x%29+%3D+4x%5E3-15x2+%2B+17x-6&bg=ffffff&fg=666666&s=0)

**iterasi 1 :**

ambil ![x_0 = -1](https://s0.wp.com/latex.php?latex=x_0+%3D+-1&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

![f(-1) = 4(-1)^3 -15(-1)^2 + 17(-1) -6 = -42](https://s0.wp.com/latex.php?latex=f%28-1%29+%3D+4%28-1%29%5E3+-15%28-1%29%5E2+%2B+17%28-1%29+-6+%3D+-42&bg=ffffff&fg=666666&s=0)

![f(3) = 4(3)^3 -15(3)^2 + 17(3) -6 = 18](https://s0.wp.com/latex.php?latex=f%283%29+%3D+4%283%29%5E3+-15%283%29%5E2+%2B+17%283%29+-6+%3D+18&bg=ffffff&fg=666666&s=0)

![x_2 = 3 -\dfrac{(18)[3-(-1)]}{18-(-42)} = 1.8](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-%28-1%29%5D%7D%7B18-%28-42%29%7D+%3D+1.8&bg=ffffff&fg=666666&s=0)

![f(1.8) = 4(1.8)^3 -15(1.8)^2 + 17(1.8) -6 = -0.672](https://s0.wp.com/latex.php?latex=f%281.8%29+%3D+4%281.8%29%5E3+-15%281.8%29%5E2+%2B+17%281.8%29+-6+%3D+-0.672&bg=ffffff&fg=666666&s=0)

![f(3) f(1.8) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.8%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.8](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D+1.8&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 2 :**

![x_2 = 3 -\dfrac{(18)[3-1.8]}{18-(-0.672)} = 1.84319](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.8%5D%7D%7B18-%28-0.672%29%7D+%3D+1.84319&bg=ffffff&fg=666666&s=0)

![f(1.84319) = 4(1.84319)^3 -15(1.84319)^2 + 17(1.84319) -6 = -0.57817](https://s0.wp.com/latex.php?latex=f%281.84319%29+%3D+4%281.84319%29%5E3+-15%281.84319%29%5E2+%2B+17%281.84319%29+-6+%3D+-0.57817&bg=ffffff&fg=666666&s=0)

![f(3) f(1.84319) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.84319%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.84319](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D+1.84319&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 3 :**

![x_2 = 3 -\dfrac{(18)[3-1.84319]}{18-(-0.57817)} = 1.87919](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.84319%5D%7D%7B18-%28-0.57817%29%7D+%3D+1.87919&bg=ffffff&fg=666666&s=0)

![f(1.87919) = 4(1.87919)^3 -15(1.87919)2 + 17(1.87919) -6 = -0.47975](https://s0.wp.com/latex.php?latex=f%281.87919%29+%3D+4%281.87919%29%5E3+-15%281.87919%292+%2B+17%281.87919%29+-6+%3D+-0.47975&bg=ffffff&fg=666666&s=0)

![f(3) f(1.87919) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.87919%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.87919](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D+1.87919&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 4 :**

![x_2 = 3 -\dfrac{(18)[3-1.84319]}{18-(-0.47975)} = 1.90829](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.84319%5D%7D%7B18-%28-0.47975%29%7D+%3D+1.90829&bg=ffffff&fg=666666&s=0)

![f(1.90829) = 4(1.90829)^3 -15(1.90829)^2 + 17(1.90829) -6 = -0.38595](https://s0.wp.com/latex.php?latex=f%281.90829%29+%3D+4%281.90829%29%5E3+-15%281.90829%29%5E2+%2B+17%281.90829%29+-6+%3D+-0.38595&bg=ffffff&fg=666666&s=0)

![f(3) f(1.90829) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.90829%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.9082](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D%C2%A01.9082&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 5 :**

![x_2 = 3 -\dfrac{(18)[3-1.90829]}{18-(-0.38595)} = 1.93120](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.90829%5D%7D%7B18-%28-0.38595%29%7D+%3D+1.93120&bg=ffffff&fg=666666&s=0)

![f(1.93120) = 4(1.93120)^3 -15(1.93120)^2 + 17(1.93120) -6 = -0.30269](https://s0.wp.com/latex.php?latex=f%281.93120%29+%3D+4%281.93120%29%5E3+-15%281.93120%29%5E2+%2B+17%281.93120%29+-6+%3D+-0.30269&bg=ffffff&fg=666666&s=0)

![f(3) f(1.93120) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.93120%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.93120](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D%C2%A01.93120&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 6 :**

![x_2 = 3 -\dfrac{(18)[3-1.93120]}{18-(-0.30269)} = 1.94888](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.93120%5D%7D%7B18-%28-0.30269%29%7D+%3D+1.94888&bg=ffffff&fg=666666&s=0)

![f(1.94888) = 4(1.94888)^3 -15(1.94888)2 + 17(1.94888) -6 = -0.23262](https://s0.wp.com/latex.php?latex=f%281.94888%29+%3D+4%281.94888%29%5E3+-15%281.94888%292+%2B+17%281.94888%29+-6+%3D+-0.23262&bg=ffffff&fg=666666&s=0)

![f(3) f(1.94888) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.94888%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.94888](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D%C2%A01.94888&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 7 :**

![x_2 = 3 -\dfrac{(18)[3-1.94888]}{18-(-0.23262)} = 1.96229](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.94888%5D%7D%7B18-%28-0.23262%29%7D+%3D+1.96229&bg=ffffff&fg=666666&s=0)

![f(1.96229) = 4(1.96229)^3 -15(1.96229)^2 + 17(1.96229) -6 = -0.17597](https://s0.wp.com/latex.php?latex=f%281.96229%29+%3D+4%281.96229%29%5E3+-15%281.96229%29%5E2+%2B+17%281.96229%29+-6+%3D+-0.17597&bg=ffffff&fg=666666&s=0)

![f(3) f(1.96229) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.96229%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.96229](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D%C2%A01.96229&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 8 :**

![x_2 = 3 -\frac{(18)[3-1.96229]}{18-(-0.17597)} = 1.97234](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cfrac%7B%2818%29%5B3-1.96229%5D%7D%7B18-%28-0.17597%29%7D+%3D+1.97234&bg=ffffff&fg=666666&s=0)

![f(1.97234) = 4(1.97234)^3 -15(1.97234)2 + 17(1.97234) -6 = -0.13152](https://s0.wp.com/latex.php?latex=f%281.97234%29+%3D+4%281.97234%29%5E3+-15%281.97234%292+%2B+17%281.97234%29+-6+%3D+-0.13152&bg=ffffff&fg=666666&s=0)

![f(3) f(1.97234) < 0](https://s0.wp.com/latex.php?latex=f%283%29+f%281.97234%29+%3C+0&bg=ffffff&fg=666666&s=0) maka ambil ![x_0 = x_2 = 1.97234](https://s0.wp.com/latex.php?latex=x_0+%3D+x_2+%3D%C2%A01.97234&bg=ffffff&fg=666666&s=0) dan ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0)

**iterasi 9 :**

![x_2 = 3 -\dfrac{(18)[3-1.97234]}{18-(-0.13152)} = 1.97979](https://s0.wp.com/latex.php?latex=x_2+%3D+3+-%5Cdfrac%7B%2818%29%5B3-1.97234%5D%7D%7B18-%28-0.13152%29%7D+%3D+1.97979&bg=ffffff&fg=666666&s=0)

| ![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=666666&s=0) | ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=666666&s=0) | ![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0) | ![x_2](https://s0.wp.com/latex.php?latex=x_2&bg=ffffff&fg=666666&s=0) | ![f(x_0)](https://s0.wp.com/latex.php?latex=f%28x_0%29&bg=ffffff&fg=666666&s=0) | ![f(x_1)](https://s0.wp.com/latex.php?latex=f%28x_1%29&bg=ffffff&fg=666666&s=0) | ![f(x_2)](https://s0.wp.com/latex.php?latex=f%28x_2%29&bg=ffffff&fg=666666&s=0) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 123456789                                                    | -11.81.843191.879191.908291.931201.948881.962291.97234       | 333333333                                                    | 1.81.843191.879191.908291.931201.948881.962291.972341.97979  | -42-0.672-0.57817-0.47975-0.38595-0.30269-0.23262-0.17597-0.13152 | 181818181818181818                                           | -0.672-0.57817-0.47975-0.38595-0.30269-0.23262-0.17597-0.13152-0.09741 |

Jadi akar dari persamaan ![4x^3-15x2 + 17x-6 = 0](https://s0.wp.com/latex.php?latex=4x%5E3-15x2+%2B+17x-6+%3D+0&bg=ffffff&fg=666666&s=0) menggunakan **Metode Regular Falsi** adalah ![1.97979](https://s0.wp.com/latex.php?latex=1.97979&bg=ffffff&fg=666666&s=0)

**Program Kode**



```
# Regula-Falsi 
def  Regfal ( a , b , n ): 
    e  =  0,001 
    fa  =  a ** 2 - 5 * a + 6 
    fb  =  b ** 2 - 5 * b + 6 
    jika  fa * fb < 0 : 
        n + = 1 
        cetak ( "iterasi kem" + str ( n )) 
        x  =  (( a* abs ( fb )) + ( b * abs ( fa ))) / ( abs ( fa ) + abs ( fb )) 
        fx  =  x ** 2 - 5 * x + 6 
        jika  fa * fx < 0 : 
            b  =  x 
        lain : 
            a  =  x 
        jika  abs ( a - b ) < e: 
            cetak ( x ) 
        lain : 
            Regfal ( a , b , n ) 
    lain : 
        jika  fa < fb : 
            a - = 0,1 
        lainnya : 
            b + = 0,1 
        Regfal ( a , b , n )

a  =  float ( input ( "Masukkan interval a:" )) 
b  =  float ( input ( "Masukkan interval b:" )) 
Regfal ( a , b , 0 )
```

**Keluaran**



```python
Masukkan interval a: 1
Masukkan interval b: 2.1
iterasi ke-1
iterasi ke-2
iterasi ke-3
iterasi ke-4
iterasi ke-5
iterasi ke-6
iterasi ke-7
iterasi ke-8
iterasi ke-9
iterasi ke-10
iterasi ke-11
iterasi ke-12
iterasi ke-13
iterasi ke-14
iterasi ke-15
iterasi ke-16
iterasi ke-17
iterasi ke-18
iterasi ke-19
iterasi ke-20
iterasi ke-21
iterasi ke-22
iterasi ke-23
iterasi ke-24
iterasi ke-25
iterasi ke-26
iterasi ke-27
iterasi ke-28
iterasi ke-29
iterasi ke-30
iterasi ke-31
iterasi ke-32
iterasi ke-33
iterasi ke-34
iterasi ke-35
iterasi ke-36
iterasi ke-37
iterasi ke-38
iterasi ke-39
iterasi ke-40
iterasi ke-41
iterasi ke-42
iterasi ke-43
iterasi ke-44
iterasi ke-45
iterasi ke-46
iterasi ke-47
2.0000000000000004
```

# Metode Newton-Raphson (Newton-Raphson Method)



**Metode Newton-Raphson** adalah metode pencarian akar suatu fungsi ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=666666&s=0) dengan pendekatan satu titik, dimana fungsi ![f(x](https://s0.wp.com/latex.php?latex=f%28x&bg=ffffff&fg=666666&s=0) mempunyai turunan. Metode ini dianggap lebih mudah dari [**Metode Bagi-Dua**](https://aimprof08.wordpress.com/2012/08/30/metode-bagi-dua-bisection-method/) (Bisection Method) karena metode ini menggunakan pendekatan satu titik sebagai titik awal. Semakin dekat titik awal yang kita pilih dengan akar sebenarnya, maka semakin cepat konvergen ke akarnya.



[![Photobucket](https://i2.wp.com/i1172.photobucket.com/albums/r578/aimprof08/MetodeNewton-Rapshon.jpg)](http://s1172.photobucket.com/albums/r578/aimprof08/?action=view&current=MetodeNewton-Rapshon.jpg)

Prosedur Metode Newton :



menentukan ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=666666&s=0) sebagai titik awal, kemudian menarik garis lurus (misal garis*![l](https://s0.wp.com/latex.php?latex=l&bg=ffffff&fg=666666&s=0)*) yang menyinggung titik ![f(x_0)](https://s0.wp.com/latex.php?latex=f%28x_0%29&bg=ffffff&fg=666666&s=0). Hal ini berakibat garis ![l](https://s0.wp.com/latex.php?latex=l&bg=ffffff&fg=666666&s=0) memotong sumbu-![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=666666&s=0)di titik ![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0). Setelah itu diulangi langkah sebelumnya tapi sekarang ![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0)dianggap sebagai titik awalnya. Dari mengulang langkah-langkah sebelumnya akan mendapatkan ![x_2, x_3, \ldots, x_n](https://s0.wp.com/latex.php?latex=x_2%2C+x_3%2C+%5Cldots%2C+x_n&bg=ffffff&fg=666666&s=0) dengan ![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=666666&s=0) yang diperoleh adalah bilangan riil yang merupakan akar atau mendekati akar yang sebenarnya.



Perhatikan gambar diatas untuk menurunkan rumus **Metode Newton-Raphson**

persamaan garis ![l : y -y_0 = m(x- x_0)](https://s0.wp.com/latex.php?latex=l+%3A+y+-y_0+%3D+m%28x-+x_0%29&bg=ffffff&fg=666666&s=0)

![y -f(x_0) = f'(x_0)(x -x_0)](https://s0.wp.com/latex.php?latex=y+-f%28x_0%29+%3D+f%27%28x_0%29%28x+-x_0%29&bg=ffffff&fg=666666&s=0)

![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0) adalah perpotongan garis ![l](https://s0.wp.com/latex.php?latex=l&bg=ffffff&fg=666666&s=0) dengan sumbu-![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=666666&s=0)

![0-f(x_0) = f'(x_0)(x -x_0)](https://s0.wp.com/latex.php?latex=0-f%28x_0%29+%3D+f%27%28x_0%29%28x+-x_0%29&bg=ffffff&fg=666666&s=0)

![y = 0](https://s0.wp.com/latex.php?latex=y+%3D+0&bg=ffffff&fg=666666&s=0) dan ![x = x_1](https://s0.wp.com/latex.php?latex=x+%3D+x_1&bg=ffffff&fg=666666&s=0) maka koordinat titik ![(x_1, 0)](https://s0.wp.com/latex.php?latex=%28x_1%2C+0%29&bg=ffffff&fg=666666&s=0)

![-\dfrac{f(x_{0})}{f'(x_{0})} = (x_1-x_0)](https://s0.wp.com/latex.php?latex=-%5Cdfrac%7Bf%28x_%7B0%7D%29%7D%7Bf%27%28x_%7B0%7D%29%7D+%3D+%28x_1-x_0%29&bg=ffffff&fg=666666&s=0)

![x_1 = x_0- \dfrac{f(x_0)}{f'(x_0)}](https://s0.wp.com/latex.php?latex=x_1+%3D+x_0-+%5Cdfrac%7Bf%28x_0%29%7D%7Bf%27%28x_0%29%7D&bg=ffffff&fg=666666&s=0)

![x_2 = x_1- \dfrac{f(x_1)}{f'(x_1)}](https://s0.wp.com/latex.php?latex=x_2+%3D+x_1-+%5Cdfrac%7Bf%28x_1%29%7D%7Bf%27%28x_1%29%7D&bg=ffffff&fg=666666&s=0)



.



.



.



![x_n = x_{n-1}- \dfrac{f(x_{n-1})}{f'(x_{n-1})}](https://s0.wp.com/latex.php?latex=x_n+%3D+x_%7Bn-1%7D-+%5Cdfrac%7Bf%28x_%7Bn-1%7D%29%7D%7Bf%27%28x_%7Bn-1%7D%29%7D&bg=ffffff&fg=666666&s=0) untuk n = 1, 2, 3, …

**Contoh :**

Tentukan akar dari persamaan ![4x^3-15x^2 + 17x-6 = 0](https://s0.wp.com/latex.php?latex=4x%5E3-15x%5E2+%2B+17x-6+%3D+0&bg=ffffff&fg=666666&s=0) menggunakan Metode Newton-Raphson.

**Penyelesaian :**

![f(x) = 4x^3-15x^2 + 17x-6](https://s0.wp.com/latex.php?latex=f%28x%29+%3D+4x%5E3-15x%5E2+%2B+17x-6&bg=ffffff&fg=666666&s=0)

![f'(x) = 12x^2-30x + 17](https://s0.wp.com/latex.php?latex=f%27%28x%29+%3D+12x%5E2-30x+%2B+17&bg=ffffff&fg=666666&s=0)

iterasi 1 :

ambil titik awal x0 = 3

f(3) = 4(3)3 – 15(3)2 + 17(3) – 6 = 18

f’(3) = 12(3)2 – 30(3) + 17 = 35

x1 = 3 – ![\frac{18}{35} ](https://s0.wp.com/latex.php?latex=%5Cfrac%7B18%7D%7B35%7D+&bg=ffffff&fg=666666&s=2) = 2.48571

iterasi 2 :

f(2.48571) = 4(2.48571)3 – 15(2.48571)2 + 17(2.48571) – 6 = 5.01019

f’(2.48571) = 12(2.48571)2 – 30(2.48571) + 17 = 16.57388

x2 = 2.48571 – ![\frac{5.01019}{16.57388} ](https://s0.wp.com/latex.php?latex=%5Cfrac%7B5.01019%7D%7B16.57388%7D+&bg=ffffff&fg=666666&s=2) = 2.18342

iterasi 3 :

f(2.18342) = 4(2.18342)3 – 15(2.18342)2 + 17(2.18342) – 6 = 1.24457

f’(2.18342) = 12(2.18342)2 – 30(2.18342) + 17 = 8.70527

x3 = 2.18342 – ![\frac{1.24457}{8.70527} ](https://s0.wp.com/latex.php?latex=%5Cfrac%7B1.24457%7D%7B8.70527%7D+&bg=ffffff&fg=666666&s=2) = 2.04045

iterasi 4 :

f(2.04045) = 4(2.04045)3 – 15(2.04045)2 + 17(2.04045) – 6 = 0.21726

f’(2.04045) = 12(2.04045)2 – 30(2.04045) + 17 = 5.74778

x4 = 2.04045 – ![\frac{0.21726}{5.74778} ](https://s0.wp.com/latex.php?latex=%5Cfrac%7B0.21726%7D%7B5.74778%7D+&bg=ffffff&fg=666666&s=2) = 2.00265

iterasi 5 :

f(3) = 4(2.00265)3 – 15(2.00265)2 + 17(2.00265) – 6 = 0.01334

f’(2.00265) = 12(2.00265)2 – 30(2.00265) + 17 = 5.04787

x5 = 2.00265 – ![\frac{0.01334}{5.04787} ](https://s0.wp.com/latex.php?latex=%5Cfrac%7B0.01334%7D%7B5.04787%7D+&bg=ffffff&fg=666666&s=2) = 2.00001

iterasi 6 :

f(2.00001) = 4(2.00001)3 – 15(2.00001)2 + 17(2.00001) – 6 = 0.00006

f’(2.00001) = 12(2.00001)2 – 30(2.00001) + 17 = 5.00023

x6 = 2.00001 – ![\frac{0.00006}{5.00023} ](https://s0.wp.com/latex.php?latex=%5Cfrac%7B0.00006%7D%7B5.00023%7D+&bg=ffffff&fg=666666&s=2) = 2.00000

iterasi 7 :

f(2) = 4(2)3 – 15(2)2 + 17(2) – 6 = 0

jika disajikan dalam tabel, maka seperti tabel dibawah ini.



| ![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=666666&s=0) | ![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=666666&s=0) | ![f(x_n)](https://s0.wp.com/latex.php?latex=f%28x_n%29&bg=ffffff&fg=666666&s=0) | ![f'(x_n)](https://s0.wp.com/latex.php?latex=f%27%28x_n%29&bg=ffffff&fg=666666&s=0) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 0123456                                                      | 32.485712.183422.040452.002652.000012.00000                  | 185.010191.244570.217260.013340.000060.00000                 | 3516.573888.705275.747785.047875.000235.00000                |

karena pada iterasi ketujuh ![f(x_6) = 0](https://s0.wp.com/latex.php?latex=f%28x_6%29+%3D+0&bg=ffffff&fg=666666&s=0) maka akar dari persamaan tersebut adalah ![x = 2](https://s0.wp.com/latex.php?latex=x+%3D+2&bg=ffffff&fg=666666&s=0).

**Program**



```python
# Newton-Raphson 
x  =  float ( input ( "Masukkan nilai awal x:" )) 
n  =  0 
e  =  0,001 
sedangkan  n > = 0 : 
    print ( "iterasi saat X" + str ( n )) 
    fx  =  x ** 2 - 5 * x + 6 
    faks  =  2 * x - 5 
    x1  =  x  -  ( fx / faks )
    jika  abs ( x1 - x ) < e  atau  n > = 100 : 
        print ( "Jumlah iterasi:" , n + 1 ) 
        print ( x ) 
        memecah 
    lain : 
        x = x1 
    n + = 1
```

**Keluaran**



```python
Masukkan nilai awal x: 2.4
iterasi saat X0
iterasi saat X1
iterasi saat X2
iterasi saat X3
iterasi saat X4
iterasi saat X5
Jumlah iterasi: 6
1.9999976821746035
```

# Metode Secant (Secant Method)

Pada **Metode Newton-Raphson** memerlukan syarat wajib yaitu fungsi ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=666666&s=0) harus memiliki turunan ![f'(x)](https://s0.wp.com/latex.php?latex=f%27%28x%29&bg=ffffff&fg=666666&s=0). Sehingga syarat wajib ini dianggap sulit karena tidak semua fungsi bisa dengan mudah mencari turunannya. Oleh karena itu muncul ide dari yaitu mencari persamaan yang ekivalen dengan rumus turunan fungsi. Ide ini lebih dikenal dengan nama **Metode Secant**. Ide dari metode ini yaitu menggunakan gradien garis yang melalui titik ![(x_0, f(x_0))](https://s0.wp.com/latex.php?latex=%28x_0%2C+f%28x_0%29%29&bg=ffffff&fg=666666&s=0) dan ![(x_1, f(x_1))](https://s0.wp.com/latex.php?latex=%28x_1%2C+f%28x_1%29%29&bg=ffffff&fg=666666&s=0). Perhatikan gambar dibawah ini.



[![Photobucket](https://i2.wp.com/i1172.photobucket.com/albums/r578/aimprof08/SecantMethod.jpg)](http://s1172.photobucket.com/albums/r578/aimprof08/?action=view&current=SecantMethod.jpg)

Persamaan garis *l* adalah

![\dfrac{x-x_1}{x_0-x_1} = \dfrac{y-f(x_1)}{f(x_0)-f(x_1)}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bx-x_1%7D%7Bx_0-x_1%7D+%3D+%5Cdfrac%7By-f%28x_1%29%7D%7Bf%28x_0%29-f%28x_1%29%7D&bg=ffffff&fg=666666&s=0)

Karena ![x = x_2](https://s0.wp.com/latex.php?latex=x+%3D+x_2&bg=ffffff&fg=666666&s=0) maka ![y = 0](https://s0.wp.com/latex.php?latex=y+%3D+0&bg=ffffff&fg=666666&s=0), sehingga diperoleh

![\dfrac{x_2-x_1}{x_0-x_1} = \dfrac{0-f(x_1)}{f(x_0)-f(x_1)}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bx_2-x_1%7D%7Bx_0-x_1%7D+%3D+%5Cdfrac%7B0-f%28x_1%29%7D%7Bf%28x_0%29-f%28x_1%29%7D&bg=ffffff&fg=666666&s=0)

![x_2-x_1 = -\dfrac{f(x_1)[x_0-x_1]}{f(x_0)-f(x_1)}](https://s0.wp.com/latex.php?latex=x_2-x_1+%3D+-%5Cdfrac%7Bf%28x_1%29%5Bx_0-x_1%5D%7D%7Bf%28x_0%29-f%28x_1%29%7D&bg=ffffff&fg=666666&s=0)

![x_2 = x_1-\dfrac{f(x_1)[x_0-x_1]}{f(x_0)-f(x_1)}](https://s0.wp.com/latex.php?latex=x_2+%3D+x_1-%5Cdfrac%7Bf%28x_1%29%5Bx_0-x_1%5D%7D%7Bf%28x_0%29-f%28x_1%29%7D&bg=ffffff&fg=666666&s=0)

![= x_1-\dfrac{f(x_1)[x_0-x_1]}{f(x_1)-f(x_0)}](https://s0.wp.com/latex.php?latex=%3D+x_1-%5Cdfrac%7Bf%28x_1%29%5Bx_0-x_1%5D%7D%7Bf%28x_1%29-f%28x_0%29%7D&bg=ffffff&fg=666666&s=0)

secara umum rumus Metode Secant ini ditulis

![x_{n+1} = x_n -\dfrac{f(x_n)[x_n-x_{n-1}]}{f(x_n)-f(x_{n-1})}](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D+%3D+x_n+-%5Cdfrac%7Bf%28x_n%29%5Bx_n-x_%7Bn-1%7D%5D%7D%7Bf%28x_n%29-f%28x_%7Bn-1%7D%29%7D&bg=ffffff&fg=666666&s=0)

Prosedur Metode Secant :

Ambil dua titik awal, misal ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=666666&s=0) dan ![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0). Ingat bahwa pengambilan titik awal tidak disyaratkan alias pengambilan secara sebarang. Setelah itu hitung ![x_2](https://s0.wp.com/latex.php?latex=x_2&bg=ffffff&fg=666666&s=0)menggunakan rumus diatas. Kemudian pada iterasi selanjutnya ambil ![x_1](https://s0.wp.com/latex.php?latex=x_1&bg=ffffff&fg=666666&s=0) dan ![x_2](https://s0.wp.com/latex.php?latex=x_2&bg=ffffff&fg=666666&s=0)sebagai titik awal dan hitung ![x_3](https://s0.wp.com/latex.php?latex=x_3&bg=ffffff&fg=666666&s=0). Kemudian ambil ![x_2](https://s0.wp.com/latex.php?latex=x_2&bg=ffffff&fg=666666&s=0) dan ![x_3](https://s0.wp.com/latex.php?latex=x_3&bg=ffffff&fg=666666&s=0) sebagai titik awal dan hitung ![x_4](https://s0.wp.com/latex.php?latex=x_4&bg=ffffff&fg=666666&s=0). Begitu seterusnya sampai iterasi yang diingankan atau sampai mencapai error yang cukup kecil.

**Contoh :
**

Tentukan salah satu akar dari ![4x^3-15x2 + 17x -6 = 0](https://s0.wp.com/latex.php?latex=4x%5E3-15x2+%2B+17x+-6+%3D+0&bg=ffffff&fg=666666&s=0) menggunakan **Metode Secant** sampai 9 iterasi.

**Penyelesaian :
**

![f(x) = 4x^3-15x2 + 17x -6](https://s0.wp.com/latex.php?latex=f%28x%29+%3D+4x%5E3-15x2+%2B+17x+-6&bg=ffffff&fg=666666&s=0)

iterasi 1 :

ambil ![x_0 = -1](https://s0.wp.com/latex.php?latex=x_0+%3D+-1&bg=ffffff&fg=666666&s=0) dan ![x_0 = 3](https://s0.wp.com/latex.php?latex=x_0+%3D+3&bg=ffffff&fg=666666&s=0) (ngambil titik awal ini sebarang saja, tidak ada syarat apapun)



![\begin{aligned} f(-1) &= 4(-1)^3 -15(-1)^2 + 17(-1) -6 = -42\\ f(3) &= 4(3)^3 -15(3)^2 + 17(3) -6 = 18\\ x_2 &= 3 -\dfrac{(18)[3-(-1)]}{18-(-42)} = 1.8 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%28-1%29+%26%3D+4%28-1%29%5E3+-15%28-1%29%5E2+%2B+17%28-1%29+-6+%3D+-42%5C%5C+f%283%29+%26%3D+4%283%29%5E3+-15%283%29%5E2+%2B+17%283%29+-6+%3D+18%5C%5C+x_2+%26%3D+3+-%5Cdfrac%7B%2818%29%5B3-%28-1%29%5D%7D%7B18-%28-42%29%7D+%3D+1.8+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 2 :

ambil ![x_1 = 3](https://s0.wp.com/latex.php?latex=x_1+%3D+3&bg=ffffff&fg=666666&s=0) dan ![x_2 = 1.8](https://s0.wp.com/latex.php?latex=x_2+%3D+1.8&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(1.8) &= 4(1.8)^3 -15(1.8)2 + 17(1.8) -6 = -0.672\\ x_3 &= 1.8 -\dfrac{(-0.672)[1.8-(3)]}{-0.672-18} = 1.84319 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%281.8%29+%26%3D+4%281.8%29%5E3+-15%281.8%292+%2B+17%281.8%29+-6+%3D+-0.672%5C%5C+x_3+%26%3D+1.8+-%5Cdfrac%7B%28-0.672%29%5B1.8-%283%29%5D%7D%7B-0.672-18%7D+%3D+1.84319+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 3 :

ambil ![x_2 = 1.8](https://s0.wp.com/latex.php?latex=x_2+%3D%C2%A01.8&bg=ffffff&fg=666666&s=0) dan ![x_3 = 1.84319](https://s0.wp.com/latex.php?latex=x_3+%3D%C2%A01.84319&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(1.84319) &= 4(1.84319)^3 -15(1.84319)^2 + 17(1.84319) -6 = -0.57817\\ x_4 &= (1.84319) -\dfrac{(-0.57817)[1.84319-1.8]}{-0.57817-(0.672)} = 2.10932 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%281.84319%29+%26%3D+4%281.84319%29%5E3+-15%281.84319%29%5E2+%2B+17%281.84319%29+-6+%3D+-0.57817%5C%5C+x_4+%26%3D+%281.84319%29+-%5Cdfrac%7B%28-0.57817%29%5B1.84319-1.8%5D%7D%7B-0.57817-%280.672%29%7D+%3D+2.10932+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 4 :

ambil ![x_3 = 1.84319](https://s0.wp.com/latex.php?latex=x_3+%3D+1.84319&bg=ffffff&fg=666666&s=0) dan ![x_4 = 2.10932](https://s0.wp.com/latex.php?latex=x_4+%3D%C2%A02.10932&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(2.10932) &= 4(2.10932)^3 -15(2.10932)^2 + 17(2.10932) -6 = 0.65939\\ x_5 &= 2.10932 -\dfrac{(0.65939)[2.10932-1.84319]}{0.65939-(-0.57817)} = 1.96752 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%282.10932%29+%26%3D+4%282.10932%29%5E3+-15%282.10932%29%5E2+%2B+17%282.10932%29+-6+%3D+0.65939%5C%5C+x_5+%26%3D+2.10932+-%5Cdfrac%7B%280.65939%29%5B2.10932-1.84319%5D%7D%7B0.65939-%28-0.57817%29%7D+%3D+1.96752+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 5 :

ambil ![x_4 = 2.10932](https://s0.wp.com/latex.php?latex=x_4+%3D%C2%A02.10932&bg=ffffff&fg=666666&s=0) dan ![x_5 = 1.96752](https://s0.wp.com/latex.php?latex=x_5+%3D%C2%A01.96752&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(1.96752) &= 4(1.96752)^3 -15(1.96752)2 + 17(1.96752) -6 = -0.15303\\ x_6 &= (1.96752) -\dfrac{(-0.15303)[1.96752-2.10932]}{-0.15303-0.65939)} = 1.99423 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%281.96752%29+%26%3D+4%281.96752%29%5E3+-15%281.96752%292+%2B+17%281.96752%29+-6+%3D+-0.15303%5C%5C+x_6+%26%3D+%281.96752%29+-%5Cdfrac%7B%28-0.15303%29%5B1.96752-2.10932%5D%7D%7B-0.15303-0.65939%29%7D+%3D+1.99423+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 6 :

ambil ![x_5 = 1.96752](https://s0.wp.com/latex.php?latex=x_5+%3D%C2%A01.96752&bg=ffffff&fg=666666&s=0) dan ![x_6 = 1.99423](https://s0.wp.com/latex.php?latex=x_6+%3D%C2%A01.99423&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(1.99423) &= 4(1.99423)^3 -15(1.99423)^2 + 17(1.99423) -6 = -0.02854\\ x_7 &= (1.99423) -\dfrac{(-0.02854)[1.99423-1.96752]}{-0.02854-(-0.15303)} = 2.00036 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%281.99423%29+%26%3D+4%281.99423%29%5E3+-15%281.99423%29%5E2+%2B+17%281.99423%29+-6+%3D+-0.02854%5C%5C+x_7+%26%3D+%281.99423%29+-%5Cdfrac%7B%28-0.02854%29%5B1.99423-1.96752%5D%7D%7B-0.02854-%28-0.15303%29%7D+%3D+2.00036+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 7 :

ambil ![x_6 = 1.99423](https://s0.wp.com/latex.php?latex=x_6+%3D%C2%A01.99423&bg=ffffff&fg=666666&s=0) dan ![x_7 = 2.00036](https://s0.wp.com/latex.php?latex=x_7+%3D%C2%A02.00036&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(2.00036) &= 4(2.00036)^3 -15(2.00036)2 + 17(2.00036) -6 = 0.00178\\ x_8 &= 2.00036 -\dfrac{(0.00178)[2.00036-1.99423]}{0.00178-(-0.02854)} = 2.00000 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%282.00036%29+%26%3D+4%282.00036%29%5E3+-15%282.00036%292+%2B+17%282.00036%29+-6+%3D+0.00178%5C%5C+x_8+%26%3D+2.00036+-%5Cdfrac%7B%280.00178%29%5B2.00036-1.99423%5D%7D%7B0.00178-%28-0.02854%29%7D+%3D+2.00000+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 8 :

ambil ![x_7 = 2.00036](https://s0.wp.com/latex.php?latex=x_7+%3D%C2%A02.00036&bg=ffffff&fg=666666&s=0) dan ![x_8 = 1.999996](https://s0.wp.com/latex.php?latex=x_8+%3D%C2%A01.999996&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(1.999996) &= 4(1.999996)^3 -15(1.999996)^2 + 17(1.999996) -6 = -0.0002\\ x_9 &= (1.999996) -\dfrac{(-0.0002)[1.999996-2.00036]}{-0.0002-0.00178} = 2.0000 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%281.999996%29+%26%3D+4%281.999996%29%5E3+-15%281.999996%29%5E2+%2B+17%281.999996%29+-6+%3D+-0.0002%5C%5C+x_9+%26%3D+%281.999996%29+-%5Cdfrac%7B%28-0.0002%29%5B1.999996-2.00036%5D%7D%7B-0.0002-0.00178%7D+%3D+2.0000+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)

iterasi 9 :

ambil ![x_8 = 1.999996](https://s0.wp.com/latex.php?latex=x_8+%3D%C2%A01.999996&bg=ffffff&fg=666666&s=0) dan ![x_9 = 2.00000](https://s0.wp.com/latex.php?latex=x_9+%3D%C2%A02.00000&bg=ffffff&fg=666666&s=0)

![\begin{aligned} f(2.00000) &= 4(2.00000)^3 -15(2.00000)^2 + 17(2.00000) -6 = 0.00000\\ x_{10} &= (2.00000) -\dfrac{(0.00000)[2.00000-1.999996]}{0.00000-(-0.00002)} = 0.00000 \end{aligned}](https://s0.wp.com/latex.php?latex=%5Cbegin%7Baligned%7D+f%282.00000%29+%26%3D+4%282.00000%29%5E3+-15%282.00000%29%5E2+%2B+17%282.00000%29+-6+%3D+0.00000%5C%5C+x_%7B10%7D+%26%3D+%282.00000%29+-%5Cdfrac%7B%280.00000%29%5B2.00000-1.999996%5D%7D%7B0.00000-%28-0.00002%29%7D+%3D+0.00000+%5Cend%7Baligned%7D&bg=ffffff&fg=666666&s=0)



| ![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=666666&s=0) | ![x_{n-1}](https://s0.wp.com/latex.php?latex=x_%7Bn-1%7D&bg=ffffff&fg=666666&s=0) | ![x_{n}](https://s0.wp.com/latex.php?latex=x_%7Bn%7D&bg=ffffff&fg=666666&s=0) | ![x_{n+1}](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D&bg=ffffff&fg=666666&s=0) | ![f(x_{n-1})](https://s0.wp.com/latex.php?latex=f%28x_%7Bn-1%7D%29&bg=ffffff&fg=666666&s=0) | ![f(x_{n})](https://s0.wp.com/latex.php?latex=f%28x_%7Bn%7D%29&bg=ffffff&fg=666666&s=0) | ![f(x_{n+1})](https://s0.wp.com/latex.php?latex=f%28x_%7Bn%2B1%7D%29&bg=ffffff&fg=666666&s=0) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 123456789                                                    | -131.81.843192.109321.967521.994232.000362.00000             | 31.81.843192.109321.967521.994232.000362.000002.00000        | 1.81.843192.109321.967521.994232.000362.000002.000002.00000  | -4218-0.672-0.578170.65939-0.15303-0.028540.00178-0.00002    | 18-0.672-0.578170.65939-0.15303-0.028540.00178-0.000020.00000 | -0.672-0.578170.65939-0.15303-0.028540.00178-0.000020.000000.00000 |

Jadi salah satu akar dari ![4x^3-15x2 + 17x -6 = 0](https://s0.wp.com/latex.php?latex=4x%5E3-15x2+%2B+17x+-6+%3D+0&bg=ffffff&fg=666666&s=0) adalah 2

**Program**



```python
#Secant 
def  garis potong ( a , b , n ): 
    e  =  0,001 
    fa  =  a ** 2 - 5 * a + * x + 6 n + = 1 print ( "iterasi ke-" + str ( n )) jika abs ( a - b ) 6 
    fb  =  b ** 2 - 5 * b + 6 
    x  =  a - (( b - a ) / ( fb - fa )) * fa 
    fx  =  x ** 2 - 5
    
    
      < e : 
        print ( "Jumlah iterasi:" , n ) 
        cetak ( x ) 
    lain-lain : 
        a = b 
        b = x 
        Garis potong ( a , b , n ) 
a  =  float ( input( "Masukkan nilai a:" )) 
b  =  float ( input ( "Masukkan nilai b:" )) 
n  =  0 
Garis potong ( a , b , 0 )
```

**Keluaran**



```python
Masukkan nilai a: 1
Masukkan nilai b: 1.5
iterasi ke-1
iterasi ke-2
iterasi ke-3
iterasi ke-4
iterasi ke-5
iterasi ke-6
Jumlah iterasi: 6
1.9999999975499005
```