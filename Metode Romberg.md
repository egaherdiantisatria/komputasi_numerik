# Metode Romberg[¶](https://lukmanarimashuri.github.io/metode_romberg/#metode-romberg)

Integrasi Romberg ialah teknik yang digunakan untuk menganalisis kasus fungsi yang diintegrasikan telah tersedia. Teknik ini memiliki keunggulan untuk menghasilkan nilai-nilai dari fungsi yang digunakan secara efisien bagi pengintegrasian secara numerik. Integrasi Romberg didasarkan pada ekstrapolasi Richardson, yaitu metode untuk mengkombinasikan dua perkiraan integral secara numerik untuk memperoleh nilai ketiga, yang lebih akurat, misal: O(h2N)O(h2N) --> O(h2N+2)O(h2N+2)

Misal *I(h)* dan *I(2h)* dihitung dengan metode Trapesium dengan orde galat O(h2)O(h2), maka ekstrapolasi Richardson menghasilkan metode Simpson ⅓ dengan orde galat O(h4)O(h4). Kemudian jika I(h) *dan* I(2h)* dihitung dengan metode Simpson ⅓, maka akan menghasilkan kaidah Boole denganrorde galat O(h6)O(h6).

Persamaan ekstrapolasi Richardson :

J=I(h)+I(h)−I(2h)2q−1J=I(h)+I(h)−I(2h)2q−1

Misalkan *I* adalah nilai integrasi yang dinyatakan sebagai I=Ak+Ch2+Dh4+Eh6+...I=Ak+Ch2+Dh4+Eh6+... dalam hal ini h=(b−a)nh=(b−a)n dan AkAk merupakan nilai integrasi dengan metode Trapesium dengan jumlah pias n=2kn=2k dan Orde galatnya adalah O(h2)O(h2). A0,A1,...AkA0,A1,...Ak digunakan dalam persamaan ekstrapolasi Richardson untuk mendapatkan B1,B2,...,BkB1,B2,...,Bk, yaitu

Bk=Ak+Ak−Ak−122−1Bk=Ak+Ak−Ak−122−1

Jadi, nilai I setelah diupdate adalah I=Bk+D′h4+E′h6+…I=Bk+D′h4+E′h6+… dengan orde galat BkBk adalah O(h4)O(h4).

Selanjutnya, menggunakan B1,B2,..,BkB1,B2,..,Bk pada persamaan ekstrapolasi Richardson untuk mendapatkan runtunan C2,C3,...,CkC2,C3,...,Ck, yaitu

Ck=Bk+Bk−Bk−124−1Ck=Bk+Bk−Bk−124−1

nilai I saat ini adalah I=Ck+E"h6+...I=Ck+E"h6+... dengan orde galat CkCk adalah O(h6)O(h6). Demikian seterusnya.

Dari runtunan diatas diperoleh tabel Romberg berikut:

| *O*(*h*2) Metode Trapesium | *O*(*h*4) Metode Simpson | *O*(*h*6) Metode Boole | *O*(*h*8) Perbaikan ketiga | *O*(*h*10) *dst* |
| -------------------------- | ------------------------ | ---------------------- | -------------------------- | ---------------- |
| *A*0                       |                          |                        |                            |                  |
| *A*1                       | *B*1                     |                        |                            |                  |
| *A*2                       | *B*2                     | *C*2                   |                            |                  |
| *A*3                       | *B*3                     | *C*3                   | *D3*                       |                  |
| *A*4                       | *B*4                     | *C*4                   | *D4*                       | *E4*             |

E4 ialah nilai integrasi yang lebih baik.

## **Listing Pemrograman**[¶](https://lukmanarimashuri.github.io/metode_romberg/#listing-pemrograman)

**Contoh 1 :** Dalam contoh ini kita dapat melihat bahwa dengan menggunakan metode `scipy.integrate.romberg()` , kita bisa mendapatkan integrasi romberg dari fungsi yang dapat dipanggil dari batas a ke b dengan menggunakan metode `scipy.integrate.romberg()`.



```python
# import numpy and scipy.integrate 
  import numpy as np 
  from integrate import scipy 
  gfg = lambda x: np.exp( - x * * 2 ) 

 # using scipy.integrate.romberg() 
  geek = integrate.romberg(gfg, 0 , 3 , show = True ) 

  print (geek) 
```

Output:



```python
 Romberg integrasi <function vectorize1..vfunc di 0x00000209C3641EA0> dari [0, 3]

  Langkah StepSize Hasil
      1 3.000000 1.500185
      2 1.500000 0,908191 0,710860
      4 0.750000 0.886180 0.878843 0.890042
      8 0.375000 0.886199 0.886206 0.886696 0.886643
     16 0.187500 0.886205 0.886207 0.886207 0.886200 0.886198
     32 0,093750 0.886207 0.886207 0.886207 0.886207 0.886207 0.886207
     64 0.046875 0.886207 0.886207 0.886207 0.886207 0.886207 0.886207 0.886207
    128 0.023438 0.886207 0.886207 0.886207 0.886207 0.886207 0.886207 0.886207 0.886207

 Hasil akhir adalah 0,8862073482595311 setelah 129 evaluasi fungsi.
```

Contoh 2:



```python
# import numpy and scipy.integrate 
  import numpy as np 
  from integrate import scipy 
  gfg = lambda x: np.exp( - x * * 2 ) + 1 / np.sqrt(np.pi) 

 # using scipy.integrate.romberg() 
  geek = integrate.romberg(gfg, 1 , 2 , show = True ) 

  print (geek)
```

Output:



```python
Integrasi Romberg dari <function vectorize1..vfunc at 0x00000209E1605400> dari [1, 2]

  Langkah StepSize Hasil
      1 1,000000 0,757287
      2 0,500000 0,713438 0,698822
      4 0.250000 0.702909 0.699400 0.699438
      8 0.125000 0.700310 0.699444 0.699447 0.699447
     16 0,062500 0,699663 0,699447 0,699447 0,699447 0,699447
     32 0.031250 0.699501 0.699447 0.699447 0.699447 0.699447 0.699447

 Hasil akhir adalah 0,6994468414978009 setelah 33 evaluasi fungsi.
```