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



## NumPy – Operaciones estadísticas y funciones avanzadas


## Pandas – Creación y manipulación de DataFrames y Series


## Pandas – Operaciones avanzadas en DataFrames


