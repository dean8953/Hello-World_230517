# Tops
Tops 명령어는 현재 OS (운영 체재)의 상태를 나타내주 CLI (명령 줄 인터페이스) 어플리케이션이다.

Tops 명령어를 치면 아래와 같이 실행된다.
![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/563fd9bd-4156-4593-83df-5ad9828f5b48)
| 기본 정보 | 설명 |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/6765bd37-08cb-4c60-bfc4-0d0bda0c812e)| 현재 시각 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/517b812b-a9b8-4226-9704-171ee0945972)| 서버 활동 시간 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/560576f2-f4dc-47df-9085-a829b10ec66f)| 접속중인 유저의 수 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/77967a1b-944d-44bc-882a-4f735022cf13)| 리눅스에서는 실행되거나 대기중인 프로세스의 평균 (앞에서 부터 1분, 5분, 그리고 15분에 대한 평균값) |


| Tasks | 설명 |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/581bd6cc-6ab4-4b0d-a784-1cbf8bdbb065)| 전체 프로세스 수 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/eee9f290-4750-48a6-9175-c43583f1e74b)| 실행(Running) - CPU에 의해서 명령어가 실행중인 Process |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/d0b4915c-0ee4-47f5-9000-6532144237d1)| 대기(Sleeping) - CPU의 명령어 실행을 기다리는 Process |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/b4e5c2fb-e5cc-44b1-80dd-2591559a6be1)| 종료(Stopped) - Ctrl + Z 등의 signal로 종료된 Process |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/f5f2e641-88cc-40ab-a33d-795679fe4c64)| 뿌리구조(Zombie) - Root Process로 부터 뿌리내린 자식 Process의 형식으로 트리구조를 형성

CPU 사용량

 %Cpu(s)라는 영역은 CPU가 어떻게 사용되고 있는지 그 사용율을 보여주는 영역이며 모든 값의 총 합은 100% 이고 이를 퍼센테이지로 나누어서 보여준다.
 
 * us : 프로세스의 유저 영역에서의 CPU 사용률
 * sy : 프로세스의 커널 영역에서의 CPU 사용률
 * ni : 프로세스의 우선순위(priority) 설정에 사용하는 CPU 사용률
 * id : 사용하고 있지 않는 비율
 * wa : IO가 완료될때까지 기다리고 있는 CPU 비율
 * hi : 하드웨어 인터럽트에 사용되는 CPU 사용률
 * si : 소프트웨어 인터럽트에 사용되는 CPU 사용률
 * st : CPU를 VM에서 사용하여 대기하는 CPU 비율

| 메모리 사용량 |  |
| ------------ | -------------------------------------------------- |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/05e37b71-84e8-4cc2-bccf-efd2a70618d8)| RAM의 메모리 영역 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/11ebe076-bb13-4f6d-b921-04cf3bd40e20)| 디스크 메모리 영역 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/d5499fe0-1197-4691-a7ad-f7befba6016d)| Total : 총 메모리 양 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/3eea4cd6-bc0c-4ac8-b97d-efe84bfb2b0c)| Free : 사용가능한 메모리 양 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/203298ea-ce26-499f-ba0d-e4b6df250be1)| Used : 사용중인 메모리 양 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/72687629-0ed7-4b47-bc56-e9743d6ddda5)| Buff/Cache는 IO와 관련되어 사용되는 버퍼에 사용되는 메모리 |
|![image](https://github.com/dean8953/Helloworld_230522/assets/133843595/bd3721d0-c6ed-4d0a-b93a-d7a5a3331aa5)| Avail Mem : swap 메모리를 사용하지 않고 사용할 수 있는 메모리의 크기 |

디테일 영역

* PID :  프로세스 ID이며 프로세스를 구분하기 위한 겹치지않는 고유한 값
* USER : 해당 프로세스를 실행한 USER 이름 또는 효과를 받는 USER의 이름
* PR & NI : PR : 커널에 의해서 스케줄링되는 우선순위 NI : PR에 영향을 주는 nice라는 값
* VIRT : 프로세스가 소비하고 있는 총 메모리
* RES : RAM에서 사용중인 메모리의 크기
* SHR S : 다른 프로세스와의 공유메모리 및 현재 상태
* %MEM : RAM에서 RES가 차지하는 비율
* TIME+ : 프로세스가 사용한 토탈 CPU 시간
* COMMAND : 해당 프로세스를 실행한 커맨드

