# Level 31

- git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
- cd repo
- ls
- cat README.md
- echo 'May I come in?' > key.txt
- git add key.txt -f
- git config --global user.email "kittykittenkittykat@gmail.com"
- git config --global user.name "kittykittenkittykat"
- git commit -m 'kit'
- git push origin master

repo 가져옵니다. README에서 하라는대로 key.txt에 내용을 넣어 만들어주고 처음에는 -f없이 add했는데 -f옵션 쓰라 해서 그대로 해줬구요.
commit 하려니까 이메일주소랑 사용자 이름 쓰라 그래서 그대로 해줬습니다.
commit하고 master에 push 해줬습니다.
그럼 출력되는 문구중에 다음 레벨의 비밀번호가 있음을 알 수 있습니다.
