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
<hr>
<p><em><strong>Run:</strong></em></p>
<p>10</p>
