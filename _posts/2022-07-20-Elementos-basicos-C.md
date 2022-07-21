---
layout: single
title: Elementos basicos en C
excerpt: "Pequeño apunte en markdown sobre el lenguaje C." # resumen
date: 2022-07-20 # fecha
classes: wide #ni idea que es esto
header: #ni idea que es esto
  teaser: /assets/images/2022-07-20-Elementos-basicos-C/C_Logo.png
  teaser_home_page: true
categories: #estas son las categorias
  - Lenguaje de programación
tags: #estos son los tags
  - C
  - Sintaxis
  - Documentación
---
<p align="center">
<img src="/assets/images/2022-07-20-Elementos-basicos-C/C_Logo.png">
</p>

## Librerías basicas
Las librerías son palabras reservadas y funciones. Que nos sirven como base o ayuda en nuestro propio codigo.
Para incluir una librería en tu codigo:
~~~
#include <"librería">
~~~

### Librería estándar de entrada y salida de datos.
~~~
#include <stdio.h>
/*Funcion principal*/
int main(){
  int a;                // Declarar una variable entera
  fflush(stdin);        // Limpia la entrada de datos para evitar el desbordamiento de datos
  scanf("%d", &a);      // Escanear el teclado y asignarlo a la variable 'a'
  printf("\n%d", a);    // Mostrar el valor de la variable
  return 0;
}
~~~
### Librería matematíca.
~~~
#include <stdio.h>
#include <math.h>
/*Funcion principal*/
int main(){
  int a = 3;            // Declarar y asigna una variable
  a = pow(a,2);         // Eleva la variable 'a' al cuadrado [a^2]
  printf("\n%d", a);    // Mostrar el valor de la variable
  
  a = sqrt(a);          // Raiz cuadrada de a 
  printf("\n%d", a);    // Mostrar el valor de la variable
  return 0;
}
~~~
### Librería estándar de propósito general.
~~~
#include <stdio.h>
#include <stdlib.h>
/*Funcion principal*/
int main(){
  int min = 0, max = 10, resultado;       // Declarar y asigna las variables
  resultado = rand() % (max-min+1) + min; // Genera un numero seudoaletoreo entre min y max incluyendolos
  printf("\n%d", resultado);              // Mostrar el valor de la variable resultado
  system("pause");                        // Pausa la consola hasta que el usuario aprete cualquier tecla
  return 0;
}
~~~
## Documentación de codigo
La documentación de codigo es explicar el funcionamiento de un fragmento de codigo con comentarios
~~~
// Una linea

/*
Multiples lineas
*/
~~~
## Identación
La identacion es aquello que nos permite tener un mayor orden visual sobre el codigo, permitiendonos identificar mejor hasta donde engloba una llave, corchete o parentesis.

SIN
~~~
#include <stdio.h>

int main(){
int n = 2;
if (n == 1)
{
printf("\nHola");  
}
else if (n == 2)
{
printf("\nChao");  
}
else
{
printf("\n...");
}
}
~~~
CON
~~~
#include <stdio.h>

int main(){
  int n = 2;
  if (n == 1)
  {
    printf("\nHola");  
  }
  else if (n == 2)
  {
    printf("\nChao");  
  }
  else
  {
    printf("\n...");
  }
}
~~~
## Tipos de datos
| TIPO             | FORMATO    | DECLARACIÓN | EJEMPLO| MOSTRAR |ESCANEAR|
|-------------------|---------|---------------|-----------------|-------------------|-------------------|
| Entero | %d | int a; | int a = 10; | *printf("%d", a);* | *scanf("%d", &a);* |
| Decimal | %f | float b; | float b = 3.14; | *printf("%f", b);* | *scanf("%f", &b);* |
| Caracter | %c | char c; | char c = 'A'; | *printf("%c", c);* | *scanf("%c", &c);* |
| Cadena | %s | char d[size+1]; | char d[5] = "Hola"; | *printf("%s", d);* | *scanf("%4d", c);* |
## Control de flujo
### Condicional
IF-ELSE
~~~
if (condición)
{
  //Codigo SI se cumple la condición
}
else
{
  //Codigo NO se cumple la condición
}
~~~
SWITCH
~~~
switch(variable){
  case 1: // Si la variable es 1
    break;
  case "hola": // Si la variable es hola
    break;
  default:
    break;
}

~~~
### Bucles
WHILE
~~~
while(condición)
{
  //Repetir codigo de manera indeterminada mientras se cumpla la condición
}
~~~
FOR
~~~
for(int i = 0; condición; i++)
{
  //Repetir codigo de manera determinada mientras se cumpla la condición
}
~~~
DO-WHILE Lo uso normalmente para validar un dato que es ingresa a la fuerza. Ej: quiero ingresar un numero positivo, entonces la condicion es variable < 0
~~~
do
{
  //Repetir codigo de manera indeterminada mientras se cumpla la condición
} while(condición);
~~~
## Array o Vectores
Es una estructura de dato no dinamica (que tiene un tamaño determinado y finito)

Unidimensional **a[n]**
| 0 | 1 | ... | n-2  | n-1  |
:---:|:---:|:---:|:---:|:---:|
~~~
int main(){
  int a[n];
  a[0] = 10;    // Posicion inicial
  a[n-1] = 20;  // Posicion final
}
~~~

Bidimensional **b[i][j]**
| 0, 0 | 0, 1 |... | 0, j-2  | 0, j-1  |
:---:|:---:|:---:|:---:|:---:|
| 1, 0 | 1, 1 | ... | 1, j-2  | 1, j-1  |
| ... | ... | ... | ...  | ...  |
| i-2, 0 | i-2, 1 | ... | i-2, j-2 | i-2, j-1|
| i-1, 0 | i-1, 1 | ... | i-1, j-2 | i-1, j-1|
~~~
int main(){
  int a[i][j];
  a[0][0] = 10;    // Posicion inicial
  a[i-1][j-1] = 20;  // Posicion final
}
~~~

[Documentación C](https://devdocs.io/c/)