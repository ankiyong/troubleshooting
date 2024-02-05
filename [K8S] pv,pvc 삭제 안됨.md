# [K8S] pv,pvc 삭제 안됨

1. 환경

- Ubuntu
- K3S

2. 상황

- persistent volume 삭제 안됨

3. 오류 내용

```
pv 삭제시 STATUS가 Terminating 상태에서 멈춰있으며, 삭제되지 않는다.
```

4. 해결 방법

```bash
$ sudo kubectl edit pv
$ sudo kubectl edit pvc
```

- 위 두 명령어를 각각 사용했을 때 나오는 설정들에서 "finalizers"를 찾아 삭제한다.

```
Finalizers는 리소스의 삭제 이전까지 삭제 표시를 위해 특정 조건이 퉁족될 때까지 대기하도록 알려주기 위한 키이다.
```

