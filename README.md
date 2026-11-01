# 세팔론아라 (Cephalon Ara) — 릴리스

워프레임(Warframe)용 **비공식 팬 제작 도구** 세팔론아라의 배포 파일을 올리는 저장소입니다. **소스 코드는 이 저장소에 없습니다.**
앱의 자동 업데이트가 이 저장소의 [Releases](../../releases)에서 새 버전 정보(`latest.json`)와 압축 파일을 받아 갑니다.

소개와 안내: https://cephalonara.xyz · 문의: [디스코드](https://discord.gg/PRsfnpFSdP)

- Warframe 및 관련 이름·게임 문구·이미지는 Digital Extremes Ltd.의 자산이며, 이 프로그램은 Digital Extremes와 제휴·승인 관계가 없습니다. 게임 이용에 따른 책임은 사용자에게 있습니다.
- 라이선스: All rights reserved(개인·비상업 사용 허락) — 압축 파일 안 `Licenses\LICENSE.txt`. 서드파티 라이선스 고지는 `Licenses\THIRD-PARTY-NOTICES.md`.

## 설치

1. [.NET 8 Desktop Runtime(x64)](https://dotnet.microsoft.com/download/dotnet/8.0)을 설치합니다(이미 있으면 건너뜀).
2. Releases에서 최신 `CephalonAra-*-win-x64.zip`을 받아 원하는 폴더(쓰기 가능한 곳, 예: 문서 폴더 아래)에 풉니다.
3. `Cephalonara.App.exe`를 실행합니다. "Windows의 PC 보호" 창이 뜨면 **추가 정보 → 실행**을 누릅니다. 코드 서명 인증서가 없어서 나오는 안내입니다.
4. 게임 화면 모드는 **테두리 없는 창**을 권장합니다. 독점 전체 화면에서는 결과 창이 보이지 않을 수 있습니다.

새 버전은 자동으로 받아 두었다가 다음 실행 때 적용합니다(설정 탭에서 끌 수 있음).

스캔에 필요한 Visual C++ 런타임은 압축 파일에 들어 있어 따로 설치하지 않아도 됩니다. Windows N·KN 에디션은 [미디어 기능 팩](https://support.microsoft.com/ko-kr/topic/media-feature-pack-list-for-windows-n-editions-c1c6fffa-d052-8338-7a79-a4bb980a700a)이 필요합니다.

## 프로그램이 하는 일과 개인정보

- **게임**: 게임 창 화면 캡처, `EE.log`·`EE.cfg` 읽기, 게임이 내보내는 디버그 출력 듣기만 합니다. 게임 메모리·입력·패킷에는 접근하지 않습니다. 디버그 출력 듣기는 설정 탭에서 끌 수 있습니다.
- **내 PC**: 게임 창을 찾으려고 실행 중인 프로그램의 이름과 창 제목을 확인합니다. 저장하거나 보내지 않습니다. 설정과 기록은 `%LOCALAPPDATA%\CephalonAra`에만 저장합니다.
- **warframe.market 로그인(선택)**: 이메일과 비밀번호는 warframe.market으로만 보내고 저장하지 않습니다. 받은 토큰은 Windows 암호화(DPAPI)로 이 PC에만 저장합니다.
- **접속하는 곳**: 세팔론 아라 서버(월드 정보·시세·데이터), warframe.market(시세·주문), Digital Extremes 공개 이미지, GitHub(업데이트·모드 그림). 서버는 Cloudflare를 거치며, 요청 제한과 접속자 수 집계에 IP를 메모리에서만 쓰고 저장하지 않습니다. 서버가 응답하지 않으면 예전 서버(cephalonara.xyz)로 대신 접속합니다. 사이트와 예전 서버는 접속 기록(IP·시각·브라우저 정보)을 서버 로그에 남깁니다.

---

# Cephalon Ara — releases

Release files for **Cephalon Ara**, an unofficial fan-made companion tool for Warframe. **No source code is hosted here.** The app's auto-updater downloads signed update manifests (`latest.json`) and packages from this repository's Releases.
Not affiliated with or endorsed by Digital Extremes Ltd. Warframe and related names, in-game text and images are property of Digital Extremes. All rights reserved (personal, non-commercial use permitted); see `Licenses\` inside the package.

The app only captures the game window, reads `EE.log`/`EE.cfg` and listens to the game's debug output. It does not touch game memory, input or network traffic.
