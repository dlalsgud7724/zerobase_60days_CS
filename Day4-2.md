# Day4-2

### 인터럽트

- cpu가 프로그램을 실행하고 있을때, 하드웨어 장치나 예외상황이 발생하여 처리가 필요할 경우  cpu에 알려서 처리하는 기술
- cpu 온도가 급격하게 올라간다던지, 0으로 나눈다던지..



### 인터럽트 필요 이유

- 선점형 스케쥴러 : 프로세스 running 중 스케줄러가 이를 중단시키고 다른 프로세스로 교체시켜야함
- io 와의 커뮤니케이션 : io 작업 완료시 프로세스를 block에서 ready로 깨워야함



### 주요 인터럽트

- Divide-by-Zero Interrupt

  ![image-20211117224302601](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211117224302601.png)

- 타이머 인터럽트
  ![image-20211117224500723](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211117224500723.png)
  일정 시간마다 프로세스를 교체해줌 (선점형 스케쥴러)
- io 인터럽트
  ![image-20211117224627002](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20211117224627002.png)
  하드웨어에서 이벤트가 발생했을 때 발생



### 인터럽트 종류

- 내부 인터럽트
  - 주요 프로그램에서 잘못된 명령이나 데이터 사용시 발생
    * 0으로 나눌때
    * 사용자 모드에서 허용되지 않은 명령이나 공간 접근시
    * 계산 결과가 overflow 날때
  - 소프트웨어 인터럽트라고도 함
    
- 외부 인터럽트
  - 하드웨어에서 발생하는 이벤트
    - 전원이상
    - 기계문제
    - 커보드 등 io 관련 이벤트
    - timer 이벤트\
  - 하드웨어 인터럽트라고도 함