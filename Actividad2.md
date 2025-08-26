# USO DE NUMPY Y PANDAS

## NumPy – Creación y manipulación de arreglos


## NumPy – Operaciones estadísticas y funciones avanzadas
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

**3. Numeros aleatorios**
NumPy incluye un módulo de generación de números aleatorios que permite crear matrices y vectores con valores distribuidos uniformemente o bajo otras distribuciones estadísticas.

**np.random.rand()**
Descripción: Genera un número aleatorio entre 0 y 1

Ejemplo en colab:
rand_num = np.random.rand()
print("Número aleatorio:", rand_num)

Resultado en colab:
Número aleatorio: 0.13466293807842122

**np.random.rand(m,n)**
Descripción: Genera una matriz aleatoria de dimensiones (m,n)

Ejemplo en colab:
rand_arr = np.random.rand(2, 2)
print("Arreglo aleatorio:\n", rand_arr)

Resultado en colab:
Arreglo aleatorio:
 [[0.6895847  0.868229  ]
 [0.94500376 0.4323496 ]]

**4. Álgebra lineal**
El submódulo numpy.linalg proporciona herramientas para realizar cálculos matriciales avanzados, como productos, determinantes e inversas. Es fundamental en aplicaciones de machine learning, gráficos computacionales y métodos numéricos.

**np.dot()**
Descripción: Realiza el producto matricia

Ejemplo en colab:
#Definir matrices
A = np.array([[1, 2], [3, 4]])
B = np.array([[2, 0], [1, 3]])

#Producto matricial
C = np.dot(A, B)
print("Producto matricial:\n", C)

Resultado en colab:
Producto matricial:
 [[ 4  6]
 [10 12]]

**np.linalg.inv()**
Descripción: Calcula la matriz inversa

Ejemplo en colab:
#Definir matrices
A = np.array([[1, 2], [3, 4]])
B = np.array([[2, 0], [1, 3]])

#Determinante de A
det = np.linalg.det(A)
print("Determinante de A:", det)

Resultado en colab:
Determinante de A: -2.0000000000000004

**np.linalg.det()**
Descripción: Calcula el determinante

Ejemplo en colab:
#Definir matrices
A = np.array([[1, 2], [3, 4]])
B = np.array([[2, 0], [1, 3]])

#Inversa de A
inv_A = np.linalg.inv(A)
print("Inversa de A:\n", inv_A)

Resultado en colab:
Inversa de A:
 [[-2.   1. ]
 [ 1.5 -0.5]]

 **Referencias**

**1. 	Universidad de la República (Udelar). Funciones estadísticas con NumPy.**
Documento técnico que explica funciones estadísticas básicas en NumPy.
Enlace: https://eva.interior.udelar.edu.uy/pluginfile.php/68969/mod_resource/content/0/Funciones%20Estadisticas%20con%20Numpy.pdf

**2. 	EntreData. Explorando el Álgebra Lineal con NumPy en Proyectos Reales.**
Artículo que muestra aplicaciones prácticas de álgebra lineal con NumPy.
Enlace: https://www.entredata.org/ciencia-de-datos-con-python/explorando-el-algebra-lineal-con-numpy-en-proyectos-reales

**3. 	FreeCodeCamp Español. La guía definitiva del paquete NumPy para computación científica en Python.**
Recurso introductorio completo sobre NumPy, ideal para principiantes.
Enlace: https://www.freecodecamp.org/espanol/news/la-guia-definitiva-del-paquete-numpy-para-computacion-cientifica-en-python/

**4.  Google Scholar. Buscador académico de literatura científica.**
Ideal para encontrar artículos académicos sobre NumPy y sus aplicaciones.
Enlace: https://scholar.google.com.mx/

## Pandas – Creación y manipulación de DataFrames y Series


## Pandas – Operaciones avanzadas en DataFrames


