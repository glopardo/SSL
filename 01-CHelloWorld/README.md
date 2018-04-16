# TP1 - Fases de la traducción y errores
Gabriel Lopardo  
K2051  
Pasos realizados:  
2.- cc hello2.c -E -P -o hello2.i  
Se genera archivo de texto de texto cuyo contenido es: el contenido de stdio.h seguido del contenido de hello2.c, el preprocesador reemplazo la línea #include <stdio.h> por todas las declaraciones de las funciones que se encuentran en esa librería.  
4.- La primer línea es: int printf(const char* s, ...); su semántica es: declarar una función cuyo identificador es "printf", su tipo de datos de retorno es int, y recibe como mínimo un parámetro de tipo puntero a char y puede recibir infinitos parámetros más.  
5.- cc hello3.c -E -P -o hello3.i  
La diferencia entre hello3.c y hello3.i es que el segundo no tiene líneas en blanco y reemplaza las tabulaciones por espacios. Luego el contenido es el mismo.  
6.- Error de compilación: expected declaration or statement at end of input  
7.- cc hello4.c -E -P -o hello4.i ; cc hello4.i -S -o hello4.s  
8.- hello4.s contiene el código en Assembler del programa escrito en hello4.c  
9.- cc hello4.s -c  
10.- cc hello4.o -o hello4  
Error de vinculación, el linker no encuentra la definición de la función prontf()  
11.- cc hello5.c -o hello5  
Warning avisando que se espera un int como segundo parámetro en la llamada a printf.  
./hello5  
Al ejecutarse muestra cualquier resultado ya que no lo controlamos: La respuesta es -1674515720  
13.- cc hello6.c -o hello6  
./hello6  
Se compila y vincula sin errores ni warnings, al ejecutarse el resultado es el deseado.  
14.- El compilador detecta una declaración implícita de printf y arroja un warning diciendo que: se incluya <stdio.h> o bien se provea una declaración de "printf".  
El compilador reconoce printf como una función de la biblioteca standard  
