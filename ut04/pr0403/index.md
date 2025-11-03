# [UT04](../../ut04/)

## PR0403

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
- [Ejercicio11](./index.md/#ejercicio-11)
- [Ejercicio12](./index.md/#ejercicio-12)
- [Ejercicio13](./index.md/#ejercicio-13)

### LISTA
```python
nombres = [
    "Alejandro", "María", "Javier", "Lucía", "Carlos", "Sofía", "Miguel", "Ana", "Manuel", "Isabel", "Pedro", "Carmen",
    "Jorge", "Elena", "Juan", "Laura", "Antonio", "Patricia", "David", "Claudia", "Francisco", "Marta", "Sergio",
    "Teresa", "Luis", "Raquel", "Andrés", "Paula", "Daniel", "Verónica", "Fernando", "Sara", "Pablo", "Irene", "Álvaro",
    "Natalia", "Hugo", "Eva", "Diego", "Cristina", "Jesús", "Rosa", "Roberto", "Alicia", "Ángel", "Beatriz", "Ricardo",
    "Julia", "Adrián", "Silvia", "Alberto", "Victoria", "Raúl", "Pilar", "Ramón", "Lidia", "Óscar", "Ariadna", "Gonzalo",
    "Mónica", "Rubén", "Esther", "Santiago", "Nuria", "Iván", "Ainhoa", "Eduardo", "Berta", "Marcos", "Noelia", "Enrique",
    "Elisa", "Emilio", "Fátima", "Vicente", "Gabriela", "Mario", "Olga", "Rafael", "Lorena", "Mariano", "Cristina",
    "Eugenio", "Mercedes", "Félix", "Amparo", "Sebastián", "Rocío", "Alfredo", "Esperanza", "Álex", "Celia", "Héctor",
    "Andrea", "Tomás", "Inés", "Marcelo", "Gloria", "Marina", "Belén", "Valentín", "Miriam", "Guillermo", "Ángela",
    "Joaquín", "Gemma", "Fabián", "Daniela", "Víctor", "Dolores", "Marcos", "Tamara", "Braulio", "Lourdes", "Federico",
    "Gema", "Julián", "Nicolás", "Leandro", "Manuela", "Agustín", "Elsa", "Julio", "Consuelo", "Ismael", "Alejandra",
    "Joaquín", "Milagros", "Gregorio", "Inmaculada", "Salvador", "Carla", "Esteban", "Carolina", "Fausto", "Emilia",
    "Alfonso", "Amalia", "Baltasar", "Adela", "Humberto", "Blanca", "Aníbal", "Araceli", "César", "Candela"
]
```

### Ejercicio 1
```python
print("1️Nombres ordenados alfabéticamente en orden inverso:")
for nombre in sorted(nombres, reverse=True):
    print(nombre)
```
### Ejercicio 2
```python
contador = 0

for nombre in nombres:
    if nombre.lower().startswith("a"):
        contador += 1

print("Número de nombres que comienzan con la letra A:", contador)
```
### Ejercicio 3
```python
nombre = input("Introduce tu nombre: ")

if nombre in nombres:
    posicion = nombres.index(nombre)
    print(f"El nombre {nombre} está en la lista, en la posición {posicion}.")
else:
    print(f"El nombre {nombre} no se encuentra en la lista.")
```
### Ejercicio 4
```python
nombre = input("Introduce tu nombre: ")

if nombre in nombres:
    posicion = nombres.index(nombre)
    print("Los nombres que van antes del tuyo son:")
    print(nombres[:posicion])
else:
    print("Ese nombre no está en la lista.")
```
### Ejercicio 5
```python
numero = int(input("Introduce una longitud de nombre: "))
contador = 0

for nombre in nombres:
    if len(nombre) == numero:
        contador += 1

print(f"Hay {contador} nombres con {numero} letras.")
```
### Ejercicio 6
```python
nombres_cortos = []

for nombre in nombres:
    if len(nombre) <= 4:
        nombres_cortos.append(nombre)

print("Nombres con 4 o menos letras:")
print(nombres_cortos)
```
### Ejercicio 7
```python

```
### Ejercicio 8
```python

```
### Ejercicio 9
```python
numeros = [3, 7, 2, 9, 5]
suma = sum(numeros)
print("La suma de los elementos es:", suma)
```
### Ejercicio 10
```python
palabras = ["hola", "mundo", "hola", "python", "hola"]
palabra = input("Ingresa una palabra: ")
contador = palabras.count(palabra)
print(f"La palabra '{palabra}' aparece {contador} veces.")
```
### Ejercicio 11
```python
numeros = [1, 2, 3, 2, 4, 1, 5, 3]
sin_duplicados = []

for n in numeros:
    if n not in sin_duplicados:
        sin_duplicados.append(n)

print("Lista sin duplicados:", sin_duplicados)
```
### Ejercicio 12
```python
numeros = [5, 12, 7, 3, 9]

mayor = max(numeros)
menor = min(numeros)

print(f"Máximo: {mayor}, Mínimo: {menor}")

```
### Ejercicio 13
```python
numeros = [1, 2, 3, 4, 5, 6, 7, 8]
pares = []

for n in numeros:
    if n % 2 == 0:
        pares.append(n)

print("Números pares:", pares)
```
### Ejercicio 14
```python
numeros = [10, 20, 30, 40, 50]
invertida = numeros[::-1]
print("Lista invertida:", invertida)
```