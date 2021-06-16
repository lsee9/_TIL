###### 210616_wed

<hr>




###### 오늘의 목차 :sparkler:

#### What is Spark?

- Introduction to Spark
- Structure
- 

###### 뭘 어떻게 공부해야할까ㅏ

<hr>
<br>


# 1. What is Spark?

> Spark는 또 뭐야???

- 2011년 AMPLab에서 개발된 오픈소스

- MapReduce 형태의 클러스터 컴퓨팅 패러다임의 한계를 극복하고자 등장

  - `MapReduce`

    1. Disk로부터 데이터를 읽는다
    2. Map을 통해 흩어져 있는 데이터를 Key-Value 형태로 연관성 있는 데이터끼리 묶는다

    3. Reduce하여 중복된 데이터 제거, 원하는 데이터로 가공하여 다시 Disk에 저장한다

  - 파일 기반 Disk I/O는 성능이 좋지 않아 **In-mamory 연산을 통해 처리 성능을 향상**시키고자 Spark가 등장했다!!!

## 1.1 Introduction to Spark

- Apache Spark
- 범용적인 목적을 지닌 **분산 클러스터 컴퓨팅 프레임워크**

- Fault Tolerance(장애 허용)와 Data Parallelism(데이터 병렬 처리)을 가지고 클러스터들을 프로그래밍하기위한 인터페이스를 제공한다
- 3가지 API
  - **RDD** (Resilient Distributed Dataset)
  - **Data Frame**
  - **Data Set**
- In-memory 연산을 가능하도록 하여 디스크 기반의 Hadoop에 비해 성능을 약 100배 정도 끌어올렸다