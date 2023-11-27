# APUNTES DE LA SEGUNDA PARCIAL
## Programación Funcional 
<p><em><strong>Funciones de alto orden:</strong></em> Estas funciones tienen la peculidaridad de contener otras funciones como 
  parámetros de entrada o como salida [ como por ejemplo; filter(), map(), reduce()].</p>   

<p><em><code>def apply_operation(x, operation):
    return operation(x)

def double(x):
    return x * 2

result = apply_operation(5, double)
print(result)</code></em></p>
