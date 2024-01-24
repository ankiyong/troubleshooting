# **Error: Command '['C:\Users\euclid_edu23\workspace\python_syntax\hello\Scripts\python.exe', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1.**

1. 환경

- Ubuntu
- python3.8
- pyenv

2. 상황

- pyenv로 python3.8을 사용하여 가상환경 생성 시도할 때 발생

3. 오류 내용

- 사용중인 python 배포판에 pip등이 미설치 상태이기 때문

```bash
Error: Command '['C:\Users\euclid_edu23\workspace\python_syntax\hello\Scripts\python.exe', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1.
```

4. 해결 과정

- Python pip를 제거하고 가상환경 생성

```
python -m venv --without-pip venv
```

