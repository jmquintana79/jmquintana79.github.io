---
title: Pandas best practises
parent: Linux commands for DS
grand_parent: Tools
nav_order: 1
---

# Pandas Best Practises

## Imputando o consiguiendo valores de un dataframe más rápidamente

Testando para un DataFrame de 20,000 rows ([Here’s the notebook](https://colab.research.google.com/drive/1heqQy_55YHA9vacunPIbrf8zqd5SWqN5)).
```
# .at - 22.3 seconds
for i in range(df_size):
    df.at[i] = profile
Wall time: 22.3 s# .iloc - 15% faster than .at

for i in range(df_size):
    df.iloc[i] = profile
Wall time: 19.1 s# .loc - 30% faster than .at

for i in range(df_size):
    df.loc[i] = profile
Wall time: 16.5 s# .iat, doesn't work for replacing multiple columns of data.

# Fast but isn't comparable since I'm only replacing one column.
for i in range(df_size):
    df.iloc[i].iat[0] = profile['address']
Wall time: 3.46 s# .values / .to_numpy() - 195% faster than .at

for i in range(df_size):
    df.values[i] = profile
    # Recommend using to_numpy() instead if you have Pandas 1.0+
    # df.to_numpy()[i] = profile
Wall time: 254 ms
```
## Porqué sólo usar el 25% de la CPU?

Ya la mayoría de los pc / laptops poseen una CPU que usan al menos 4 cores. A pesar de ello Pandas sólo usa un core lo que puede ralentizar procesos pesados como la lectura de ficheros muy pesados. Para usar todo el poder de la CPU se puede usar [**Modin-Pandas**](https://www.google.com/url?q=https%3A%2F%2Fmodin.readthedocs.io%2Fen%2Flatest%2F&sa=D&sntz=1&usg=AFQjCNG29bwPv-t4T-FASNQTfPKRkXXZPA) con tan sólo usar `import modin.pandas as pd` en vez de `import pandas as pd`.

## Definir <dtypes> a la hora de importar datos en un DataFrame

Cuando se importan datos dentro de un DataFrame, si no son especificados el _datatypes,_ Pandas tendrá que revisar todos los datos para inferir su tipo ralentizando enormemente el proceso de importación. Además, al definir inicialmente el tipo de datos de cada columna, te ahorras tener que hacer transformaciones posteriores.

```
pd.read_csv(‘fake_profiles.csv’, dtype={
    ‘job’: ‘str’,
    ‘company’: ‘str’,
    ‘ssn’: ‘str’
})
```

## Evitar copias de DataFrames innecesarias

Es muy habitual cuando se hacen pruebas o revisiones de datos rápidas el hacer copias innecesarias de dataframes de un proceso a otro que se realiza sobre los datos.

```
# Change dataframe 1 and save it into a new dataframed
f1 = pd.read_csv(‘file.csv’)
df2 = df1.dropna()
df3 = df2.groupby(‘thing’)
```
Dado que de por sí un DataFrame consume una cantidad considerable de memoría con respecto a estos contenedores (Numpy Array), hay que evitar con mayor motivo su duplicación innecesaria.

## FUNCIONES INTERESANTES más desconocidas

### ne()

Dado un dataframe, esta función aplicada sobre un columna devuelve _True_ en aquellos valores que son diferentes al valor argumento:
```
# df creation
df = pd.DataFrame()
df['X'] = [0,0,0,0,1,1]

# return values diff to 0
df['X'].ne(0)

#[out]: [False,False,False,False,True,True]
```
  

### nsmallest() and nlargest()

Devuelve los n valores más pequeños / más grandes respectivamente.
```
df.nsmallest(number_return, "column name according to")
df.nlargest(number_return, "column name according to")
```