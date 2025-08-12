# Ejercicios de bucles 

## Ejercicio 2

se requiere un algoritmo para determinar, de N cantidades, cuantas son cero, cuantas son menores a cero y cuantas son mayores a cero

Realice el diagrama de flujo y el pseudocodigo representarlo utilizando el ciclo apropiado.

```
Inicio
Leer N
ceros = 0
mayores = 0
menores = 0
Mientras N > 0:
    Leer cant
    Si cant > 0:
       mayores = mayores + 1
    Si no
       Si cant = 0:
          ceros = ceros + 1
       Si no
          menores = menores + 1
       Fin si
    Fin Si
    N = N - 1
Fin Mientras
Escribir ceros, mayores, menores
Fin
```






## Ejercicio 3

calcular el factorial de un numero entero ingresado por el usuario.

```
Inicio
