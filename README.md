# 리눅스 명령어
##**top** : top 명령어는 시스템의 프로세스/메모리 사용 상태를 5초의 간격으로 업데이트하여 출력한다. 화면에 출력되는 기본값은 현재시간, 시스템 업데이트(1) 시간, 시스템에 로그인한 사용자 수, 지난 1분, 지난 5분, 지난 15분간의 시스템 평균 부하를 출력한다. 이 목록 아래에 프로세스 정보, CPU 상태, 메모리와 스왑 상태를 출력한다. top 명령어를 실행한 후 초기 화면에서  키를 입력하면 사용할 수 있는 단축키 목록을 확인할 수 있다.

>>top 옵션

1. -b : 배치모드로 정보를 출력한다. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력한다.\
2. -d delay : 지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력한다.\
3. -i idle : 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않는다.\
4. -n num : 지정한 시간(num)만큼 업데이트 정보를 출력한다.\
5. -p pid : 지정한 프로세스 ID(pid)의 정보만을 출력한다.\
6. -q : 시간의 간격 없이 계속하여 업데이트 정보를 출력한다.\
7. -s : 몇 개의 대화식 명령을 비활성화한다(시큐어 모드).\
8. -S : 누적된 정보를 출력한다(cumulative 모드).

>>top 단축기 명령어

|명령어|설명|
|-|-|
|space|정보를 업데이트한다.|
|^L|스크린을 다시 초기화한다.|
|F or f|필드를 추가나 제거한다. 아래 ‘top 항목에 대한 설명’을 참조한다. 확인하고자 하는 항목의 알파벳을 누를 때마다 선택/취소가 반복된다.|
|O or o|출력하는 필드의 정렬 순서를 변경한다. 아래 ‘top 항목에 대한 설명’을 참조하자. 대문자로 선택한 항목을 누르면 왼쪽으로 이동하고 소문자를 누르면 오른쪽으로 이동한다.|
|h or ?|사용 가능한 명령어를 출력한다.|
|k|프로세스를 종료시킨다.|
|n or #|출력할 프로세스의 수를 지정한다.|
|s|출력할 정보의 업데이트 시간을 지정한다.|
|W|~/.toprc에 설정된 내용을 저장한다.|
|q|top을 종료한다.|

![top 명령어](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705212456131_V9D3Q4JJL.jpg/ka38_331_i1.jpg?type=w575_fst_n&wm=Y)

##**ps** : ps 명령어는 프로세스의 현재 상태를 출력한다. ps로 현재 사용하는 프로세스의 상태를 살펴보자. 아래는 PID, TTY, TIME, CMD 헤더의 필드와 내용을 출력한다.\
>>ps 옵션

>전체 프로세스와 관련된 옵션

1. -A : 모든 프로세스를 출력한다.\
2. -N : -A 옵션과 비슷하나 ps 프로세스를 제외하고 출력한다.\
3. -a : 세션 리더 및 터미널에 속하지 않는 프로세스를 제외하고 출력한다.\
4. -d : 세션 리더를 제외한 모든 프로세스를 출력한다.\
5. -e : 커널 프로세스를 제외한 모든 프로세스를 출력한다.

6. T : 현재 터미널에서의 모든 프로세스를 출력한다.\
7. a : 현재 터미널의 사용자 고유 프로세스를 출력한다.\
8. r : 현재 실행 중인 프로세스를 출력한다.\
9. x : 터미널이 없는 프로세스를 출력한다.\
10. --deselect : -N 옵션과 같다.

>특정 프로세스를 선택하여 보여주는 옵션

1. -C : 지정한 명령어의 이름에 관련된 정보를 출력한다.\
2. -G : 그룹 ID에 관련된 정보를 출력한다(이름도 지원).\
3. -U : 사용자 ID에 관련된 정보를 출력한다(이름도 지원).\
4. -g : 지정한 세션 리더 혹은 그룹명에 관련한 정보를 출력한다.\
5. -p : 프로세스 ID를 출력한다.

6. -s : 세션에 속한 프로세스를 지정한다.\
7. -t : tty를 지정한다.\
8. -u : 사용자 ID를 지정한다(이름도 지원).\
9. U : 지정한 사용자의 프로세스를 출력한다.\
10. p : 프로세스 ID를 지정한다.\
11. t : tty를 지정한다.

12. --Group : 실제 그룹 이름이나 ID를 지정한다.\
13. --User : 실제 사용자 이름이나 ID를 지정한다.\
14. --group : 유효 사용자 이름이나 ID를 지정한다.\
15. --pid : 프로세스 ID를 지정한다.\
16. --sid : 세션 ID를 지정한다.

