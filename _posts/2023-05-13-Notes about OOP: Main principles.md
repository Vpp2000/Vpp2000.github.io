---
title: Notas sobre OOP -> Encapsulamienti, Herencia, Polimorfismo y Abstracción
author: Victor Ponce
date: 2023-05-13 11:33:00 -0400
categories: [Java, OOP]
tags: [Java, OOP]
math: true
mermaid: true
---

# Notas sobre OOP: Abstracción, Encapsulamiento, Decomposición y Generalización

Usualmente en las entrevistas de trabajo que me han permitido tener me han preguntado al menos 1 de estos principios y es por eso que considero bastante útil hablar de ellos en este post y darlos a conocer de la manera más clara posible.

La programación orientada a objetos es un paradigma que nos permite representar a las entidades de nuestros softwares o sistemas por medio de clases y los cuatro principios que explicaré a continuación son los pilares sobre los cuales se constituye este paradigma.

## Abstacción

Este principio de diseño consiste en determinar las características y funcionalidades más importantes de nuestras entidades y empaquetarlos en una clase y omitir aquellas características que no sean absolutamente necesarias para modelar correctamente nuestra entidades.

## Encapsulamiento

Al momento de diseñar las clases que representarán nuestras entidades existirán atributos y métodos que uno no desea que sean accesibles desde entidades externas y es esto básicamente de lo que trata el principio de encapsulamiento: tener la capacidad de exponer a entidades externas solo un conjunto determinado de características y métodos y un conjunto que se mantendrá oculto del resto.

## Decomposición

Este principio de diseño consiste en dividir un problema complejo o un sistema en varias partes que sean lo más pequeñas posibles para que sean fáciles de entender y mantener.
El principio es de gran utilidad dado que nos ayudará a evitar la existencia de entidades demasiado grandes y que posean una cantidad excesiva de responsabilidades y, aún más importante, responsabilidades que ni si quiera le competan.

## Generalización

En el contexto de la programación orientada a objetos, la generalización consiste en extraer métodos y características comunes de un conjunto de entidades, ubicarlos en una clase padre y mediante el mecanismo de la herencia dicha clase padre será extendida por el conjundo de entidades de los que se habló previamente en este párrafo (también conocidas como subclases) de modo que dichas subclases pueden o bien repertir el comportamiento de la clase padre o incluso sobreescribirlo.
