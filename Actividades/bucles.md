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
Leer valor_compra, n_cuotas
cuota_mensual = valor_compra * (tasa_interes / (1 - (1 + tasa_interes)^(-numero_cuotas)))

saldo_pendiente = valor_compra
total_intereses = 0

Escribir "--- Plan de pagos ---"
Escribir "Cuota mensual fija: " + cuota_mensual REDONDEADO_A_2_DECIMALES

    // Iterar para cada una de las cuotas
    PARA i DESDE 1 HASTA numero_cuotas HACER
        // Calcular los intereses del mes sobre el saldo pendiente
        DEFINIR intereses_cuota = saldo_pendiente * tasa_interes

        // Calcular el abono a capital (lo que se resta de la deuda principal)
        DEFINIR abono_capital = cuota_mensual - intereses_cuota

        // Actualizar el saldo pendiente
        saldo_pendiente = saldo_pendiente - abono_capital

        // Sumar los intereses al total
        total_intereses = total_intereses + intereses_cuota

        // Mostrar los detalles de la cuota actual
        MOSTRAR "Cuota " + i + ":"
        MOSTRAR "  - Intereses: " + intereses_cuota REDONDEADO_A_2_DECIMALES
        MOSTRAR "  - Abono a capital: " + abono_capital REDONDEADO_A_2_DECIMALES
        MOSTRAR "  - Saldo pendiente: " + saldo_pendiente REDONDEADO_A_2_DECIMALES
    FIN_PARA

MOSTRAR "--- Resumen ---"
MOSTRAR "Valor total a pagar: " + (valor_compra + total_intereses) REDONDEADO_A_2_DECIMALES
MOSTRAR "Total de intereses pagados: " + total_intereses REDONDEADO_A_2_DECIMALES
FIN

```















