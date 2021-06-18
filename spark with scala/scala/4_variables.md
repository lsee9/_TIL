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

