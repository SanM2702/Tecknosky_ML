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


## Pandas – Creación y manipulación de DataFrames y Series


## Pandas – Operaciones avanzadas en DataFrames


