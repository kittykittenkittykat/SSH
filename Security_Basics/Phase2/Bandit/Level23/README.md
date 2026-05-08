# Level 23

- ls /etc/cron.d
- cat /etc/cron.d/cronjob_bandit24
- cat /usr/bin/cronjob_bandit24.sh
- mktemp -d
- cd /tmp/tmp.JvUFgPji5s
- touch kit
- nano kit
- touch pw
- chmod 777 kit
- chmod 777 pw
- chmod 777 cd /tmp/tmp.JvUFgPji5s
- cp kit /var/spool/bandit24/foo
- cat pw

자 이전문제처럼, 현재 cron에서 cronjob_bandit24.sh를 bandit24권한으로 실행중임을 알 수 있습니다.
이 스크립트 내용을 간단히 해석해보면, 어쩌고저쩌고/foo 디렉토리에 있는 모든 파일중, 그 소유자가 bandit23 인 경우에 실행을 하고 삭제합니다.
소유자가 bandit23이 아닌 파일들은 실행도 안하고 삭제해버립니다.
문제에서 제가 직접 스크립트를 작성하라고 그러는데, 아마 bandit24권한으로 실행되는 점을 이용해야 할것 같습니다.
임시 디렉토리를 만들고 그 디렉토리에 스크립트를 담을 kit이라는 파일을 만들었고, 그 안에 내용은 다음과 같습니다.
'#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tmp.JvUFgPji5s/pw'
입니다. 첫줄은 이 파일을 bash로 실행하라는 명령어라고 알아보니 그런데, 저도 잘 모르겠습니다. 앞서 살펴본 cronjob_bandit24.sh의 첫줄에 있는거 저도 따라 써봤습니다.
그리고 두번째 줄을 보면, ~~~/foo디렉토리안에 파일들이 bandit24권한으로 실행됨을 이용해 다음 레벨의 비밀번호가 담긴 파일을 열어 제가 임시 디렉토리에 만들어둔 pw파일에 그 출력값을 저장해주는 명령어입니다.
이제 cp로 이 kit을 ~~~/foo에 복사해주고요
cron이 지금 cronjob_bandit24.sh를 분간격으로 수행하므로 원하는 내용이 pw에 저장될때까지 기다렸다가 열어주면, 짜잔! 다음 비밀번호가 있습니다.



