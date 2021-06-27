###### 210621_mon

<hr>



###### 오늘의 목차 :dog:

#### conditional

- If Statement
- If-else Statement
- If-else-if-else Statement
- Nested if-else Statement

###### 조건문은 프로그래밍에서 필수!! 매우 유용합니다

<hr>
<br>


# 8. conditional

> scala에서의 conditional statement를 알아보겠습니다

#### Flow Chart

- conditional statement의 flow chart diagram

  ```flow
  st=>start: Start
  cond=>condition: If condition is true?
  op1=>operation: Conditional Code
  end=>end: End
  
  st->cond->op1->end
  cond(yes)->op1
  cond(no)->end
  ```

<br>

## 8.1 If Statement

> 하나 이상의 statements가 뒤따르는 Boolean expression으로 구성

### Syntax

```scala
if(Boolean_expression) {
  //Boolean_expression이 true인 경우 실행될 statement
}
```

- Boolean_expression is `true`
  - if expression 내부의 코드 블럭(block of code)이 실행(execute)
- Boolean_expression is `false`
  - if expression이후 첫번째 코드 셋(first set of code) 실행 (닫는 중괄호 뒤(curly brace))

### ex)

```scala
object IfCond {
  def main(args: Array[String]) {
    var x = 10
    
    if( x < 20 ) {
      println("If statement is True")
    }
  }
}
```

```scala
//Output
If statement is True
```

<br>

## 8.2 If-else Statement

> Boolean expression이 false일 때 실행되는 선택적 else statement가 if statement뒤에 옵니다

### Syntax

```scala
if(Boolean_expression) {
  //Boolean_expression이 true인 경우 실행될 statement
} else {
  //Boolean_expression이 false인 경우 실행될 statement
}
```

### ex)

```scala
object IfElseCond {
  def main(args: Array[String]) {
    var x = 30
    
    if( x < 20 ) {
      println("If statement is True")
    } else {
      println("If statement is false")
    }
  }
}
```

```scala
//Output
If statement is false
```

<br>

#### + Plus :star:

- **조건식(conditional expression)**: **하나의 값으로 계산**되는 식

- if, else 키워드를 사용해 조건식을 작성할 수 있다!!

  ```scala
  val num = if (false) 13 else 14  //num: Int = 14
  ```

- 중괄호를 이용해 여러식을 묶을 수 있으며, 마지막 식이 해당 조건식의 결과값이 된다

  ```scala
  if (true) {
    val x = 4
    x + x
  } else {
    val x = 5
    x * x
  }
  // res1: Int = 8
  ```

  



<br>

## 8.3 If-else-if-else Statement

> if문 뒤에 '*else if...else*' statement가 올 수 있다

- 다양한 조건을 테스트 하는데 유용
- 유의사항(points to keep in mind)
  - if는 한개 또는 0개의 else를 가질 수 있으며, else if 뒤에 와야한다
  - 0개 또는 많은 else if를 가질 수 있으며, else 전에 와야한다
  - 하나의 else if가 성공하면, 남은 else if나 else는 실행되지 않는다

### Syntax

```scala
if(Boolean_expression1) {
  //Boolean_expression1이 true인 경우 실행될 statement
} else if(Boolean_expression2) {
  //Boolean_expression2이 true인 경우 실행될 statement
} else if(Boolean_expression3) {
  //Boolean_expression3이 true인 경우 실행될 statement
} else {
  //위의 조건문 중 어떤것도 실행되지 않았을 때 실행
}
```

### ex)

```scala
object IfElseIfCond {
  def main(args: Array[String]) {
    var x = 30
    
    if( x == 10 ) {
      println("Value of x is 10")
    } else if( x == 20 ) {
      println("Value of x is 20")
    }  else if( x == 30 ) {
      println("Value of x is 30")
    } else {
      println("all statement is false")
    }
  }
}
```

```scala
//Output
Value of x is 30
```

<br>

## 8.4 Nested if-else Statement

> 중첩하는 것은 합법적!!

### Syntax

```scala
if(Boolean_expression1) {
  //Boolean_expression1이 true인 경우 실행될 statement
  
  if(Boolean_expression2) {
    //Boolean_expression2이 true인 경우 실행될 statement
  }
} 
```

### ex)

```scala
object IfNestCond {
  def main(args: Array[String]) {
    var x = 30
    var y = 20
    
    if( x == 30 ) {
      if(y == 20) {
        println("x = 30 and y = 20")
      }
    } 
  }
}
```

```scala
//Output
x = 30 and y = 20
```

<br>
