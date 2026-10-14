# 변경 이력

이 문서는 [Keep a Changelog](https://keepachangelog.com/ko/1.1.0/) 형식을 따릅니다.
릴리스 태그를 밀면 워크플로가 해당 버전 절을 릴리스 본문으로 가져갑니다.
릴리스 페이지는 영어 사용자도 보므로 버전 절마다 한국어 아래에 `---` 를 두고 같은 내용을 영어로 덧붙입니다.

## [Unreleased]

## [0.1.1] - 2026-10-14

앱 기능은 0.1.0 과 같습니다. 0.1.0 을 쓰고 있다면 앱이 이 버전을 찾아 스스로 업데이트합니다.

### 안내

- CmdQ 를 쓰려면 Claude Code CLI 를 설치한 뒤 터미널에서 `claude` 를 한 번 실행해 Claude 계정으로 로그인해 두어야 합니다. 로그인하지 않으면 큐 작업이 실행되지 않고 사용량도 보이지 않습니다. README 와 다운로드 페이지의 설치 안내에 이 단계를 넣었습니다.

---

The app works the same as 0.1.0. If you're on 0.1.0, the app finds this version and updates itself.

### Notes

- To use CmdQ, install the Claude Code CLI, then run `claude` once in a terminal and log in with your Claude account. Without a login, queued tasks don't run and usage isn't shown. The installation guides in the README and on the download page now include this step.

## [0.1.0] - 2026-10-14

첫 공개 릴리스입니다.

### 주요 기능

- 프로젝트 경로별로 Claude Code 명령을 큐에 넣고 위에서부터 차례로 실행합니다.
- 사용 한도에 걸린 작업은 실패로 끝내지 않고 리셋을 기다렸다가 이어서 실행합니다.
- 메뉴 막대에서 진행 상황과 5시간·주간 사용량, 리셋까지 남은 시간을 봅니다.
- 바로 돌릴 일은 자동 큐에, 검토할 일은 To Do 에 나눠 둡니다. claude 세션은 대화형 터미널로 직접 열 수도 있습니다.
- 자주 쓰는 세션을 즐겨찾기로 고정해 경로별로 다시 엽니다.
- 명령 입력창에서 `/` 로 스킬을 자동완성하고 파일·링크·메모를 첨부합니다.
- 한국어와 영어 화면을 지원합니다.
- Apple 공증을 받은 앱입니다. 새 버전이 나오면 서명을 확인한 뒤 스스로 업데이트합니다.

---

The first public release.

### Highlights

- Queue Claude Code commands per project path and run them in order, top to bottom.
- Tasks that hit the usage limit don't fail. They wait for the reset and then continue.
- See progress, 5-hour and weekly usage, and the time left until reset from the menu bar.
- Keep tasks to run right away in the auto queue and tasks to review in To Do. You can also open claude sessions directly in an interactive terminal.
- Pin sessions you use often as bookmarks and reopen them by path.
- Autocomplete skills with `/` in the command input, and attach files, links, and notes.
- The interface is available in Korean and English.
- The app is notarized by Apple. When a new version is out, it verifies the signature and updates itself.
