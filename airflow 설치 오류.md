# TypeError: __init__() missing 6 required positional arguments: 'sequence', 'schema', 'bind_key', 'use_signer', 'permanent', and 'sid_length'

1. 환경

- Ubuntu
- python3.8

2. 상황

- Airflow 설치 후 'airflow db init' 실행시 오류 발생

3. 오류 내용

```bash
TypeError: __init__() missing 6 required positional arguments: 'sequence', 'schema', 'bind_key', 'use_signer', 'permanent', and 'sid_length'
```

4. 해결 과정

- Python과 Airflow 간의 제약 버전 제약조건을 고려하여 설치해야한다.

```
pip install "apache-airflow[celery]==2.8.1" --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.8.1/constraints-3.8.txt"
```

