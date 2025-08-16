# Final Workshop
# Matrix–Matrix Multiplication (OpenMP)

Este programa implementa la multiplicación de matrices cuadradas en C utilizando **OpenMP** para paralelismo y vectorización con `#pragma omp simd`.  
Se generan matrices aleatorias y se mide el tiempo promedio de ejecución en varias iteraciones.

---

## 🛠 Herramientas utilizadas
- **Lenguaje:** C  
- **Compilador probado:** `gcc` (GNU Compiler Collection)  
- **Paralelismo:** OpenMP  
- **Medición de tiempo:** `clock()` de `<time.h>`  
- **Alineación de datos:** `__attribute__((aligned(64)))`  

---

## ⚙️ Compilación y Ejecución
### Optimizado
```bash
mkdir SCAR-Final-Workshop-Pablo
cd SCAR-Final-Workshop-Pablo
git clone https://github.com/pablomanjarresneg/SCAR-Final-Workshop.git
gcc -O3 -fopenmp -march=native -funroll-loops -o bin/mmm mmm_implementation.c
./bin/mmm
```

## Author
- Pablo Manjarres Negrette
