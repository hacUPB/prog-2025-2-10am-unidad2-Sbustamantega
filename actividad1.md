para hallar el espacio que ocupa en el disco tres archivos primero miramos cuanto pesa cada uno

1. archivo de texto con 52383 caracteres, se tiene en cuenta que en el formato ansii se almacena el codigo que representa un numero en un byte, por lo cual serian 52383 bytes

2. luego los datos punto flotante, suponiendo que usamos un sistema de 32 bits entonces cada dato punto flotante ocupa 32 bits, multiplicandolo por los 5433 datos y dividiendolo por 8 nos da un resultado de 21732 bytes

3. y el en



1. ¿Por qué las computadoras usan binario?
Las computadoras necesitan representar todo en binario porque, en su nivel más básico, están hechas de circuitos electrónicos que solo pueden estar en dos estados: encendido o apagado. El sistema binario, con sus dos valores (1 y 0), es la forma perfecta de representar esos dos estados. Usar este sistema hace que el procesamiento de datos sea súper eficiente y confiable para la computadora, ya que es su lenguaje "nativo".


128+0+0+16+8+0+2+1=155

El resultado es 155.

A hexadecimal: Para la conversión a hexadecimal, separamos el número en dos grupos de cuatro bits, 1001 y 1011.

1001 es un 9.

1011 es un 11, que en hexadecimal se escribe como B.

El resultado es 9B.

3. ¿Cómo se guarda una imagen PNG?
Una imagen PNG se guarda en el disco como una serie de "trozos" o bloques de datos. Cada bloque tiene información específica: hay bloques para los metadatos de la imagen (como el tamaño), otros para los datos de la imagen ya comprimidos para ahorrar espacio, y también bloques para manejar la transparencia (el famoso canal alfa). Todo está muy bien organizado.

4. ¿Qué pasa si guardas un número grande en un solo byte?
Un byte solo puede guardar números del 0 al 255. Si intentas guardar un número como 300, el byte se "desborda" porque no hay espacio suficiente.

En lenguajes como C: Ocurre un desbordamiento (overflow). En vez de guardar 300, la variable guarda el valor que resulta de "dar la vuelta al reloj" después de 255. Para 300, el resultado es 44 (300−256). Esto es un error, ya que la información se pierde.

En Python: Python es más listo con sus números enteros. Si intentas guardar 300 en una variable normal, lo hará sin problema. Sin embargo, si usas una estructura que simula bytes (bytes o bytearray), Python sí te avisará del error:

Python

bytes([300]) # Te dará un error: ValueError: bytes must be in range(0, 256)
Para guardar 300 en un formato de bytes, necesitas usar más de uno. Por ejemplo, con el método to_bytes:

Python

n = 300
b = n.to_bytes(2, byteorder='big')
print(b) # El resultado es b'\x01\x2c'
Aquí, Python usa 2 bytes:

\x01 (el primer byte) vale 1.

\x2c (el segundo byte) vale 44.

Como el orden es "big", el primer byte es el más importante. El valor completo es (1
cdot256)+44=300. Así es como Python guarda el número correctamente sin perder la información.
