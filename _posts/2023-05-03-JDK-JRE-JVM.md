---
title: JDK - JRE - JVM
author: Victor Ponce
date: 2022-07-19 11:33:00 -0400
categories: [Java]
tags: [Java]
math: true
mermaid: true
---

# JDK - JRE - JVM

- Los acrónimos de cada una de estas herramientas son:

1. JRE (Java Runtime Environment)
2. JVM (Java Virtual Machine)
3. JDK (Java Development Kit)

## Jerarquía de las herramientas

![Jerarquía de las herramientas](https://refreshjava.com/images/java/jdkJreJvm.png)

## Explicación de cada herramienta

1. JVM (Java Virtual Machine): la máquina virtual de Java es la encargada de procesar el bytecode generado por un compilador de java (se puede usar esta compilador con la herramienta **javac** que provee el JDK como se verá luego) y lo tranduce a instrucciones que pueden ser interpretadas por el CPU de nuestra computadora.
   ![Funcionamiento básico de la JVM](https://cdn.educba.com/academy/wp-content/uploads/2019/11/Java-Virtual-Machine.png.webp)_Funcionamiento básico de la JVM_

2. JRE (Java Runtime Environment): esta herramienta incluye a la JVM y además incluye otras librerías y ficheros **jar** que son utilizados por la JVM en tiempo de ejecución.
3. JDK (Java Development Kit): esta herramienta engloba a la JVM, al JRE y también herramientas **java. javac**, debuggers y JavaDoc que son las que permiten el desarrollo de software con Java.
