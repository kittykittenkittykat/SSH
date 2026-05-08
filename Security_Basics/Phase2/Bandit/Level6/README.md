# Level 6

- cd /
- ls
- find . -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
- cat ./var/lib/dpkg/info/bandit7.password

서버 전체에서 찾아야 하므로 /로 이동해줍니다. cd ..를 두번해서 홈 디렉토리를 나가도 됩니다.
뭐가 너무 많아 file 명령어를 사용해야할것 같습니다.

문제에 나온 조건대로 옵션을 추가해주고, 마지막에 2>/dev/null을 입력해줍니다.
리눅스에서 출력은 1과 2로 나눌 수 있는데, 1은 표준 출력을, 2는 표준 에러를 의미합니다.
2>/dev/null을 입력해주지 않으면 에러가 너무 많이 떠서 찾기 어렵습니다.
따라서 이를 통해 쓰레기통 격인 /dev/null로 에러 출력을 보내줍니다.

결과로 나온 파일을 열어 비밀번호를 확인해주겠습니다.

