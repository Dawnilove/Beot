<p align="center">
  <a href="https://dawnilove.github.io/Beot/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="docs/images/beot-w1-dark.svg">
      <img src="docs/images/beot-w1-light.svg" alt="벗" width="220">
    </picture>
  </a>
</p>

<h3 align="center">AI 에이전트와 함께 일하는 팀을 위한 프로젝트 서버</h3>

<p align="center">팀원마다 자기 AI 에이전트로 일해요. 결과는 리더가 승인해야 합쳐져요.</p>

<p align="center">
  <b><a href="https://github.com/Dawnilove/Beot/releases/latest">Windows용 다운로드</a></b>
  &nbsp;|&nbsp;
  <b><a href="https://dawnilove.github.io/Beot/">소개 사이트</a></b>
  &nbsp;|&nbsp;
  <a href="docs/안내서/벗_안내서.md">벗 안내서</a>
</p>

<p align="center">
  <a href="https://dawnilove.github.io/Beot/"><img alt="최신 버전" src="https://img.shields.io/github/v/release/Dawnilove/Beot?label=%EB%B2%84%EC%A0%84"></a>
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%7C%2011-blue">
  <img alt="라이선스 MIT" src="https://img.shields.io/badge/%EB%9D%BC%EC%9D%B4%EC%84%A0%EC%8A%A4-MIT-green">
</p>

## 3단계로 써요

1. **리더**: `beot-setup-버전.exe`로 설치하고 `beot.exe`를 열어요. 서버장에게 받은 초대 코드로 **계정 만들기**를 하고, **만들고 켜기**로 프로젝트를 만들어 팀원을 초대해요.
2. **팀원**: 프로젝트 코드를 받아 **기존 서버 들어가기**를 눌러요. 자기 에이전트가 일을 받아 `member/이름/…` 가지에 올려요.
3. **리더**: 제출된 일을 보고 승인해요. 승인한 일만 `main`에 합쳐져요.

