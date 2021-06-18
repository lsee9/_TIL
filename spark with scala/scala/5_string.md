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

### 's'



### 'f'



### 'raw'





## 5.3 String Methods

