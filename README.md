# Léeme:

¡Hola, Adalaber! Lee atentamente qué encontrarás en este repositorio.

## Contenido del respositorio: 
Aquí encontrarás los archivos de la evaluación de Micaela Lafratta del Módulo 1: Descubre el poder de Pyhton. 

## Archivos:
Por un lado, encontrarás el archivo "Evaluación-final-micaelalafratta.ipynb".
En él, está el ejercicio final completo.

Por otro lado, encontrarás el archivo "Evaluación-final-micaelalafratta.ipynb".
En él, están las notas y pruebas del ejercicio.

## Estructura ejercicio:
El archivo "Evaluación-final-micaelalafratta.ipynb" se compone de varias partes:

Primero encontrarás la CLASE TiendaOnline, así como los métodos correspondientes, por orden. Después, dividido en apartados, encontrarás el resto del código que llama a esos métodos para realizar las tareas que pide el ejercicio. 

El código dispone de títulos, comentarios y prints de control para ir entendiendo el funcionamiento. 

## Ejemplo de qué encontrarás dentro:

### Por ejemplo, al principio encontrarás la CLASE y el primer método: 
```python
class TiendaOnline:
    def __init__(self):

        self.inventario = [] #lista de diccionarios
        self.ventas_totales = 0 #la tienda empieza vacía de ventas

    
    def agregar_producto(self, nombre, precio, cantidad):
        for producto in self.inventario:  #bucle for para iterar productos
            print(f"Control de producto en inventario: {producto}")
            if nombre == producto["nombre"]: #Si hay coincidencia, ya existe.
                #Obtenemos el valor usando la CLAVE del diccionario, en este caso ["nombre"]
                print(f"{producto["nombre"]} ya existe")

                producto["cantidad"] = producto["cantidad"] + cantidad  
                #Actualizar cantidad de producto. 
                #Cantidad existente actualizada usando la CLAVE del diccionario + cantidad nueva
                print(f"Control de inventario, actualización de cantidad: {self.inventario}")
                return  
        #El código llega hasta aquí en el bucle for. 
        #Si el producto está en el inventario, entra en el bucle FOR. Si no, el código sigue:
            
        nuevo_producto = {"nombre": nombre, "precio" : precio, "cantidad" : cantidad}  #Como diccionario
        print(nombre, precio, cantidad) #Print control
        print(f"Control de nuevo producto: {nuevo_producto}")
        self.inventario.append(nuevo_producto) #Añadir nuevo producto
        print(f"Control de inventario, actualización de nuevo producto: {self.inventario}")

### Después, encontrarás el código que llama a ese método: 

tienda = TiendaOnline()     
#Crear una tienda que llame a la CLASE TiendaOnline()
```
