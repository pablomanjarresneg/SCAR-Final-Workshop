# Final Workshop: OpenMP Matrix Multiplication

Este proyecto implementa la multiplicación de matrices cuadradas en C, utilizando **OpenMP** para paralelismo y vectorización con `#pragma omp simd`.  
Se generan matrices aleatorias y se mide el tiempo promedio de ejecución en múltiples iteraciones.

---

## 🛠 Herramientas Utilizadas

- **Lenguaje:** C  
- **Compilador:** `gcc` (GNU Compiler Collection)  
- **Paralelismo:** OpenMP  
- **Medición de tiempo:** `clock()` de `<time.h>`  
- **Alineación de datos:** `__attribute__((aligned(64)))`  

---

## ⚙️ Compilación y Ejecución

### Pasos

```bash
git clone https://github.com/pablomanjarresneg/SCAR-Final-Workshop.git
cd SCAR-Final-Workshop
gcc -O3 -fopenmp -march=native -funroll-loops -o bin/mmm mmm_implementation.c
./bin/mmm
```

**Descripción de las flags de compilación:**

- `-fopenmp`: Habilita soporte para OpenMP (paralelismo).
- `-O3`: Aplica optimizaciones agresivas.
- `-march=native`: Usa instrucciones SIMD específicas de la CPU local.
- `-funroll-loops`: Desenrolla bucles para mejorar el rendimiento.

---

## ⚠️ Manejo de Errores

Si ocurre un **segmentation fault** (por stack overflow debido al tamaño de las matrices), ejecuta:

```bash
ulimit -s unlimited
./bin/mmm
```

---

## 📊 Ejemplo de Resultados

Salida típica del programa:

```bash
Size of matrices: 1436
Running time: 6.181545

Size of matrices: 1311
Running time: 4.974762

Size of matrices: 1818
Running time: 11.004390
```

Donde:

- **Size of matrices:** Tamaño de la matriz utilizada en la ejecución  
- **Running time:** Tiempo promedio de ejecución (segundos) para `N` iteraciones

---

## 👤 Autor

- Pablo Manjarres Negrette

