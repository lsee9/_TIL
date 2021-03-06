###### 210621_mon

<hr>



###### 오늘의 목차 :sparkles:

#### Function

- Function Basic

- 

###### 핵심!! 매우매우 중요!!!

<hr>
<br>


# 10. Function

> scala programming의 핵심!!!

## 10.1 Function Basic

> task를 수행하는 statement의 group
>
> code를 분리된(separate) 함수로 나눌 수 있으며, 일반적으로 각 함수가 특정 잡업(specific task)을 수행하도록 한다

#### Function과 Method

- scala는 function과 method를 가지며, 약간의 차이를 제외하고 **서로 바꿔서(interchangeably) 사용**
- **method** : name, signature, 선택적으로(optionally) 일부 주석(annotations)와 일부 bytecode를 갖는 **class의 일부**
- **function** : 변수(variable)에 할당(assignment)될 수 있는 **완전한 객체(object)**

###### 즉, 일부 object의 member로 정의되는 function를 method라 한다

> #### :bulb: 참고
>
> 여기서는 function과 method를 이렇게 설명하고 있다 [링크](https://docs.scala-lang.org/tour/basics.html) :point_left:
>
> - **Function**
>
>   - 매개변수(paremeter)를 가지는 **표현식(expressions)**
>
>     ```scala
>     val func_name = (param: type) => func_exp
>     ```
>
> - **Method**
>
>   - 함수와 유사하지만 약간의 차이가 있다!
>
>   - `def` keyword를 이용하여 정의
>
>     ```scala
>     def method_name(param: type): return_type = method_exp(body)
>     ```
>
>   - multi-line expressions도 사용할 수 있으며, 가장 마지막 표현식의 결과가 return value가 된다
>
>     ```scala
>     def method_name(param: type): return_type = {
>       method_exp1
>       method_exp2
>       ...
>       method_exp_return
>     }
>     ```
>
> 완벽한 구분이 필요하기 보다는 이런식으로 쓰일 수 있음을 모두 알아주는게 좋을 것 같다!

<br>

<br>

### Function Declarations

- 함수는 source file 어디서나 나타날 수 있다 (정의된 함수 내부에서 정의될 수도 있음)

- 함수 이름으로 +, ++, ~, &,-, --, \, /, :, etc. 문자 사용 가능

  ```scala
  def functionName ([list of parameters]) : [return type]
  ```

  - equals sign이나 method body를 사용하지 않으면 method는 ***abstract***로 선언

### Function Definitions

#### Syntax

- **return type** (optional) : any valid Scala data type

- **list of parameters** (optional) : comma로 구분된 변수(variables)의 리스트(list) (매개변수)

  ```scala
  def functioName([list of parameters]) : [return type] = {
    function body
    return [expr]
  }
  ```
  
  - **대부분의 경우 return키워드를 사용하지 않는다** :star:
  
    ###### 축약해서 하나의 표현식(expression)으로!! 표현
  
  ```scala
  def functionName([variablr_name]: [data_type], ...) = [expression]
  ```
  
  

#### Example

- **return statement**

  - 함수가 값을 반환하는 경우 표현식(expression)과 함께 사용 가능

  ```scala
  object Add {
    def addInt(a: Int, b: Int) : Int = {
      var sum:Int = 0
      sum = a + b
      return sum
    }
  }
  ```

  ```scala
  def addInt(a: Int, b: Int) = a + b
  ```

- **procedures**

  - 어떤 것도 반환하지 않는 함수
  - **Unit** : Java의 **void**와 동일

  ```scala
  object HelloPrint {
    def helloPrint() : Unit = {
      println("Hi, Hello!!")
    }
  }
  ```



### Calling Functions

> method 호출(invoking)을 위한 다양한 구문 변형(syntactic variations) 제공

- standard way

  ```scala
  functionName( list of parameters )
  ```

- 객체(object)의 instance를 사용하여 함수(function)을 호출하는 경우

  ```scala
  [instance.]functionName( list of parameters )
  ```

  

#### Example

- 두 수의 합

  ```scala
  object Add {
    def main(args: Array[String]) {
      println("result: " + addInt(2, 3))
    }
    
    def addInt(a:Int, b:Int) : Int = {
      var sum:Int = 0
      sum = a + b
      
      return sum
    }
  }
  ```

  ```scala
  //Output
  result: 5
  ```

  

## 10.2 Additional Concept

### 10.2.1 Variable Arguments

- `*`

  - 동일한 타입의 매개변수(parameter)가 반복되는 경우 사용

  ```scala
  ```

  

### 10.2.2 Default Parameter Values



### 10.2.3 Nested Functions



### 10.2.4 Partially Applied Functions 

- `_`

### 10.2.5 Named Arguments

- 

<br>

## 10.3 Recursion Functions



<br>

## 10.4 Higher-Order Functions

> **다른 함수(function)을 매개변수(parameter)**로 취하는 함수
>
> 전체 **결과(result)가 함수(function)**인 함수

### Example

- `map` : collection에 대해 사용, 모든 element에 동일한 function을 적용할 때 사용한다 (collection part에서 다루자)

  ```scala
  val mySeq = Seq(1000, 3000, 2000)
  val doubleSeq = (x: Int) => x * 2
  val newSeq = mySeq.map(doubleSeq)  // Seq[Int] = List(2000, 6000, 4000)
  ```

<br>

## 10.5 Anonymous Functions

> **function literals**라고도 불린다 (in source code/ at run time)
>
> object로 설명되는 경우 **function values**라고도 불린다

### Syntax

```scala
// basic syntax
val lambda_exp = (variable: type) => Transformation_Expression

// no parameter
val lambda_exp = () => Transformation_Expression
```

### Example

- 두 parameter의 곱

  ```scala
  // define
  val mul = (x: Int, y: Int) => x * y
  
  // calling
  mul(2, 3)  //res0: Int = 6
  ```

- parameter가 없는 경우

  ```scala
  // define
  var userDir = () => { System.getProperty("user.dir") }
  
  // calling
  println(userDir)
  ```

  

<br>

## 10.6 Currying Functions



<br>



