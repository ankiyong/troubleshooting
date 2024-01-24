# Package 'python' has no installation candidate

1. 환경

- Ubuntu

2. 상황

- python 3.8 을 설치하려는 중 오류 발생

3. 오류 내용

```bash
E: Package 'python3.8' has no installation candidate
```

4. 해결 과정

```bash
$ sudo apt update

$ sudo add-apt-repository ppa:deadsnakes/ppa -y

$ sudo apt update

$ sudo apt install python3.8
```

