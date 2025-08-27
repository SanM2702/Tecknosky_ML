# USO DE NUMPY Y PANDAS

## NumPy – Creación y manipulación de arreglos


## NumPy – Operaciones estadísticas y funciones avanzadas


## Pandas – Creación y manipulación de DataFrames y Series
Describe las funciones más importantes de NumPy relacionadas con estadística, generación de secuencias, números aleatorios y álgebra lineal. Cada sección incluye una explicación breve, ejemplos y resultados prácticos.

En esta sección se documentan funciones avanzadas de NumPy para estadísticas, generación de secuencias, números aleatorios y álgebra lineal.  

Cada ejemplo ha sido ejecutado en **Google Colab** y se presenta junto con su salida:

**1. Funciones estadisticas:**
Las funciones estadísticas de NumPy permiten obtener métricas básicas para el análisis de datos, como la media, la desviación estándar y la suma total de los elementos de un arreglo.

**np. mean()**
Descripcion: Calcula el promedio de los elementos de un arreglo

Ejemplo en colab:
arr = np.array([1, 2, 3, 4, 5])
print("Arreglo:", arr)
print("Media:", np.mean(arr))

Resultado en colab:
Arreglo: [1 2 3 4 5]
Media: 3.0

**np. std()**
Descripcion: Calcula la desviacion estandar

Ejemplo en colab: 
arr = np.array([1, 2, 3, 4, 5])
print("Arreglo:", arr)
print("Desviación estándar:", np.std(arr))

Resultado en colab: 
Arreglo: [1 2 3 4 5]
Desviación estándar: 1.4142135623730951

**np. sum()**
Descripcion: Suma todos los elementos de un arreglo

Ejemplo en colab: 
arr = np.array([1, 2, 3, 4, 5])
print("Arreglo:", arr)
print("Suma:", np.sum(arr))

Resultado en colab: 
Arreglo: [1 2 3 4 5]
Suma: 15

**2. Funciones de creación de secuencias**
NumPy facilita la generación de arreglos numéricos con funciones que permiten definir secuencias, ya sea con pasos específicos o con valores equidistantes. Esto es útil para simulaciones, gráficas y cálculos numéricos.

**np.arange()**
Descripción: Genera una secuencia con un paso definido.

Ejemplo en colab:
arr1 = np.arange(0, 10, 2)
print("Arreglo con arange:", arr1)

Resultado en colab:
Arreglo con arange: [0 2 4 6 8]

**np.linspace()**
Descripción: Genera valores equidistantes en un rango.

Ejemplo en colab:
arr2 = np.linspace(0, 10, 3)
print("Arreglo con linspace:", arr2)

Resultado en colab:
Arreglo con linspace: [ 0.  5. 10.] 


## Pandas – Operaciones avanzadas en DataFrames


