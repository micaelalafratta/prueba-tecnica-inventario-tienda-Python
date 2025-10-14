# Léeme:
## /English below/ 👇🏽

¡Hola, Adalaber! Lee atentamente qué encontrarás en este repositorio.

## Contenido del respositorio: 
Aquí encontrarás los archivos de la evaluación de Micaela Lafratta del Módulo 1: Descubre el poder de Pyhton. 

## Archivos:
Por un lado, encontrarás el archivo "Evaluación-final-micaelalafratta.ipynb".
En él, está el ejercicio final completo.

Por otro lado, encontrarás el archivo "Bonus-micaelalafratta.ipynb".
En él, está el bonus del ejercicio final.

## Estructura del ejercicio final:
El archivo "Evaluación-final-micaelalafratta.ipynb" se compone de varias partes:

Primero encontrarás la CLASE TiendaOnline, así como los métodos correspondientes, por orden. Después, dividido en apartados, encontrarás el resto del código que llama a esos métodos para realizar las tareas que pide el ejercicio. 

El código dispone de títulos, comentarios y prints de control para ir entendiendo el funcionamiento. 

## Ejemplo de qué encontrarás dentro:

### Por ejemplo, al principio encontrarás la CLASE y el primer método: 
```python
class TiendaOnline:
    def __init__(self):

        self.inventario = [] #lista de diccionarios  #la tienda empieza vacía de inventario
        self.ventas_totales = float(0) #la tienda empieza vacía de ventas

    
    def agregar_producto(self, nombre, precio, cantidad):
        print(nombre, precio, cantidad) #Print control
        for producto in self.inventario:  #bucle for para iterar productos
            print(f"Control de producto en inventario: {producto}")
            if nombre.lower() == producto["nombre"]: #Si hay coincidencia, ya existe.
                #Obtenemos el valor usando la CLAVE del diccionario, en este caso ["nombre"]
                print(f"{producto["nombre"]} ya existe")

                producto["cantidad"] = producto["cantidad"] + cantidad  
                #Si el producto ya existe, actualiza cantidad de producto. 
                #Cantidad existente actualizada usando la CLAVE del diccionario + cantidad nueva. Otra manera: +=cantidad
                print(f"Control de inventario, actualización de cantidad de producto: {self.inventario}")
                return  
        #🛑El código llega hasta aquí en el BUCLE FOR. Si el producto está en el inventario, entra en el BUCLE FOR. 
        

        #👇🏽Si no, el código sigue FUERA DEL BUCLE FOR:
        nuevo_producto = {"nombre": nombre.lower(), "precio" : precio, "cantidad" : cantidad}  #Como diccionario. Cada diccionario se convierte en un elemento de la lista self.inventario.
        print(f"Control de nuevo producto: {nuevo_producto}")
        self.inventario.append(nuevo_producto) #Añadir nuevo producto
        print(f"Control de inventario, actualización de nuevo producto: {self.inventario}")

```
### Después, encontrarás el código que llama a esa CLASE y a ese MÉTODO: 
```Python
tienda = TiendaOnline()     
#Crear una tienda que llame a la CLASE TiendaOnline()

("-----------------------------")

tienda.agregar_producto("Camiseta", 12, 300) 
#El código llama por orden. Si no hay, añade producto. 

tienda.agregar_producto("Camisa", 24.99, 200)  
#Nuevo producto, no coincidencia con lo anterior.

tienda.agregar_producto("Polo", 25, 100)
tienda.agregar_producto("polo", 25, 15) 
#suma el producto a "Polo" porque .lower()

tienda.agregar_producto("Pantalón", 19.99, 250)
#Nuevo producto, no coincidencia con lo anterior.

tienda.agregar_producto("Calcetines", 2.99, 100)
#Nuevo producto, no coincidencia con lo anterior.
```
# /English/ 👇🏽

Hello, Adalaber! Please read carefully what you will find in this repository.

## Repository contents: 
Here you will find the files for Micaela Lafratta's assessment of Module 1: Discover the power of Python. 

## Files:
On the one hand, you will find the file‘Evaluación-final-micaelalafratta.ipynb’.
This contains the complete final exercise.

On the other hand, you will find the file ‘Bonus-micaelalafratta.ipynb’.
This contains the bonus exercise.

## Exercise structure:
The file ‘Final-assessment-micaelalafratta.ipynb’ consists of several parts:

First, you will find the 'TiendaOnline' CLASS, as well as the corresponding methods, in order. 
Then, divided into sections, you will find the rest of the code that calls those methods to perform the tasks required by the exercise. 

The code has titles, comments, and control prints to help you understand how it works. 

## Example of what you will find inside:

### For example, at the beginning you will find the CLASS and the first method: 

```python
class TiendaOnline:
    def __init__(self):

        self.inventario = [] #lista de diccionarios  #la tienda empieza vacía de inventario
        self.ventas_totales = float(0) #la tienda empieza vacía de ventas

    
    def agregar_producto(self, nombre, precio, cantidad):
        print(nombre, precio, cantidad) #Print control
        for producto in self.inventario:  #bucle for para iterar productos
            print(f"Control de producto en inventario: {producto}")
            if nombre.lower() == producto["nombre"]: #Si hay coincidencia, ya existe.
                #Obtenemos el valor usando la CLAVE del diccionario, en este caso ["nombre"]
                print(f"{producto["nombre"]} ya existe")

                producto["cantidad"] = producto["cantidad"] + cantidad  
                #Si el producto ya existe, actualiza cantidad de producto. 
                #Cantidad existente actualizada usando la CLAVE del diccionario + cantidad nueva. Otra manera: +=cantidad
                print(f"Control de inventario, actualización de cantidad de producto: {self.inventario}")
                return  
        #🛑El código llega hasta aquí en el BUCLE FOR. Si el producto está en el inventario, entra en el BUCLE FOR. 
        

        #👇🏽Si no, el código sigue FUERA DEL BUCLE FOR:
        nuevo_producto = {"nombre": nombre.lower(), "precio" : precio, "cantidad" : cantidad}  #Como diccionario. Cada diccionario se convierte en un elemento de la lista self.inventario.
        print(f"Control de nuevo producto: {nuevo_producto}")
        self.inventario.append(nuevo_producto) #Añadir nuevo producto
        print(f"Control de inventario, actualización de nuevo producto: {self.inventario}")

```
### Next, you will find the code that calls that CLASS and that METHOD:

```Python
tienda = TiendaOnline()     
#Crear una tienda que llame a la CLASE TiendaOnline()

("-----------------------------")

tienda.agregar_producto("Camiseta", 12, 300) 
#El código llama por orden. Si no hay, añade producto. 

tienda.agregar_producto("Camisa", 24.99, 200)  
#Nuevo producto, no coincidencia con lo anterior.

tienda.agregar_producto("Polo", 25, 100)
tienda.agregar_producto("polo", 25, 15) 
#suma el producto a "Polo" porque .lower()

tienda.agregar_producto("Pantalón", 19.99, 250)
#Nuevo producto, no coincidencia con lo anterior.

tienda.agregar_producto("Calcetines", 2.99, 100)
#Nuevo producto, no coincidencia con lo anterior.
```

