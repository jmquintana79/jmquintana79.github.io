---
title: Post1
parent: Tools
has_children: false
nav_order: 1
---

# Linux commands for Data Science

Para una primera inmersión en los datos de un proyecto no es necesario escribir Python scripts. Son tareas demasiado básicas que pueden ser hechas a traves de comandos Linux. Esto por supuesto es opcional, pero se vuelve más necesario su uso cuando tenemos **volúmenes de datos demasiado grandes**. En estos casos, Python puede que no sea la mejor opción.

## CSV TOOLS:

### CSVKIT:

Completo kit de herramientas para el manejo de csv files.

* Visualizar con estilo dataframe: `$csvlook data.csv | head`
* Excel to csv: `$in2csv data.xls > data.csv`
* Json to csv: `$in2csv data.json > data.csv`
* csv to Json: `$csvjson data.csv > data.json`
* Imprimir column names: `$csvcut -n data.csv`
* Seleccionar un subset de columnas: `$csvcut -c column_a,column_c data.csv > new.csv`
* Re-ordenar columns: `$csvcut -c column_c,column_a data.csv > new.csv`
* Generar summary statistics: `$csvstat data.csv`
* Query usando SQL commands: `$csvsql --query "select name from data where age > 30" data.csv > new.csv`
* [y mucho mas ...](https://csvkit.readthedocs.io/en/1.0.3/)

### CSVTOOL:

Este kit de herramientas es similar al anterior. Puedes encontrar más información en su [help document](https://www.google.com/url?q=https%3A%2F%2Fcolin.maudry.com%2Fcsvtool-manual-page%2F&sa=D&sntz=1&usg=AFQjCNHhs79T3OiFRQoo_76jLl9hE5fyfg).

* Install (linux): `$sudo apt-get install csvtool`
* Install (macos):
```
 $ brew install opam
 $ opam install csv
 $ sudo ln -s ~/.opam/system/bin/csvtool /usr/local/bin/
```

## UNIX COMMANDS:

### ICONV:

Comando para cambiar el formato (codificación) texto de los datos.

    $iconv -l # enumerar todas las codificaciones conocidas
    $iconv -f <codificacion inicial> -t <codificacion final> <input.txt> output.txt

### HEAD / TAIL:

Imprimir las primeras y ultimas lineas respectivamente

    $head -n <num rows> # imprime un número específico de líneas
    $head -c <num bytes> #imprime un número específico de bytes

### TR:

Es un filtro que nos permite cambiar una determinada información de un archivo por otra. Admite multiples usos de interes para cientifícos de datos.

Ejemplos:

* Replace tab delimited ("Tab" per ","): `$cat <input file> | tr "\\t" "," <output file>`
* Bash program para multiples transformaciones:
```
    $cat <input file> | tr "[:punct:][:space:]" "\n" | tr "[:upper:]" "[:lower:]" | grep . | sort | uniq -c | sort -nr
```
* Algunas opciones disponibles son:
```
    [:alnum:] all letters and digits
    [:alpha:] all letters
    [:blank:] all horizontal whitespace
    [:cntrl:] all control characters
    [:digit:] all digits
    [:graph:] all printable characters, not including space
    [:lower:] all lower case letters
    [:print:] all printable characters, including space
    [:punct:] all punctuation characters
    [:space:] all horizontal or vertical whitespace
    [:upper:] all upper case letters
    [:xdigit:] all hexadecimal digits
```
* Convertir mayusc en minusc: `$cat <input file> | tr '[A-Z]' '[a-z]'`

### WC:

Contador de lineas, caracteres, etc.

* Contador de lineas: `$wc -l <gigantic_comma.csv>`

### SPLIT:

Divide grandes ficheros de datos en otros mas pequeños según selected sizes.

* Split file en ficheros de 500 filas: `$split -l 500 filename.csv new_filename_`

El ejemplo anterior genera:
```
    # filename.csv
    # ls output
    # new_filename_aaa
    # new_filename_aab
    # new_filename_aac
```
### SORT:

Ordenar datos.

* Sorting a CSV file by the second column alphabetically: `$sort -t, -k2 filename.csv`
* Numerically: `$sort -t, -k2n filename.csv`
* Reverse order: `$sort -t, -k2nr filename.csv`

### UNIQ:

Unique values.
```
    $uniq -c <file input> # count number of occurrences
    $uniq -d <file input> # only print duplicate lines
```
### CUT:

Selección de columnas.

* Selección de las columnas 1 y 3: `$cut -d, -f 1,3 filename.csv`
* Selección de todas las columnas menos la 2: `$cut -d, -f 2- filename.csv`
* Contar los valores unicos de la columna 2: `$cat filename.csv | cut -d, -f 2 | sort | uniq | wc -l`

### PASTE:

Merge dos ficheros de datos.

    $paste -d ',' <file1> <file2> > <merged output file>

### JOIN:

Join dos files igual que con SQL (por defecto usa _inner join_ y si no especificas las columnas usa la primera como índices)
```
    # Join the first file (-1) by the second column
    # and the second file (-2) by the first
    $join -t, -1 2 -2 1 <first_file.txt> <second_file.txt>
```
### GREP:

Busca regular expresions dentro de ficheros de datos.

* Por ejemplo, lista el numero de filas que contienen una expresion:
```
    $grep -lr 'some_value' <file input> | wc -l
    $grep -c 'some_value' <file input>
```
###  SED:

Este comando es un editor de flujo que opera línea por línea que permite multiples posibilidades para el formateo de los datos.

### AWS:

Es mucho más que un simple comando: es un lenguaje completo que permite hacer todo lo visto anteriormente y mucho mas.

## Fuentes:

* "[Command line tricks for Data Science](https://www.kdnuggets.com/2018/06/command-line-tricks-data-scientists.html)"-KDnuggets Blog.
* [Manual de csvkit](https://csvkit.readthedocs.io/en/1.0.3/).
* [Manual de csvtool](https://colin.maudry.com/csvtool-manual-page/).