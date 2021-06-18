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

  

### Concatenating Strings



### Creating Format Strings 





## 5.2 String Interpolation

### 's'



### 'f'



### 'raw'





## 5.3 String Methods

