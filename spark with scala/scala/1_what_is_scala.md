###### 210616_wed

<hr>



###### 오늘의 목차 :statue_of_liberty:

#### What is Scala?

- Introduction to Scala
- Functional Programming
- Installation

###### Python과 비슷하다고 하니...빠르게 배워보자!

<hr>
<br>

# 1. What is Scala?

> Scala가 뭐야??

- 2004년 Mardin Odersky가 발표한 언어
- 기존 Java언어가 너무 복잡하다는 단점을 극복하기위해 만들어졌다

## 1.1 Introduction to Scala

- 확장 가능한 언어 (**Scal**able **La**nguage)
- 다중 패러다임 프로그래밍 언어(multiparadigm programming language)
  - **함수형**(functional)과 **객체 지향**(object-oriented) 프로그래밍의 특징을 모두 가진다

<br>

### 특징 :tropical_drink:

#### JVML (Java Virtual Machine Language)

- **자바 가상 머신(JVM)에서 동작**하는 언어
- **자바의 모든 라이브러리**를 사용할 수 있다

- 실행 구조
  - 스칼라 컴파일러(scalac): scala코드 => 바이트 코드로 변환
  - 바이트 코드는 JVM상에서 자바와 동일하게 실행

<br>

#### Object-Oriented Language



<br>

#### Functional Language

- 모든 함수(function)가 값(value)이고, 모든 값(value)이 객체(object)이고, 궁극적으로는 **모든 함수(function)가 객체(object)** 라는 점에서 함수형 언어
- 특징
  - **익명 함수(anonymous functions)**를 정의하기위한 간단한 문법 제공
  - **고차(higher-order)** 함수 지원
  - 함수 **중첩(nesting)** 허용
  - **currying** 지원
    - 여러 인자 받는 함수를 단일 인자 받는 함수의 체인 이용하는 방식으로 바꾸는 것

<br>

#### Concurrent & Synchronize processing



<br>

<br>

## 1.2 Functional Programming



<br>

<br>

## 1.3 Installation

> scala를 사용하려면 Java가 기본적으로 필요합니다!!!

##### 호환을 위해 JDK 8 (Java SE 8)과 Scala 2.13.6

### JDK 설치

- 터미널(cmd)에 `java -version`으로 버전 확인

  ```shell
  >java -version
  'java'은(는) 내부 또는 외부 명령, 실행할 수 있는 프로그램, 또는 배치 파일이 아닙니다.
  ```

  ###### 이런 문구가 나오면 설치하면 된다@

  ###### 이미 있는데 버전이 맞지 않다면 제어판에서 java 삭제후 재설치하자

- 운영체제에 맞게 JDK를 설치한다 [링크](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)

  - Windows x64 설치 (window+ R : control system에서 확인)
  - 설치는 next만 누르면 OK

- **환경변수** 설정

  - window+ R : `control system`
  - [고급 시스템 설정] - [고급] - [환경 변수]
  - 시스템 변수 - [새로 만들기]
    - 이름 : `JAVA_HOME` 
    - 값 : `C:\Program Files\Java\jdk1.8.0_291`
  - 시스템 변수 - [Path] - [편집]
    - `%JAVA_HOME%\bin` 추가
  - 확인 눌러서 변경 내용 적용하기

- 터미널(cmd)에 `java -version`으로 버전 확인

  ```shell
  C:\Users\local>java -version
  java version "1.8.0_291"
  Java(TM) SE Runtime Environment (build 1.8.0_291-b10)
  Java HotSpot(TM) 64-Bit Server VM (build 25.291-b10, mixed mode)
  
  C:\Users\local>javac -version
  javac 1.8.0_291
  ```

<br>

### Scala 설치

- scala binaries를 다운받자 [링크](https://www.scala-lang.org/download/scala2.html)

  - other ways to install Scala
  - [Download the Scala binaries for windows] 클릭

- 다운받은 "**scala-2.13.3.msi"**를 실행

  - Custom Setup

    - Spark를 사용하기위해 설치하는 경우 경로를 변경하자!!

      ###### 기본 설치 폴더인 `C:\Program Files (x86)\scala\`는 띄어쓰기때문에 spark가 인식할 수 없다고 합니다

    - [Browse..]

      `C:\Users\local\scala` 이런식으로 원하는 경로로 지정

  - 설치 완료

- **환경변수** 설정

  - window+ R : `control system`
  - [고급 시스템 설정] - [고급] - [환경 변수]
  - 시스템 변수 - [새로 만들기]
    - 이름 : `SCALA_HOME` 
    - 값 : `C:\Users\local\scala`
  - 시스템 변수 - [Path] - [편집]
    - `%SCALA_HOME%\bin` 추가
  - 확인 눌러서 변경 내용 적용하기

- **scala 실행**

  - cmd에서 `scala`
  - `scala>`로 변경되면 OK

  ```shell
  C:\Users\local>scala
  Welcome to Scala 2.13.6 (Java HotSpot(TM) 64-Bit Server VM, Java 1.8.0_291).
  Type in expressions for evaluation. Or try :help.
  
  scala>
  ```

  
