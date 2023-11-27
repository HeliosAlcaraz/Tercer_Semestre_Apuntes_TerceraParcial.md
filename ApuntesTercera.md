# APUNTES DE LA SEGUNDA PARCIAL
## Programación Funcional 
<p><em><strong>Funciones de alto orden:</strong></em> Estas funciones tienen la peculidaridad de contener otras funciones como 
  parámetros de entrada o como salida [ como por ejemplo; filter(), map(), reduce()].</p>
<hr>
  EJEMPLO 1:

<p><code><em>def apply_operation(x, operation):
    return operation(x)
def double(x):
    return x * 2
result = apply_operation(5, double)
print(result)</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>10</p>
<hr>
  EJEMPLO 2:
<p><code><em>def repeat_func(func, n):
    def new_func(x):
        for i in range(n):
          x = func(x)
          return x
    return new_func
def double(x):
    return x * 2
double_three_times = repeat_func(double, 3)
print(double_three_times(5)) </em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>10</p>
<hr>
<hr>
<p><strong>FUNCIONES max() y min()</strong></p>
<p>Las funciones max() y min() son herramientas para encontrar el valor <em>máximo</em> y <em>mínimo</em> en un iterable o entre varios argumentos. Estas funciones pueden ser utilizadas con una amplia gama de tipos de datos.</p>

Ambias pueden utilizarse con un parámetro <em>key</em> para especificar una función que se aplique a los elementos del iterable antes de realizar la comparación. Esto es muy útil para estructuras de datos más complejas como listas de diccionarios, donde se podría querer encontrar el elemento con el valor más bajo de una clave específica.

<p><strong>FUNCIÓN max()</strong></p>
<hr>
EJEMPLO 1:

<p><code><em>numeros = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
print(max(numeros))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>9</p>
<hr>
EJEMPLO 2:

<p><code><em>caracteres = "hola mundo"
print(max(caracteres))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>u</p>
<hr>
EJEMPLO 3:

<p><code><em>palabras = ["manzana", "banana", "cereza"]
print(max(palabras))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>manzana</p>
<hr>
EJEMPLO 4:

<p><code><em>print(max(1, 2, 3, 4, 5))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>5</p>
<hr>
EJEMPLO 5:

<p><code><em>tuplas = [(1, 'uno'), (2, 'dos', 'extra'), (3, 'tres')]
print(max(tuplas, key=len))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>(2, 'dos', 'extra')</p>
<hr>
EJEMPLO 6:

<p><code><em>estudiantes = [{'nombre': 'Ana', 'calificacion': 90}, {'nombre': 'Juan', 'calificacion': 85}]
print(max(estudiantes, key=lambda x: x['calificacion']))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>{'nombre': 'Ana', 'calificacion': 90}</p>
<hr>
EJEMPLO 7:

<p><code><em>listas = [[15, 5], [30, 40, 50], [5, 15]]
print(max(listas, key=sum))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>[30, 40, 50]</p>
<hr>
EJEMPLO 8:

<p><code><em>listas = [[15, 5], [30, 40, 50], [5, 15]]
print(sum(max(listas, key=sum)))</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>120</p>
<hr>
EJEMPLO 9:

<p><code><em>class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
personas = [Persona("Santiago", 36), Persona("Israel", 36), Persona("Andrés", 23)]
mayor = max(personas, key=lambda x: x.edad)
print(mayor.nombre)</em></code></p>

<p><em><strong>Run:</strong></em></p>
<p>Santiago</p>
<hr>
