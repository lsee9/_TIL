###### 210621_mon

<hr>



###### 오늘의 목차 :car:

#### Loop

- for
- while
- do while
- Loop Control Statement

###### 반복하는 일은 무조건 많다!!

<hr>
<br>


# 7. Loop

> 코드 블럭(block of code)을 여러번 실행해야할 경우가 종종 발생합니다!

### Flow Chart

- Loop statement의 flow chart

  ```flow
  st=>start: Start
  cond=>condition: If condition is true?
  op1=>operation: Conditional Code
  end=>end: End
  
  st->cond
  cond(yes, right)->op1(right)->cond
  cond(no, bottom)->end
  ```

<br>

## 7.1 for

> 특정 횟수를 싱행해야하는 루프를 효율적으로 작성할 수 있는 반복 제어 구조

### 7.1.1 Syntax - for loop with ranges

- Range : 숫자 범위(range of numbers, `i to j` or `i until j`)

- generator : left-arrow, 범위에서 개별값 생성

  ```scala
  for( var x <- Range ) {
    statement(s)
  }
  ```

<br>

#### Example

- **`i to j`**
  - i부터 **j번 까지** 반복
  
  ```scala
  object ToLoop {
    def main(args: Array[String]) {
      
      for( num <- 1 to 10 ) {
        println(num)
      }
    }
  }
  ```
  
  ```scala
  1
  2
  3
  4
  5
  6
  7
  8
  9
  10
  ```
  
  <br>
  
- **`i until j`**

  - i부터 **j - 1번 까지** 반복

  ```scala
  object ToLoop {
    def main(args: Array[String]) {
      
      for( num <- 1 until 10 ) {
        println(num)
      }
    }
  }
  ```

  ```scala
  1
  2
  3
  4
  5
  6
  7
  8
  9
  ```

- **multiple ranges (nested for loop)**

  - 세미콜론(`;`)으로 구분된 여러 범위 사용 가능 (중첩 for문)
  - 주어진 범위내에 가능한 모든 계산 반복

  ```scala
  object NestLoop {
    def main(args: Array[String]) {
      
      for( x <- 1 to 2; y <- 1 to 3 ) {
        println(x, y)
      }
    }
  }
  ```

  ```scala
  (0,0)
  (0,1)
  (0,2)
  (0,3)
  (1,0)
  (1,1)
  (1,2)
  (1,3)
  (2,0)
  (2,1)
  (2,2)
  (2,3)
  ```

<br>

### 7.1.2 Syntax - for loop with Collections

> collection에는 array, list, tuple, set, map이 있으며, 이는 뒤에서 학습하겠습니다

- **List**

  - element의 리스트를 가지는 collection type
  - for loop는 한번에 한 element씩 모든 element를 반환

  ```scala
  for( var x <- List ) {
    statement(s)
  }
  ```

<br>

#### Example

- List() : collection 생성

  ```scala
  object CollecLoop {
    def main(args: Array[String]) {
      val numList = List(0, 1, 2, 3, 4, 5)
      
      for( num <- numList ) {
        println( num )
      }
    }
  }
  ```

  ```scala
  0
  1
  2
  3
  4
  5
  ```

<br>

### 7.1.3 Syntax − for loop with Filters

- 하나 또는 이상의 **if** statement를 사용해 일부 element의 필터링 가능

  ```scala
  for( var x <- List
     		if condition1; if condition2 ... ) {
    statement(s)
  }
  ```

<br>

#### Example

- List() : collection 생성

  ```scala
  object CollecLoop {
    def main(args: Array[String]) {
      val numList = List(0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
      
      for( num <- numList 
           if num > 2; if num % 2 == 1 ) {
        println( num )
      }
    }
  }
  ```

  ```scala
  3
  5
  7
  9
  ```

<br>

### 7.1.4 Syntax − for loop with yield

- List

  ```scala
  for( var x <- List ) {
    statement(s)
  }
  ```

<br>

#### Example

- List() : collection 생성

  ```scala
  object CollecLoop {
    def main(args: Array[String]) {
      val numList = List(0, 1, 2, 3, 4, 5)
      
      for( num <- numList ) {
        println( num )
      }
    }
  }
  ```

  ```scala
  0
  1
  2
  3
  4
  5
  ```

<br>

<br>

## 7.2 while



## 7.3 do while



## 7.4 Loop Control Statement

