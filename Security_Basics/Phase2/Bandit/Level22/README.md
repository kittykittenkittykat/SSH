# Level 22

- ls /etc/cron.d/
- cat /etc/cron.d/cronjob_bandit23
- cat /usr/bin/cronjob_bandit23.sh
- echo I am user bandit22 | md5sum
- cat /tmp/8169b67bd894ddbb4412f91573b38db3

이전 문제와 똑같은 방식으로 수상한 파일 /usr/bin/cronjob_bandit23.sh을 열어 스크립트를 확인해봅니다.
그 내용은 다음과 같습니다.

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget

스크립트를 그대로 해석해 양상을 살펴보면 먼저 myname 변수에 bandit22를 저장합니다(whoami 명령어의 출력).
mytarget 변수에는 뒤에 나온 명령어를 실행한 출력을 저장하는데, 그 명령어는 I am user bandit22를 md5해시함수를 이용해 나타내고, 이 결과를 공백으로 구분해 첫번째 내용만 가져온다는 명령어입니다.
그리고 맨 마지막줄을 통해 우리는 /tmp/$mytarget경로에 우리가 원하는 bandit23의 비밀번호를 저장하고 있음을 알 수 있습니다.
I am user bandit22의 md5해시값을 모르니 셸에서 직접 실행을 하는 겁니다.
그렇게 얻은 출력값을 갖고 파일을 열어 비밀번호를 확인합니다.
