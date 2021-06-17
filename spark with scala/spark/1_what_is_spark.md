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

  (분산된 여러대의 노드에서 연산을 할 수 있게 해주는)

- Fault Tolerance(장애 허용)와 Data Parallelism(데이터 병렬 처리)을 가지고 클러스터들을 프로그래밍하기위한 인터페이스를 제공한다

- 3가지 API
  
  - **RDD** (Resilient Distributed Dataset)
  - **Data Frame**
  - **Data Set**
  
- **In-memory 연산**을 가능하도록 하여 디스크 기반의 Hadoop에 비해 **성능을 약 100배 정도 끌어올렸다**

- **주요 기능**
  - Map & Reduce (cf. Haddop) 
  - Streaming 데이터 핸들링 (cf. Apache Storm) 
  - SQL 기반 데이터 쿼리 (cf. Hadoop의 Hive)
  - 머신 러닝 라이브러리 (cf. Apache Mahout)

- **장점**
  - 빠른 속도 (In-Memory 기반)
  - 하나의 플랫폼에서 **다양한 데이터 처리** 기능
    - SQL, Streaming, Machine Learning(MLlib), graph(GraphX) 등
  - 다양한 언어지원
    - Java, Python, Scala, R 등 (성능 위해서는 Scala 추천)
  - 다양한 **Cluster Manager(클러스트 매니저)** (cluster관리)
    - Hadoop의 YARN
    - Apache Mesos
  - 다양한 **Data Storage (데이터 스토리지)** (데이터 저장)
    - Hadoop
    - Amazon S3
    - Cassandra