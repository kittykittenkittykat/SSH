# Level 30

- git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
- cd repo
- ls
- cat README.md
- ls -la .git
- cat packed-refs
- git tags
- git show secret

repo 가져오고, README안에는 아무것도 없고. 다른 브랜치를 살펴봐도 아무것도 없습니다.
그래서 .git 디렉토리를 살펴보니 refs, packed-refs등 여러 디렉토리와 파일들이 있고 하나하나 열어봤습니다.
근데 packed-refs에 secret이라는 태그가 있길래 그 내용을 살펴봤더니 다음 비밀번호가 있었습니다.