17. --tty : 터미널을 지정한다.\
18. --user : 유효 사용자 이름이나 ID를 지정한다.\
19. -123 : --sid 123과 같은 의미이다.\
20. 123 : --pid 123과 같은 의미이다.

>출력 결과 필드를 제어하는 옵션

1. -0 : PID, TTY, STAT, TIME, COMMAND 등의 필드 목록을 출력한다.\
2. -c : PID, CLS, PRI, TTY, TIME. CMD 등의 필드 목록을 출력한다.\
3. -f : UID, PID, PPID, C, STIME, TTY, TIME, CMD 등의 필드를 CMD 필드의 전체 명령어 형태로 출력한다.\
4. -j : PID, PGID, SID, TTY, TIME, CMD 등의 필드 목록을 출력한다.\
5. -l : F, S, UID, PID, PPID, C, PRI, NI, ADDR, SZ, WCHAN, TTY, TIME, CMD 필드의 상세 정보를 출력한다.

6. -o : 사용자가 정의한 포맷을 지정한다.\
7. -y : -l 이나 l 옵션과 함께 ADDR 필드를 RSS 필드로 출력한다.\
8. 0 : PID, TTY, STAT, IME COMMAND 필드 정보를 출력한다.\
9. X : PID, STACKP, ESP, EIP, TMOUT, ALARM, STAT, TTY, TIME, COMMAND 필드의 정보를 리눅스 i386 레지스터 형식으로 출력한다.

10. j : PPID, PID, PGID, SID, TTY, TPGID, STAT, UID, TIME, COMMAND 필드의 정보를 작업 제어에 관련된 형식으로 출력한다.\
11. l : F, S, UID, PID, PPID, C, PRI, NI, ADDR, SZ, PSS, WCHAN, TTY, TIME, CMD 필드의 정보를 출력하고 -l 옵션과 함께 PSS 필드를 추가하여 출력한다.

12. o : 사용자 지정 형식으로 출력한다.\
13. s : UID, PID, PENDING, BLOCKED, IGNORED, CAUGHT, STAT, TTY, TIME, COMMAND 필드의 정보를 출력한다.\
14. u : USER, PID, %CPU, %MEM, VSZ, RSS, TTY, STAT, START, TIME, COMMAND 필드의 정보를 출력한다.\
15. v : PID, TTY, STAT, TIME, MAJFL, TRS, DRS, RSS, %MEM, COMMAND 필드의 정보를 출력한다.\
16. --format : 사용자 지정 형식으로 출력한다.

>출력 필드의 내용을 변경하는 옵션

1. -H : 프로세스를 계층형으로 출력한다.\
2. -m : 스레드 정보를 출력한다.\
3. -n namelist : 시스템 이름 리스트 파일(namelist)을 지정한다.\
4. -w : 너비에 맞게 잘려진 내용을 제한이 없는 너비의 내용으로 상세하게 출력한다.

5. --cols : 스크린의 너비를 설정한다.\
6. --columns : 스크린의 너비를 설정한다.\
7. --cumulative : 죽은 자식 프로세스 데이터를 포함하여 출력한다.\
8. --forest : 아스키 문자의 프로세스 트리 형태로 출력한다.\
9. --html : HTML 이스케이프로 출력한다.

