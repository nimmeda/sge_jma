# [UT04](../../ut04/)

## PR0401

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
isnum = False;

while isnum == False :
    num = input("Introduce un numero: ")
    if num.isnumeric():
        print("Correcto, es un numero")
        isnum = True
```

### Ejercicio 02

```python
isnum = False;

while isnum == False :
    num = input("Introduce un numero: ")
    if num.isnumeric():
        print("Correcto, es un numero")
        isnum = True
```

### Ejercicio 03
```python
n = int(input("Introduce la cantidad de * que deseas: "))

for i in range(1, n+1):
    print("*" * i)
```

### Ejercicio 04
```python
ispar = True

while ispar == True:
    n = int(input("Introduce la cantidad de * que deseas que tenga la piramide: "))
    if n % 2 != 0:
        ispar = False
        
for i in range(1,n+1,2):
    print(" " * ((n - i) // 2) + "*" * i)
```

### Ejercicio 05
```python
nmayor = float("-inf")
nmenor = float("inf")
    
for i in range (5):
    n = int(input (f"Introduce el numero {i+1}: "))
    
    if n <= nmenor:
        nmenor = n
    if n >= nmayor:
        nmayor = n
        
print("El número mayor es ",nmayor," y el menor es ",nmenor)
```

### Ejercicio 06
