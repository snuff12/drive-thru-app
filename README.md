# Drive-thru-app

## Wireframe

와이어프레임은 [이곳](https://ovenapp.io/view/TPpwSKyqkmp6YRMUCOpwJnmkm7I7QKBR/Bwrws)에서 확인할 수 있습니다.

## Template

화면 마크업을 하실 때, `header`, `nav` 템플릿을 사용해주세요.
`template.html` 과 `styles/template.css` 를 참조하시면 됩니다.

<img src="https://user-images.githubusercontent.com/13795717/85216120-f6420700-b3bb-11ea-8ce6-47624629c65f.png" width="300">

## Development Guide

가장 먼저 Project repository를 본인의 원격 저장소로 fork 합니다.

![image](https://user-images.githubusercontent.com/13795717/85205573-23a89980-b357-11ea-9b9f-8f6b477148f8.png)


Fork 한 repository를 로컬에 clone 받습니다.

``` bash
$ git clone https://github.com/{본인_GitHub_계정}/drive-thru-app.git
$ cd drive-thru-app
```

원본 repository를 `upstream` 이라는 이름으로 remote에 추가합니다.
잘 추가가 되었는지 `git remote -v` 명령어로 확인할 수 있습니다.

``` bash
$ git remote add upstream https://github.com/Pigrabbit/drive-thru-app.git
```

새로운 기능을 추가할 때는 develop branch에서 branch를 새로 생성합니다.
Branch 이름은 아래 규칙에 맞도록 생성합시다.

- 기능을 추가하는 경우, `feature/{기능 이름}`
- 레이아웃을 추가하는 경우, `layout/{화면 이름}`

예를 들어 마이페이지 화면을 추가하는 경우, 아래와 같이 branch를 생성하시면 됩니다.

``` bash
// develop Branch에서 layout/mypage Branch를 생성
$ git checkout -b layout/mypage develop
```

작업을 마친 뒤에는 커밋을 하시면 됩니다.
다만, 커밋 메세지 작성에 유의합시다.
[다음 글](https://meetup.toast.com/posts/106)을 읽어보시면 좋을 것 같아요!

``` bash
$ git add .
$ git commit -m "Add mypage layout"
```

커밋한 이후에는 `rebase`를 해주세요!
`rebase`에 대한 자세한 설명은 [다음 글](https://velog.io/@godori/Git-Rebase)을 참조해주세요.
`rebase`이후 push 하시면 됩니다.

``` bash
$ git fetch upstream
$ git rebase origin/develop
$ git push origin layout/mypage
```

그 다음 원본 저장소로 오셔서 Pull Request를 생성해주시면 됩니다!

![image](https://user-images.githubusercontent.com/13795717/85207306-dcc0a100-b362-11ea-9fef-c0ad2042410d.png)


Pull Request는 팀원들의 review를 받은 뒤, PR을 올린 사람이 직접 merge 하도록 해요 :)