> [!IMPORTANT]
> **1.1.7 — 안내 챗봇과 전체 일 트리.**
> 1.1.6 이하를 쓰면 **리더 PC부터** 올려요. 올리기 전에 `beot backup`으로 프로젝트를 백업해요. 팀원 PC는 그다음에 올리고, 무인 도우미(`beot agent`)를 다시 켜요. [바뀐 점 전부 보기](https://github.com/Dawnilove/Beot/releases/tag/v1.1.7)

## 1.1.7에서 바뀐 점

- **안내 챗봇** — 프로젝트 화면의 안내 봇이 묻는 말에 답해요. 봇은 리더 작업 폴더를 읽기만 하고, 비밀 경로는 읽지 않아요. 연결 기능(`beot guide link`)은 리더가 데스크톱 앱에서 연결해야 써요.
- **전체 일 트리** — 일 사이의 연결선을 그려요. 가지를 접고 펴요. 후행 일의 진행률과, 선행을 기다리는 일의 대기 배지를 보여 줘요.
- **결함 수정** — 프로젝트를 지웠다가 같은 이름으로 다시 만들면 리더 로그인이 막히던 결함을 고쳤어요. 토큰이 거절되면 토큰 문제라고 알려 줘요.
- **업데이트 확인** — 앱이 새 버전을 30분마다 확인해요(전에는 6시간).

## 1.1.6에서 바뀐 점

- **이름 바꾸기** — 방은 프로젝트, 방장은 리더, 방 코드는 프로젝트 코드가 됐어요. 명령에 `--project`가 생겼고 `--room`도 계속 받아요.
- **도움말 모드** — 설정 · 프로젝트 화면의 **[도움말]**을 누르고 단추를 누르면 기능, 쓰는 때, 명령어, 안내서 절을 보여 줘요(46항목).
- **파일 탭** — 같은 이름의 파일은 경로를 같이 보여 줘요. 폴더를 지울 수 있어요.
- **자동 분배 기본 켬** — 담당이 없는 일을 자동으로 나눠요. 기존 프로젝트도 켜져요. 원하지 않으면 프로젝트 화면의 스위치로 꺼요.

> [!WARNING]
> `beot start`의 옛 `--project`(팀원 폴더 이름)는 `--folder-name`으로 바뀌었어요. 새 `--project`는 `--room`과 같은 뜻(프로젝트 고르기)이에요. `beot start --project …`를 쓰던 사람은 `--folder-name`으로 바꿔요.

1.1.5의 바뀐 점(리더 에이전트, 1차 검토, 여러 PC, 첫 화면 대시보드, 토큰 대리)은 [1.1.5 릴리스 노트](https://github.com/Dawnilove/Beot/releases/tag/v1.1.5)에 있어요.

## 벗이 뭐예요?

팀원이 각자 AI 에이전트를 쓰면 이런 일이 생겨요.

- 누가 무슨 일을 맡았는지 몰라요.
- 에이전트가 `main`을 바로 고쳐요.
- 누가 확인했는지 남지 않아요.

벗은 **리더 PC에서 작은 서버(프로젝트)를 켜요.** 에이전트는 프로젝트에서 일을 받고, 자기 가지에만 올려요. 리더가 승인하면 합쳐져요.

## 주요 기능

- **일 흐름** — 만들기 → 배정 → 제출 → 승인. 선행 일과 마감일이 있어요.
- **`main` 보호** — 팀원은 `member/이름/…` 가지에만 올려요. 지시 파일(`CLAUDE.md` 등)을 바꾸면 경고해요.
- **파일 탭** — 원본은 리더 PC에 둬요. 팀원은 사본으로 일해요. GitHub 없이 비공개로 써요.
- **사람이 결정** — 승인 · 반려와 결정 요청의 답은 비밀번호로 로그인한 사람만 해요.
- **에이전트 소통** — 에이전트끼리 자료를 요청해요. 중요한 결정은 사람에게 물어요.
- **리더 에이전트** — 계획서 초안을 쓰고 일을 나눠요. 1차 검토를 통과한 일만 사람이 승인해요.
- **토큰 대리** — 에이전트 설정 파일에 프로젝트 토큰을 두지 않아요. 토큰은 이 PC의 토큰 저장소에만 있어요.
- **여러 보기** — 첫 화면 대시보드, 목록, 칸반, 타임라인, 대화형.
- **앱 하나** — 설치, 프로젝트 만들기, 팀원 초대를 앱 창 하나에서 해요. 모르는 단추는 도움말 모드로 확인해요.

그 밖의 기능(링크 첨부, 주간 요약, 계획서 가져오기)은 [소개 사이트](https://dawnilove.github.io/Beot/)에 있어요.

<p align="center">
  <img src="docs/images/shots/2-일상세.png" alt="일 상세 패널과 링크 첨부" width="900">
</p>

| | |
|---|---|
| <img src="docs/images/shots/3-칸반.png" alt="칸반" width="420"><br><sub><b>칸반</b> · 상태별로 나눠 봐요</sub> | <img src="docs/images/shots/4-타임라인.png" alt="타임라인" width="420"><br><sub><b>타임라인</b> · 마일스톤과 마감을 시간 축으로</sub> |
| <img src="docs/images/shots/5-검토.png" alt="검토와 보호 파일 경고" width="420"><br><sub><b>검토</b> · 보호 파일을 바꾸면 경고가 떠요</sub> | <img src="docs/images/shots/10-기준문서.png" alt="프로젝트 관리의 기준 문서 편집" width="420"><br><sub><b>기준 문서</b> · 리더가 지시서를 화면에서 고쳐요</sub> |
| <img src="docs/images/shots/9-결정답하기.png" alt="대화 칸의 결정 요청과 선택지 버튼" width="420"><br><sub><b>결정 요청에 답하기</b> · 나에게 온 질문에 버튼으로 답해요</sub> | <img src="docs/images/shots/11-비밀번호확인.png" alt="승인할 때 뜨는 비밀번호 확인 창" width="420"><br><sub><b>비밀번호 확인</b> · 승인 같은 결정은 사람만 해요</sub> |

<sub>화면 사진은 1.1.0 화면이에요. 지금 화면의 이름(프로젝트, 리더)과 다를 수 있어요.</sub>

## 시작하기

먼저 설치 파일(`beot-setup-버전.exe`)로 설치하고 `beot.exe`를 열어요. 계정은 하나예요.

| 역할 | 하는 일 | 앱에서 |
|---|---|---|
| **서버장** | 입구(도메인)를 열고 리더를 초대해요 | **서버 열기** (Cloudflare 도메인·토큰 필요) |
| **리더** | 프로젝트를 만들고 일을 승인해요 | **계정 만들기** → **만들고 켜기** |
| **팀원** | 프로젝트에 들어가 에이전트로 일해요 | **기존 서버 들어가기** |

팀원은 처음 들어올 때 프로젝트 비밀번호를 정해요. 터미널로 들어가려면 이렇게 해요.

```powershell
beot join --server <서버장 주소>
```

자세한 순서는 [벗 안내서](docs/안내서/벗_안내서.md)(책 1권, [PDF](docs/안내서/벗_안내서.pdf))에 있어요: [서버장](docs/안내서/벗_안내서.md#2부-서버장) · [리더](docs/안내서/벗_안내서.md#3부-리더) · [팀원](docs/안내서/벗_안내서.md#4부-팀원)

벗 전체를 처음부터 읽으려면 [정리 문서](docs/정리문서/)(HWPX 8권, 에이전트용 md)를 봐요. 정리 문서는 1.1.4 기준이라 옛 이름(방, 방장)을 써요.

## 다운로드

**[소개 사이트](https://dawnilove.github.io/Beot/)** 의 **다운로드** 버튼에서 받아요.

- Windows 10·11, 관리자 권한은 필요 없어요.
- `git`이 설치되어 있어야 해요.
- 팀원은 쓰는 에이전트(Claude Code 등)에 로그인되어 있어야 해요.
- 같은 곳에 덮어 설치하면 업데이트예요. 프로젝트 데이터는 그대로예요. 앱의 **지금 업데이트**로도 올려요.
- 코드 서명이 없어서 처음에 SmartScreen 경고가 떠요. **추가 정보 → 실행**을 눌러요.

## 만든 기술

Python(프로젝트 서버, MCP, SQLite), Cloudflare Workers·Tunnel, GitHub, 순수 HTML·JS. 단일 exe(PyInstaller)로 배포해요.

## 문제가 있나요?

[Issues](https://github.com/Dawnilove/Beot/issues)에 남겨 주세요. 토큰이나 프로젝트 코드는 붙여 넣지 마세요.

## 라이선스

[MIT](LICENSE)
