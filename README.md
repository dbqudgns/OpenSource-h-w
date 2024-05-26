## 리눅스 명령어 : top 

* 시스템에서 실행 중인 프로세스들을 실시간으로 모니터링 할 수 있게 해주는 명령어

* 실시간으로 현재 운영체제의 상태를 출력해줌으로써 운영체제 문제가 있을 시 원인을 찾아준다.
  
* CPU 사용량, 메모리 사용량 등을 보여준다. 

- 터미널 출력 : `$ top`

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/e49dc262-fcfc-44d1-b2dd-2de4c3411d61)


* 위 그림은 터미널에 top 명령어 출력시 나오는 결과 화면이다. 

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/ba57ac56-bceb-47f9-9788-e76a650ca95d)

* 시스템 현재시간, 서버 구동시간, 현재 접속 사용자 수, 로드 에버리지를 출력한다.
  
  * 로드 에버리지 : 얼마나 많은 프로세스가 실행 중인지 대기중인지를 나타내는 수치
  
  *  1분, 5분, 15분 동안 시스템 부하량의 평균

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/b674a1ed-5deb-42de-93d4-bca06cfc047c)

* 현재 프로세스들의 상태를 나타내며 전체 프로세스 수, 실행 중인 프로세스 수, 대기 중인 프로세스 수, 종료된 프로세스 수, 좀비 수

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/86301028-06e0-476e-b3a1-acaf9943862c)

* CPU 사용량을 나타낸다.

  * 사용자 프로세스 [us], 커널 프로세스 [sy], 프로세스 우선순위 [ni], 사용안하는 비율 [id],
  * 입출력 완료 대기 비율 [wa], 소프트웨어 충돌 [si], VM에 할당된 비율 [st]

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/e8b46eda-d225-4602-9da3-8117c71a9290)

* RAM의 메모리 영역과 디스크를 메모리처럼 이용하는 Swap 메모리 영역

  * 총 메모리 양, 사용 가능한 메모리 양, 사용중인 메모리 양, 커널 버퍼 사용메모리 양, 물리적 메모리 양

---

## 리눅스 명령어 : ps 

* 현재 구동 중인 프로세스 정보를 확인할 수 있는 명령

* ps 명령어와 사용되는 옵션

|옵션|내용|
|------|---|
|-e|현재 사용자뿐만이 아닌 다른 사용자들이 구동시킨 모든 프로세스를 보여준다.|
|-f|프로세스의 상세한 정보를 보여준다.|
|-l|-f 옵션보다 더욱 상세한 프로세서의 정보를 보여준다.|

- 터미널 출력 : `$ ps -efl`    

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/c1db551a-cd8a-480b-b9f0-3a5f1221d6fd)

---

## 리눅스 명령어 : jobs

* 백그라운드로 실행중인 프로세스와 현재 중지된 프로세스의 상태 정보를 출력해주는 명령어

* 상태 정보
  
|상태|내용|
|------|---|
|Running|실행중|
|Stopped|일시 중단|
|Done|완료|
|Terminated|강제 종료|

- 터미널 출력 : `$ jobs`    

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/b01787ca-f714-4cf4-ba17-1c00edd773c6)

* 옵션 종류

|옵션|내용|
|------|---|
|-l|프로세스 그룹 ID를 상태 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|

---

## 리눅스 명령어 : kill

* 프로세스에 특정 신호를 보내어 종료시키는 명령어
* 프로세스를 강제 종료할 때 사용된다. 

- 터미널 출력 : '$ kill [신호] [PID]

* 신호 종류

|신호|신호 번호|내용|
|------|---|---|
|SIGHUP|1|프로세스 재시작|
|SITINT|2|프로세스 실행 중지|
|SIGKILL|9|강제 종료|
|SIGTERM|15|프로세스와 관련된 파일을 정리하고 종료|
|SIGCHLD|17|좀비 프로세스를 종료할 때 사용|

![image](https://github.com/dbqudgns/OpenSource-h-w/assets/68501204/08b6d5a8-dc62-416b-983e-22f1a1906b2c)
