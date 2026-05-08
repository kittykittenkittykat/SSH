# Level 16

- nmap -p 31000-32000 localhost
- nc localhost 31046
- nc localhost 31518
- nc localhost 31691
- nc localhost 31790
- nc localhost 31960
- openssl s_client -connect localhost:31518 -quiet
- openssl s_client -connect localhost:31790 -quiet

먼저 nmap 명령어에 포트 범위를 지정해줍니다.
그럼 결과로 현재 열려있는 포트 5개를 출력해줍니다.
받은 말을 그대로 내뱉는 포트를 걸러내기 위해 각각을 nc로 접속해 아무거나 입력해줍니다.
31518 포트와 31790 포트를 제외한 나머지 포트들은 입력한 값 그대로를 echo해주고 있으니 이 포트들을 제외한 31518과 31790 포트를 살펴보겠습니다.
이 두 포트를 s_client로 접속할건데, 인증서 정보가 제대로 뜨면 SSL/TLS클라이언트 입니다.
해당 포트에 접속하고 비밀번호를 입력하니까 KEYUPDATE 라는 문구가 출력되고 우리가 원하는 값은 안나옵니다.
그래서 이를 무시하라는 옵션 -quiet을 추가해주는겁니다.
결론적으로 두 포트 모두 해보면, 31790이 원하는 결과를 출력해주는 포트임을 알 수 있습니다.

