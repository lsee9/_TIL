###### 210625_fri

<hr>



###### 오늘의 목차 :dizzy_face:

#### Collections

- Arrays
- Lists
- Sets

- Maps
- Tuples
- Options

- Iterators

###### 유용하게 쓰이는 Collection!

<hr>

<br>


# 11. Collections

> containers of things

- **Lazy**
  - 접근될때 까지 메모리를 소비하지 않는다(not comsume memory until tyey are accessesd)
- Mutable or Immutable
  - immutable collections이 mutable items를 포함할 수 있다

## 11.1 Arrays

> 같은 타입(same type)의 element의 fixed-size(길이가 고정된) sequential collection을 저장하는 자료구조(data structure)
>
> index로 각각의 variable처럼 사용할 수 있다

### Example

- Array 

  ```scala
  // defining
  val myArray1 = Array(1, 2, 3)
  
  // 개별 데이터 접근 및 변경
  myArray1(0)  // Int = 1
  myArray1(0) = 10
  ```

- `++`

  - 배열 연결

  ```scala
  val myArray2 = Array(3, 4, 5)
  val myArray3 = myArray1 ++ myArray2
  ```

<br>

## 11.2 Lists

> 같은 타입의 가변 길이 데이터를 저장하는 자료구조
>
> immutable로 각 element를 변경할 수 없다
>
> List[T] : type T의 element를 가지는 list의 type

### Example

- List 

  ```scala
  // defining
  val myList1 = List(1, 2, 3)
  val myList2 = (1 to 10).toList
  
  myList1  // List[Int] = List(1, 2, 3)
  myList1(0)  // Int = 1
  ```

- `.head`, `.tail`

  ```scala
  myList1.head  // Int = 1
  myList1.tail  // List[Int] = List(2, 3)

<br>

## 11.3 Sets

> 동안한 타입(same type)의 다른 요소 쌍(pairwise different elements)의 collection
>
> 즉, 중복 요소(duplicate elements)가 없다

- **immutable Set**
  - Default

- **mytable Set**
  - import **scala.collection.mutable.Set** class 를 통해 사용 가능

### Example

- Set 선언

  ```scala
  val s = Set(1, 3, 5, 7)
  
  // 값의 존재 여부 확인
  s(1)  //true
  s(2)  //false
  ```

- min, max

  ```scala
  s.min  // 1
  s.max  // 7
  ```

<br>

## 11.4 Maps

> 사전 형식의 데이터 구조, key/value pair의 collection
>
> key를 기준으로 value를 검색할 수 있으며, key는 unique한 값이어야한다

- **immutable Set**
  - Default

- **mytable Set**
  - import **scala.collection.mutable.Map** class 를 통해 사용 가능

### Example

- Map 선언

  ```scala
  val mapNum = Map(1 -> 2, 2 -> 3)
  val colors = Map("red" -> "#FF0000", "azure" -> "#F0FFFF")
  ```

- **get**

  - Option type으로 데이터를 반환한다

  ```scala
  mapNum.get(1)  // Option[Int] = Some(2)
  ```

- **getOrElse**

  - key와 일치하는 value를 가져오거나, 없다면 지정한 값을 반환

  ```scala
  mapNum.getOrElse(1, 0)  // Int = 2
  mapNum.getOrElse(10, 0)  // Int = 0
  ```

<br>

## 11.5 Tuples

> immutable이며, 다른 타입을 묶을 수 있는 자료구조
>
> 패턴 매칭에 사용할 수 있다

### Example

- Tuple 선언

  ```scala
  val myTuple = (1, "Hello", 'A')
  ```

- _1, _2와 같은 형태로 각 값에 접근 가능

  ```scala
  myTuple._1  // Int = 1
  myTuple._2  // String = Hello
  ```

<br>

## 11.6 Options



## 11.7 Iterators

