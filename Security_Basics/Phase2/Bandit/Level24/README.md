# Level 24

- mktemp -d
- cd /tmp/tmp.v3XorD6ocU
- touch kit
- for i in $(seq 0 9999); do printf "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 %04d\n" $i; done > kit
- cat kit | nc localhost 30002

처음에는 그냥 홈에 파일 만들려 했는데, 권한이 없다네요. 그래서 임시 디렉토리를 만들어 그안에서 파일을 만들었습니다.
일일히 네자리 수를 0부터 9999까지 입력해댈수 없으므로, for문을 활용해 30002포트로 보낼 텍스트 1000개를 미리 cat에 저장해두고, 이 내용을 그대로 보냈습니다.
'Wrong! Please enter the correct current password and pincode. Try again.' 문구가 쭉 출력되다가
마지막에는 Correct라는 문구와 함께 다음 비밀번호가 출력됩니다.
