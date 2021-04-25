```{.bash}
warning: LF will be replaced by CRLF in empty-cra/.gitignore.
```
<br/>

### 문제의 원인
window/DOS는 줄바꿈을 `CR+LF`로 표현하고, MAC/Linux는 `LF`로표현하기 때문에 git이 OS에 따라 달라지는 줄바꿈을 어떻게 처리할지 물어보는 오류이다.<br/>
<br/>
_**참고**_<br/>
`CR`은 "Carriage-Return"의 약자이고 `\r`과 같다. 이는 커서를 맨 앞으로 옮겨주는 동작이다.<br/>
`LF`는 "Line-Feed"의 약자이고 `\n`과 같다. 이는 한 줄을 내리는 동작이다.<br/>
<br/>

### 해결방법
`git push`할 때 `LF`만을 사용하도록 설정한다. window컴퓨터라면 다음의 명령어를 이용하여 pull받을때는 `LF`를 `CRLF`로 바꾸고 push할때는 `CRLF`를 `LF`로 바꿀 수 있다.<br/>
<br/>
_**window**_<br/>
```{.bash}
git config --global core.autocrlf true
```
(해당 프로젝트에만 설정을 적용시키고 싶다면 `--global`뺀다.)
