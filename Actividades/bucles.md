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
Leer N


  SI numero < 0 ENTONCES
    ESCRIBIR "No se puede calcular el factorial de un número negativo."
  SINO SI numero == 0 ENTONCES
    ESCRIBIR "El factorial de 0 es 1."
  SINO
    ASIGNAR contador = numero
    MIENTRAS contador > 0 HACER
      factorial = factorial * contador
      contador = contador - 1
    FIN MIENTRAS
    ESCRIBIR "El factorial de ", numero, " es ", factorial
  FIN SI
FIN
```





## Ejercicio 1 tarea











## Ejercicio 2 tarea

Consultar cómo funcionan las tarjetas de crédito. Asumir una tasa de interés fija (2%). Preguntar al usuario el valor de la compra y el número de cuotas. Calcular y mostrar en pantalla. El valor de cada una de las cuotas que debe pagar hasta saldar la deuda.


|variables|tipo|
|---------|----|
valor_compra|Entrada|
n_cuotas|Entrada
valor_cuota|salida|
2% |constante

```
Inicio
Definir tasa_interes = 0.02

Leer valor_compra, n_cuotas

cuota = valor_compra / n_cuotas
saldo = valor_compra
total_intereses = 0
cuota_actual = 1
  Mientras saldo > 0 Hacer
        interes = saldo * tasa_interes
        abono = cuota
        pago = interes + abono

        saldo = saldo - abono
        total_intereses = total_intereses + interes

        Escribir "Cuota " + cuota_actual + ":"
        Escribir "  - Intereses: " + interes REDONDEADO_A_2_DECIMALES
        Escribir "  - Abono a capital: " + abono REDONDEADO_A_2_DECIMALES
        Escribir "  - Total a pagar: " + pago REDONDEADO_A_2_DECIMALES
        Escribir "  - Saldo restante: " + saldo REDONDEADO_A_2_DECIMALES

        cuota_actual = cuota_actual + 1
  Fin_Mientras

    Escribir "--- Resumen ---"
    Escribir "Total intereses pagados: " + total_intereses REDONDEADO_A_2_DECIMALES
    Escribir "Total pagado: " + (valor_compra + total_intereses) REDONDEADO_A_2_DECIMALES
Fin

```


## ejercicio 4.5 libro

se requiere un algoritmo para determinar cuanto ahorrara en pesos una persona diariamente, y en un año si ahorra 3 pesos el primero de enero, 9 el dos de enero, 27 el 3 de enero y asi sucesivamente todo el año. represente la solucion mediante un diagrema de flujo

|variables|tipo|comentario|
|---------|----|----------|
|ahorro_año|salida
|monto_diario|


```
Inicio
monto_diario = 1
ahorro_acomulado = 0

  Desde i=1 hasta i=365 
      aporte_diario = monto diario * 3 
      ahorro_acomulado = ahorro_acomulado + aporte_diario
      escribir "lleva ahorrado:", ahorro_acomulado
      monto_diario = monto diario * 3
  Fin Desde
Escrbir "ahorro total del año:", ahorro_acomulado
Fin

```


