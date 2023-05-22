# TOPS
**Tops 명령어는 현재 OS (운영 체재)의 상태를 나타내주 CLI (명령 줄 인터페이스) 어플리케이션이다.**

**Tops 명령어를 치면 아래와 같이 실행된다.**
![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/08863a64-f3e6-4cad-b1b7-1b256abafa90)
| **기본 정보** | **설명** |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/03ab150d-57bb-4900-b869-b4d56c679896)| 현재 시각 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/dac9b631-50df-4d9b-9e26-7934d21b3bc9)| 서버 활동 시간 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/2ea63326-9aae-4206-a2e3-ae8831fd231c)| 접속중인 유저의 수 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/455a83e6-8701-4458-a29e-b4b2fa773ad4)| 리눅스에서는 실행되거나 대기중인 프로세스의 평균 (앞에서 부터 1분, 5분, 그리고 15분에 대한 평균값) |



| **Tasks** | **설명** |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/79079cac-bea6-485d-a22f-2dd471385fb3)| 전체 프로세스 수 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/686fad33-4d68-4e33-82aa-47bb26c5234d)| 실행(Running) - CPU에 의해서 명령어가 실행중인 Process |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/57f54ecf-28b7-4753-ae8a-0254e258e179)| 대기(Sleeping) - CPU의 명령어 실행을 기다리는 Process |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/8486bb3e-f684-48f4-a466-dfc01322360d)| 종료(Stopped) - Ctrl + Z 등의 signal로 종료된 Process |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/c075d9d6-9fb1-40f7-bf40-be3f10d35d5b)| 뿌리구조(Zombie) - Root Process로 부터 뿌리내린 자식 Process의 형식으로 트리구조를 형성

**CPU 사용량**

**%Cpu(s)라는 영역은 CPU가 어떻게 사용되고 있는지 그 사용율을 보여주는 영역이며 모든 값의 총 합은 100% 이고 이를 퍼센테이지로 나누어서 보여준다.**
 
 * us : 프로세스의 유저 영역에서의 CPU 사용률
 * sy : 프로세스의 커널 영역에서의 CPU 사용률
 * ni : 프로세스의 우선순위(priority) 설정에 사용하는 CPU 사용률
 * id : 사용하고 있지 않는 비율
 * wa : IO가 완료될때까지 기다리고 있는 CPU 비율
 * hi : 하드웨어 인터럽트에 사용되는 CPU 사용률
 * si : 소프트웨어 인터럽트에 사용되는 CPU 사용률
 * st : CPU를 VM에서 사용하여 대기하는 CPU 비율

| **메모리 사용량** |  |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/71063870-79c5-4e53-9488-46fd803861df)| RAM의 메모리 영역 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/8ca8f94d-8d60-413e-b947-5a8feebc9299)| 디스크 메모리 영역 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/c57ead94-7954-4ba2-8d79-63fb208cddab)| Total : 총 메모리 양 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/aea6e7a3-7360-468d-952a-214d0fa683d4)| Free : 사용가능한 메모리 양 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/fad387ce-8685-40ad-9a6f-cb16c21f956a)| Used : 사용중인 메모리 양 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/1e01766d-3177-4a48-aaec-91225b515a0a)| Buff/Cache는 IO와 관련되어 사용되는 버퍼에 사용되는 메모리 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/b6188a16-9336-4018-8e4d-5c7a531b6a62)| Avail Mem : swap 메모리를 사용하지 않고 사용할 수 있는 메모리의 크기 |

**디테일 영역**

* PID :  프로세스 ID이며 프로세스를 구분하기 위한 겹치지않는 고유한 값
* USER : 해당 프로세스를 실행한 USER 이름 또는 효과를 받는 USER의 이름
* PR & NI : PR : 커널에 의해서 스케줄링되는 우선순위 NI : PR에 영향을 주는 nice라는 값
* VIRT : 프로세스가 소비하고 있는 총 메모리
* RES : RAM에서 사용중인 메모리의 크기
* SHR S : 다른 프로세스와의 공유메모리 및 현재 상태
* %MEM : RAM에서 RES가 차지하는 비율
* TIME+ : 프로세스가 사용한 토탈 CPU 시간
* COMMAND : 해당 프로세스를 실행한 커맨드

# KILL
**KILL 명령어는 대개 프로세스를 죽일 때 사용한다.**

**하지만 내부적으로는 프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어이다.**

**※예시※**
![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/a1e26aa5-b032-4b2f-a31d-113fecc706d2)
**여기서 [옵션]은 명령어의 동작을 조정하는 데 사용된다.**

**[PID 또는 신호]는 종료할 프로세스를 식별하는 데 사용된다.**

**[프로세스 ID 또는 신호 번호]는 PID(프로세스 ID) 또는 프로세스에 보낼 신호 번호를 의미한다.**

| **KILL 명령어** | **설명** |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/736bb8d2-4a01-4600-a7e4-6d24e68eafb9)| 특정 프로세스 ID(PID)에 신호를 보내어 프로세스 종료 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/49916f36-e6c8-4490-9d38-dd852a853d49)| 특정 프로세스 그룹에 신호를 보내어 그룹 내 모든 프로세스 종료|
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/7e9bc366-4ea7-4a5a-bde2-a7f5744086c5)| 프로세스 이름으로 프로세스를 종료 |
|![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/bad6a48e-5ee1-42ba-bfa6-05c049a948f0)| 특정 사용자의 모든 프로세스를 종료|

**가장 많이 쓰는 KILL 신호 종류**
* SIGTERM (15): 기본적인 종료 신호로, 프로세스에게 정상 종료를 요청
* SIGKILL (9): 강제 종료 신호로, 프로세스를 즉시 종료
* SIGSTOP (19): 프로세스를 일시 중지
* SIGHUP (1): 프로세스를 다시 로드
* SIGQUIT (3): 키보 종료
* SIGINT (2): 현재 작동중인 프로그램의 동작을 멈출때 사용
* SIGSEGV (11): 잘못된 메모리 관리시 생기는 신호
* SIGCONT (18): 중지 되어 있는 프로그램을 재실행 하는데 사용되는 신호
* SIGSTOP (19): 프로그램을 중지 하는데 사용되는 신호
* SIGTSTP (20): 터미널에서 중지되어 있는 신호

**이외에도 아래와 같이 64가지의 종류가 있다.**
![image](https://github.com/dean8953/Hello-World_230517/assets/133843595/98e3edcf-d239-4785-b7f6-c4dbd3284619)

