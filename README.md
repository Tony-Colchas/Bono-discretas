# 🔢 Combinatoria y Conteo en Python

Implementación en Python de algoritmos para resolver problemas de conteo: permutaciones (con y sin repetición) y cálculo de factoriales, sin librerías externas.

---

## 📂 Archivos del proyecto

```
├── combinatorias_bono.ipynb   # Cuaderno principal con funciones, explicaciones y pruebas
└── README.md    # Este archivo
```

---

## 🚀 Cómo ejecutar

**En Google Colab o Jupyter:** abre `combinatorias_bono.ipynb` y ejecuta las celdas en orden.

**En terminal con Python 3:**
```bash
jupyter nbconvert --to script combinatorias_bono.ipynb
python combinatorias_bono.py
```

No requiere instalar ninguna librería externa.

---

## 🧠 Problemas resueltos

### 1. Permutaciones — `P(n, r)`

Ordena `r` elementos tomados de un conjunto de `n`. Se puede pensar como distribuir objetos en cajas: `n` es la cantidad de objetos disponibles y `r` el número de cajas.

$$P(n, r) = \frac{n!}{(n-r)!}$$

Implementado en dos versiones:

- **Iterativa** — tiempo `O(n)`, espacio `O(1)`
- **Recursiva** — tiempo `O(n)`, espacio `O(n)` (cuidado con el límite de recursión de Python)

---

### 2. Coeficientes multinomiales — palabras con letras repetidas

Calcula cuántas palabras distintas se pueden formar con los caracteres de una cadena (ej. `"BANANA"`). Divide el factorial del total de caracteres entre el producto de los factoriales de cada frecuencia de repetición.

$$\frac{n!}{n_1! \cdot n_2! \cdots n_k!}$$

Acepta dos tipos de entrada:

- **`str`** — extrae las frecuencias automáticamente; tiempo `O(n·u)`, espacio `O(u)` donde `u` = letras únicas
- **`list`** — recibe las frecuencias directamente; tiempo `O(k)`, espacio `O(1)`

---

## 🧪 Ejemplos de entrada y salida

### Permutaciones

| Llamada | Resultado |
|---|---|
| `permutaciones_iterado(10, 3)` | `720.0` |
| `permutaciones_iterado(20, 5)` | `1860480.0` |
| `permutaciones_iterado(11, 6)` | `332640.0` |

### Palabras con letras repetidas

| Llamada | Resultado |
|---|---|
| `contar_palabras('BANANA')` | `60` |
| `contar_palabras([4, 3, 2])` | `1260` |
| `contar_palabras('PUMA')` | `24` |
| `contar_palabras('AAAAA')` | `1` |

---

## ⚠️ Casos especiales y manejo de errores

| Caso | Entrada | Salida |
|---|---|---|
| `r > n` | `permutaciones_iterado(3, 5)` | `"si r es menor a 'n' no hay permutaciones"` |
| Factorial negativo | `factorial_iterado(-5)` | `"no hay factorial de un numero negativo"` |
| Lista con negativos | `contar_palabras([4, -2, 3])` | `"no es posible realizar la operacion porque no existe factorial para negativos"` |
| Cadena o lista vacía | `contar_palabras('')` | `1` |
| `P(0, 0)` | `permutaciones_iterado(0, 0)` | `1.0` |
