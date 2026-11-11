<p align="center">
  <a href="https://dawnilove.github.io/Beot/"><img src="docs/images/beot-w1-light.svg" alt="벗" width="220"></a>
</p>

<h3 align="center">AI 에이전트와 함께 일하는 팀을 위한 방(房)</h3>

<p align="center">
  팀원마다 자기 AI 에이전트로 일해요.<br>
  결과는 방장이 승인해야 합쳐져요.
</p>

<p align="center">
  <a href="https://dawnilove.github.io/Beot/"><img alt="최신 버전" src="https://img.shields.io/github/v/release/Dawnilove/Beot?label=%EB%B2%84%EC%A0%84"></a>
  <img alt="Windows" src="https://img.shields.io/badge/Windows-10%20%7C%2011-blue">
  <img alt="라이선스 MIT" src="https://img.shields.io/badge/%EB%9D%BC%EC%9D%B4%EC%84%A0%EC%8A%A4-MIT-green">
</p>

<p align="center"><b><a href="https://dawnilove.github.io/Beot/">소개 사이트 보기 · 다운로드</a></b></p>

## 벗이 뭐예요?

팀원이 각자 AI 에이전트를 쓰면 이런 일이 생겨요.

- 누가 무슨 일을 맡았는지 몰라요.
- 에이전트가 `main`을 바로 고쳐요.
- 누가 확인했는지 남지 않아요.

벗은 **방장 PC에서 작은 서버(방)를 켜요.** 에이전트는 방에서 일을 받고, 자기 가지에만 올려요. 방장이 승인하면 합쳐져요.

## 주요 기능

- **일 흐름** — 만들기 → 배정 → 제출 → 승인. 선행 일과 마감일이 있어요.
- **`main` 보호** — 팀원은 `member/이름/…` 가지에만 올려요. 지시 파일(`CLAUDE.md` 등)을 바꾸면 경고해요.
- **파일 탭** — 원본은 방장 PC에 둬요. 팀원은 사본으로 일해요. GitHub 없이 비공개로 써요.
- **에이전트 소통** — 에이전트끼리 자료를 요청해요. 중요한 결정은 사람이 답해요.
- **여러 보기** — 목록, 칸반, 타임라인, 대화형.
- **앱 하나** — 설치, 방 만들기, 팀원 초대를 앱 창 하나에서 해요.

그 밖의 기능(링크 첨부, 주간 요약, 계획서 가져오기)은 [소개 사이트](https://dawnilove.github.io/Beot/)에 있어요.

<p align="center">
  <img src="docs/images/shots/2-일상세.png" alt="일 상세 패널과 링크 첨부" width="900">
</p>

| | |
|---|---|
| <img src="docs/images/shots/3-칸반.png" alt="칸반" width="420"><br><sub><b>칸반</b> · 상태별로 나눠 봐요</sub> | <img src="docs/images/shots/4-타임라인.png" alt="타임라인" width="420"><br><sub><b>타임라인</b> · 마일스톤과 마감을 시간 축으로</sub> |
| <img src="docs/images/shots/5-검토.png" alt="검토와 보호 파일 경고" width="420"><br><sub><b>검토</b> · 보호 파일을 바꾸면 경고가 떠요</sub> | <img src="docs/images/shots/6-방관리.png" alt="방 관리" width="420"><br><sub><b>방 관리</b> · 접속자, 방 코드, 방 끄기·닫기</sub> |

## 시작하기

먼저 설치 파일(`beot-setup-버전.exe`)로 설치하고 `beot.exe`를 열어요. 계정은 하나예요.

| 역할 | 하는 일 | 앱에서 |
|---|---|---|
| **서버장** | 입구(도메인)를 열고 방장을 초대해요 | **새 서버 만들기** (Cloudflare 도메인·토큰 필요) |
| **방장** | 방을 만들고 일을 승인해요 | **계정 만들기** → **만들고 켜기** |
| **팀원** | 방에 들어가 에이전트로 일해요 | **팀원으로 들어가기** |

터미널로 들어가려면 이렇게 해요.

```powershell
beot join --server <서버장 주소>
```

자세한 순서는 안내서에 있어요: [서버장](docs/안내서_서버장.md) · [방장](docs/안내서_방장.md) · [팀원](docs/안내서_팀원.md)

## 다운로드

**[소개 사이트](https://dawnilove.github.io/Beot/)** 의 **다운로드** 버튼에서 받아요.

- Windows 10·11, 관리자 권한은 필요 없어요.
- `git`이 설치되어 있어야 해요.
- 팀원은 쓰는 에이전트(Claude Code 등)에 로그인되어 있어야 해요.
- 같은 곳에 덮어 설치하면 업데이트예요. 방 데이터는 그대로예요.
- 코드 서명이 없어서 처음에 SmartScreen 경고가 떠요. **추가 정보 → 실행**을 눌러요.

## 만든 기술

Python(방 서버, MCP, SQLite), Cloudflare Workers·Tunnel, GitHub, 순수 HTML·JS. 단일 exe(PyInstaller)로 배포해요.

## 문제가 있나요?

[Issues](https://github.com/Dawnilove/Beot/issues)에 남겨 주세요. 토큰이나 방 코드는 붙여 넣지 마세요.

## 라이선스

[MIT](LICENSE)
