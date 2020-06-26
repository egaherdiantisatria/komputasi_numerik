### Apa sih **Nilai Error** ituu ??

Secara umum terdapat dua sumber utama penyebab terjadinya error dalam perhitungan numerik, yaitu:

1. Error pembulatan ( round-off error )

Perhitungan dengan metode numerik hampir selalu menggunakan bilangan riil.Masalah timbul apabila komputasi numerik dikerjakan oleh mesin (dalam hal ini dengan menggunakan komputer) karena semua bilangan riil tidak dapat disajikan secara tepat di dalam komputer. Keterbatasan komputer dalam menyajikan bilangan riil menghasilkan error yang disebut error pembulatan.

Sebagai contoh 1/6 = 0.166666666… tidak dapat dinyatakan secara tepat oleh komputer karena digit 6 panjangnya tidak terbatas. Komputer hanya mampu merepresentasikan sejumlah digit (atau bit dalam sistem biner) saja. Bilangan riil yang panjangnya melebihi jumlah digit (bit) yang dapat direpresentasikan oleh komputer dibulatkan ke bilangan terdekat. Misalnya sebuah komputer hanya dapat merepresentasikan bilangan riil dalam 6 digit angka berarti, maka representasi bilangan 1/6 = 0.1666666666… di dalam komputer 6-digit tersebut adalah 0.166667. Galat pembulatannya adalah 1/6 – 0.166667 = -0.000000333.

Contoh dalam sistem biner misalnya 1/10 = 0.000110011001100110011 00110011…2 direpresentasikan di dalam komputer dalam jumlah bit yang terbatas. Kebanyakan komputer digital mempunyai dua buah cara penyajian bilangan riil, yaitu bilangan titik-tetap (fixed point) dan bilangan titik-kambang (floatingpoint). Dalam format bilangan titik -tetap setiap bilangan disajikan dengan jumlah tempat desimal yang tetap, misalnya 62.358, 0.013, 1.000. Sedangkan dalam format bilangan titik-kambang setiap bilangan disajikan dengan jumlah digit berarti yang sudah tetap, misalnya 0.6238 103 0.1714 ^10-13 atau ditulis juga 0.6238E+03 0.1714E-13. Digit-digit berarti di dalam format bilangan titik-kambang disebut juga angka bena (significant figure).

2. Galat Pemotongan ( truncation error )

Galat pemotongan adalah galat yang ditimbulkan oleh pembatasan jumlah komputasi yang digunakan pada proses metode numerik. Banyak metode dalam metode numerik yang penurunan rumusnya menggunakan proses iterasi yang jumlahnya tak terhingga, sehingga untuk membatasi proses penghitungan, jumlah iterasi dibatasi sampai langkah ke n. Hasil penghitungan sampai langkah ke n akan menjadi hasil hampiran dan nilai penghitungan langkah n keatas akan menjadi galat pemotongan. dalam hal ini galat pemotongan kan menjadi sangat kecil sekali jika nilai n di perbesar. Konsekuensinya tentu saja jumlah proses penghitungannya akan semakin banyak.

#### Contoh Kasus :

1. Diketahui:

y = x2 + 5x + 6

x=3

h=0.3

h=0.2

h=0.1

Ditanya : Et, Ea, εt, εa  ?

   Jawab :

- Saat **h=0,3**

– **Approximate Value (Va)**

