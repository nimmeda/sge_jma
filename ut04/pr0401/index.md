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
```python
c = int(input("Introduce la cantidad: "))
u = input("Introduce la unidad de medida (mm,cm,m,km): ")
uc = input("Intrduce la unidad a la que se va a convertir (mm,cm,m,km): ")

if u == "mm":
    c = c / 1000
elif u == "cm":
    c = c / 100
elif u == "km":
    c = c * 1000
    
if uc == "mm":
    c = c*1000
elif uc == "cm":
    c = c * 100
elif uc == "km":
    c = c / 1000

print("Resultado: ",c)
```
### Ejercicio 07
```python
import random

numero = random.randint(0,100)

while True:
    
    adivinado = int(input("Introduce un numero para adivinarlo: "))

    if adivinado == numero:
        print("Correcto")
        break
    else:
        print("Incorrecto")
        if adivinado < numero:
            print("Es un numero mayor")
        else:
            print("Es un numero menor")
```

### Ejercicio 08
```python
import random

cvu = 0 # Contador victorias usuario
cvr = 0 # Contador victorias rival

while cvu < 5 and cvr < 5:
    
    ou = None #opcion usuario
    
    while ou not in [1, 2, 3, 4, 5]:
        print("Introduce la opción en número: ")
        print("1- Piedra")
        print("2- Papel")
        print("3- Tijera")
        print("4- Lagarto")
        print("5- Spock")
        
        ou = int(input("Opción: "))
        
        if ou not in [1, 2, 3, 4, 5]:
            print("Opción no válida. Intenta de nuevo.")
    print("")

    oo = random.randint(1,5) #opcion ordenador (por si suena raro)
    print("Tu rival ha elegido: ")

    match oo:
        case 1:
            print("Piedra")
        case 2:
            print("Papel")
        case 3:
            print("Tijera")
        case 4:
            print("Lagarto")
        case 5:
            print("Spock")

    print("")

    match ou:
        case 1:
            if oo == 1:
                print("Empate!")
            elif oo in [2,5]:
                print("Derrota!")
                cvr = cvr + 1
            elif oo in [3,4]:
                print("Victoria!")
                cvu = cvu + 1
        case 2:
            if oo == 2:
                print("Empate!")
            elif oo in [1,5]:
                print("Victoria!")
                cvu = cvu + 1
            elif oo in [3,4]:
                print("Derrota!")
                cvr = cvr + 1
        case 3:
            if oo == 3:
                print("Empate!")
            elif oo in [2,4]:
                print("Victoria!")
                cvu = cvu + 1
            elif oo in [1,5]:
                print("Derrota!")
                cvr = cvr + 1
        case 4:
            if oo == 4:
                print("empate!")
            elif oo in [2,5]:
                print("Victoria!")
                cvu = cvu + 1
            elif oo in [1,3]:
                print("Derrota!")
                cvr = cvr + 1
        case 5:
            if oo == 5:
                print("Empate!")
            elif oo == [2,4]:
                print("Derrota!")
                cvr = cvr + 1
            elif oo == [1,3]:
                print("Victoria!")
                cvu = cvu + 1

    print("")
    print("Puntuaciones")
    print(f"Tu {cvu}")
    print(f"Rival {cvr}")
    print("")
    
print("")    
if cvu == 5:
    print("¡Has ganado la partida!")
else:
    print("El rival ha ganado la partida")
```

### Ejercicio 09
```python
nf = int(input("Cuantos numeros de la secuencia de Fibonacci quieres ver?: "))

n1 = 0
n2 = 1

for i in range(nf):
    print(n1," ")
    n1, n2= n2, n1+n2
```

### Ejercicio 10
```python
nu = int(input("Introduce un numero para saber si es primo o no: ")) #numero usuario

primo = True

for i in range(2,nu):
    if nu % i == 0:
        print("No es primo,", i, "Es divisor de ", nu)
        primo = False
if primo == True:
    print(nu," Es primo")
```
