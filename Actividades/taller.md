## Taller Ejercicio 1
En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.


|Variables|Tipo|Notas|
|---------|----|-----|
|peso maximo|Entrada|el peso maximo para despegar|
|peso_aeronave|Entrada|el peso calculado con combustible y carga|
|peso_exceso|salida|el peso por el que la aeronave supera el maximo




```
Inicio
Leer peso_aeronave
    Si peso_aeronave > peso_maximo
        peso_exceso = peso_aeronave - peso_maximo
        Escribir "La aeronave no puede despegar", "su aeronave supera el peso maximo por:", peso_exceso "Kg"
    Si no 
        Escribir "La aeronave esta lista para despegar"
    Fin Si
Fin
```