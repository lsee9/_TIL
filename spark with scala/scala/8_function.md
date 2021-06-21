###### 210621_mon

<hr>



###### 오늘의 목차 :sparkles:

#### Function

- Function Basic

- 

###### 핵심!! 매우매우 중요!!!

<hr>
<br>


# 8. Function

> scala programming의 핵심!!!

## 8.1 Function Basic

> task를 수행하는 statement의 group
>
> code를 분리된(separate) 함수로 나눌 수 있으며, 일반적으로 각 함수가 특정 잡업(specific task)을 수행하도록 한다

#### Function과 Method

- scala는 function과 method를 가지며, 약간의 차이를 제외하고 **서로 바꿔서(interchangeably) 사용**
- **method** : name, signature, 선택적으로(optionally) 일부 주석(annotations)와 일부 bytecode를 갖는 **class의 일부**
- **function** : 변수(variable)에 할당(assignment)될 수 있는 **완전한 객체(object)**

###### 즉, 일부 object의 member로 정의되는 function를 method라 한다

<br>

### 8.1.1 Function Declarations

- 함수는 source file 어디서나 나타날 수 있다 (정의된 함수 내부에서 정의될 수도 있음)

- 함수 이름으로 +, ++, ~, &,-, --, \, /, :, etc. 문자 사용 가능

  ```scala
  def functionName ([list of parameters]) : [return type]
  ```

  - equals sign이나 method body를 사용하지 않으면 method는 ***abstract***로 선언

### 8.1.2 Function Definitions

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



### 8.1.3 Calling Functions

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

  

