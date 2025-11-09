# [UT04](../../ut04/)

## PR0404

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
frutas = {
    "Manzana": 0.21,
    "Pera": 0.22,
    "Sandia": 1.20
}

f = input("Introduce la fruta a buscar: ")

if f in frutas:
    print("El preco de",f,"es",frutas[f],"€")
else:
    print("Esa fruta no está en la lista")
```
### Ejercicio 02
```python
productos = {
    "Electrónica": ["Smartphone", "Laptop", "Tablet", "Auriculares", "Smartwatch"],
    "Hogar": ["Aspiradora", "Microondas", "Lámpara", "Sofá", "Cafetera"],
    "Ropa": ["Camisa", "Pantalones", "Chaqueta", "Zapatos", "Bufanda"],
    "Deportes": ["Pelota de fútbol", "Raqueta de tenis", "Bicicleta", "Pesas", "Cuerda de saltar"],
    "Juguetes": ["Muñeca", "Bloques de construcción", "Peluche", "Rompecabezas", "Coche de juguete"],
}

total = 0

print("Hay", len(productos),"Categorias")

for i in productos:
    cantidad = len(productos[i])
    total += len(productos[i])
    print("Categoria: ", i ,":", cantidad, "productos")
    
print("Hay",total, "producots en total")
```
### Ejercicio 03
```python
productos = {
    "Electrónica": ["Smartphone", "Laptop", "Tablet", "Auriculares", "Smartwatch"],
    "Hogar": ["Aspiradora", "Microondas", "Lámpara", "Sofá", "Cafetera"],
    "Ropa": ["Camisa", "Pantalones", "Chaqueta", "Zapatos", "Bufanda"],
    "Deportes": ["Pelota de fútbol", "Raqueta de tenis", "Bicicleta", "Pesas", "Cuerda de saltar"],
    "Juguetes": ["Muñeca", "Bloques de construcción", "Peluche", "Rompecabezas", "Coche de juguete"],
}

total = 0

print("Hay", len(productos),"Categorias")

for i in productos:
    cantidad = len(productos[i])
    total += len(productos[i])
    print("Categoria: ", i ,":", cantidad, "productos")
    
print("Hay",total, "producots en total")
```
### Ejercicio 04
```python
asignaturas = {
    "Matemáticas": ["Ana", "Carlos", "Luis", "María", "Jorge"],
    "Física": ["Elena", "Luis", "Juan", "Sofía"],
    "Programación": ["Ana", "Carlos", "Sofía", "Jorge", "Pedro"],
    "Historia": ["María", "Juan", "Elena", "Ana"],
    "Inglés": ["Carlos", "Sofía", "Jorge", "María"],
}

while True:
    print("\n--- Menú ---")
    print("1. Listar estudiantes matriculados en una asignatura")
    print("2. Matricular un estudiante en una asignatura")
    print("3. Dar de baja un estudiante de una asignatura")
    print("4. Salir")

    opcion = input("Elige una opción (1-4): ")
    
    if opcion == "1":
        asignatura = input("introduce el nombre de la asignatura: ").strip().title()
        if asignatura in asignaturas:
            print(f"Estudiantes en {asignatura}: {asignaturas[asignatura]} ")
        else:
            print("Introduce una asignatura real.")
    
    elif opcion == "2":
        asignatura = input("introduce el nombre de la asignatura: ").title()
        if asignatura in asignaturas:
            print(f"Estudiantes en {asignatura}: {asignaturas[asignatura]} ")
            estudiante = input("introduce el nombre del estudiante: ").title()
            if estudiante not in asignaturas[asignatura]:
                asignaturas[asignatura].append(estudiante)
                print(f"Se ha matriculado a {estudiante} correctamente en {asignatura}.")        
    elif opcion == "3":
        asignatura = input("introduce el nombre de la asignatura: ").title()
        if asignatura in asignaturas:
            print(f"Estudiantes en {asignatura}: {asignaturas[asignatura]} ")
            estudiante = input("introduce el nombre del estudiante: ").title()
            if estudiante in asignaturas[asignatura]:
                asignaturas[asignatura].remove(estudiante)
                print(f"Se ha dado de baja a {estudiante} correctamente de {asignatura}.")   
    elif opcion == "4":
        print("Adiós")
        break
    else:
        print("opcion no valida")
```
### Ejercicio 05
```python
diccionario = {
    "a": 1,
    "b": 2,
    "c": 3
}

invertido = {}

for clave, valor in diccionario.items():
    invertido[valor] = clave

print(invertido)
```
### Ejercicio 06
```python
diccionario1 = {"a":1,"b":2}
diccionario2 = {"a":2,"b":3, "d":400}

for clave, valor in diccionario2.items():
    diccionario1[clave] = diccionario1.get(clave,0) + valor
print(diccionario1)
```
### Ejercicio 07
```python
empleados = {
    "Ana": 1200,
    "Luis": 950,
    "María": 1800,
    "Carlos": 1100,
    "Sofía": 2100
}

umbral = int(input("Introduce el umbral: "))

print(f"empleados con mayor salario que el umbral{umbral}: ")

for nombre, salario in empleados.items():
    if salario > umbral:
        print(f"{nombre}: {salario}€")
```
### Ejercicio 08
```python
departamentos = {
    "Recursos Humanos": {
        "Ana": "Gerente de Recursos Humanos",
        "Luis": "Especialista en Reclutamiento",
        "Elena": "Asistente de Recursos Humanos"
    },
    "Tecnología": {
        "Carlos": "Desarrollador Backend",
        "María": "Desarrolladora Frontend",
        "Pedro": "Administrador de Sistemas"
    },
    "Marketing": {
        "Sofía": "Directora de Marketing",
        "Jorge": "Especialista en SEO",
        "Laura": "Community Manager"
    },
    "Finanzas": {
        "Juan": "Analista Financiero",
        "Lucía": "Contadora",
        "Raúl": "Asesor Financiero"
    }
}

while True:
    print("\n---Menú---")
    print("1. listado de emplados por departamaento")
    print("2. Añadir un empleado a un departamento")
    print("3. Eliminar un empleado de un departamento")
    print("4. Salir")
    
    opcion = input("Introduce una opción: ")
    
    if opcion == "1":
        depart = input("Introduce el departamento: ")
        if depart in departamentos:
            print(f"Empleads en {depart}: {departamentos[depart]}")
        else:
                print("Ese departamento no existe.")    
    elif opcion == "2":
            depart = input("Introduce el departamento donde añadir un empleado: ")
            if depart in departamentos:
                empleado = input("Introduce el nombre del empleado nuevo: ")
                if empleado not in departamentos[depart]:
                    puesto = input("Introduce el puesto del empleado: ")
                    departamentos[depart][empleado] = puesto
                    print(f"Se ha añadido a {empleado} como '{puesto}' en {depart}.")
                else:
                    print("Ese empleado ya existe en el departamento.")
            else:
                print("Ese departamento no existe.")
    elif opcion == "3":
        depart = input("Introduce el departamento donde eliminar un empleado: ")
        if depart in departamentos:
            empleado = input("Introduce el nombre del empleado a eliminar: ")
            if empleado in departamentos[depart]:
                departamentos[depart].pop(empleado)
                print(f"Se ha eliminado a {empleado} de {depart}.")
            else:
                print("Ese empleado no existe en el departamento.")
        else:
            print("Ese departamento no existe.")
    elif opcion == "4":
        print("Adiós")
        break
    else:
        print("opcion no valida")
```