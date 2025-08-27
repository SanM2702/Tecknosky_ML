# USO DE NUMPY Y PANDAS

## NumPy – Creación y manipulación de arreglos
NUMPY: Es una biblioteca de Python  que permite trabajar con arreglos multidimensionales de forma rápida y eficiente. Proporciona herramientas para realizar operaciones matemáticas avanzadas, estadísticas, álgebra lineal y generación de números aleatorios, siendo la base de muchas otras librerías de ciencia de datos, machine learning e inteligencia artificial.

1. IMPORTAR LIBRERIA NUMPY:

    import numpy as np

2. CREAR ARREGLOS:

    np.array(): Convierte listas o listas de listas en arreglos NumPy de n cantidad de dimensiones.

    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.array([0, 1, 2, 3])         #Arreglo de 1 dimesion
            Arr2 = np.array([[4, 5],[6, 7]])        #Arreglo de 2 dimesion
            Arr3 = np.array([[[8, 9],[10, 11]],[[12, 13],[14, 15]]])        #Arreglo de 3 dimesion

            print(Arr1)
            print(Arr2)
            print(Arr3)

        Resultado:
            [0 1 2 3]
            [[4 5]
            [6 7]]
            [[[ 8  9]
            [10 11]]

            [[12 13]
            [14 15]]]

    np.zeros(): Crea un arreglo lleno de ceros
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.zeros((2, 3)) #Arreglo lleno de ceros de dimensions 2x3 (2 filas, 3 columnas)
            Arr2 = np.zeros((1, 4, 2, 2)) # Arreglo lleno de ceros de dimensiones 1x4x2x2 (4 matrices de 2x2 dentro de un bloque) 

            print(Arr1)
            print(Arr2)
        
        Resultado
            [[0. 0. 0.]
            [0. 0. 0.]]
            [[[[0. 0.]
            [0. 0.]]

            [[0. 0.]
            [0. 0.]]

            [[0. 0.]
            [0. 0.]]

            [[0. 0.]
            [0. 0.]]]]

    np.ones(): Crea un arreglo lleno de unos
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.ones((4, 2)) #Arreglo lleno de unos de dimensiones 4x2 (4 filas, 2 columnas)
            Arr2 = np.ones((1, 3, 2, 4)) # Arreglo lleno de unos de dimensiones 1x3x2x4 (3 matrices de 2x4 dentro de un bloque) 

            print(Arr1)
            print(Arr2)
        
        Resultado:
            [[1. 1.]
            [1. 1.]
            [1. 1.]
            [1. 1.]]
            [[[[1. 1. 1. 1.]
            [1. 1. 1. 1.]]

            [[1. 1. 1. 1.]
            [1. 1. 1. 1.]]

            [[1. 1. 1. 1.]
            [1. 1. 1. 1.]]]]

    np.eye(): Crea una matriz de identidad
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.eye(5) #Arreglo de identidad de 5x5
            Arr2 = np.eye(3, 4) #Arreglo de identidad de 3x4

            print(Arr1)
            print(Arr2)

        Resultado:
            [[1. 0. 0. 0. 0.]
            [0. 1. 0. 0. 0.]
            [0. 0. 1. 0. 0.]
            [0. 0. 0. 1. 0.]
            [0. 0. 0. 0. 1.]]
            [[1. 0. 0. 0.]
            [0. 1. 0. 0.]
            [0. 0. 1. 0.]]

    np.arange(): Crea un arreglo con un rango de números
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.arange(5) #Arreglo de 1 dimension en el rango de 0 a 4 
            Arr2 = np.arange(0, 10, 2) #Arreglo de 1 dimension en el rango de 0 a 8 con salto 2

            print(Arr1)
            print(Arr2)

        Resultado:
            [0 1 2 3 4]
            [0 2 4 6 8]
    
    Nota: np.arange() no puede crear por si sola arreglos de mas de 1 dimension.

    np.linspace(): Crea un arreglo con n valores igualmente espaciados entre un rango  
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.linspace(0, 2, 5) #Arreglo de 5 valores entre 0 y 2

            print(Arr1)
        Resultado:
            [0.  0.5 1.  1.5 2. ]

