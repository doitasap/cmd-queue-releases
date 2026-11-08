# 변경 이력

이 문서는 [Keep a Changelog](https://keepachangelog.com/ko/1.1.0/) 형식을 따릅니다.
릴리스 태그를 밀면 워크플로가 해당 버전 절을 릴리스 본문으로 가져갑니다.
릴리스 페이지는 영어 사용자도 보므로 버전 절마다 한국어 아래에 `---` 를 두고 같은 내용을 영어로 덧붙입니다.

## [Unreleased]

## [0.4.0] - 2026-11-09

### 추가

- 스케줄 화면이 생겼습니다. 특정일·매일·매주·매월·리셋 직후 같은 반복 규칙을 정해 두면 그 시각에 큐 항목을 만듭니다. 주간 한도·이전 회차·놓친 회차 조건을 걸 수 있고, 연속 3회 실패하면 규칙이 꺼집니다. ⌘1·⌘2 로 큐와 스케줄을 오가며, 단축키는 설정에서 바꿉니다.
- 헤더 결정함이 claude 세션이 사람의 결정을 기다리며 멈춘 질문을 카드로 모읍니다. 그 자리에서 답하면 대화형 터미널을 띄워 보내고, 「큐로 보내기」로 자동 큐 이어실행도 고를 수 있습니다.
- 헤더 🔍 또는 ⌘K 로 모든 세션에서 내가 했던 질문을 찾고, 결과를 눌러 그 세션 이력으로 바로 갑니다.
- 대화형 터미널 창 헤더의 ✎ 로 창을 닫지 않고 터미널 이름을 바꿉니다.
- 트레이 메뉴에 「후원하기…」를 넣었습니다. 누르면 GitHub Sponsors 페이지가 열립니다.

### 변경

- 대화형 터미널이 떠 있을 때 터미널 목록 단축키(기본 ⇧⌘T)를 누르면 「백그라운드로 계속」처럼 터미널을 내립니다. 프로세스는 계속 돕니다.
- 카드 세션 칩과 대화형 터미널 헤더의 세션 표기를 누르면 resume 명령 대신 전체 세션 ID 만 복사합니다.
- 자동 큐에서 같은 세션의 카드는 체인으로 묶여 차례로 이어 실행됩니다.

### 수정

- 리셋 시각이 잘린 채 다시 그려진 지난 한도 배너 때문에 큐가 멈추고 터미널이 회수되던 문제를 고쳤습니다.
- 터미널 이름을 편집하는 중에 즐겨찾기 별칭 편집이 함께 열리던 문제를 고쳤습니다.
- 업데이트 확인에 쓰는 인증서 검증 라이브러리(rustls-webpki)와 루트 인증서 묶음을, 신뢰가 철회된 중간 인증서를 받아들이던 보안 권고가 해소된 버전으로 올렸습니다.

---

### Added

- A new Schedule screen. Set a repeating rule (a specific date, daily, weekly, monthly, or right after a usage reset) and CmdQ creates a queue item at that time. Rules can depend on the weekly limit, the previous run, or missed runs, and a rule turns itself off after 3 failures in a row. Switch between Queue and Schedule with ⌘1 and ⌘2; you can change the shortcuts in Settings.
- The Decision inbox in the header collects questions where a claude session stopped to wait for your decision. Answer on the spot and CmdQ sends it through an interactive terminal, or pick "Send to queue" to continue it in the auto queue.
- Search your own prompts across every session with 🔍 in the header or ⌘K, and jump straight to that session's history.
- Rename a terminal with ✎ in the interactive terminal window header without closing the window.
- The tray menu has a "Sponsor…" item that opens the GitHub Sponsors page.

### Changed

- When an interactive terminal is open, the terminal list shortcut (⇧⌘T by default) sends it to the background like "Keep running in background". The process keeps running.
- Clicking the session chip on a card or the session label in the interactive terminal header copies only the full session ID instead of a resume command.
- In the auto queue, cards for the same session are chained and run one after another.

### Fixed

- A previous usage-limit banner redrawn with its reset time cut off no longer stops the queue and reclaims terminals.
- The bookmark alias editor no longer opens while you are renaming a terminal.
- The certificate verification library (rustls-webpki) and the bundled root certificates used for update checks are upgraded to versions that resolve advisories about trusting distrusted intermediate certificates.

## [0.3.0] - 2026-10-16

### 추가

- 백그라운드 터미널 목록에서 ✎ 를 눌러 터미널에 이름을 붙입니다. 이름은 목록·리셋 대기 행·터미널 창 헤더에 함께 보이고 앱을 다시 켜도 남습니다. 비우고 확정하면 자동 제목으로 돌아갑니다.
- 대화형 터미널 헤더의 🕐 로 그 세션의 질문 이력을 터미널 위에 엽니다. 닫으면 보던 터미널로 돌아갑니다.

### 변경

- 큐 작업은 시작 후 30분이 지났다고 멈추지 않고, 출력 없이 30분이 지났을 때 멈춥니다. 출력이 계속 나와도 6시간이 지나면 멈춥니다. 실패 사유에 둘 중 어느 쪽인지 남습니다.
- 앱 아이콘을 새 로고로 바꿨습니다.

### 수정

- 업데이트 확인 대화상자의 "CmdQ 을 다시 시작합니다" 조사 오류를 "앱이 다시 시작됩니다"로 고쳤습니다.
- 한도로 터미널이 회수되면 헤더 🕐 로 연 세션 이력도 함께 닫힙니다. 이력 창이 메인 화면 위에 남지 않습니다.
- 업데이트 확인에 쓰는 TLS 라이브러리(rustls)를 보안 권고가 해소된 버전으로 올렸습니다.

---

### Added

- Name a terminal with ✎ in the background terminal list. The name shows in the list, the waiting-for-reset row, and the terminal window header, and it stays after you restart the app. Clear it and confirm to go back to the automatic title.
- Open the session's prompt history over the terminal with 🕐 in the interactive terminal header. Closing it takes you back to the same terminal.

### Changed

- Queue tasks no longer stop 30 minutes after they start. They stop after 30 minutes with no output, and after 6 hours at most even if output keeps coming. The failure reason says which one applied.
- The app icon uses the new logo.

### Fixed

- The update dialog no longer shows a wrong Korean particle after the app name.
- When a terminal is reclaimed at the usage limit, the session history opened with 🕐 closes with it instead of staying over the main window.
- The TLS library (rustls) used for update checks is upgraded to a version that resolves recent security advisories.

## [0.2.0] - 2026-10-14

### 변경

- 트레이 「업데이트 확인…」에서 배포된 업데이트 정보를 찾지 못하면, 네트워크를 확인하라는 문구 대신 그 사실을 그대로 알립니다.
- 업데이트를 설치할 때 멈추는 작업 안내가 실제로 멈출 것만 말합니다. 실행 중인 자동 큐 작업이나 열린 대화형 터미널 중 0개인 쪽은 빠집니다.

---

### Changes

- When Check for Updates… in the tray can't find published update information, it now says so instead of asking you to check your network.
- Before installing an update, the warning lists only the work that will actually stop. Running auto-queue tasks or open interactive terminals are left out when there are none.

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
- Apple 공증을 받은 앱입니다. 새 버전이 나오면 설치할지 묻고, 서명을 확인한 뒤 업데이트합니다. 트레이의 「업데이트 확인…」으로 직접 확인할 수도 있습니다.

### 시작하기 전에

- Claude Code CLI 를 설치한 뒤 터미널에서 `claude` 를 한 번 실행해 Claude 계정으로 로그인해 두십시오. 로그인하지 않으면 큐 작업이 실행되지 않고 사용량도 보이지 않습니다.

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
- The app is notarized by Apple. When a new version is out, it asks before installing and verifies the signature before it updates. You can also check from Check for Updates… in the tray.

### Before you start

- Install the Claude Code CLI, then run `claude` once in a terminal and log in with your Claude account. Without a login, queued tasks don't run and usage isn't shown.
