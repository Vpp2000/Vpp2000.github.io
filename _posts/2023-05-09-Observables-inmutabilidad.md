---
title: Inmutabilidad de los observables
author: Victor Ponce
date: 2023-05-09 11:33:00 -0400
categories: [Java, Project Reactor]
tags: [Java, Project Reactor]
math: true
mermaid: true
---

# Inmutabilidad de los observables

Supongamos que tenemos el siguiente código:

```java
  public static void main(String[] args) {
        Flux<Integer> numbers = Flux.just(1, 2, 3, 4, 5, 6, 7).map(n -> n * 10); (1)

        numbers.filter(n -> n % 20 == 0);  (2)

        numbers.subscribe(n -> System.out.println("Number " + n)); (3)
    }
```

Inicialmente pensé que en (1) se generaba nuestro flujo de datos (u observable) y se definía que al recorrerlos se les multiplica por 10, que en (2) se filtran los multiplos de 20 y que en (3) se accede al flujo de datos final y se imprimirían todos los números múltiplos de 20. Sin embargo, la salida final del programa es la siguiente:

```
Number 10
Number 20
Number 30
Number 40
Number 50
Number 60
Number 70
```

¿Por qué ocurre esto?

Esto ocurre debido a que **LOS OBSERVABLES SON INMUTABLES**.
Lo que ocurre en cada línea es lo siguiente:

- En (1) se genera un observable con el flujo inicial de datos y se especifica que se desea que se multiplique por 10 a cada valor al momento de acceder a dicho flujo de datos.
- En (2) no se filtran los valores de nuestro observable inicial, sino que **SE GENERA UN NUEVO OBSERVABLE Y NUESTRO OBSERVABLE INICIAL PERMANECE INALTERADO**. De hecho podríamos tranquilamente guardar dicho observable en otra variable así:

```java
  Flux<Integer> numbersOf20 = numbers.filter(n -> n % 20 == 0);
```

Recordar que muchos operadores como filter lo que hacen es simplemente generar o retornar un nuevo observable a partir del original

- Finalmente en (3) accedemos a los datos de nuestro observable mediante nuestro método **subscribe**.
