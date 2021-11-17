# Day3

#### FIFO 스케줄러

- 가장 간단한 스케줄러 (배치 처리 스스텀)
- 큐처럼 사용
- 프로세스 동시 사용 불가능



### SJF 스케줄러

- 실행시간이 가장 짧은 프로세스부터 실행시킴
- 대부분의 경우 각 프로세스의 실행시간을 몰라 사용하기 어려움, 특정 상황에서만 사용
- 역시 동시 사용 불가능



#### 우선순위 기반 스케줄러

- 정적 우선순위
  - 프로세스마다 미리 정해진 우선순위로 cpu에 할당

- 동적 우선순위
  - 스케줄러가 상황에 따라 우선순위를 변경하여 cpu에 할당

### Round Robin 스케쥴러

![image-20211116230325119](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211116230325119.png)

- 시분할 시스템



### 멀티 프로그래밍과 wait

![image-20211116231224546](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211116231224546.png)





### 프로세스 상태

![image-20211116231238386](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211116231238386.png)

- ready : 지금 cpu에 넣으면 바로 동작할 수 있음
- block : 특정 이벤트 발생 대기 상태
- running : cpu에서 실행중
- exit : 프로세스가 잡고 있는 시스템 리소스들을 풀어줘야하는 경우가 있기 때문에 별도의 상태로 관리



### 프로세스 상태간 관계

![image-20211116231748541](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211116231748541.png)



### 