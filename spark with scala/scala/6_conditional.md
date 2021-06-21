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


# 6. conditional

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

## 6.1 If Statement

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

## 6.2 If-else Statement



## 6.3 If-else-if-else Statement



## 6.4 Nested if-else Statement

