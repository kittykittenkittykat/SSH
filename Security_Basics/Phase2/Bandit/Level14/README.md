# Level 14

- cat /etc/bandit_pass/bandit14
- nc localhost 30000

bandit14로 로그인을 비밀키로 했으므로 해당 레벨의 비밀번호를 모르는 상태입니다.
그래서 이 비밀번호가 저장되어있는 파일을 열어 비밀번호를 복사해둡니다.
nc(netcat)로 localhost(현재 서버)의 30000번 포트로 접속해 복사해둔 비밀번호를 붙여넣어주면 다음 레벨의 비밀번호를 응답으로 줍니다.

