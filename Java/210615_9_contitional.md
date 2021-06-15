###### 210610_thu

##### 필기만 한거... 정리중!

<hr>




###### 오늘의 목차 :lemon:

#### Basic Syntax

- Java 프로그램의 실행 구조 
- 변수 
- 기본 자료형 
- 특수 문자와 서식 문자 
- 연산자 
- 배열 
- 배열과 메모리 
- **조건문** :heavy_check_mark:
- 반복문

###### 배열과 메모리 함께 생각해보쟈

<hr>



<br>

# 8. 조건문

> 어떤 조건에 따라서 프로그램의 흐름이 결정되는 것, 변경될 수 있는 것



## 8.1 조건문이란?

- 둘 중 하나택 : 양자책일
  - if
- 여러가지중 하나 택 : 다자택일
  - switch
- 다른 프로그래밍언어에서도 2가지 쓰임

## 8.2 if문

- 어떻게 구현하는지 보자

  ```java
  if (조건식) {
      //True이면 실행문 수행
      실행문;
  }
  //거짓이면 다음 실행
  ```



- if else

  ```java
  if (조건식) {
    //True이면 실행문 수행
    실행문;
  } else {  //False이면 다음 실행
    실행문;
  }
  ```

- else if : 다자택일

  - 여러가지의 조건 나타낼 수 있음

  ```java
  if (조건식) {
    //True이면 실행문 수행
    실행문;
  } else if {
    실행문;
  } else {
    실행문;
  }
  ```

- 데이터 주고받고 할 때 어떤 조건을 지정해야함

  - 돈을 주고받는다고 하면 id가 맞는지 금액이 맞는제 그런것들
  - 안맞으면 동작하지 않아야함

- if (true) : 항상 실행, false항상 틀림 => 궅이 쓸 필요는 거의 없을 듯

- 조건문 묘사하는 가장 대표

## 8.3 switch문

- 여러가지중 하나 택

- 선택사항 많을 때 수행

  - 다른 위치에 있는 객체를 쓴 경우 java.utll.Scan~ 구문 써줘야함 (스캐너 쓴다고 하면 자동으로 해줌)

  ```java
  System.out.println  //개행까지 들어감
  // scanner 객체 사용해서 입력 받음
  Scanner inputNum = new Scanner(System.in);
  //nextInt을 이용해 입력받은 숫자 이용
  int score = inputNum.nextInt();
  
  switch (비교할 대상의 값) {
  	case value1:
      score == value인 경우의 동작;
      break;  //switch 문을 바로 빠져 나가라, 빼먹으면 아래를 모두 실행
      
  	default:
      모두 아닌경우 실행;
      없으면 어떤 구문도 실행하지 않고 빠져나옴
  }
  
  
  inputNum.close()  //자원을 사용한 뒤 다시 돌려줌
  ```



```java
switch (비교할 대상의 값) {
  case value1
	case value2:
    score == value1 or value2 인 경우의 동작;
    break;
```



- 상대적으로 if가 더 많이쓰임