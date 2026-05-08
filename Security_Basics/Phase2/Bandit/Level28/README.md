# Level 28

- git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
- cd repo
- ls
- cat README.md
- git log
- git show 00daa614aac60bd2981c381484191eb7bc4dcfd9

이전 단계처럼 문제에서 알려준 repo를 가져옵니다.
그다음에 README.md를 열어 보면, password가 가려졌음을 알 수 있습니다.
커밋이 이루어진거 같고, git log로 확인해봅니다.
내역중에 fix info leak라는게 있는데, 수상합니다. 유출을 막았다는 내용인데 이 유출이 왠지 비밀번호 같더라는겁니다.
그래서 해당 커밋에 대한 내용을 열어 보면, password를 xxxxxxxx로 바꾸기전에 어떤거였는지 확인할 수 있습니다.

