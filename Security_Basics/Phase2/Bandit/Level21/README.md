# Level 21

- ls /etc/cron.d/
- cat /etc/cron.d/cronjob_bandit22
- cat /usr/bin/cronjob_bandit22.sh
- cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

뭐가있는지부터 봅시다. 매우 수상한 bandit22관련된 cronjob이 있어 바로 열어봤습니다.
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

이게 해당 스크립트 내용인데, bandit22 권한으로 /usr/bin/cronjob_bandit22.sh 스크립트를 실행하고 있습니다.
매우 수상하므로 스크립트를 보겠습니다.

chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

이게 내용인데, 2번째 줄에 찾고자 하는 비밀번호가 담긴 파일의 내용을 어떤 파일에다가 저장하는 스크립트 입니다.
따라서 /tmp디렉토리 안에 있는 이 파일을 열어 비밀번호를 확인할 수 있습니다.