3. PROPIEDADES DE LOS ARREGLOS:
    arr.shape   # Devuelve las dimensiones del arreglo (filas, columnas)
    arr.ndim    # Devuelve el número de dimensiones del arreglo
    arr.size    # Devuelve la cantidad total de elementos del arreglo
    arr.dtype   # Devuelve el tipo de dato del arreglo
    
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.array([0, 1, 2, 3])         
            Arr2 = np.array([[4, 5],[6, 7]])        
            Arr3 = np.array([[[8, 9],[10, 11]],[[12, 13],[14, 15]]])        

            print("Arreglo 1\n", Arr1, "\nDimensiones:", Arr1.shape, "\nNo. Dimensiones:", Arr1.ndim, "\nNo. Elementos:", Arr1.size, "\nTipo de datos:", Arr1.dtype)
            print("\nArreglo 2\n", Arr2, "\nDimensiones:", Arr2.shape, "\nNo. Dimensiones:", Arr2.ndim, "\nNo. Elementos:", Arr2.size, "\nTipo de datos:", Arr2.dtype)
            print("\nArreglo 3\n", Arr3, "\nDimensiones:", Arr3.shape, "\nNo. Dimensiones:", Arr3.ndim, "\nNo. Elementos:", Arr3.size, "\nTipo de datos:", Arr3.dtype)
        Resultado:
            Arreglo 1
            [0 1 2 3] 
            Dimensiones: (4,) 
            No. Dimensiones: 1 
            No. Elementos: 4 
            Tipo de datos: int64

            Arreglo 2
            [[4 5]
            [6 7]] 
            Dimensiones: (2, 2) 
            No. Dimensiones: 2 
            No. Elementos: 4 
            Tipo de datos: int64

            Arreglo 3
            [[[ 8  9]
            [10 11]]

            [[12 13]
            [14 15]]] 
            Dimensiones: (2, 2, 2) 
            No. Dimensiones: 3 
            No. Elementos: 8 
            Tipo de datos: int64

4. MANIPULACION DE FORMA:
    arr.reshape(): Cambia la forma del arreglo (filas × columnas) sin alterar los datos almacenados.
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.array([0, 1, 2, 3])         
            Arr2 = np.array([[4, 5],[6, 7]])        
            Arr3 = np.array([[[8, 9],[10, 11]],[[12, 13],[14, 15]]])        


            print(Arr1.reshape(2, 2), "\n")
            print(Arr2.reshape(4, 1), "\n")
            print(Arr3.reshape(4, 2), "\n")
        Resultado:
            [[0 1]
            [2 3]] 

            [[4]
            [5]
            [6]
            [7]] 

            [[ 8  9]
            [10 11]
            [12 13]
            [14 15]] 

    arr.flatten(): Convierte cualquier arreglo en 1D. Muy útil para aplanar matrices.
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.array([0, 1, 2, 3])         
            Arr2 = np.array([[4, 5],[6, 7]])        
            Arr3 = np.array([[[8, 9],[10, 11]],[[12, 13],[14, 15]]])        


            print(Arr1.flatten(), "\n")
            print(Arr2.flatten(), "\n")
            print(Arr3.flatten(), "\n")
        Resultado:
            [0 1 2 3] 

            [4 5 6 7] 

            [ 8  9 10 11 12 13 14 15] 

    arr.T: Intercambia filas ↔ columnas.
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.array([0, 1, 2, 3])         
            Arr2 = np.array([[4, 5],[6, 7]])        
            Arr3 = np.array([[[8, 9],[10, 11]],[[12, 13],[14, 15]]])        

            print("ORIGINAL\n", Arr1, "\n")
            print(Arr2, "\n")
            print(Arr3, "\n") 

            print("MODIFICADO\n", Arr1.T, "\n")
            print(Arr2.T, "\n")
            print(Arr3.T, "\n")
        Resultado:
            ORIGINAL
            [0 1 2 3] 

            [[4 5]
            [6 7]] 

            [[[ 8  9]
            [10 11]]

            [[12 13]
            [14 15]]] 

            MODIFICADO
            [0 1 2 3] 

            [[4 6]
            [5 7]] 

            [[[ 8 12]
            [10 14]]

            [[ 9 13]
            [11 15]]] 

5. Indexacion:
    Ejemplo:
        Codigo:
            import numpy as np

            Arr1 = np.array([0, 1, 2, 3])         
            Arr2 = np.array([[4, 5],[6, 7]])        

            print("Arreglo1: \n", Arr1[0],        #Muestra primer elemento
                "\n", Arr1[-1],                 #Muestra ultimo elemento
                "\n", Arr1[1:3])                #Muestra una parte del arreglo

            print("Arreglo2: \n", Arr2[0, 1],     # Elemento fila 0, col 1 → 5
                "\n", Arr2[:, 0],               # Primera columna → [4 6]
                "\n", Arr2[1, :])               # Segunda fila → [6 7]
        Resultado:
            Arreglo1: 
            0 
            3 
            [1 2]
            Arreglo2: 
            5 
            [4 6] 
            [6 7]


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


