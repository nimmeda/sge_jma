# [UT04](../../ut04/)

## PR0402

## Índice
- [Ejercicio1](./index.md/#ejercicio-01)
- [Ejercicio2](./index.md/#ejercicio-02)
- [Ejercicio3](./index.md/#ejercicio-03)
- [Ejercicio4](./index.md/#ejercicio-04)
- [Ejercicio5](./index.md/#ejercicio-05)
- [Ejercicio6](./index.md/#ejercicio-06)
- [Ejercicio7](./index.md/#ejercicio-07)
- [Ejercicio8](./index.md/#ejercicio-08)
- [Ejercicio9](./index.md/#ejercicio-09)
- [Ejercicio10](./index.md/#ejercicio-10)

### Ejercicio 01

```python
cadenaUsuario = input("Introduce la cadena a analizar: ")

vocales = "aeiouAEIOU"
nVocales = 0
nConsonantes = 0

for i in cadenaUsuario:
    if i in vocales:
        nVocales += 1
    else:
        nConsonantes += 1

print(f"Hay {nVocales} vocales en la cadena")
print(f"Hay {nConsonantes} consonantes en la cadena")
```

### Ejercicio 02

```python
cadenaUsuario = input("Introduce la cadena a invertir: ")

print(cadenaUsuario[::-1])
```

### Ejercicio 03

```python
cadenaUsuario = input("Introduce la cadena a comprobar: ")

cadenaLimpia = cadenaUsuario.replace(" ", "").lower()

if cadenaLimpia[::-1] == cadenaLimpia:
    print("Es un palindromo")
else:
    print("No es un palindromo")
```

### Ejercicio 04

```python
cadenaUsuario = input("Introduce la cadena a analizar: ")

palabras = cadenaUsuario.split()
cantidadPalabras = len(palabras)

print(f"Hay {cantidadPalabras} palabrasen la frase")
```

### Ejercicio 05
```python
cadenaUsuario = input("Introduce la cadena a analizar: ")

resultado = ""

for i in cadenaUsuario:
    if i not in resultado :
        resultado += i
print(resultado)
```
### Ejercicio 06
```python
cadena = input("Introduce la cadena que deseas cambiar: ")

r = ""

for i in cadena:
    if i.isupper():
        r += i.lower()
    else:
        r += i.upper()
               
print(r)
```
### Ejercicio 07
```python
c = input("Introduce una cadena: ")
n = int(input("Introduce el numero de posiciones a rotar: "))

resultado = c[n:] + c[:n]

print(resultado)
```
### Ejercicio 08
```python
c = input("Introduce la primera cadena: ")
c2 = input("Introduce la segunda cadena: ")

if sorted(c) == sorted(c2):
    print(f"{c} y {c2} son anagramas")
else:
    print(f"{c} y {c2} no son anagramas")
```
### Ejercicio 09
```python

```
### Ejercicio 10
```python
c = input("Introduce la cadena: ")

cadenaNueva = ""

for i in c:
    if i.isalnum():
        cadenaNueva += i
print(cadenaNueva)
```
### Ejercicio 11
```python
c = input("Introduce la cadena: ")

c = c.title()
c = c.replace("-","")
c = c.replace(" ","")

print(c)
```
### Ejercicio 12
```python
c = input("Introduce la cadena: ")
pc = c[0]
cantidad = 0
s = ""

for i in range (len(c)):
    caracter = c[i]
    
    if pc == caracter:
        cantidad += 1
    else:
        s += pc + str(cantidad)
        cantidad = 1
    pc = caracter

s += pc + str(cantidad)
print(s)
```
### Ejercicio 12
```python
c = input("Introduce la cadena codificada: ")
s = ""

for i in range(0, len(c), 2):
    caracter = c[i]
    cantidad = int(c[i + 1])
    s += caracter * cantidad

print(s)
```

