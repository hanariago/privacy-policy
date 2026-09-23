# TestPin for Mac — 앱 위치 테스트용 컴패니언

TestPin iPhone 앱은 **Safari 웹페이지**가 읽는 위치만 바꿉니다. 회사 앱 같은 **네이티브 앱**까지 같은 좌표에서 테스트하려면 Mac이 필요합니다. TestPin for Mac은 케이블로 연결된 iPhone의 시스템 위치를 시뮬레이션합니다 — Xcode의 "위치 시뮬레이션"과 같은 개발자 기능을 쓰는 것이라 Xcode 없이도, 코드 없이도 됩니다.

## 필요한 것
- Mac (macOS 14 Sonoma 이상)
- iPhone (iOS 17 이상) + 케이블
- iPhone의 **개발자 모드** 켜기: 설정 → 개인정보 보호 및 보안 → 개발자 모드 → 켬 → 재시동 후 확인
- 무료. 계정·서버·데이터 수집 없음

## 다운로드
- 최신 버전: GitHub Releases의 `TestPinMac-x.y.z.dmg` (링크는 출시 후 갱신)
- Mac App Store에는 없습니다. 기기 연결에 필요한 접근이 App Store 샌드박스에서 막히기 때문에 공증(notarized)된 DMG로 배포합니다. 처음 열 때 "확인되지 않은 개발자" 경고가 뜨면 공증이 안 된 빌드이니 사용하지 마세요.

## 사용 순서
1. iPhone을 케이블로 연결하고, 폰에 뜨는 "이 컴퓨터를 신뢰하시겠습니까?"에서 **신뢰**를 누릅니다.
2. TestPin for Mac을 열고 왼쪽 기기 목록에서 iPhone을 선택합니다. (안 보이면 새로고침 ↻)
3. 핀을 고르고 **이 기기에 적용**을 누릅니다. iOS 17 이상은 앱이 자동으로 개발자 서비스 터널을 엽니다 — 관리자 암호는 필요 없습니다.
4. iPhone에서 지도 앱이나 테스트할 앱을 열어 위치를 확인합니다.
5. 끝나면 **실제 위치로 복귀**. 앱을 종료하거나 케이블을 뽑아도 실제 위치로 돌아갑니다.

핀은 iPhone TestPin 앱의 "좌표 세트 공유" 링크를 붙여넣어 그대로 가져올 수 있습니다 (툴바의 링크 아이콘).

## 이 앱이 바꾸는 것 / 바꾸지 않는 것
- 바뀜: 연결된 iPhone의 시스템 위치 → **모든 앱**이 그 좌표를 봅니다 (연결 중에만)
- 안 바뀜: **IP 주소 기반 위치**. 통신사·Wi-Fi로 위치를 추정하는 서비스는 그대로입니다
- 안 바뀜: 다른 기기, Mac 자신의 위치

## 문제 해결
| 증상 | 확인할 것 |
|---|---|
| 기기 목록이 비어 있음 | 케이블 연결(Wi-Fi 아님) · 폰 잠금 해제 · "신뢰" 눌렀는지 · 다른 Mac 도구(Xcode 등)가 기기를 점유 중인지 |
| "터널 실패" | 개발자 모드가 켜져 있는지 · 폰을 다시 꽂기 · 로그(툴바 터미널 아이콘)의 마지막 오류 |
| 적용을 눌렀는데 위치가 그대로 | 테스트 앱을 완전히 종료 후 다시 열기 · 지도 앱으로 먼저 확인 |
| iOS 17.0–17.3 | 유저스페이스 터널이 지원되지 않는 조합이 있어 Xcode의 위치 시뮬레이션을 대신 사용하세요 |

## 개인정보
TestPin for Mac은 어떤 데이터도 수집·전송하지 않습니다. 핀은 Mac의 `~/Library/Application Support/TestPin/`에만 저장됩니다. 기기 통신은 로컬(USB)에서만 일어납니다. 위치 시뮬레이션 엔진으로 오픈소스 [go-ios](https://github.com/danielpaulus/go-ios)(MIT)를 내장합니다.

→ [개인정보처리방침](../) · [지원](../support/) · [Safari 적용 확인 페이지](../check/)

---

## TestPin for Mac (English)

The TestPin iPhone app changes only what **Safari web pages** read. To test **native apps** at the same coordinate you need a Mac: TestPin for Mac simulates the system location of an iPhone connected by cable, using the same developer facility as Xcode's location simulation — no Xcode, no code.

**Requirements**: macOS 14+, iPhone on iOS 17+ with **Developer Mode** enabled (Settings → Privacy & Security → Developer Mode), a cable. Free; no account, no server, no data collection.

**Steps**: connect by cable and tap **Trust** on the iPhone → pick the device in the sidebar → pick a pin → **Apply to this device** → verify in Maps or the app under test → **Return to real location** when done (disconnecting or quitting also restores it).

**Not changed**: IP-based location; other devices; the Mac's own location.

Distributed as a notarized DMG on GitHub Releases (not on the Mac App Store, whose sandbox blocks device access). Built on the open-source [go-ios](https://github.com/danielpaulus/go-ios) (MIT).
