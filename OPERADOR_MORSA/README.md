# OPERADOR MORSA
El operador morsa, también conocido como el operador de asignación de expresiones de fusión, es una característica relativamente nueva del lenguaje. El operador se representa mediante dos puntos seguidos de un signo igual `:=`. Su principal función es permitir la asignación de valores a variable dentro de una expresión, al mismo tiempo que se evalúa esta. 
# Asignación de variables en condicionales
Uno de los usos más habituales del operador morsa es dentro de los condicionales. Es posible que sea necesario realizar una operación, comprobar si cumple una condición y sacar el valor por pantalla. Esto, antes de la aparición del operador morsa se debía hacer en varias líneas.
>ejemplo
```python
suma = a + b
if suma > 100:
    print(f'La suma es {suma}')
Una operación que se puede simplificar mucho con esta operación.

if (suma:= a + b) > 100:
    print(f'La suma es {suma}')
```
>ejemplo:
```python
suma = a + b
if suma > 100:
    print(f'La suma es {suma}')
##Una operación que se puede simplificar mucho con esta operación.

if (suma:= a + b) > 100:
    print(f'La suma es {suma}')
```
#
>ejemplo2
```python
lista = []

while (numero := int(input('Añade número: '))) != 0:
    lista.append(numero)
    
print(lista)
```
# Asignación de variables en bucles
Otro posible uso del operador aparece en los bucles, pudiendo asignar el valor en el momento que se valida. Por ejemplo, en un bucle while en el que se está procesando un archivo se puede cargar la línea de esta antes de procesarla.
>ejemplo
```python
while (linea := archivo.readline()) != "":
    procesar_linea(linea)
Sin el operador, el código necesario sería bastante más complejo.

linea = archivo.readline()
while linea != "":
    procesar_linea(linea)
    
    linea = archivo.readline()
```