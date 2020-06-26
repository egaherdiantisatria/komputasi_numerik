## JAWABAN

### no. 1

```
from math import exp
def midpoint(f, a, b, n):
    h = 0.1
    result = 0
    for i in range(n):
        result += f((a + h/2.0) + i*h)
    result *= h
    return result
g = lambda y: exp(1+(2*a*a)+b)
a = 0.1
b = 0.3
print ('    n        midpoint   ')
for i in range(1, 21):
    n = 2**i
    m = midpoint(g, a, b, n)
    print ('%7d %.16f ' % (n, m))
```

output :

```
  n                        midpoint   
      2                 0.7486842754521725 
      4                 1.4973685509043451 
      8                 2.9947371018086901 
     16                 5.9894742036173829 
     32                 11.9789484072347587 
     64                 23.9578968144695068 
    128                 47.9157936289390065 
    256                 95.8315872578786809 
    512                 191.6631745157554008 
   1024                 383.3263490315084709 
   2048                 766.6526980630579828 
   4096                 1533.3053961261632594 
   8192                 3066.6107922523738125 
  16384                 6133.2215845020191409 
  32768                 12266.4431690120054554 
  65536                 24532.8863380336115370 
 131072                 49065.7726760768273380 
 262144                 98131.5453521632589400 
 524288                 196263.0907014935219195 
1048576                 392526.1813997357385233 
```

### no. 2

```
alpha = .8
M = [
    [1, 2, 3],
    [2, 3, 3],
    [1, 1, 1],
]
n = len(M)
rj = [1.0/n for _ in range(n)]
p = [1.0/n for _ in range(n)]

for _ in range(4):
    p_old = [x for x in p]
    for i in range(n):
        pi = 0.0
        for j in range(n):
            pi += alpha * M[i][j] * p_old[j]
        pi += (1-alpha) * rj[i]
        p[i] = pi
    print(p)
```

output:

```
iterasi ke 1 :[1.6666666666666667, 2.2, 0.8666666666666667]
iterasi ke 2 :[7.0, 10.093333333333335, 3.8533333333333335]
iterasi ke 3 :[31.064000000000007, 44.73866666666668, 16.824000000000005]
iterasi ke 4 :[136.87733333333338, 197.51946666666674, 74.16800000000002]
```

### no. 3

```
def fungsi(x):
    y=2*x
    return y
print ("f(x)=2*x")
hasileksak=0.693147180
a=float(input("masukkan batas bawah integral:"))
b=float(input("masukkan batas atas integral:"))
print ("iterasi","\t","n","\t","trapezoid")
for iterasi in range(1,16,1):
    n=2*iterasi
    h=(b-a)/n
    xi=a
    y=0
    for i in range (1,n):
        xi=xi+h
        y+=fungsi(xi)
    It=(h)*((fungsi(a)+(2*y)+fungsi(b))/2)
    jmlganjil=0
    jmlgenap=0
    xi=a+h
    xj=a+(2*h)
    print (iterasi,"\t""\t",n,"\t",It)
```

output :

```
f(x)=2*x
masukkan batas bawah integral:1
masukkan batas atas integral:3
iterasi      n   trapezoid
1            2   8.0
2            4   8.0
3            6   8.0
4            8   8.0
5           10   8.0
6           12   8.0
7           14   7.999999999999998
8           16   8.0
9           18   8.000000000000004
10          20   8.000000000000004
11          22   7.999999999999995
12          24   7.999999999999998
13          26   8.0
14          28   8.0
15          30   8.000000000000002
```