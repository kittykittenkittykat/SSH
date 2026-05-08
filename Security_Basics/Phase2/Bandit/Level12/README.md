# Level 12

- mktemp -d
- cp data.txt /tmp/tmp.SvktNixAVd
- xxd -r data.txt > data.bin
- file data.bin
- mv data.bin data.bin.gz
- gzip -d data.bin.gz
- file data.bin
- mv data.bin data.bin.bz2
- bzip -d data.bin.bz2
- file data.bin
- mv data.bin data.bin.gz
- gzip -d data.bin.gz
- file data.bin
- tar xf data.bin
- ls
- file data5.bin
- tar xf data5.bin
- ls
- file data6.bin
- mv data6.bin data6.bin.bz2
- bzip2 -d data6.bin.bz2
- file data6.bin
- tar xf data6.bin
- ls
- file data8.bin
- mv data8.bin data8.bin.gz
- gzip -d data8.bin.gz
- file data8.bin
- cat data8.bin

문제에서 시키는대로 mktemp -d로 임시 디렉토리를 만들고 해당 디렉토리에 이동해줍니다.
그리고 이 작업할 공간에 data.txt 파일을 cp로 복사해주고
xxd에 -r 옵션을 추가해 16진수로 표현된 data.txt 파일을 원래 값인 2진수로 돌려줍니다.
2진수로 복원했으므로 파일 명은 bin을 붙였습니다.

이후에는 다음과 같은 방식이 반복됩니다.

file 명령어로 어떻게 압축됐는지, 파일 형식이 뭔지 살핍니다.
gzip이냐 bzip2냐에 따라 압축을 풀기 위해 이름에 확장자 명 각각 gz, bz2를 붙여주고 압축을 풀어줍니다.
형식이 tar이면 여러 파일들이 묶였단 의미고 xf(파일을 대상으로 묶음을 풀어라) 옵션으로 풀어줍니다.
tar로 풀었으면 어떤 파일들이 풀렸는지 ls로 확인하고, 새로 보이는 파일을 대상으로 file 명령어를 통해 어떤 형태인지 살핍니다.

마지막에 data8.bin이 제가 읽을 수 있는 ASCII text임이 확인 되었으므로 cat으로 열어 비밀번호를 확인합니다.
