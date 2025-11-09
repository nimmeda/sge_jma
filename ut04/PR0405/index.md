# [UT04](../../ut04/)

## PR0405

## Índice
- [Ejercicio1](./index.md/#ejercicio-01)
- [Ejercicio2](./index.md/#ejercicio-02)
- [Ejercicio3](./index.md/#ejercicio-03)
- [Ejercicio4](./index.md/#ejercicio-04)
- [Ejercicio5](./index.md/#ejercicio-05)
- [Ejercicio6](./index.md/#ejercicio-06)
- [Ejercicio7](./index.md/#ejercicio-07)
- [Ejercicio8](./index.md/#ejercicio-08)

### Ejercicio 01
```python
numeros = []
numero = 0

while numero != -1:
    numero = int(input("Introduce un número (-1 para salir): "))
    if numero != -1:
        numeros.append(numero)

def filtro_pares(lista):
    pares = []
    
    for n in lista:
        if n % 2 == 0:
            pares.append(n)
        n = n + 1
    return pares

pares = filtro_pares(numeros)
print(pares)

```
### Ejercicio 02
```python
celsius = []
numero = 0

while numero != -1:
    numero = int(input("Introduce un los valores celsius (-1 para salir): "))
    if numero != -1:
        celsius.append(numero)
        
def conversion(listsa):
    fahrenheit = list(map(lambda x: (x * 9/5 + 32),listsa))
    return fahrenheit

fahrenheit = conversion(celsius)
print(fahrenheit)
    
```
### Ejercicio 03
```python
from functools import reduce

numeros = [1, 2, 3, 4, 5]

suma = reduce(lambda acc, val: acc + val, numeros,0)
print(suma)

```
### Ejercicio 04
```python
palabras = []
numero = ""

while numero != "-1":
    numero = input("Introduce una palabra (-1 para salir): ")
    if numero != "-1":
        palabras.append(numero)

largas = filter(lambda p: len(p) > 5,palabras)
mayus = map(lambda x: x.upper(), largas)

print(list(mayus))
```
### Ejercicio 05
```python
from functools import reduce

lista = []
numero = 0

while numero != -1:
    numero = int(input("Introduce un los valores(-1 para salir): "))
    if numero != -1:
        lista.append(numero)
        
pares = filter(lambda x: x % 2 == 0, lista)
producto = reduce(lambda acc, val: acc * val, pares, 1)

print(f"Resultado: {producto}")
```
### Ejercicio 06
```python

```
### Ejercicio 07
```python
from functools import reduce


texto = input("Introduce la cadena: ")
resultado = {}

palabras = list(map(str.lower, texto.split()))

frecuencia = reduce(lambda acc, palabra: {**acc, palabra: acc.get(palabra, 0) + 1},palabras, {})

print(frecuencia)
```