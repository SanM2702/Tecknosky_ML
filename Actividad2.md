# USO DE NUMPY Y PANDAS

## NumPy – Creación y manipulación de arreglos

## NumPy – Operaciones estadísticas y funciones avanzadas


## Pandas – Creación y manipulación de DataFrames y Series


## Pandas – Operaciones avanzadas en DataFrames

Ejemplo de estructura inicial
--------------------------------------------------------------------------------
1.Filtros en DataFrames
```python
import pandas as pd

Crear un DataFrame de ejemplo
data = {'Nombre': ['Ana', 'Luis', 'Pedro', 'Marta'],
        'Edad': [23, 35, 29, 40],
        'Ciudad': ['Bogotá', 'Medellín', 'Cali', 'Bogotá']}

df = pd.DataFrame(data)
print(df)

Filtrar personas mayores de 30
print(df[df['Edad'] > 30])

Resultado esperado:
  Nombre  Edad    Ciudad
1   Luis    35  Medellín
3  Marta    40   Bogotá
--------------------------------------------------------------------------------
2.Agrupamiento con groupby

Agrupar por ciudad y calcular edad promedio

print(df.groupby('Ciudad')['Edad'].mean())

Resultado esperado:
Ciudad
Bogotá      31.5
Cali        29.0
Medellín    35.0

Name: Edad, dtype: float64
--------------------------------------------------------------------------------
3.Merge y Join

 import pandas as pd

data = {'Nombre': ['Ana', 'Luis', 'Pedro', 'Marta'],
        'Edad': [23, 35, 29, 40],
        'Ciudad': ['Bogotá', 'Medellín', 'Cali', 'Bogotá']}
df = pd.DataFrame(data)

data2 = {'Ciudad': ['Bogotá', 'Medellín', 'Cali'],
         'Habitantes': [8000000, 2500000, 2200000]}
df2 = pd.DataFrame(data2)

merged = pd.merge(df, df2, on="Ciudad")
print(merged)

Resultado esperado:

  Nombre  Edad    Ciudad  Habitantes
0    Ana    23    Bogotá     8000000
1   Marta    40    Bogotá     8000000
2    Luis    35  Medellín     2500000
3   Pedro    29      Cali     2200000
--------------------------------------------------------------------------------
4.Manejo de valores nulos
df.loc[2, 'Ciudad'] = None   Introducimos un NaN
print(df)

 Rellenar valores nulos con "Desconocido"
print(df.fillna("Desconocido"))

 Eliminar filas con nulos
print(df.dropna())
--------------------------------------------------------------------------------
5.Exportación e importación
df.to_csv("datos.csv", index=False)
df_csv = pd.read_csv("datos.csv")
print(df_csv)

Resultado esperado (al volver a leer el CSV):

  Nombre  Edad      Ciudad
0    Ana    23      Bogotá
1   Luis    35    Medellín
2  Pedro    29         NaN
3  Marta    40      Bogotá
--------------------------------------------------------------------------------