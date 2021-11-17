# Day 2

#### CPU Protection Rings

- 응용 프로그램이 전체 컴퓨터 시스템에 데미지를 못 입힘

- 사용자 모드 (user mode for application)
- 커널 모드 (kernel mode for OS) : 특별한 명령과 작업을 수행할 수 있는 모드?

![image-20211115234124367](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211115234124367.png)

> kernel 이란?  알맹이? 핵심? - OS kernel

##### kernel의 껍데기가 shell

![image-20211115234524991](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211115234524991.png)

보통은 application이 사용자 영역에서 놀지만, 필요한 경우 시스템 콜을 통해 커널 영역에 접근한다.

Example

1. 1~1000 를 더한다.
2. 파일에서 데이터 가져오고
3. 해당 데이터와 1~1000 값을 더한다.

2.번 명령은 커널 영역에 실행됨

### 

### 시스템 콜은 커널 모드로 실행

- 커널모드에서만 실행 가능한 기능들이 있음
- 커널 모도르 실행하려면 반드시 시스템 콜을 사용해야함
- 시스템 콜은 운영체제가 제공해줌



![image-20211115235536482](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211115235536482.png)



![image-20211115235607811](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211115235607811.png)

### 배치 처리 시스템

- 단일 cpu 하나에 queue처럼 응용 프로그램들을 줄줄이 할당함
- 동시 처리 불가
- 하나의 프로그램이 오래 실행될 경우, 나머지 프로그램 사용 불가
- 응답시간 엄청 길어짐



> 그래서 나온게 시분할 시스템과 멀티 프로그래밍



### 시분할 시스템

- 빠른 속도로 cpu를 여러 프로그램들이 번걸아가면서 사용함
- 응답시간이 짧아짐
- 프로그램 별로 실행 시간이 다르더라도 문제 없음



### 멀티 태스킹

- 단일 CPU에서 여러 프로그램이 동시에 실행되는 것처럼 보이게 만듦
- 시분할 시스템에서 실행된 작업이 오래 가도록(?) 하는거 같음
- 멀티 프로레싱과의 차이점은 여러 프로그램이 cpu 하나 사용 = 멀티 태스킹
  하나의 프로그램이 여러 cpu 사용 = 멀티 프로세싱

![image-20211116130958918](C:\Users\LMH\AppData\Roaming\Typora\typora-user-images\image-20211116130958918.png)



### 멀티 프로그래밍

- 응용 프로그램이란 녀석들은 CPU만 온전히 쓰는게 아니라 다른 리소스들을 사용함
  ex) 파일 읽기, 프린팅...
- ![image-20211116131032888](C:\Users\LMH\AppData\Roaming\Typora\typora-user-images\image-20211116131032888.png)
- 때문에 이때  cpu 안 쓰는데, 해당 프로그램에 cpu 자원 할당하는게 아까움
- 그래서 프로그램이 다른 리소스를 사용하는 동안에는 해당 프로그램에 cpu 자원을 할당 안 해줌

