# Atom

## Packages
#### sync-settings
atom의 설정과 설치한 패키지들을 여러 기기에서 동기화할 수 있게 해준다.  
Github 설정에서 `Personal access tokens`에서 토큰 생성. gist 권한은 필수.
임의의 Gist 생성 후 주소에서 gist id.

#### project-manager
sublime text처럼 프로젝트 단위로 여러 폴더를 묶어서 저장, 로드할 수 있다.  
프로젝트를 저장하면 .project 파일이 해당 폴더에 생기는데, `Open folder`로 이 폴더를 열면 프로젝트 전체가 불러와진다.

#### linter
문법 검사. linter-flake8 등을 설치하려면 필수.

#### terminal-plus
atom에서 터미널 기능을 확장 시켜준다.

#### activate-power-mode
팡팡 이펙트!

#### autocomplete-python
파이썬 자동완성. virtualenv가 프로젝트 내에 있는 경우, 따로 경로를 바꿔주지 않아도 알아서 site-package의 모듈들을 인식하는 듯?

#### emmet
html 만질 땐 필수

#### file-icons
좌측 파일 트리의 아이콘들을 파일 타입에 매칭되도록 보기 좋게 바꿔준다.

#### minimap
sublime text에 있던 미니맵

## 단축키
모르고 있는 단축키 중에 유용한 것들만 정리했다.

- `Ctrl + Shift + P`: 커맨드 콘솔. 우분투에서 `L-Alt`와 비슷한 기능
- `Ctrl + \`: 트리 창 토글
- `Ctrl + g`: 행:열로 이동
- `Ctrl + r`: 코드의 목차 보기 및 이동

- `Ctrl + l`: 한 줄 선택
- `Shift + delete`: 한 줄 삭제

- `Ctrl + m`: 현재 커서의 괄호로 이동. 여는 괄호 닫는 괄호 모두 가능
- `Ctrl + Alt + m`: 현재 커서의 괄호 내용 선택

- `F11`: 전체화면
- `Ctrl + ,`: 설정 탭 열기
- `Ctrl + w`: 탭 닫기

- `Ctrl + Shift + M`: 마크다운 프리뷰
