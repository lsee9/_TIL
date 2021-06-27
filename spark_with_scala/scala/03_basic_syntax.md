###### 210617_thu

<hr>



###### 오늘의 목차 :dizzy_face:

#### Basic Syntax

- Hello world
- Basic Syntax

###### 잘 정리하면서 하고싶은데 어렵다!!!

<hr>
<br>


# 3. Basic Syntax

> Java를 잘 안다면 Scala를 배우기 쉽다!!! (문장 끝에 ;가 없다는 차이?)

### Scala

- 서로의 메서드를 호출하여 소통하는 **객체의 모음(a collection of objects** (으로 정의될 수 있다!!)

### 용어 정리 :hatching_chick:

- **Object**
  - `상태(state)`와 `행위(behaviors)`를 가진다
  - class의 `instance`
  - 예) 강아지: state - 색, 이름, 품종 / behaviors - 짖는다, 먹는다
- **Class**
  - 클래스와 관련된 상태(state)와 행위(behaviors)를 묘사하는 `템플릿(template)/청사진(blueprint)`
- **Methods**
  - `동작 (behavior)`
  - 클래스는 많은 메서드를 포함
  - 논리가 작성되고, 데이터 조작(manipulate)과 모든 작업(action)이 실행됨
- **Fields**
  - 각 객체가 가지는 `고유한 인스턴스 변수 집합(unique set of instance variables)`
- **Closure**
  - `반환값(return value)`이 이 함수 외부에 선언된 하나 이상의 `변수(variables)에 의존`하는 `함수(function)`
- **Traits**
  - 메서드(method)와 필드(field) 정의를 `캡슐화(encapsulation)`하고, 클래스로 혼합(mixing)하여 `재사용(resue)`할 수 있다 
  - 지원된 메서드의 signature를 지정하여 객체 타입을 정의하는데 사용된다

###### 이것들에 대해서는 앞으로 차차 알아보도록 하자

<br>

### Scala 실행

- **Interactive Mode**

  - 대화형 모드, 입력 결과를 바로 보여준다
  - cmd창에서 scala 입력 후 원하는 식 작성하기

  ```shell
  \User\local>scala
  Welcome to Scala 2.13.6 (Java HotSpot(TM) 64-Bit Server VM, Java 1.8.0_291).
  Type in expressions for evaluation. Or try :help.
  
  scala> println("Hello, World")
  Hello, World
  ```

- **Script Mode**

  - 스크립트 모드, 코드를 스크립트에 작성한 뒤 컴파일

  - text에 코드를 작성한 뒤, `.scala`로 저장

  ```scala
  //HelloWorld.scala
  object HelloWorld {
  
     def main(args: Array[String]) {
        println("Hello, world!") // prints Hello World
     }
  }
  ```

  - cmd에서 scalac로 컴파일한 뒤, 실행한다

  ```shell
  \> scalac HelloWorld.scala
  \> scala HelloWorld
  ```

<br>

## 3.1 Hello world

> Hello World.. 무슨 언어를 시작하든 처음 접하는!! 여기서도 출력해봅시다

- **싱글톤 객체**
- **App Trait 상속**



<br>

## 3.2 Basic Syntax

- Case Seneitivity

- 이름 규칙
  - Class
  - Method
  - Program File
- def main()



### Identifiers



### Keywords



### Comments



### scala Packages



