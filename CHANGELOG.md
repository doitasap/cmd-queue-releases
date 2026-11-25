# 변경 이력

이 문서는 [Keep a Changelog](https://keepachangelog.com/ko/1.1.0/) 형식을 따릅니다.
릴리스 태그를 밀면 워크플로가 해당 버전 절을 릴리스 본문으로 가져갑니다.
릴리스 페이지는 영어 사용자도 보므로 버전 절마다 한국어 아래에 `---` 를 두고 같은 내용을 영어로 덧붙입니다.

## [Unreleased]

### 추가
- MCP 허브에서 서버를 찾아 프로젝트에 추가하고 자료 대화·수집·큐 실행에서 쓴다 (5d1934c)
- 외부 일감을 받은 일감 인박스로 받아 승인하면 큐에 넣고 성공하면 원본에 회신한다 (b3d9f26)
- 받은 일감 연결 마법사·승인 화면을 다듬고 Todoist 프로젝트 규칙과 승인 때 명령 수정·큐 선택을 더한다 (ced218b)
- 자료 링크가 스크립트로 늦게 그리는 페이지·표·이미지를 받고, 격리 밖 수정과 원본 변경을 보여 준다 (9c64ea5)
- 자료를 확장자에 맞게 보고 저장한 페이지를 고치며 자료 대화에 파일을 첨부하고 지난 대화로 돌아간다 (32cbb29)
- 반복 스케줄에 하루 여러 시각과 매월 여러 날짜를 지정한다 (f6d6947)
- 자동 큐에 완료 항목 모두 지우기 버튼을 단다 (5a55b84)
- \#230 아이디어 탭에서 주제로 대화하고, 제안·큐로 실행한 결과를 다시 대화로 돌려받는다 (063fabb)
- 연결 모듈까지 읽어 분석하고, 다른 모듈 변경은 제안함으로 받는다 (bbf5be7)
- 알림 팝업에서 여러 질문 결정에 답하고 제안을 수락·기각한다 (47c55a3)
- 응답 보기·세션 이력 창에 ⌘F 찾기 막대를 추가한다 (4723051)
- 아이디어 대화에 상태·목표, 스케줄 회차 추적, 리포트 파일을 더한다 (490355a)
- 스케줄 규칙에 커넥터 이벤트 트리거를 더한다 (5ffcc89)
- 커넥터 규칙 편집기에서 조회 인자 형식과 필터 값 후보, 커넥터 선택 순서를 알려 준다 (3d7b7fd)

### 변경
- 스케줄 회차를 큐 화면에서 숨기고 실행 기록에서 응답·터미널·세션 이력을 열며, 스케줄 회차는 동시 실행 상한에 세지 않는다 (0825dc2)
- 이름을 붙인 터미널은 ☆ 로 즐겨찾기할 때 그 이름을 별칭으로 저장한다 (6847e61)
- 첨부 다이얼로그에서도 링크 이름을 바꿀 수 있게 한다 (28ddaee)
- 연결 추가 샘플 표에서 본문 열을 빼고, 회신 단계에 마친 뒤 Claude 에게 시킬 일 입력란을 더한다 (8d22a03)
- 소스 설정에서 마친 뒤 Claude 에게 시킬 일을 고칠 수 있게 한다 (0770e5d)
- 일감으로 받아온 작업은 세션이 조용해진 뒤 닫고 카드에 처리 완료 버튼을 둔다 (ebdcafa)
- 카드 첨부를 마커 없이도 목차로 넘겨 작업 중 필요한 것만 읽게 한다 (969eb8f)
- 대화형으로 넘긴 카드의 터미널도 한도 리셋 뒤 자동으로 이어 간다 (d1130b1)
- 큐 카드·헤더·제안 칩에 색과 위계를 되살리고 목록만 스크롤한다 (3f9bbd7)
- 받은 일감을 ⌘L 로 여닫고 단축키 설정에서 바꿀 수 있게 한다 (9798756)
- 받은 일감 승인의 기본값을 To Do 큐와 격리 끔으로 바꾼다 (c603f5a)
- 아이디어 링크 첨부에서 「로그인이 필요한 링크」 체크를 없앤다 (741d8c4)
- 아이디어 탭에서도 / 를 누르면 대화하기 입력칸으로 포커스를 옮긴다 (4996530)
- 격리 결과 diff 본문을 git diff 처럼 추가·제거 줄마다 색칠한다 (7f2777a)
- 제안 「바로 큐에 넣기」 카드를 제안 경로의 탭에 넣고 그 탭을 열어 활성화한다 (ab28cb4)
- [자료] 표시가 없어도 첫 실행에 프로젝트 자료 목차 경로를 안내 블록으로 넘긴다 (fce43f7)
- 소스 설정에서 연결 규칙의 연결 키를 고치고 규칙을 지울 수 있게 한다 (eaff606)
- 격리 세션 결정 답신을 원 경로 카드로 잇는다 (fd167be)
- 격리 worktree 안에서 생긴 카드의 경로를 탭으로 더한다 (52f746a)
- 회차 감지 첨부를 서랍에서 따로 보이고 실행 기록에서 연다 (5649593)

### 수정
- 큐 항목이 턴을 끝냈는데도 실행 중으로 남지 않게 마지막 결과로 확정한다 (5aa3ab2)
- 격리 결과 diff 창에서 변경 파일 없음 문구가 세로로 꺾이지 않게 한다 (d037a3f)
- 자료 목록에서 요약 없음과 원본이 바뀜 배지가 겹치지 않게 나란히 둔다 (64c7174)
- 자료 대화 빈 화면이 재시작하면 대화가 비워진다고 잘못 안내하지 않게 한다 (fad0d01)
- 한도로 회수돼 리셋을 기다리는 터미널을 트레이 줄과 리셋 대기 점에 센다 (5957975)
- 트레이 영어 문구에서 터미널 리셋 대기 칸이 자동 큐 대기와 구분되게 한다 (e27d2e6)
- 트레이 아이콘 갱신이 메인 스레드와 서로 기다려 앱이 멈추던 문제를 고친다 (831c6b1)
- 자료 드로어 단축키를 한 번 더 누르면 드로어를 닫는다 (0f875bf)
- \#226 개발 DB 의 메타 42 에서 기동하지 못하던 마이그레이션 복구 순서를 고친다 (abb70e7)
- 변경 없이 정리된 격리 worktree 를 되살려 결정 답신·터미널로 잇고, 결정함·제안함은 맨 위 카드를 펼쳐 이어 펼친다 (b25396d)
- 제안함 처리 기록 행이 칩을 타원으로 늘리고 결과를 잘라 먹던 배치를 고친다 (6ff27ce)
- 대화형으로 넘긴 카드가 한도 회수 뒤 리셋 대기에 갇히지 않게 한다 (985b316)
- 트레이 상태 점 색을 되살리고 메뉴 항목에 이모지를 붙인다 (d273f93)
- 결정함에서 펼친 카드를 처리하면 다음 카드가 펼쳐지게 한다 (3248b0d)
- MCP 서버를 바꾸면 열어 둔 자료 대화의 MCP 상태를 다시 읽는다 (05a62bb)
- 연계 조회가 게이트웨이 오류(502·503·504)를 받으면 두 번까지 다시 보낸다 (fe0e154)
- 결정함 ↗ 터미널이 변경 없이 정리된 격리 worktree 를 되살린 뒤 세션을 연다 (2bd8c94)
- 격리 결과의 변경 파일 수와 diff 에 커밋 전 변경도 보인다 (a18ce98)
- 감지 첨부 줄의 × 를 사용자 첨부 줄과 같은 칸에 둔다 (14df22e)

## [0.5.0] - 2026-11-16

### 추가

- 큐 항목을 격리 실행할 수 있습니다. 추가바 아래 줄의 「격리 실행」을 켜면 그 항목을 별도 git worktree 에서 돌리고, 끝나면 병합·버리기·브랜치로 남기기 중에서 고릅니다. git 저장소가 아닌 경로에서는 이 토글이 보이지 않습니다.
- 스케줄 규칙의 「완료 후 카드」로 성공한 회차의 카드를 큐에서 지울 수 있습니다. 경로별 기본 규칙은 설정 › 스케줄 카드 정리에서 경로마다 탭을 나눠 정하고, 지울 카드를 미리 보고 확인해야 적용됩니다. 지운 내역은 실행 기록의 「정리 기록」 탭에 남습니다.
- 자료 드로어가 대화·자료·연결 세 탭으로 나뉘었고, 큐 작성 화면은 대화 탭 자리에 뜹니다.
- 자료 대화가 저장되어 앱을 다시 띄워도 이어서 물을 수 있습니다. 결정함에서 처리한 결과는 다음 질문에 함께 전달됩니다.
- 자료 대화에서 「MCP 도 함께 묻기」를 켜면 MCP 서버가 연결된 프로젝트에서 그 서버의 읽기 도구로 원본에도 묻습니다. 답의 근거는 「자료」와 「원본(MCP)」로 나눠 보여 줍니다. 쓰기 도구와 다른 MCP 서버, 저장소 파일 읽기는 막혀 있고, 지금은 GitHub 서버만 지원합니다.
- MCP 서버로 하위 본문과 본문 안 링크를 재귀로 수집합니다. 지금은 GitHub 이슈·PR·파일 주소만 되고, 깊이는 기본 3(1~10)이며 페이지마다 claude 를 한 번씩 실행합니다.
- MCP 로 수집한 페이지에서 「원본과 대조」를 누르면 그 페이지만 다시 받아 줄 번호와 바뀐 단어를 보여 줍니다. 저장본을 바꾸거나 원본 갱신 필요 제안으로 남길 수 있습니다.
- 웹뷰 수집이 로그인 화면에 닿으면 멈춥니다. 같은 웹뷰에서 로그인한 뒤 이어 받으면 됩니다.
- 연결 모듈을 「폴더 고르기」로 직접 잇습니다. 열린 탭 여러 개를 한 번에 고를 수 있고, 자료가 아직 없는 폴더도 연결됩니다. 모듈마다 붙임을 끄고 켤 수 있으며, 경로가 없는 모듈은 붙이지 않습니다. 끊었던 모듈을 다시 연결하면 붙은 상태로 시작합니다.
- 연결 탭에서 연결 모듈을 목록과 그래프로 바꿔 봅니다. 그래프는 관계 종류와 방향 화살표, 노드 역할을 겹치지 않게 그리고, 빌드 도구에서 알 수 있는 의존 관계는 자동으로 채웁니다. 그래프에서 바로 탭을 열거나 연결을 끊을 수도 있습니다.
- 연결 폴더 루트의 CLAUDE.md·AGENTS.md·README.md 를 질문과 `[자료]` 실행, 자료 대화에 문서로 붙입니다. 이 사본은 앱 데이터의 `linked-docs/` 에 생깁니다.
- 자료 목록의 「선택」으로 여러 자료를 골라 한 번에 지웁니다.
- 결정 요청과 🔔 를 켠 카드의 완료를 데스크톱 팝업이나 상단 위젯으로 알립니다. 알림 방식은 설정 › 알림에서 고릅니다.
- 「뒤로」로 빠져나온 화면을 「앞으로」 단축키(⌃→)로 다시 엽니다.

### 변경

- 데이터베이스가 v38 로 올라갑니다(v33~v38 마이그레이션). 기존 스케줄 규칙의 「카드 유지」는 「경로 기본값 따름」으로 바뀌지만, 경로 규칙이 없거나 꺼져 있으면 예전처럼 카드를 남기므로 동작은 그대로입니다.
- 연결 모듈 개수 상한 설정을 없앴습니다. 업데이트하면 그동안 상한 때문에 빠지던 연결 모듈도 모두 붙고, 한 번에 붙는 수는 내부 안전 한도인 200개까지입니다.
- 결정함 답신은 기본으로 큐로 보내고, 「터미널로 보내기」는 보조 버튼으로 옮겼습니다. 큐로 간 답신은 그 세션을 처음 실행한 경로의 카드 아래에 묶입니다.
- 추가바의 알림 체크박스를 없앴습니다. 새 카드는 설정의 「새 카드 🔔 기본값」을 따르고, 🔔 는 카드나 대화형 터미널 머리에서 켜고 끕니다.
- 자료 수집 중 공개 사이트에서 사설 주소로 넘어가는 리다이렉트와 iframe 을 막습니다. 확인 대기 중인 자료 변경이 있으면 링크 다시 저장과 폴더 다시 가져오기를 멈추는 식으로 자료 무결성 검사도 보강했습니다.
- 자료 이름을 바꾸면 상세 화면 제목이 웹뷰를 다시 불러오지 않고 바로 바뀝니다.

### 수정

- 본문이 sandbox iframe 안에만 있는 링크(Drop 등)도 본문 저장과 웹뷰 수집이 됩니다. iframe 주소에 든 토큰은 기록이나 화면에 남기지 않습니다.
- 저장된 자료 대화를 읽지 못하면 새 질문이 대화 전체를 덮어쓰던 문제를 고쳤습니다. 이제 원래 파일을 앱 데이터의 `ask-chat-backup/` 에 옮겨 둔 뒤 저장합니다.
- 결정함에서 정정 제안을 승인해도 열려 있던 자료 화면에 옛 본문이 보이던 문제를 고쳤습니다.
- 저장소 경로를 대소문자만 다르게 적었을 때 아직 없는 자료 폴더가 저장소 안에 있다는 것을 놓쳐 자료 폴더 읽기까지 막히던 문제를 고쳤습니다.
- 자료 대화와 결정함의 작은 화면 문제를 고쳤습니다. 무결성 카드가 내부 라벨 대신 「항목 #1」처럼 보이고, 「큐로 이어가기」 인용 카드에서 마크다운 기호가 빠지며, 후속 지시 템플릿 관리 화면에서 겹치던 제목을 정리했습니다.

---

### Added

- Run a queue item in isolation. Turn on "Isolated run" in the row under the add bar and the item runs in a separate git worktree; when it finishes, you choose to merge, discard, or keep it as a branch. The toggle is hidden for paths that are not git repositories.
- With "Card after the run completes" on a schedule rule, the card of a successful run can be removed from the queue. Set a per-path default under Settings › Schedule card cleanup, which now has a tab for each path; a path rule takes effect only after you preview and confirm the cards it would remove. Removed cards are listed on the "Cleanup log" tab of the run history.
- The materials drawer now has three tabs, Chat, Materials, and Links, and the queue composer opens in place of the Chat tab.
- Materials chat is saved, so you can keep asking after restarting the app. Results you handled in the Decision inbox are passed along with your next question.
- Turn on "Also ask MCP" in materials chat and, in a project with a connected MCP server, claude also asks the source through that server's read-only tools. Answers show their sources split into "Material" and "Source (MCP)". Write tools, other MCP servers, and reading repository files are blocked. Only the GitHub server is supported for now.
- Collect sub-pages and in-body links recursively through an MCP server. Only GitHub issue, PR, and file URLs are supported for now; depth defaults to 3 (1–10), and claude runs once per page.
- On a page collected through MCP, "Compare with source" re-fetches just that page and shows line numbers and changed words. You can replace the saved copy or leave a source-outdated proposal.
- Webview collection pauses when it reaches a sign-in page. Sign in in the same webview, then resume.
- Link a module directly with "Choose folder". You can pick several open tabs at once, and folders that have no materials yet can be linked too. Attach can be turned on or off per module, and modules whose path is missing are not attached. A module you unlinked and link again starts out attached.
- Switch the Links tab between List and Graph. The graph draws relation types, direction arrows, and node roles without overlapping, and fills in dependencies that the build tools reveal. You can open a tab or unlink a module right from the graph.
- CLAUDE.md, AGENTS.md, and README.md at the root of a linked folder are attached as documents to questions, `[자료]` runs, and materials chat. These copies are stored under `linked-docs/` in the app data.
- Use "Select" in the materials list to pick several materials and delete them at once.
- Decision requests and the completion of cards with 🔔 on can now appear as a desktop popup or a top widget. Choose the style in Settings › Notifications.
- Reopen a screen you left with "Back" using the "Forward" shortcut (⌃→).

### Changed

- The database moves to v38 (migrations v33–v38). "Keep the card" on existing schedule rules becomes "Follow path default", but when there is no path rule or it is off, the card is kept as before, so behavior does not change.
- The setting that capped the number of linked modules is gone. After updating, linked modules that the cap used to leave out are all attached, up to an internal safety limit of 200 at a time.
- Replies from the Decision inbox now go to the queue by default, and "Send to terminal" moved to a secondary button. A reply sent to the queue is grouped under the card of the path where that session first ran.
- The notification checkbox in the add bar is gone. New cards follow "🔔 on new cards" in Settings, and you turn 🔔 on or off in the card or interactive terminal header.
- Material collection blocks redirects and iframes that lead from a public site to a private address. Material integrity checks are stricter too; for example, saving a link again or re-importing a folder pauses while a material change is waiting for review.
- Renaming a material updates the detail header title right away without reloading the webview.

### Fixed

- Links whose body lives only inside a sandboxed iframe (such as Drop) can now be saved and collected through the webview. Tokens in the iframe URL are not kept in logs or shown on screen.
- If a saved materials chat could not be read, a new question no longer overwrites the whole chat. The original file is moved to `ask-chat-backup/` in the app data before saving.
- Approving a correction proposal in the Decision inbox no longer leaves the old text on an open materials screen.
- Fixed a case where, if the repository path was written with different letter case, CmdQ missed that a not-yet-created materials folder sits inside the repository and reading the materials folder was blocked.
- Fixed minor display issues in materials chat and the Decision inbox: integrity cards show labels such as "Item #1" instead of internal ones, quote cards in "Continue in queue" drop Markdown symbols, and the overlapping title on the follow-up template screen is cleaned up.

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
