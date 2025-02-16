# reto10_Nicolas_Alejandro_Monroy_Gomez

Desarrolle la mayoría de ejercicios en clase, por cado punto resuelto en clase tendrá media décima en el examen 2 (créanme, las van a necesitar). Para cada punto cree un programa individual. Al finalizar suba todo a un repo y súbalo al canal reto_11 en slack.

1. Desarrolle un programa que permita realizar la [suma/resta de matrices](https://es.wikipedia.org/wiki/Adici%C3%B3n_matricial). El programa debe validar las condiciones necesarias para ejecutar la operación.

```python
##Suma de matrices

def imprimir_matriz(matriz): #Funcion para mostrar la matriz como se debe ver
    for fila in matriz:
        print(fila)

def ingresar_matriz(filas, columnas):#Funcion para ingresar las matrices por consola
    matriz = [] #Lista vacia donde se almacenara la matriz ingresada
    print(f"Ingrese los elementos de la matriz {filas}x{columnas}:")
    for i in range(filas): #Rango para las filas
        fila = [] #Lista vacia donde se almacenara cada fila
        for j in range(columnas): #Rango para las columnas, recorre cada fila con un numeo determinado de iteraciones
            valor = float(input(f"Elemento [{i+1}][{j+1}]: ")) #Ingreso del valor de cada elemento de acuerdo a su pocision en la matriz
            fila.append(valor) #Añade el valor al final de la fila
        matriz.append(fila) #Añade cada fila a la matriz
    return matriz

def suma_matriz(matriz1, matriz2): #Función para sumar las dos matrices
    filas = len(matriz1)
    columnas = len(matriz1[0])
    resultado = [] #Lista donde se acumulara el resultado
    for i in range(filas): #Recorrido de cada fila
        fila_resultado = [] #Lista donde se acumulara el resultado de cada fila
        for j in range(columnas): #Recorrido para las columnas
            fila_resultado.append(matriz1[i][j] + matriz2[i][j]) #Añade la suma de los elemntos de la smatrices a la lista vacia de las filas
        resultado.append(fila_resultado) #Se añade a la matriz resultado la fla despues de haberse sumado todo
    return resultado


if __name__ == "__main__": #Función principal

    filas = int(input("Ingresa el número de filas para las matrices: ")) #ingreso de las filas de las dos matrices
    columnas = int(input("Ingresa el número de columnas para las matrices: ")) #Ingreso de las columnas de las dos matrices
    
    print("Ingresa la primera matriz:")
    matriz1 = ingresar_matriz(filas, columnas) #ingresamos la primera matriz
    
    print("Ingresa la segunda matriz:")
    matriz2 = ingresar_matriz(filas, columnas) #Ingresamos la segunda matriz
    
    print("Matriz 1:")
    imprimir_matriz(matriz1) #Imprimimos la primera matriz como se debe de ver una
    
    print("Matriz 2:")
    imprimir_matriz(matriz2) #Imprimimos la segunda matriz como se debe de ver una
    
    print("Resultado de la suma de matrices:") #Sumamos las dos matrices usando la función de suma
    suma = suma_matriz(matriz1, matriz2) 
    imprimir_matriz(suma) #imprimimos la suma
```

```python
##Resta de matrices

def imprimir_matriz(matriz): #Funcion para mostrar la matriz como se debe ver
    for fila in matriz:
        print(fila)

def ingresar_matriz(filas, columnas):#Funcion para ingresar las matrices por consola
    matriz = [] #Lista vacia donde se almacenara la matriz ingresada
    print(f"Ingrese los elementos de la matriz {filas}x{columnas}:")
    for i in range(filas): #Rango para las filas
        fila = [] #Lista vacia donde se almacenara cada fila
        for j in range(columnas): #Rango para las columnas, recorre cada fila con un numeo determinado de iteraciones
            valor = float(input(f"Elemento [{i+1}][{j+1}]: ")) #Ingreso del valor de cada elemento de acuerdo a su pocision en la matriz
            fila.append(valor) #Añade el valor al final de la fila
        matriz.append(fila) #Añade cada fila a la matriz
    return matriz

def resta_matriz(matriz1, matriz2): #Función para sumar las dos matrices
    filas = len(matriz1)
    columnas = len(matriz1[0])
    resultado = [] #Lista donde se acumulara el resultado
    for i in range(filas): #Recorrido de cada fila
        fila_resultado = [] #Lista donde se acumulara el resultado de cada fila
        for j in range(columnas): #Recorrido para las columnas
            fila_resultado.append(matriz1[i][j] - matriz2[i][j]) #Añade la resta de los elemntos de las matrices a la lista vacia de las filas
        resultado.append(fila_resultado) #Se añade a la matriz resultado la fla despues de haberse restado todo
    return resultado


if __name__ == "__main__": #Función principal

    filas = int(input("Ingresa el número de filas para las matrices: ")) #ingreso de las filas de las dos matrices
    columnas = int(input("Ingresa el número de columnas para las matrices: ")) #Ingreso de las columnas de las dos matrices
    
    print("Ingresa la primera matriz:")
    matriz1 = ingresar_matriz(filas, columnas) #ingresamos la primera matriz
    
    print("Ingresa la segunda matriz:")
    matriz2 = ingresar_matriz(filas, columnas) #Ingresamos la segunda matriz
    
    print("Matriz 1:")
    imprimir_matriz(matriz1) #Imprimimos la primera matriz como se debe de ver una
    
    print("Matriz 2:")
    imprimir_matriz(matriz2) #Imprimimos la segunda matriz como se debe de ver una
    
    print("Resultado de la resta de matrices:") #Restamos las dos matrices usando la función de suma
    resta = resta_matriz(matriz1, matriz2) 
    imprimir_matriz(resta) #Imprimimos la resta
```

2. Desarrolle un programa que permita realizar el [producto de matrices](https://es.wikipedia.org/wiki/Multiplicaci%C3%B3n_de_matrices). El programa debe validar las condiciones necesarias para ejecutar la operación.

```python
def imprimir_matriz(matriz):  #Funcion para mostrar la matriz como se debe ver
    for fila in matriz:
        print(fila)

def ingresar_matriz(filas, columnas):  #Funcion para ingresar las matrices por consola
    matriz = []  #Lista vacia donde se almacenara la matriz ingresada
    print(f"Ingrese los elementos de la matriz {filas}x{columnas}:")
    for i in range(filas):  #Rango para las filas
        fila = []  #Lista vacia donde se almacenara cada fila
        for j in range(columnas):  #Rango para las columnas, recorre cada fila con un número determinado de iteraciones
            valor = float(input(f"Elemento [{i+1}][{j+1}]: "))  #Ingreso del valor de cada elemento de acuerdo a su posición en la matriz
            fila.append(valor)  #Añade el valor al final de la fila
        matriz.append(fila)  #Añade cada fila a la matriz
    return matriz

def multiplicar_matrices(matriz1, matriz2):  #Funcion para multiplicar las dos matrices
    filas_m1 = len(matriz1)
    columnas_m1 = len(matriz1[0])
    filas_m2 = len(matriz2)
    columnas_m2 = len(matriz2[0])
    
    if columnas_m1 != filas_m2: #Aqui se verifica si las dimensiones son compatibles para la multiplicacion
        print("No se puede multiplicar las matrices, el número de columnas de la primera matriz debe ser igual al número de filas de la segunda matriz.")
        return None
    
    resultado = [[0 for _ in range(columnas_m2)] for _ in range(filas_m1)] #Crear una matriz de resultado con las dimensiones correctas
    
    for i in range(filas_m1): #Realizar el producto de las dos matrices
        for j in range(columnas_m2):
            for k in range(columnas_m1): 
                resultado[i][j] += matriz1[i][k] * matriz2[k][j]
    
    return resultado

if __name__ == "__main__":

    filas_m1 = int(input("Ingrese el número de filas para la primera matriz: ")) #Ingreso de las filas de la primera matriz
    columnas_m1 = int(input("Ingrese el número de columnas para la primera matriz: ")) #Ingreso de las columnas de la primera matriz
    
    filas_m2 = int(input("Ingrese el número de filas para la segunda matriz: ")) #Ingreso de las filas de la segunda matriz
    columnas_m2 = int(input("Ingrese el número de columnas para la segunda matriz: ")) #Ingreso de las columnas de la segunda matriz
    
    if columnas_m1 != filas_m2: #Verificacion de si las matrices se pueden multiplicar
        print("Las matrices no son compatibles para multiplicarse.")
    else:
        print("Ingresa la primera matriz:")
        matriz1 = ingresar_matriz(filas_m1, columnas_m1) #Ingresamos la primera matriz
        
        print("Ingresa la segunda matriz:")
        matriz2 = ingresar_matriz(filas_m2, columnas_m2)  #Ingresamos la segunda matriz
        
        print("Matriz 1:")
        imprimir_matriz(matriz1) #Imprimimos la primera matriz
        
        print("Matriz 2:")
        imprimir_matriz(matriz2) #Imprimimos la segunda matriz
        
        print("Resultado del producto de matrices:") #Aqui se multiplican las matrices
        producto = multiplicar_matrices(matriz1, matriz2)
        
        if producto is not None:
            imprimir_matriz(producto) #Imprimimos el resultado de la multiplicación

```

3. Desarrolle un programa que permita obtener la  [matriz transpuesta](https://es.wikipedia.org/wiki/Matriz_transpuesta) de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la operación.

```python
def es_matriz_valida(matriz): #Funcion para validar la matriz ingresada
    if not matriz: #Verifica si la matriz esta vacia
        return False
    num_columnas = len(matriz[0]) #Obtiene el numero de columnas de la primera fila
    for fila in matriz:  #Recorre cada fila de la matriz
        if len(fila) != num_columnas:  #Verifica si todas las filas tienen el mismo numero de columnas
            return False
    return True  

def transponer_matriz(matriz): #Funcion para obtener la transpuesta de una matriz valida
    if not es_matriz_valida(matriz): #Verifica si la matriz es valida
        return None
      
    matriz_transpuesta = [] #Lista vacia para la nueva matriz, la transpuesta
    num_filas = len(matriz)
    num_columnas = len(matriz[0])
    for i in range(num_columnas):  # Recorre cada columna de la matriz original
        nueva_fila = []  #Lista vacia para las filas de la matriz transpuesta
        for j in range(num_filas):  # Recorre cada fila de la matriz original
            nueva_fila.append(matriz[j][i])  #Añade el elemento a la nueva matriz
        matriz_transpuesta.append(nueva_fila)  #Añade la nueva fila a la matriz transpuesta
    return matriz_transpuesta  #Devuelve la matriz transpuesta

def ingresar_matriz(): #Funcion para ingresar por consola la matriz
    matriz = []  #Lista vacia para la matriz
    num_filas = int(input("Ingrese el número de filas de la matriz: "))  #Numero de filas
    num_columnas = int(input("Ingrese el número de columnas de la matriz: "))  #Numero de columnas
    for i in range(num_filas):
        fila = input(f"Ingrese los elementos de la fila {i+1} separados por espacio: ").split()
        fila = [int(elemento) for elemento in fila]  # Convertir cada elemento a entero usando un bucle
        matriz.append(fila)
    return matriz


if __name__ == "__main__":
    matriz = ingresar_matriz() #Llama a la función para ingresar la matriz
    if es_matriz_valida(matriz): #Verifica si la matriz ingresada es valida
        matriz_transpuesta = transponer_matriz(matriz) #Llama a la función para transponer la matriz
        print("Matriz transpuesta:")
        for fila in matriz_transpuesta: # Recorre cada fila de la matriz transpuesta
            print(fila)  # Imprime la fila
    else:
        print("La matriz ingresada no es válida.")  # Imprime un mensaje indicando que la matriz no es válida
```

4. Desarrollar un programa que sume los elementos de una columna dada de una matriz.

```python
def ingresar_matriz(): #Función para el ingreso de la matriz
    filas = int(input("Ingresa el número de filas de la matriz: ")) #ingreso de filas
    columnas = int(input("Ingresa el número de columnas de la matriz: ")) #Ingreso de columnas
    matriz = [] #Lista vacia apara acumular la matriz
   
    for i in range(filas):
        elementos_fila = input(f"Ingresar los elementos de la fila {i + 1}, separados por espacios: ").split() #Ingreso de los elementos
        fila = [int(elemento) for elemento in elementos_fila]
        matriz.append(fila)  #Añadir la fila a la matriz
    return matriz

def suma_columna(matriz, columna):
    suma = 0 #iniciamos la suma en 0
    for fila in matriz: #recorre la matriz en busca de los elemntos de la columna dada
        suma += fila[columna]
    return suma

if __name__ == "__main__":
    matriz = ingresar_matriz() #Llamar a la función para ingresar la matriz por consola
    columna = int(input("Ingresa el índice de la columna que deseas sumar (indexada desde 0): ")) #Ingreso de la columna a sumar
    resultado = suma_columna(matriz, columna) #llama a la funcion para sumar la columna
    print(f'La suma de los elementos de la columna {columna} es: {resultado}') #Se imprime el resultado
```

5. Desarrollar un programa que sume los elementos de una fila dada de una matriz.

```python
def ingresar_matriz(): # Función para el ingreso de la matriz
    filas = int(input("Ingresa el número de filas de la matriz: ")) # Ingreso de filas
    columnas = int(input("Ingresa el número de columnas de la matriz: ")) # Ingreso de columnas
    matriz = [] # Lista vacía para acumular la matriz
    
    for i in range(filas):
        elementos_fila = input(f"Ingresar los elementos de la fila {i + 1}, separados por espacios: ").split() # Ingreso de los elementos
        fila = [int(elemento) for elemento in elementos_fila]  # Convertir cada elemento a entero
        matriz.append(fila)  # Añadir la fila a la matriz
    return matriz

def suma_fila(matriz, fila_index):
    suma = 0 # Inicializamos la suma en 0
    for elemento in matriz[fila_index]: # Recorremos los elementos de la fila especificada
        suma += elemento
    return suma

if __name__ == "__main__":
    matriz = ingresar_matriz() # Llamar a la función para ingresar la matriz por consola
    fila_index = int(input("Ingresa el índice de la fila que deseas sumar (indexada desde 0): ")) # Ingreso de la fila a sumar
    resultado = suma_fila(matriz, fila_index) # Llama a la función para sumar la fila
    print(f'La suma de los elementos de la fila {fila_index} es: {resultado}') # Se imprime el resultado
```

**Nota:** Todos los puntos deben estar debidamente comentados y utilizar funciones para su desarrollo.
