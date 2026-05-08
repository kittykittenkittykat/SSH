# Level 25

- scp -P 2220 bandit25@bandit.labs.overthewire.org:~/bandit26.sshkey .
- cat /etc/passwd
- cat /usr/bin/showtext
- exit
- stty rows 5 cols 80
- ssh bandit26@bandit.labs.overthewire.org -p 2220 -i bandit26.sshkey
- v
- :set shell=/bin/bash
- :shell

다음 레벨의 키를 복사해 저장해둡니다.
bandit 서버에 접속한 상태에서 셸에 대한 정보를 보기 위해 /etc/passwd 내용을 보면, bandit26의 경우 다른 사용자들 처럼 /bin/bash대신 /usr/bin/showtext를 실행합니다.
그러니 이 파일의 내용을 열어 확인해보면 현재 셸을 text.txt를 more로 출력하는 걸로 바꾸라는 명령어 입니다.
more이 터미널의 화면을 기준으로 출력할 내용이 화면 범위를 넘어가면 인터랙티브 모드로 바뀌는데, 이 허점을 노려 vi로 접근해 명령어를 쳐줄겁니다.
원래는 창 크기를 줄이고 진행하려 했으나, 이유는 모르겠지만 이 방법이 먹히지 않아서 직접 창 크기를 지정해주었습니다(stty rows 5 cols 80).
이제 아까 복사해둔 bandit26.sshkey를 활용해 접속해주면, 평소처럼 환영하는 문구가 출력되다가 마지막에 --More--이 있믐을 알 수 있는데, 이는 현재 more의 인터랙티브 모드임을 의미합니다.
따라서 v를 눌러 편집 모드에 들어가고, :를 눌러 명령어를 하나씩 쳐줍니다. 이때 명령어로는 셸을 /usr/bin/showtext를 실행하는게 아닌, 다른 사용자들의 경우와 마찬가지로 /bin/bash를 실행하도록 해주는것, 방금 설정한 셸을 실행하는것 두개 입니다.
결과적으로 정상적으로 bash가 실행되었고, bandit26으로 접속 성공 했음을 알 수 있습니다.

