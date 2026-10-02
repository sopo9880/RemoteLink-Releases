# RemoteLink · Windows Agent

Windows PC에서 RDP·SSH와 허용한 TCP 서비스를 연결하는 RemoteLink Agent의 공개 배포 저장소입니다. 이 저장소에는 설치 파일, SHA256 체크섬과 버전 안내만 게시합니다. 개발 소스는 별도의 비공개 저장소에서 관리합니다.

## 다운로드

[공개 Releases](https://github.com/sopo9880/RemoteLink-Releases/releases)에서 `RemoteLink-Setup-Windows-x64.exe`와 `SHA256SUMS.txt`를 받을 수 있습니다. 첫 공개 버전은 **v0.1.0**입니다. GitHub 로그인 없이 다운로드할 수 있습니다.

[Windows 설치 파일 다운로드](https://github.com/sopo9880/RemoteLink-Releases/releases/latest/download/RemoteLink-Setup-Windows-x64.exe) · [SHA256 체크섬](https://github.com/sopo9880/RemoteLink-Releases/releases/latest/download/SHA256SUMS.txt)

## 설치와 연결

- Windows 10·11 x64를 지원합니다. 연결할 두 PC에 설치하세요.
- Agent에 운영자가 안내한 RemoteLink 제어 서버의 HTTPS 주소를 입력하세요.
- 접속 대상 PC에서만 RDP/SSH 공유를 허용하세요. 해당 서비스는 별도로 활성화되어 있어야 합니다.
- Discord `/remote pair`로 등록하고 Agent에서 계정과 기기 키 확인값을 확인하세요.
- `/remote devices`와 `/remote connect`로 연결하고 `/remote status`의 로컬 주소로 접속하세요.

설치 파일에는 운영자의 봇 토큰이나 제어 서버 비밀키를 포함하지 않습니다. 초기 버전은 코드 서명되지 않아 Windows 실행 경고가 표시될 수 있습니다. Windows Home은 기본 RDP 호스트를 지원하지 않습니다.
