---
jupyter:
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.11.8
  nbformat: 4
  nbformat_minor: 2
---

::: {.cell .markdown}
# Reto 4

En este repositorio se encontrarán mis soluciones propuestas a los
puntos asignados como parte de este reto

## 1. Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula. {#1-dado-un-número-entero-determinar-si-ese-número-corresponde-al-código-ascii-de-una-vocal-minúscula}
:::

::: {.cell .code}
``` python
try:
    numero_minuscula : int
    numero_minuscula = int(input("Ingrese un numero entero: "))
    match numero_minuscula:
        case 97:
            print("El entero ingresado corresponde al codigo ASCII de la vocal minuscula a")
        case 101:
            print("El entero ingresado corresponde al codigo ASCII de la vocal minuscula e")
        case 105:
            print("El entero ingresado corresponde al codigo ASCII de la vocal minuscula i")
        case 111:
            print("El entero ingresado corresponde al codigo ASCII de la vocal minuscula o")
        case 117:
            print("El entero ingresado corresponde al codigo ASCII de la vocal minuscula u")
        case _:
            print("El entero ingresado no corresponde con el codigo ASCII de alguna vocal minuscula")
except ValueError :
    print("El dato ingresado no es un numero entero")
```
:::

::: {.cell .markdown}
## 2. Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no. {#2-dada-una-cadena-de-longitud-1-determine-si-el-código-ascii-de-primera-letra-de-la-cadena-es-par-o-no}
:::

::: {.cell .code}
``` python
try:
    cadena : str
    cadena = str(input("Ingrese una cadena de longitud 1: "))
    if len(cadena) == 1:
        ASCII : int
        ASCII = ord(cadena)
        if ASCII%2 == 0:
            print("El codigo ASCII de la cadena ingresada " ,cadena, " es par con un valor de " ,ASCII)
        else:
            print("El codigo ASCII de la cadena ingresada " ,cadena, " es impar con un valor de " ,ASCII)
    else:
        print("la cadena ingresada no tiene la longitud solicitada de 1")
except ValueError:
    print("La cadena ingresada no es valida")
```
:::

::: {.cell .markdown}
## 3. Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no. {#3-dado-un-carácter-construya-un-programa-en-python-para-determinar-si-el-carácter-es-un-dígito-o-no}
:::

::: {.cell .code}
``` python
try: 
    caracter : str
    caracter = str(input("Ingrese un caracter para evaluar: "))
    if len(caracter) == 1:
        digito : int
        digito = ord(caracter)
        if digito >= 48 and digito <= 57:
            print("El caracter ingresado corresponde al digito " ,caracter)
        else:
            print("El caracter ingresado no corresponde a ningun digito")
    else:
        print("el caracter ingresado no es valido")
except ValueError: 
    print("La cadena ingresada no es valida")
```
:::

::: {.cell .markdown}
## 4. Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación: {#4-dado-un-número-real-x-construya-un-programa-que-permita-determinar-si-el-número-es-positivo-negativo-o-cero-para-cada-caso-de-debe-imprimir-el-texto-que-se-especifica-a-continuación}

Positivo: \"El número x es positivo\" Negativo: \"El número x es
negativo\" Cero (0): \"El número x es el neutro para la suma\"
:::

::: {.cell .code}
``` python
try:
    numero_signo : int 
    numero_signo = int(input("Ingrese un numero entero: "))
    if numero_signo > 0:
        print("El numero ingresado " ,numero_signo, " es positivo (n > 0)")
    elif numero_signo < 0:
        print("El numero ingresado " ,numero_signo, " es negativo (n < 0)")
    else:
        print("El numero ingresado " ,numero_signo, " es neutro (n = 0)")
except ValueError :
    print("El dato ingresado no es un numero entero")
```
:::

::: {.cell .markdown}
## 5. Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo. {#5-dado-el-centro-y-el-radio-de-un-círculo-determinar-si-un-punto-de-r2-pertenece-o-no-al-interior-del-círculo}
:::

::: {.cell .code}
``` python
try:
    centro1 : float
    centro2 : float
    radio : float
    punto1 : float
    punto2 : float
    centro1 = float(input("Ingrese la coordenada x para el centro del circulo: "))
    centro2 = float(input("Ingrese la coordenada y para el centro del circulo: "))
    radio = float(input("Ingrese el radio del circulo: "))
    punto1 = float(input("Ingrese la coordenada x del punto a verificar: "))
    punto2 = float(input("Ingrese la coordenada y del punto a verificar: "))
    if (punto1 - centro1)**2 + (punto2- centro2)** 2<= radio**2:
        print("La coordenada ingresada (" ,punto1, " , " ,punto2, ") se encuentra dentro del circulo formado por el centro (" ,centro1, " , " ,centro2, ") con radio " ,radio)
    else:
        print("La coordenada ingresada (" ,punto1, " , " ,punto2, ") no se encuentra dentro del circulo formado por el centro (" ,centro1, " , " ,centro2, ") con radio " ,radio)
except ValueError:
    print("El valor ingresado no es un numero real")
```
:::

::: {.cell .markdown}
## 6. Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo. {#6-dadas-tres-longitudes-positivas-determinar-si-con-esas-longitudes-se-puede-construir-un-triángulo}
:::

::: {.cell .code}
``` python
try:
    longitud1 : float
    longitud2 : float
    longitud3 : float
    longitud1 = float(input("Por favor, ingrese la primera longitud: "))
    longitud2 = float(input("Por favor, ingrese la segunda longitud: "))
    longitud3 = float(input("Por favor, ingrese la tercera longitud: "))
    if longitud1 > 0 and longitud2 > 0 and longitud3 > 0:
        if longitud1 + longitud2 > longitud3 and longitud1 + longitud3 > longitud2 and longitud2 + longitud3 > longitud1:
            print("Las longitudes ingresadas corresponden a las validas para crear un triangulo a partir del teorema de desigualdad")
        else:
            print("Las longitudes ingresadas no corresponden a las validas para crear un triangulo a partir del teorema de desigualdad")
    else:
        print("no existen longitudes negativas")
except ValueError:
    print("El dato ingresado no es un numero real")
```
:::
