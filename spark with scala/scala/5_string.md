###### 210618_fri

<hr>



###### 오늘의 목차 :deer:

#### String

- String
- String Interpolation
- String Methods

###### 문자열은 아주 유용한 객체 입니다@@

<hr>
<br>

# 5. String

> String은 **Immutable object**로 수정 불가합니다!
>
> 이제부터 java.lang.String 클래스의 중요 메서드를 알아봅시다

## 5.1 String

### Creating String

- compiler가 string literal을 만나면 String object를 만든다

  ```scala
  val greeting = "Hello Scala"
  or
  val greeting:String = "Hello Scala"
  ```

  ```scala
  object Greet {
    val greeting: String = "Hello, Scala"
    
    def main(args: Array[String]) {
      println(greeting)
    }
  }
  
  //output
  Hello, Scala
  ```

<br>

### String Length

> accessor methods : object에 대한 정보를 얻기위해 사용되는 메서드

- **`length()`**

  - string과 함께 사용
  - 문자열에 포함된 문자의 수 반환

  ```scala
  object Len {
     def main(args: Array[String]) {
        var palindrome = "Dot saw I was Tod";
        var len = palindrome.length();
        
        println( "String Length is : " + len );
     }
  }
  ```

  ```shell
  //save Len.scala
  >scalac Len.scala
  >scala Len
  ```

  ```shell
  //output
  String Length is : 17
  ```

<br>

### Concatenating Strings

- `.concat()`

  - 두 문자열을 연결(concatenating)하기위한 String 클래스(class)의 메서드(method)
  - string1뒤에 string2가 더해진 새로운 문자열 반환

  ```scala
  string1.concat(string2)
  ```

  - string literals를 사용한 경우

  ```scala
  "My name is ".concat("Mina")  //My name is Mina
  ```

- `+` operator

  - 문자열 연결에 사용되는 더 일반적인 방법

  ```scala
  "My name " + "is " + "Mina" + "!"  //My name is Mina!
  ```

<br>

### Creating Format Strings 





## 5.2 String Interpolation

> String을 만들기 위한 새로운 방법!
>
> string literal 프로세스(process)에 변수 참조(variable reference)를 직접 포함하는 매커니즘(mechanism)

### 's'

- string processing에 **직접적인 변수(variable) 사용**을 허용

- 같은 범위(scope)내에 있는 String variable을 문자열과 함께 사용 가능

- **예)**

  - Srting variable(`name`)을 normal String(`Hello`)에 추가

  ```scala
  val name = "Mina"
  println(s"Hello, $name")  //Hello, Mina
  ```

  - 임의의 표현식(arbitray expressions, `${1 + 2}`) 처리

  ```scala
  println(s"1 + 2 = ${1 + 2}")  //1 + 2 = 3
  ```

<br>

### 'f'

- 형식화된 문자열(`formatted String`)을 만드는 것을 허용 (cf. C의 **printf**)

- 모든 variable reference는  the **printf** style format specifiers(형식 지정자, %d, %i, %f, ect.) 필요

- **예)**

  - `$변수명%format_specifiers`
  - variable reference와 format specifiers 일치 해야함

  ```scala
  val height = 1.72d
  val name = "Jieun"
  println(f"$name%s is $height%2.3f meters tall")  //Jieun is 1.720 meters tall
  ```

  ###### `f`를 쓰지 않는 경우, 기본적으로는 %를 쓰지 않으며 %s로 가정합니다

### 'raw'

- 문자열내에서 **escaping을 수행하지 않는다**는 것을 제외하면 `s` interpolator와 동일

- **비교**

  - **s** interpolator

    ```scala
    object SPrac {
       def main(args: Array[String]) {
          println(s"Result = \n a \n b")
       }
    }
    ```

    ```scala
    //Output, 공백도 출력
    Result =
     a
     b
    ```

  - **raw** interpolator

    ```scala
    object RawPrac {
       def main(args: Array[String]) {
          println(raw"Result = \n a \n b")
       }
    }
    ```

    ```scala
    //Output
    Result = \n a \n b
    ```

<br>

## 5.3 String Methods

> **java.lang.String** class에 정의된 메서드(method)를 알아보자
>
> 모두 scala 에서 사용할 수 있다!!

- **char charAt(int index)**
  - 지정된 `index에 있는 문자`(character)를 반환
- **int compareTo(Object o)**
  - 해당 String을 `다른 Object와 비교`한다
- **int compareTo(String anotherString)**
  - 두 string을 `사전적으로(lexicographically) 비교`

- **int compareToIgnoreCase(String str)**
  - 두 string을 `사전적으로 비교`하고, `대소문자 차이(case differences)는 무시`한다
- **String concat(String str)**
  - 해당 string의 끝에 `지정된 string을 연결`한다(concatenate)
- **boolean contentEquals(StringBuffer sb)**
  - 해당 string이 지정된 `StringBuffer와 동일한 문자 시퀀스`(sequence of characters)를 나타내는 경우만(if and only if) `true`반환
- 

