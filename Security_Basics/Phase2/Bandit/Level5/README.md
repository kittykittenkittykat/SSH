# Level 5

- cd ./inhere
- find . -type f -size 1033c ! -executable
- file ./maybehere07/.file2
- cat ./maybehere07/.file2

find 명령어를 활용해 사이즈가 1033바이트이며 실행 불가능한 일반파일을 현재 디렉토리에서  찾아봅니다.
이때 -type f는 필요가 없을듯 합니다.
결과로는 maybehere07 디렉토리 안에 .file2 하나가 나옵니다.

이 파일이 정답이겠지만, human-readable조건이 문제에 있으므로 file명령어로 확인해줍니다.
ASCII text임을 알 수 있으니 조건을 모두 만족시키고, 이제 열어서 비밀번호를 얻겠습니다.
