# Level 15

- openssl s_client -connect localhost:30001

nc는 평문 통신용인데, 문제에서는 SSL/TLS 통신을 사용하라고 나와있습니다.
따라서 openssl을 써야합니다.
이 openssl은 툴킷인데, 프로그래밍에서 라이브러리 같은 역할을 한다고 알고 있습니다.
즉, openssl뒤에 하위 명령어를 입력해서 openssl안에 있는 명령어중 어떤걸 쓸지 정해줍니다.
SSL/TLS 클라이언트로 서버에 접속하는 명령어인 s_client를 사용해주고 -connect옵션을 사용해 이전 레벨과 같이 같은 서버내의 30001번 포트로 연결합니다.
이제 Level 15의 비밀번호를 그대로 입력해주면, Correct! 라는 문구와 함께 다음 레벨의 비밀번호를 구할 수 있습니다.


