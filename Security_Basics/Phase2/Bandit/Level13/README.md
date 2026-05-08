# Level 13

- ls
- cat HINT
- exit
- scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private .
- chmod 700 sshkey.private
- ssh bandit14@bandit.labs.overthewire.org -p 2220 -i sshkey.private

뭐가 있는지 부터 보면, 수상한 HINT파일이 있습니다.
열어보니 localhost를 통한 접속이 막혀있다고 합니다.
제컴퓨터로 파일을 복사하고, 권한을 안전하게 설정한 뒤에 -i 옵션으로 비밀번호 없이 이 파일을 써서 로그인 해주면 됩니다.

