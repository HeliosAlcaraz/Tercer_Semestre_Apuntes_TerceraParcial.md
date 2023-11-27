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
<p><strong>FUNCIONES max() y min()</strong></p>
<p>Las funciones max() y min() son herramientas para encontrar el valor <em>máximo</em> y <em>mínimo</em> en un iterable o entre varios argumentos. Estas funciones pueden ser utilizadas con una amplia gama de tipos de datos.</p>

Ambias pueden utilizarse con un parámetro <em>key</em> para especificar una función que se aplique a los elementos del iterable antes de realizar la comparación. Esto es muy útil para estructuras de datos más complejas como listas de diccionarios, donde se podría querer encontrar el elemento con el valor más bajo de una clave específica.

<p><strong>FUNCIÓN max()</strong></p>

EJEMPLO 1:

<p><code><em>numeros = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
print(max(numeros))</em></code></p>
