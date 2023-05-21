# 오픈소스SW개론 과제
***
## 1. top
* top 명령어는 리눅스 시스템의 현재 상태를 보여주는 명령  

  CPU 사용량, 메모리 사용량, 디스크 사용량, 네트워크 사용량을 포함한 다양한 정보를 표시 

  또한 시스템에서 실행 중인 프로세스 목록도 표시함
  
  __top 명령어는 리눅스 시스템의 상태를 모니터링하고, 문제를 해결하고, 성능을 최적화하는 데 사용할 수 있음__
* 명령어 사용법
```
$ top
```
* top 명령어 실행 화면
![image](https://github.com/EHmin2/Opensource_SW/blob/master/%EC%98%A4%ED%94%88%EC%86%8C%EC%8A%A4SW%20%EC%8B%A4%EC%8A%B5.png)
  + 상태줄: 시스템의 현재 상태를 보여주는 줄. 

    여기에는 시스템의 현재 시간, 업타임, CPU 사용량, 메모리 사용량, 디스크 사용량, 네트워크 사용량이 표시
  + 메뉴 줄: top 명령어의 다양한 기능을 제어하는 데 사용할 수 있는 메뉴. 
 
    이 메뉴에는 화면을 업데이트하고, 프로세스를 정렬하고, 프로세스를 중지하거나 종료하는 데 사용할 수 있는 명령이 표시
  + 프로세스 목록: 시스템에서 실행 중인 프로세스의 목록을 보여주는 영역. 

    각 프로세스에는 PID, PPID 상태, CPU 사용량, 메모리 사용량, 실행 시간, 커맨드가 표시
* top 명령어의 키보드 단축키
  | __단축키__ |                                    |
  |------------|------------------------------------|
  |     q      | top 명령어를 종료                   |
  |     f      | 필드 추가, 제거, 순서 변경 또는 정렬 |
  |     s      | 업데이트 간격 설정                  |
  |     H      | CPU 코어 별로 세부 정보를 표시       |
    * <details>
      <summary>그외 더 많은 단축키</summary>
    
***  
## 2. ps
* ps 명령어는 리눅스에서 현재 실행 중인 프로세스에 대한 정보를 보여주는 명령어

  실행 중인 프로세스의 상태, PID, PPID, CPU 및 메모리 사용량 등 다양한 정보를 확인한 수 있음

  __윈도우의 작업 관리자와 유사함__
* 명령어 사용법
```
$ ps
```
* ps 명령어 실행 화면
  

  
  
***
## 3. jobs
* jobs 명령어는 현재 쉘 세션에서 실행 중인 백그라운드 작업의 목록을 표시하는 명령어
  
* 명령어 사용법
```
$ jobs [옵션][작업번호]
```
* jobs 명령어 실행 화면

* jobs로 출력되는 백그라운 작업의 상태값
  | __상태__         |              __설명__                  |
  |-----------------|----------------------------------------|
  | Running         | 작업이 계속 진행중임                     |
  | Done            | 작업이 완료되어 0를 반환                 | 
  | Done(code)      | 작업이 종료되었으며 0이 아닌 코드를 반환  |
  | Stopped         | 작업이 일시 중단                        |
  | Stopped(SIGTSTP)| SIGTSTP 시그널이 작업을 일시 중단        |
  | Stopped(SIGSTOP)| SIGSTOP 시그널이 작업을 일시 중단        | 
  | Stopped(SIGTTIN)| SIGTTIN 시그널이 작업을 일시 중단        |
  | Stopped(SIGTTOU)| SIGTTOU 시그널이 작업을 일시 중단        |
* jobs 명령어 옵션
  | __옵션__ |  __설명__                                |
  |---------|------------------------------------------|
  | -l      | 프로세스 그룹 ID를 state 필드 앞에 출력    |
  | -n      | 프로세스 그룹 중에 대표 프로세스 ID를 출력  |
  |  -p     | 각 프로세스 ID에 대해 한 행씩 출력         |
  | command | 지정한 명령어를 실행                      |

  
## 4. kill
* kill 명령어는 프로세스를 종료시키는 데 사용되는 명령어
  
  모든 프로세스에는 고유한 식별 번호인 PID가 있으며 
  
  kill 명령어는 이 PID 기반으로 특정 프로세스를 식별하여 종료
  
* 명령어 상용법
```
$ kill [옵션] [PID]
```
* kill 명령어 실행 화면( -l(사용 가능한 종료 신호의 목록) 옵션) 
 

  
