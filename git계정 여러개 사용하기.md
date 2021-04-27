## 계정 여러개 사용하기

계정등록은 config파일의 `user.name`, `user.email`속성값을 이용한다. 이 계정은 기본적으로 global하게 사용하지만 특정 디렉토리 내에서 이를 private하게 사용할 수도 있다.

## 특정 디렉토리에서 사용할 계정 등록

`vi ~/.gitconfig`명령어로 git의 구성파일을 열고 다음을 맨밑에 추가한다.

```
[includeIf "gitdir:~/_study/"]
        path=.gitconfig-my
```

(`~`는 계정 홈을 의미한다.)

이후 `~/_study`경로에 `.gitconfig-my`파일을 추가하고 다음을 추가한다.

```
[user]
    email = 내 이메일
    name = 내 이름
```
