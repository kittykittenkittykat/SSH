# Level 19

- ls -l
- ./bandit20-do
- ./bandit20-do whoami
- ./bandit20-do cat /etc/bandit_pass/bandit20

먼저 어떤 파일이 setuid를 갖고 있는지 확인하고, 파일 소유자가 bandit20인것도 확인해줍니다.
setuid가 있는 파일이므로 일단 실행하면, 예시가 있습니다. 
이 예시를 입력해보면 이 프로그램은 bandit20의 권한으로 명령어를 실행시킨다는 것을 알 수 있습니다.
따라서 bandit20권한으로 bandit20의 비밀번호를 보는 명령어를 입력해줍니다.

