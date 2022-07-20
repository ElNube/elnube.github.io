---
layout: single
title: Elementos basicos en C
excerpt: "Pequeño apunte en markdown sobre el lenguaje C." # resumen
date: 2022-07-20 # fecha
classes: wide #ni idea que es esto
header: #ni idea que es esto
  teaser: /assets/images/2022-07-19-base-post/header.png
  teaser_home_page: true
categories: #estas son las categorias
  - Lenguaje C
tags: #estos son los tags
  - Aprender
---


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
  printf("\nHola Mundo"); //Mostrar información
  int a; // Iniciar una variable entera
  scanf("%d", &a); //Escanear el teclado y asignarlo a la variable 'a'
  printf("\n%d", a); //Mostrar el valor de la variable
  return 0; //
}
~~~
Esta libreria nos permite usando la palabra reservada *printf("el mostrar información en consola");*
usualmente se usa para mostrar log y errores. Aunque tambien se usa bastante para hacer programas básicos 
cuando uno esta aprendiendo el lenguaje.


[Documentación C](https://devdocs.io/c/)