![Capture](https://d4anm2017a.files.wordpress.com/2017/09/capture.png?w=210&h=49)

![1](https://d4anm2017a.files.wordpress.com/2017/09/1.png?w=212&h=54)

![15](https://d4anm2017a.files.wordpress.com/2017/09/15.png?w=375&h=69)![17](https://d4anm2017a.files.wordpress.com/2017/09/17.png?w=236&h=68)![18](https://d4anm2017a.files.wordpress.com/2017/09/18.png?w=181&h=82)![19](https://d4anm2017a.files.wordpress.com/2017/09/19.png?w=147&h=65)

Jadi Va yang didapatkan adalah **11,3**

– **True Value (Vt)**

![7](https://d4anm2017a.files.wordpress.com/2017/09/7.png?w=188&h=40)
![8](https://d4anm2017a.files.wordpress.com/2017/09/8.png?w=200&h=59)![9](https://d4anm2017a.files.wordpress.com/2017/09/9.png?w=176&h=53)![10](https://d4anm2017a.files.wordpress.com/2017/09/10.png?w=133&h=56)

Jadi Vt yang didapatkan adalah **11**

 – **True Error (Et)**

![12](https://d4anm2017a.files.wordpress.com/2017/09/12.png?w=164&h=50)

![13](https://d4anm2017a.files.wordpress.com/2017/09/13.png?w=183&h=49)

![14.PNG](https://d4anm2017a.files.wordpress.com/2017/09/14.png?w=109&h=37)

Jadi Et yang didapat adalah **-0,3**

– **Relative True Error (εt )**  

![11](https://d4anm2017a.files.wordpress.com/2017/09/111.png?w=269&h=71)

Jadi **εt** yang didapatkan adalah **-0,027**

- Saat **h = 0,2**

**– Approximate Value (Va)**

![VA 1](https://d4anm2017a.files.wordpress.com/2017/09/va-1.jpg?w=264&h=72)

![VA 2](https://d4anm2017a.files.wordpress.com/2017/09/va-2.jpg?w=261&h=83)

![VA 3](https://d4anm2017a.files.wordpress.com/2017/09/va-3.jpg?w=248&h=72)

![VA 4](https://d4anm2017a.files.wordpress.com/2017/09/va-4.jpg?w=472&h=84)![VA 5](https://d4anm2017a.files.wordpress.com/2017/09/va-5.jpg?w=238&h=86)![VA 6](https://d4anm2017a.files.wordpress.com/2017/09/va-6.jpg?w=182&h=70)![VA 7](https://d4anm2017a.files.wordpress.com/2017/09/va-7.jpg?w=159&h=53)

 Jadi Va yang didapatkan adalah **11,2**

 **– True Value (Vt)**

![VT 1](https://d4anm2017a.files.wordpress.com/2017/09/vt-1.jpg?w=205&h=67)![VT 2](https://d4anm2017a.files.wordpress.com/2017/09/vt-2.jpg?w=170&h=77)![VT 3](https://d4anm2017a.files.wordpress.com/2017/09/vt-3.jpg?w=196&h=78)![VT 4](https://d4anm2017a.files.wordpress.com/2017/09/vt-4.jpg?w=190&h=67)![VT 5](https://d4anm2017a.files.wordpress.com/2017/09/vt-5.jpg?w=139&h=61)

Jadi Vt yang didapatkan adalah **11**

–**True Error (Et)**

![EA 1](https://d4anm2017a.files.wordpress.com/2017/09/ea-1.jpg?w=175&h=63)

![EA 2](https://d4anm2017a.files.wordpress.com/2017/09/ea-2.jpg?w=135&h=52)

Jadi Et yang didapat adalah **-0,1**

**-Approximate Error (Ea)**

![ET 1](https://d4anm2017a.files.wordpress.com/2017/09/et-1.jpg?w=173&h=58)(Et = Va – Va sebelum)![ET 2](https://d4anm2017a.files.wordpress.com/2017/09/et-2.jpg?w=148&h=64)

Jadi Ea yang didapat adalah **-0,2**

–**Relative True Error (εt )**

![epsilont1](https://d4anm2017a.files.wordpress.com/2017/09/epsilont1.jpg?w=161&h=71)

![epsilont2](https://d4anm2017a.files.wordpress.com/2017/09/epsilont2.jpg?w=208&h=51)

 Jadi **εt** yang didapatkan adalah **-0,02**

  **– Relative Approximate Error (εa)**

![epsilona1](https://d4anm2017a.files.wordpress.com/2017/09/epsilona1.jpg?w=182&h=91)

![epsilona2](https://d4anm2017a.files.wordpress.com/2017/09/epsilona2.jpg?w=184&h=86)

![epsilona3](https://d4anm2017a.files.wordpress.com/2017/09/epsilona3.jpg?w=208&h=68)

 Jadi **εa** yang didapatkan adalah **-0,00892** jika di persenkan menjadi -0.0089%

- Saat **h = 0,1**

– **Approximate Value (Va)**![6694193430417](https://d4anm2017a.files.wordpress.com/2017/09/6694193430417.png?w=529&h=541)

Jadi Va yang didapatkan adalah **11,1**

– **True Error (Et)**

![Et](https://d4anm2017a.files.wordpress.com/2017/09/et.png?w=452&h=176)

Jadi Et yang didapat adalah **-0,1**

**-Approximate Error (Ea)**

![Ea](https://d4anm2017a.files.wordpress.com/2017/09/ea.png?w=254&h=121)

Jadi Ea yang didapat adalah **-0,1**

–**Relative True Error (εt )**

![epsiolont](https://d4anm2017a.files.wordpress.com/2017/09/epsiolont.png?w=394&h=157) Jadi **εt** yang didapatkan adalah **-0,01**

**– Relative Approximate Error (εa)**

![epsilona](https://d4anm2017a.files.wordpress.com/2017/09/epsilona.png?w=380&h=130) Jadi **εt** yang didapatkan adalah **-0,0901** jika di persenkan menjadi -0.0901%



```python
import math

x = 4
check = 1
a = 0
b = 1

while check > 0.001 :
    f_x = 0
    f_y = 0
    for i in range(a):
        f_x += (2**i)*x**i/math.factorial(i)

    for j in range(b):
        f_y += (2**j)*x**j/math.factorial(j)

    check = f_y - f_x
    a+=1
    b+=1
    print('iterasi ke-',a,'= ',check)
```

```python
output:

iterasi ke- 1 =  1.0
iterasi ke- 2 =  8.0
iterasi ke- 3 =  32.0
iterasi ke- 4 =  85.33333333333333
iterasi ke- 5 =  170.66666666666669
iterasi ke- 6 =  273.0666666666666
iterasi ke- 7 =  364.08888888888896
iterasi ke- 8 =  416.1015873015872
iterasi ke- 9 =  416.1015873015872
iterasi ke- 10 =  369.8680776014112
iterasi ke- 11 =  295.89446208112895
iterasi ke- 12 =  215.195972422639
iterasi ke- 13 =  143.46398161509296
iterasi ke- 14 =  88.28552714774924
iterasi ke- 15 =  50.448872655856576
iterasi ke- 16 =  26.90606541645684
iterasi ke- 17 =  13.45303270822842
iterasi ke- 18 =  6.330838921519444
iterasi ke- 19 =  2.8137061873417224
iterasi ke- 20 =  1.184718394670199
iterasi ke- 21 =  0.47388735786807956
iterasi ke- 22 =  0.18052851728316455
iterasi ke- 23 =  0.06564673355751438
iterasi ke- 24 =  0.022833646454728296
iterasi ke- 25 =  0.0076112154847578495
iterasi ke- 26 =  0.0024355889549951826
iterasi ke- 27 =  0.0007494119863622473
```

