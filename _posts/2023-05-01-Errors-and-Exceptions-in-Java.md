---
title: Errores y Excepciones en Java
author: Victor Ponce
date: 2023-05-01 11:33:00 -0400
categories: [Java]
tags: [Java]
math: true
mermaid: true
---

# Errores y Excepciones en Java

## Jerarquía de errores y excepciones

- Teóricamente los errores y excepciones no son más que clases que se encuentran dentro del package **java.lang** y su jerarquía se muestra en la imagen a continuación:
  ![Jerarquía de errores y excepciones](https://www.buscaminegocio.com/img/excepciones-capturar.png)

### Errores

- Según la imagen mostrada los errores pueden entenderse como excepciones o eventos que ocurren y son revisados en tiempo de ejecución. A diferencia de las excepciones, que se manejan con bloques **try-catch** por ejemplo, los errores no deben ser manejados ya que son eventos que no deberían ocurrir y uno nunca quiere que ocurran errores. Tomemos por ejemplo un **AssertionFailedError** en un test que ocurre porque una aserción falló. Esto no se debe manejar porque nunca debería ocurrir ya que uno no programa sus tests para que fallen.
  ![AssertionFailedError](/assets/img/assertion_failed_error.png)

### Checked Exceptions

Estas excepciones se llaman así debido a que son verificadas en tiempo de compilación. El compilador de Java e incluso un IDE avanzado como IntelliJ nos alertan si el código que estamos escribiendo nos lanzará una Checked Exception. Entre estas excepciones tenemos:

- ClassNotFoundException
- SocketException
- SQLException
- IOException
- FileNotFoundException

### Unchecked Exceptions

Son excepciones que son subclaes de **RuntimeException** debido a que ocurren en tiempo de ejecición. Entre estas excepciones tenemos:

- NullPointerException
- ClassCastException
- ArithmeticException
- DateTimeException
- ArrayStoreException
