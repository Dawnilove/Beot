# 외부 프로그램·라이브러리 고지 (Third-party notices)

`beot-0.1.1-windows.zip`에는 아래 소프트웨어가 함께 들어 있습니다. 각 라이선스는 해당 프로젝트에 따릅니다. 전체 라이선스 문구는 각 프로젝트 저장소(또는 PyPI 배포본의 LICENSE 파일)에서 볼 수 있습니다.

## 함께 배포하는 실행 파일
| 이름 | 라이선스 | 출처 |
|---|---|---|
| **cloudflared** (`tools/cloudflared.exe`) | Apache-2.0 | https://github.com/cloudflare/cloudflared (Cloudflare, Inc.) 수정 없이 그대로 넣었습니다 |
| **Python** 런타임 | PSF License | https://www.python.org |

## Python 라이브러리 (exe 안에 묶임)
| 이름 | 버전 | 라이선스 |
|---|---|---|
| annotated-types | 0.8.0 | MIT |
| anyio | 4.15.1 | MIT |
| attrs | 26.1.0 | MIT |
| certifi | 2026.10.23 | MPL-2.0 (인증서 목록 `cacert.pem`, https://github.com/certifi/python-certifi) |
| cffi | 2.1.1 | MIT-0 |
| click | 8.5.0 | BSD-3-Clause |
| cryptography | 50.0.2 | Apache-2.0 OR BSD-3-Clause |
| h11 | 0.16.0 | MIT |
| httpcore / httpx | 1.0.9 / 0.28.1 | BSD-3-Clause |
| httpx-sse | 0.4.3 | MIT |
| idna | 3.20 | BSD-3-Clause |
| jsonschema / jsonschema-specifications / referencing / rpds-py | 4.26.0 / 2025.9.1 / 0.37.0 / 2026.9.1 | MIT |
| mcp (Model Context Protocol SDK) | 1.30.0 | MIT |
| pillow | 13.0.0 | MIT-CMU |
| pycparser | 3.12 | BSD-3-Clause |
| pydantic / pydantic-settings / pydantic_core | 2.14.2 / 2.16.2 / 2.50.2 | MIT |
| PyJWT | 2.15.1 | MIT |
| python-dotenv | 1.2.4 | BSD-3-Clause |
| python-multipart | 0.0.32 | Apache-2.0 |
| pywin32 | 312 | PSF |
| six | 1.17.0 | MIT |
| sse-starlette / starlette / uvicorn | 3.6.0 / 1.10.0 / 0.54.0 | BSD-3-Clause |
| typing-inspection | 0.4.4 | MIT |
| typing_extensions | 4.16.0 | PSF-2.0 |
| **pystray** | 0.19.5 | **LGPL-3.0** (https://github.com/moses-palmer/pystray) |

### pystray (LGPL-3.0)에 대해
알림 영역 아이콘에 pystray를 씁니다. 이 라이브러리는 수정 없이, 별도 모듈 파일로 `_internal` 폴더 안에 들어 있습니다. LGPL-3.0에 따라 사용자는 이 모듈을 같은 인터페이스의 다른 버전으로 바꿔 쓸 수 있습니다. 소스는 위 저장소와 PyPI에서 받을 수 있습니다.

## 빌드 도구
exe는 **PyInstaller**(GPL-2.0, 부트로더 예외 포함)로 만들었습니다. PyInstaller의 예외 조항에 따라 만들어진 프로그램에는 GPL이 적용되지 않습니다.
