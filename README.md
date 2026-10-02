# RemoteLink · Windows Agent

Windows PC에서 RDP·SSH와 허용한 TCP 서비스를 연결하는 RemoteLink Agent의 공개 배포 저장소입니다. 설치 파일, SHA256 체크섬과 사용 안내만 게시하며 개발 소스는 비공개 저장소에서 관리합니다.

## 다운로드

현재 공개 버전은 **v0.3.0**입니다. GitHub 로그인 없이 다운로드할 수 있습니다.

[Windows 설치 파일 다운로드](https://github.com/sopo9880/RemoteLink-Releases/releases/latest/download/RemoteLink-Setup-Windows-x64.exe) · [SHA256 체크섬](https://github.com/sopo9880/RemoteLink-Releases/releases/latest/download/SHA256SUMS.txt) · [버전 목록](https://github.com/sopo9880/RemoteLink-Releases/releases)

## v0.3.0 변경

Agent에 기본 제어 서버 주소가 들어 있습니다: `https://rural-cheslie-veryverysecrtet-a468507a.koyeb.app`. 기존 빈 주소 설정도 아직 등록하지 않은 경우 기본값으로 채웁니다. 서버 주소를 비우더라도 기기 이름·세션 시간·공유 서비스를 오프라인에서 저장할 수 있습니다.

제어 서버는 기존 Koyeb 봇 웹 주소에서 제공하고 기존 MongoDB에 기기·그룹을 보관합니다. 브라우저 등록은 서버의 기존 Discord OAuth 콜백 설정을 재사용합니다.

## 설치와 연결

- Windows 10·11 x64를 지원합니다. 연결할 두 PC에 설치하세요. 기존 설치 위에 설치하면 업데이트로 진행하고, 같은 버전을 다시 설치하면 복구로 진행합니다. 실행 중인 Agent는 종료되며 설정과 기기 키는 유지합니다. 설치 후 원격 연결을 다시 요청하세요.
- 설정에서 운영자가 안내한 제어 서버의 HTTPS 주소와 기기 이름을 입력하세요.
- 세션 기본 시간은 **1시간**입니다. 계속 연결하려면 **설정 → 세션 기본 시간 → 무제한**으로 변경하세요. 변경은 새 세션부터 적용됩니다.
- 접속 대상 PC에서만 RDP/SSH 또는 사용자 지정 TCP 공유를 허용하세요. 해당 서비스는 별도로 활성화되어 있어야 합니다.
- 서버 연결 후 **Discord로 등록**을 눌러 브라우저에서 계정을 인증하세요. 서버에 OAuth 설정이 필요합니다. 이미 등록된 Agent에서 새 PC의 등록 코드를 입력하거나 Discord `/remote pair`로 등록할 수도 있습니다.
- Agent에서 계정과 기기 키 확인값을 확인하고 승인하세요. 기기 탭에서 상대와 서비스를 선택해 연결합니다. 처음 연결하는 상대 키도 양쪽에서 확인합니다.
- 세션 탭에서 주소를 복사하거나 RDP/SSH를 열고 연결을 종료할 수 있습니다. 그룹 탭에서 그룹을 만들고 기기 관리에서 이름·그룹 변경과 등록 해제가 가능합니다.
- Discord `/remote` 명령도 계속 지원합니다.

설치 파일에는 봇 토큰이나 제어 서버 비밀키를 포함하지 않습니다. 설치 파일은 코드 서명되지 않아 Windows 실행 경고가 표시될 수 있습니다. Windows Home은 기본 RDP 호스트를 지원하지 않습니다.

기본 제어 서버는 기존 Koyeb 봇과 함께 운영됩니다. [서버 상태](https://rural-cheslie-veryverysecrtet-a468507a.koyeb.app/remote/health)에서 준비 상태를 확인할 수 있습니다. 다른 서버를 운영하려면 해당 서버를 별도로 준비해야 합니다. 무제한은 앱의 만료 제한을 없애며 네트워크 단절·Agent 종료·제어 서버 재시작 시 연결은 종료됩니다.
