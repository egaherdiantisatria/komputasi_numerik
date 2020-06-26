```python
# metode numerik
f1 <- function(x,y){y/(2*x+1)}
num <- euler(f1, x0=0, y0=1, h=0.05, n=100)

# metode analitik
f2 <- function(x){sqrt(2*x+1)}
x0 <- 0
y0 <- 1
x <- x0
y <- y0

for(i in 1:100){
  y0 <- f2(x0+0.05)
  x0 <- x0+0.05
  x <- c(x, x0)
  y <- c(y, y0)
}
true <- data.frame(x=x, y=y)
```

![Visualisasi integrasi numerik dengan metode Euler dan metode analitik](https://bookdown.org/moh_rosidi2610/Metode_Numerik/Metode_Numerik_files/figure-html/eulerviz-1.png)

Gambar 10.1: Visualisasi integrasi numerik dengan metode Euler dan metode analitik

Berdasarkan hasil visualisasi dapat dilihat bahwa metode Euler dapat dengan baik memberikan pendekatan nilai integrasi persamaan. Pembaca dapat mencoba untuk melakukan simulasi kembali dengan nilai hh yang lebih kecil.