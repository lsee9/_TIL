###### 210618_fri

<hr>


###### 오늘의 목차 :dizzy_face:

#### Data Type

- Basic Literals
- Escape Sequences

###### 잘 정리하면서 하고싶은데 어렵다!!!

<hr>
<br>


# 3. Data Type

> Java와 동일하다!!!

### Data Type of Scala

- Java의 데이터 타입과 동일하다
- **primitive types**이 없다
  - `모든 데이터 타입이 object`
  - 각각은 method를 호출할 수 있다

| Data Type | Description                                                  |
| :-------- | ------------------------------------------------------------ |
| Byte      | 8 bit signed value<br />from -128 to 127                     |
| Short     | 16 bit signed value<br />from -(2<sup>15</sup>) to 2<sup>15</sup> - 1 |
| Int       | 32 bit signed value<br />from -(2<sup>31</sup>) to 2<sup>31</sup> - 1 |
| Long      | 64 bit signed value<br />from -(2<sup>63</sup>) to 2<sup>63</sup> - 1 |
| Float     | 32 bit IEEE 754 single-precision float                       |
| Double    | 64 bit IEEE 754 double-precision float                       |
| Char      | 16 bit unsigned Unicode character<br />from U+0000 to U+FFFF |
| String    | A sequence of Chars                                          |
| Boolean   | Either the literal true or the literal false                 |
| Unit      | no value                                                     |
| Null      | null or empty reference                                      |
| Nothing   | The subtype of every other type<br />includes no values      |
| Any       | The supertype of any type<br />any object is of type *Any*   |
| AnyRef    | The supertype(부모타입) of any reference type                |

<br>

## 3.1 Basic Literals

> Literal은 고정된 값을 의미합니다!

- **정수형(Integral Literals)**

  - Int, Long(suffix L)

  ```scal
  0
  035
  21 
  0xFFFFFFFF 
  0777L
  ```

- **부동소수점(Floating Point Literals)**

  - Float (suffix F or f), Double

  ```scala
  0.0 
  1e30f 
  3.14159f 
  1.0e100
  .1
  ```

- **논리형(Boolean Literals)**

  - Boolean type
  - true, false

- **문자형(Character Literals)**

  - 작은 따옴표(quotes)로 감싸진 단일 문자

  ```scala
  'a' 
  '\u0041'
  '\n'
  '\t'
  ```

- **문자열(String Literals)**

  - 큰 따옴표(double quotes)로 감싸진 문자의 시퀀스(a sequence of characters)

  ```scala
  "Hello,\nWorld!"
  "This string contains a \" character."
  ```

- **Multi-Line Strings**

  - triple quotes `""" ... """`로 감싸진 a sequence of characters

  ```scala
  """the present string
  spans three
  lines."""
  ```

  ```shell
  scala> val str2 = """a
       | b
       | c"""
  val str2: String =
  a
  b
  c
  ```

  

### Type Casting

- 자동 형변환

- 명시적 형변환

  ```shell
  scala> var i = 1
  var i: Int = 1
  
  scala> var l = 10L
  var l: Long = 10
  
  scala> i = l
             ^
         error: type mismatch;
          found   : Long
          required: Int
  
  scala> i = l.toInt
  // mutated i
  
  scala> i
  val res12: Int = 10
  ```

  

## 3.2 Escape Sequences