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


# 9. Loop

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

## 9.1 for

> 특정 횟수를 싱행해야하는 루프를 효율적으로 작성할 수 있는 반복 제어 구조

### 9.1.1 Syntax - for loop with ranges

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

### 9.1.2 Syntax - for loop with Collections

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

### 9.1.3 Syntax − for loop with Filters

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

### 9.1.4 Syntax − for loop with yield

- for loop의 반환값(return value)를 변수에 저장하거나 함수를 통해 반환

- for loop의 body에 접두사(prefix)로 yield를 붙임

  ```scala
  val retVal = for{ var x <- List
     		if condition1; if condition2 ... 
  } yield x
  ```
  
  - 중괄호(curly braces) : 변수(variables)와 조건(condition)을 유지하기위해 사용
  - retVal : x의 모든 값이 collection형태로 저장

<br>

#### Example

- for의 결과를 retNum에 저장, for문으로 출력

  ```scala
  object YieldLoop {
    def main(args: Array[String]) {
      val numList = List(0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
      
      val retNum = for{ num <- numList if num > 2; if num % 2 == 1 } yield num
      
      println(retNum)
      for(num <- retNum) {
        println(num)
      }
    }
  }
  ```

  ```scala
  List(3, 5, 7, 9)
  3
  5
  7
  9
  ```

<br>

<br>

## 9.2 while

> 주어진 조건(condition)이 **true**인 동안 statement나 statement의 group을 반복(repeats)
>
> loop body를 **실행하기 전에 조건(condition) 테스트**
>
> loop가 실행되지 않을 수도 있다

### Syntax

- **statement(s)** : single statement or block statement

- **condition** : 모든 표현식(any expression) 가능 (true = 0이 아닌 값)

  - 조건이 false가 되면, loop 다음으로 즉시 넘어간다

  ```scala
  while(condition){
    statement(s)
  }
  ```

### Flow Chart

```flow
st=>start: Start
cond=>condition: Is the condition true?
op1=>operation: Conditional Code
end=>end: next statement

st->cond
cond(yes)->op1(left)->cond
cond(no)->end
```

### Example

- 조건이 참인 동안 1씩 증가

  ```scala
  object WhileLoop {
    def main(args: Array[String]) {
      var num = 10
      
      while(num < 20) {
        println(num)
  			num += 1
      }
    }
  }
  ```

  ```scala
  10
  11
  12
  13
  14
  15
  16
  17
  18
  19
  ```

<br>

## 9.3 do-while

> while와 달리 **loop의 아래(bottom)에서 조건(condition)을 체크**
>
> while과 달리 **적어도 한 번(at least one time)은 실행**된다

### Syntax

- condition : loop의 끝에 위치

- statement(s) : 조건 테스트 전에 한번 실행

  - 조건이 참이라면 do로 돌아가 다시 실행

- 조건이 false일때까지 반복

  ```scala
  do {
    statement(s)
  } 
  while(condition)
  ```

### Flow Chart

```flow
st=>start: Start
cond=>condition: Is the condition true?
op1=>operation: Conditional Code
end=>end: next statement

st->op1->cond
cond(yes, right)->op1
cond(no, bottom)->end
```

### Example

- 조건이 참인 동안 1씩 증가

  ```scala
  object DoWhileLoop {
    def main(args: Array[String]) {
      var num = 10
      
      do {
        println(num)
        num += 1
      }
      while(num < 20)
    }
  }
  ```

  ```scala
  10
  11
  12
  13
  14
  15
  16
  17
  18
  19
  ```

<br>

## 9.4 Loop Control Statement

> 정상적인 순서(normal sequence)에서의 실행을 바꾼다

- break, continue를 지원하지 않음
- scala ver 2.8부터 끊는 방법 존재

###### 자세한 내용은 [여기](https://www.tutorialspoint.com/scala/scala_break_statement.htm) :point_left:

### Syntax

- break statement를 위한 syntax

  ```scala
  // import following package
  import scala.util.control._
  
  // create a Breaks object as follows
  val loop = new Breaks;
  
  // Keep the loop inside breakable as follows
  loop.breakable {
     // Loop will go here
     for(...){
        ....
        
        // Break will go here
        loop.break;
     }
  }
  ```

  
