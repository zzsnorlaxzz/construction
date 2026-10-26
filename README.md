# 수학 작도 교실

중학교 1학년 수학의 선분·각·삼각형 작도를 위한 두 가지 프로그램입니다.
하나의 GitHub 저장소에서 각 프로그램을 서로 다른 주소로 제공합니다.

## 프로그램 바로 열기

- [프로그램 선택 화면](https://zzsnorlaxzz.github.io/construction/)
- [프로그램 1 · 선분과 각 작도](https://zzsnorlaxzz.github.io/construction/program1/)
- [프로그램 2 · 삼각형 작도](https://zzsnorlaxzz.github.io/construction/program2/)

## 배포할 파일

```text
docs/
├─ .nojekyll
├─ index.html          # 프로그램 선택 화면
├─ program1/
│  └─ index.html       # 선분과 각 작도
└─ program2/
   └─ index.html       # 삼각형 작도
```

각 프로그램은 필요한 기능이 HTML 파일 안에 들어 있어 별도 설치나 서버 프로그램 없이 실행할 수 있습니다.
PC에서 확인할 때는 `docs/index.html`을 브라우저로 여세요.

## GitHub Pages 배포

1. GitHub 저장소의 최상위 위치에 `docs` 폴더를 업로드합니다. 하위 두 프로그램 폴더도 함께 올립니다.
2. 저장소의 **Settings → Pages**로 이동합니다.
3. **Source**에서 **Deploy from a branch**를 선택합니다.
4. **Branch**에서 파일을 올린 브랜치(보통 `main`)와 **`/docs`**를 선택하고 **Save**를 누릅니다.
5. 배포가 완료되면 Pages 화면에 표시된 주소로 접속합니다.

주소는 다음처럼 나뉩니다. `아이디`와 `저장소이름`은 실제 값으로 바꾸세요.

| 화면 | 주소 형식 |
|---|---|
| 프로그램 선택 | `https://아이디.github.io/저장소이름/` |
| 선분과 각 작도 | `https://아이디.github.io/저장소이름/program1/` |
| 삼각형 작도 | `https://아이디.github.io/저장소이름/program2/` |

학생들에게는 프로그램별 주소를 직접 안내하거나 각각 QR코드로 만들어 제공하면 됩니다.
저장소 이름에 계정 사이트 규칙(`아이디.github.io`)을 사용하는 경우에는 주소에서 저장소 이름 부분이 빠집니다.

## 프로그램 업데이트

배포된 프로그램을 바꾸려면 해당 `docs/program1/index.html` 또는 `docs/program2/index.html`을 교체하고 저장소에 반영하세요.

제작 작업 폴더에서는 다음 명령으로 원본 출력 파일과 `docs`의 배포용 파일을 함께 갱신합니다.

```powershell
python tmp/build_programs.py
node tmp/test-programs.cjs
```

이 명령은 제작용 `tmp` 파일이 있는 작업 폴더에서 사용합니다. GitHub Pages에 업로드할 때는 `docs` 폴더만으로 실행됩니다.

배포용 압축 파일은 `output/github-pages/triangle-construction-pages.zip`에 생성됩니다. 압축을 풀면 `docs` 폴더와 이 안내 파일이 나옵니다.
