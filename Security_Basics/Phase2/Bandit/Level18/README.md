# Level 18

- ssh bandit18@bandit.labs.overthewire.org -p 2220 'cat readme'

원래 ssh는 접속하면 서버가 셸을 실행시키는데, 이때 같이 실행되는게 .bashrc입니다.
이 .bashrc에 누가 이상한 코드를 집어넣어 접속하자마자 로그아웃 되는건데, 이를 우회하기 위해 뒤에 명령어를 추가해줬습니다.
이로써 ssh로 접속해 제가 쓴 명령어를 한번 실행시키고 바로 종료하는 작업을 수행하게 됩니다.
이 명령어로는 문제에 나온대로 cat readme를 입력해주겠습니다.

