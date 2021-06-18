###### 210618_fri

<hr>



###### 오늘의 목차 :dizzy_face:

#### Variables

- Variable Declaration

- 

###### 변수! 이건 써야 뭐라도 할 수 있다!!

<hr>

<br>


# 4. Variables

> 변수는 값(values)을 저장하기위한 메모리 공간입니다!!

- 변수를 선언하면, 메모리에 일정 공간이 생성됩니다
- 변수의 데이터 타입에 기반하여, 컴파일러가 메모리를 할당하고 저장될 수 있는  항목이 결정됩니다

<br>

## 4.1 Variable Declaration

> value로서 variable로서 정의할 때 사용하는 syntax가 다릅니다!!

### value

- `var`

  ```scala
  var myVar : String = "Foo"
  ```

- mutable(가변) variables

- 재할당 가능

  ```shell
  scala> myVar = "Poo"
  myVar: String = Poo
  ```

### Variable

- `val`

  ```scala
  val myVal : String = "Foo"
  ```

- immutable(가변) variable

- 재할당 불가, 데이터 처리에 있어 **단순하게 처리 가능**

  ```shell
  scala> myVal = "Poo"
  <console>:12: error: reassignment to val
         myVal = "Poo"
  ```

<br>

> #### :bulb:Tip
>
> - scala는 동시 처리를 중요하세 생각하기 때문에 변경 불가능한 데이터를 중요하게 생각합니다!
> - 데이터가 변경 가능하면, 동시처리시 데이터에 대한 고민이 많아집니다
> - 따라서 `val (불변 변수)로 설정`하는 것을 선호합니다!!

<br>

## 4.2 Variable Data Type

### Data Type Assignments

- Data Type은 variable의 이름 뒤, 초기값 앞에 지정합니다

  ```scala
  val or var VariableName : DataType = [Initial Value]
  ```

  ###### 예시

  ```scala
  val myNum : Int = 10
  var myBool : Boolean = true
  ```

- 초기값 없이 데이터 타입만 지정할 수 있습니다

  - 다만 REPL을 사용하는 경우, 초기값이 없으면 에러가 발생합니다

<br>

### Variable Type Inference

- 초기값을 지정하면, 컴파일러는 할당된 값에 따라 변수의 타입을 파악할 수 있습니다

- 정수형은 Int, 부동소수점은 Double를 default값으로 합니다

  ```shell
  scala> val myNum2 = 10
  myNum2: Int = 10
  
  scala> val myStr2 = "scala!"
  myStr2: String = scala!
  ```

<br>

### Multiple Assignments

- 다중 지정(Multiple Assignments) 지원

- code block이나 method가 Tuple를 반환하면, val ariable에 할당됩니다

  ```scala
  val (myNum5: Int, myStr5: String) = Pair(10, "Foo")
  ```

  type inference

  ```scala
  val (myNum6, myStr6) = Pair(10, "Foo")
  ```

<br>

## 4.3 Variable Scope

