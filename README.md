Combinatoria y Conteo en Python
Este repositorio contiene la implementación en Python de algoritmos fundamentales para resolver problemas de conteo, específicamente permutaciones (con y sin repetición) y el cálculo de factoriales.
 Archivos del Proyecto
combinatorias_bono.ipynb: Archivo principal que contiene toda la lógica matemática, las funciones implementadas y los casos de prueba.
README.md: Este archivo de documentación.
 Problemas Resueltos
1. Permutaciones y k-permutaciones
Este problema surge cuando tratamos de ordenar un conjunto en un subconjunto más pequeño. Se puede ver como ordenar cierta cantidad de objetos en cajas, donde los objetos son nuestro valor  y  representa la cantidad de cajas disponibles.
Fórmula:

Análisis de Eficiencia:
Iterativo: Tiene un crecimiento temporal lineal  y un uso de almacenamiento constante .
Recursivo: Tiene un crecimiento lineal en tiempo y espacio . Puede ser peligroso en lenguajes como Python donde la pila de recursión está acotada por defecto.
2. Coeficientes Multinomiales y Palabras con Letras Repetidas
Utilizado en expansiones algebraicas y combinatoria con elementos idénticos. El ejercicio canónico es calcular cuántas palabras distintas se pueden formar con los caracteres de "BANANA". Se calcula dividiendo el factorial del total de caracteres () entre el producto de los factoriales de la cantidad de veces que se repite cada elemento ().
Fórmula:

Análisis de Eficiencia:
Entrada de Texto (str): Crecimiento temporal  (donde  es el tiempo filtrando letras y  la cantidad de letras únicas). Gasto de memoria lineal .
Entrada Numérica (list): Eficiencia temporal lineal  y eficiencia de almacenamiento constante , ya que no requiere crear estructuras adicionales.
 Instrucciones de Ejecución
El código está escrito en Python puro y no requiere la instalación de librerías externas.
Asegúrate de tener Python 3.x instalado en tu sistema, o utiliza un entorno virtual en la nube como Google Colab.
Clona este repositorio o descarga el archivo principal del código.
Si usas terminal, navega a la carpeta del proyecto y ejecuta: python combinatorias_bono.ipynb. Si usas un entorno interactivo (como Jupyter o Colab), simplemente ejecuta las celdas en orden secuencial.
🧪 Ejemplos de Entrada, Salida y Evidencias de Pruebas
El código incluye un banco de pruebas para verificar su correcto funcionamiento, cubriendo tanto casos de éxito como el manejo de errores (casos especiales).
Ejemplos de Permutaciones P(n, r)
Entrada: permutaciones_iterado(10, 3) ➔ Salida: 720.0
Entrada: permutaciones_iterado(20, 5) ➔ Salida: 1860480.0
Entrada: permutaciones_iterado(11, 6) ➔ Salida: 332640.0
Ejemplos de Permutaciones con Repetición (Palabras)
Entrada: contar_palabras('BANANA') ➔ Salida: 60
Entrada: contar_palabras([4, 3, 2]) ➔ Salida: 1260
Entrada: contar_palabras('PUMA') ➔ Salida: 24
Entrada: contar_palabras('AAAAA') ➔ Salida: 1
Evidencias de Casos Especiales y Manejo de Errores
El sistema valida que no se procesen operaciones matemáticas inválidas:
Error por :
Entrada: permutaciones_iterado(3, 5)
Salida: "si r es menor a 'n' no hay permutaciones"
Error por valores negativos:
Entrada: factorial_iterado(-5)
Salida: "no hay factorial de un numero negativo"
Error por listas con negativos:
Entrada: contar_palabras([4, -2, 3])
Salida: "no es posible realizar la operacion porque no existe factorial para negativos"
Cadenas vacías (n=0):
Entrada: contar_palabras('')
Salida: 1
contar_palabras('BANANA') ➔ Salida: 60Entrada: contar_palabras([4, 3, 2]) ➔ Salida: 1260Entrada: contar_palabras('PUMA') ➔ Salida: 24Entrada: contar_palabras('AAAAA') ➔ Salida: 1Evidencias de Casos Especiales y Manejo de ErroresEl sistema valida que no se procesen operaciones matemáticas inválidas:Error por $r > n$:Entrada: permutaciones_iterado(3, 5)Salida: "si r es menor a 'n' no hay permutaciones"Error por valores negativos:Entrada: factorial_iterado(-5)Salida: "no hay factorial de un numero negativo"Error por listas con negativos:Entrada: contar_palabras([4, -2, 3])Salida: "no es posible realizar la operacion porque no existe factorial para negativos"Cadenas vacías (n=0):Entrada: contar_palabras('')Salida: 1