10. --headers : 헤더 라인을 반복한다.\
11. --no-headers : 헤더를 보이지 않는다.\
12. --lines : 스크린의 높이를 설정한다.\
13. --rows : 스크린의 높이를 설정한다.\
14. --sort : 정렬 방식을 지정한다. --sort＝[+|-]key[,[+|-]key[,···] 형식으로 여기서 사용할 수 있는 키(key)는 예제에서 설명한다. 예를 들어 ps jax --sort＝uid,-ppid,+pid 형식으로 지정할 수 있다.

15. C : CPU 시간을 이용한다.\
16. N : 지정한 시스템 이름의 리스트 파일을 사용한다.\
17. O : 정렬 순서 지정하기 위한 옵션으로 O[+|-]K[,[+|-]K[,···]]의 형식으로 지정한다. K는 예제로 설명한다. +는 오름차순 정렬, –는 내림차순 정렬이다.

18. S : 죽은 자식 프로세스의 데이터를 포함한다.\
19. c : 시스템 내부에 보관 중인 명령어 이름을 출력한다.\
20. e : 명령어에 대한 매개 변수와 함께 환경 변수를 출력한다.\
21. f : 아스키(*) 아트로 프로세스 트리를 출력한다.

22. h : 헤더 라인은 출력하지 않는다.\
23. m : 모든 스레드 정보를 출력한다.\
24. n : WCHAN과 USER 필드를 숫자 값으로 출력한다.\
25. w : 필드의 너비에 맞게 잘려진 내용을 너비보다 상세하게 출력한다.

26. --cols : 스크린의 너비를 설정한다.\
27. --columns : 스크린의 너비를 설정한다.\
28. --cumulative : 죽은 자식 프로세스 데이터를 포함한다.\
29. --forest : 아스키 아트의 프로세스 트리를 출력한다.\
30. --html : HTML 이스케이프를 출력한다.\
31. --headers : 헤더 라인을 반복한다.

32. --no-headers : 헤더를 출력하지 않는다.\
33. --lines : 스크린의 높이를 설정한다.\
34. --rows : 스크린의 높이를 설정한다.\
35. --sort : 지정한 정렬 방식으로 출력한다.\
36. --sort＝[+|-]key[,[+|-]key[,···] 형식이다. 여기서 사용할 수 있는 키(key)는 설명 및 예제에서 설명한다. 예를 들어 ps jax --sort＝uid,-ppid,+pid 형식으로 할 수 있다.

##__jobs__ : jobs는 작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경되었지만 보고되지 않은 상태 등을 표시한다.

>>현재 환경의 작업 상태를 아래와 같이 확인할 수 있다.
![jobs1](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170710154910976_RX87MMBQ3.jpg/ka38_149_i2.jpg?type=w575_fst_n&wm=Y)

>>-l 옵션은 state 필드 앞에 프로세스 ID를 출력한다.\
![jobs2](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170710154937795_26VDE1O3H.jpg/ka38_149_i3.jpg?type=w575_fst_n&wm=Y)

>>jobs 명령어로 확인할 수 있는 세션의 상태값은 다음과 같다.

|상태|설명|
|-|-|
|Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임을 뜻한다.|
|Done|작업이 완료되어 0을 반환하고 종료했음을 뜻한다.|
|Done (code)|작업이 정상적으로 완료했으며, 0이 아닌 코드를 반환했음을 뜻한다.|
|Stopped|작업이 일시 중단됨을 뜻한다.|
|Stopped (SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단했음을 뜻한다.|
|Stopped (SIGSTOP)|SIGSTOP 신호가 일시 중단했음을 뜻한다.|
|Stopped (SIGTTIN)|SIGTTIN 신호가 작업을 일시 중단했음을 뜻한다.|
|Stopped (SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단했음을 뜻한다.|

>>다음과 같이 하면 v로 시작하는 모든 프로세스 ID를 확인할 수 있다.
![jobs3](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170710155004268_W9X1UY7YP.jpg/ka38_149_i4.jpg?type=w575_fst_n&wm=Y)

##__kill__ : kill 명령어는 프로세스에 종료 시그널을 보낸다. 시스템에 얘기치 않은 문제가 생긴 프로세스를 종료시킬 수 있다. 만일 kill 명령으로 종료되지 않는 프로세스는 -9 옵션을 사용해서 강제로 종료하면 된다.

>>아래와 같이 ps 명령어로 sshd 프로세스를 확인할 수 있다.
![kill1](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705204102763_BIV3YDDFB.jpg/ka38_154_i2.jpg?type=w575_fst_n&wm=Y)

>>현재 sshd 프로세스는 root 사용자 권한으로 동작하고 있으며 PID는 2518와 12095이다. 참고로 ps aux 명령에서 볼 수 있는 프로세스 정보에 대한 각각의 필드 내용은 다음과 같다.

|root|USER|프로세스의 사용자|
|-|-|-|
|2518|PID|프로세스 ID|
|0.0|%CPU|마지막 1분 동안 프로세스가 사용한 CPU 점유율|
|0.1|%MEM|마지막 1분 동안 프로세스가 사용한 메모리의 점유율|
|7084|VSZ|가상메모리에 있는 프로세스의 KB 단위 크기|
|1076|RSS|프로세스의 실제 메모리의 크기로 KB 단위|
|?|TTY|연결되어 있는 터미널|
|Ss|STAT|실행되고 있는 프로세스 상태|
|Jun07|START|프로세스가 시작된 날짜|
|0:00|TIME|프로세스가 소비한 총 시간|
|/usr/sbin/sshd|COMMAND|사용자가 실행한 명령 이름|

>>ps 명령으로 확인한 PID를 이용하면 원하는 프로세스를 종료시킬 수 있다.
![kill2](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705204104854_AGTP0ICWJ.jpg/ka38_154_i3.jpg?type=w575_fst_n&wm=Y)

>>만일 kill 명령으로 종료되지 않으면 -9 옵션으로 강제 종료해보자.
![kill3](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705204106437_6SLL1A37G.jpg/ka38_154_i4.jpg?type=w575_fst_n&wm=Y)

>>kill -HUP pid 명령을 이용하면 프로세스를 종료 후 다시 재실행한다.
![kill4](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705204116061_OOROPJWAA.jpg/ka38_154_i5.jpg?type=w575_fst_n&wm=Y)
