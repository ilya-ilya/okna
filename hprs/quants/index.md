---
layout: default
title: Количественные формулы
use_math: true

---

# Количественные формулы. Домашнее задание

### Оглавление
1. [Закон Амдала](#amdahl)
2. [Средние](#means)

## Закон Амдала <a name="amdahl" />

1. A common transformation required in graphics processors is square root.
Implementations of floating-point ``(FP)`` square root vary significantly in performance,
especially among processors designed for graphics. Suppose FP square root
``(FSQRT)`` is responsible for 20% of the execution time of a critical graphics benchmark.
One proposal is to enhance the FSQRT hardware and speed up this operation
by a factor of 10. The other alternative is just to try to make all FP instructions in the
graphics processor run faster by a factor of 1.6; FP instructions are responsible for
half of the execution time for the application. The design team believes that they
can make all FP instructions run 1.6 times faster with the same effort as required for
the fast square root. Compare these two design alternatives.
1.  Assume that we are considering enhancing a quad-core machine by adding encryption hardware to it. When computing
encryption operations, it is 20 times faster than the normal mode of execution.
We will define percentage of encryption as the percentage of time in the original
execution that is spent performing encryption operations.
  * With what percentage of encryption will adding encryption hard-
ware result in a speedup of 2?
  * What percentage of time in the new execution will be spent on
encryption operations if a speedup of 2 is achieved?
  *  Suppose you have measured the percentage of encryption to be
50%. The hardware design group estimates it can speed up the encryption hard-
ware even more with significant additional investment. You wonder whether
adding a second unit in order to support parallel encryption operations would
be more useful. Imagine that in the original program, 90% of the encryption
operations could be performed in parallel. What is the speedup of providing
two or four encryption units, assuming that the parallelization allowed is limited
to the number of encryption units?
1. Assume that we make an enhancement to a computer that improves
some mode of execution by a factor of 10. Enhanced mode is used 50% of the time,
measured as a percentage of the execution time *when the enhanced mode is in use*.
Recall that Amdahl’s Law depends on the fraction of the original, unenhanced execution time that could make use of enhanced mode.
Thus we cannot directly use
this 50% measurement to compute speedup with Amdahl’s Law.
  * What is the speedup we have obtained from fast mode?
  * What percentage of the original execution time has been converted to fast mode?

## Средние <a name="means">
1. Пусть у нас имеются два набора чисел $a_1, \ldots, a_n$ и $b_1, \ldots, b_n$.
Покажите, что:

$$
	GM(\cfrac{a_1}{b_1}, \ldots, \cfrac{a_n}{b_n}) =
	\cfrac{GM(a_1, \ldots, a_n)}{GM(b_1, \ldots, b_n)},
$$

где $GM$ -- геометричесоке среднее.
1. В обозначениях из [теории]({{ site.baseurl }}/theory/quants/#means) покажите, что отношение
$GM(A_1, \dots, A_n)$ к $GM(B_1, \dots, B_n)$ равно среднему отношению производительности систем $A$ и $B$.
1. Покажите, что для *арифметического среднего* утверждения задач 1 и 2 не выполняются.
