###### 210622_tue

<hr>




###### 오늘의 목차 :bowling:

#### Functional Programming

- Definition of Functional Programming
- The Advantages of Immutability

###### 함수형 프로그래밍?? 중요하다는데 뭔지 이해해보자

<hr>
<br>


# 2. Functional Programming

> scala는 함수형 프로그래밍이므로 그 특징을 이해하고 사용하는 것이 중요하다

## 2.1 Definition of Functional Programming

### What is functional programming?

- English Wikipedia

  > Functional Programming is a programming paradigm that treats computation as **the evaluation of mathematical functions** and **avoids changing-state and mutable data**
  >
  > - 계산을 수학적 함수의 평가로 취급
  >
  > - state 변화와 변경가능한(mutable) 데이터를 피함

- the book "Functional Programming in Scala"

  > Functional programming (FP) is based on a simple premise with far-reaching implications: we construct our proograms **using only pure functions**--in other words, functions that have no side effects.
  >
  > - 오직 순수 함수(pure functions)만 사용

###### 두 문장이 함수형 프로그래밍을 잘 설명해준다고 한다! 하나하나 살펴보자

<br>

### 1. the evaluation of mathematical functions

- Scala에서 모든 것은 표현식(expression)이고, 표현식은 값으로 평가된다(an expression is evaluated into a value)
- 프로그램은 **하나의 표현식(a single expression)**이고, 프로그램의 실행은 표현식으로 표시된 **값을 찾는 것**



<br>

## 2.2 The Advantages of Immutability

