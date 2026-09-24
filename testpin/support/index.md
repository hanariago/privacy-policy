# testpin-support

## TestPin (테스트핀) 지원

TestPin은 **Safari 웹페이지가 읽는 위치만 바꾸는** 웹 개발·QA용 테스트 도구입니다. iPhone(iOS 17 이상) 전용, 무료, 광고 없음, 앱 내 구매 없음.

---

### 이 앱이 하는 일 / 하지 않는 일

**하는 일**

- Safari에서 연 웹페이지가 브라우저 위치 정보 API(`getCurrentPosition`, `watchPosition`, Permissions API)로 읽는 위치를, 앱에서 고른 좌표(핀)로 바꿉니다.
- 페이지 스크립트보다 먼저 설치되므로, 적용 중에는 실제 위치가 페이지로 전달되지 않습니다.

**하지 않는 일**

- **IP 기반 위치는 바뀌지 않습니다.** TestPin은 IP 주소를 바꾸지 않으며 VPN·프록시가 아닙니다. IP로 위치를 추정하는 사이트는 원래 위치를 그대로 보여줍니다.
- 기기·시스템의 GPS는 바뀌지 않습니다. 지도 앱, 날씨 앱 등 다른 앱의 위치는 그대로입니다.
- Safari 외의 앱(카카오맵·네이버지도 등 네이티브 앱)에는 영향을 주지 않습니다.
- 데이터를 수집하거나 외부로 전송하지 않습니다.

---

### 확장 프로그램 켜는 방법

1. Safari를 엽니다.
2. 주소창 왼쪽 **"aA"**(iOS 17) 또는 페이지 메뉴/확장 아이콘(iOS 18 이상)을 탭합니다.
3. **"확장 프로그램 관리"**를 탭합니다.
4. **TestPin**을 켭니다.
5. 웹사이트 접근을 **"허용"**합니다. (권장: 모든 웹사이트)

또는: **설정 앱 → 앱 → Safari → 확장 프로그램 → TestPin**

---

### 빠른 시작 3단계

1. **핀 만들기** — TestPin 앱에서 좌표를 직접 입력하거나, 지도를 탭하거나, 주소·장소 이름으로 검색해 핀을 추가합니다.
2. **확장 켜기** — 위 "확장 프로그램 켜는 방법"대로 Safari에서 TestPin을 켜고, 앱의 마스터 스위치를 켭니다.
3. **확인하기** — 앱의 **"적용 확인"** 버튼을 누르면 확인 페이지가 열립니다. 위치 정보 API가 반환하는 값이 선택한 핀 좌표와 같으면 정상입니다.

확인 페이지: <https://hanariago.github.io/privacy-policy/testpin/check/>

---

### 자주 묻는 질문

**Q. GPS가 안 바뀌어요.**
의도된 동작입니다. TestPin은 시스템 GPS를 바꾸지 않습니다. 바뀌는 것은 **Safari 웹페이지가 위치 정보 API로 읽는 값**뿐입니다. 지도 앱이나 설정의 위치 서비스는 그대로입니다.

**Q. IP 위치가 그대로예요.**
정상입니다. **IP 기반 위치는 바뀌지 않습니다.** TestPin은 IP 주소를 바꾸지 않습니다. 사이트가 위치 정보 API 대신 IP로 위치를 추정하면 원래 위치가 나옵니다. 사이트가 어느 방식을 쓰는지 확인하려면 확인 페이지를 참고하세요.

**Q. 어떤 사이트에서는 안 돼요.**
다음 경우에는 적용되지 않습니다.
- 사이트의 CSP(Content Security Policy) 설정 때문에 확장 스크립트가 제한되는 경우
- Safari가 아니라 **다른 앱 안의 내장 브라우저(WKWebView)** 에서 연 페이지 — 인스타그램·카카오톡 등 앱 내 브라우저는 대상이 아닙니다.
- 적용 범위를 "지정 도메인만"으로 두고 해당 도메인을 목록에 넣지 않은 경우 (이때는 실제 위치가 그대로 전달됩니다)
- 사이트가 위치 정보 API가 아닌 IP·기지국 등 다른 방식으로 위치를 추정하는 경우

**Q. 카카오맵·네이버지도 앱에서도 되나요?**
아니요. 네이티브 앱은 대상이 아닙니다. TestPin은 **Safari에서 연 웹페이지**에만 적용됩니다. 같은 서비스라도 Safari에서 웹 버전으로 열면 적용됩니다.

**Q. 적용됐는지 어떻게 확인하나요?**
두 가지 방법이 있습니다.
- Safari ⋯(또는 aA) 메뉴의 TestPin 팝업을 열면 **지금 페이지에 전달되는 좌표**와 이 사이트가 적용 범위에 들어 있는지 표시됩니다.
- 앱의 "적용 확인" 버튼으로 확인 페이지를 열면, 위치 정보 API가 실제로 반환하는 값을 눈으로 볼 수 있습니다.

**Q. 새로고침해도 유지되나요?**
네. 켜져 있는 동안에는 새로고침·페이지 이동 후에도 계속 적용됩니다. 팝업에서 핀을 바꾸면 이미 열린 페이지의 `watchPosition` 콜백에도 즉시 반영됩니다. 다만 페이지가 처음 로드될 때의 동작을 다시 보려면 새로고침하세요.

**Q. 팀원에게 좌표 세트를 공유하려면?**
앱에서 핀 세트를 **링크 또는 QR 코드**로 공유하세요. 받은 사람이 링크를 열면 안내 페이지가 뜨고, **"TestPin에서 열기"** 를 누르면 앱이 미리보기와 함께 핀을 가져옵니다. 서버를 거치지 않습니다.

**Q. 공유 링크에 내 정보가 들어가나요?**
아니요. 링크에는 **사용자가 공유하기로 고른 핀 정보(이름·좌표)만** 들어가며, 그것도 주소의 프래그먼트(`#` 뒷부분)에 담깁니다. 프래그먼트는 서버로 전송되지 않습니다. 계정·기기 정보·실제 위치는 포함되지 않습니다.

**Q. 앱을 삭제하면 데이터는요?**
앱과 함께 삭제됩니다. 핀과 설정은 기기 내 App Group 컨테이너에만 저장되며, 외부 백업 서버가 없습니다. 중요한 핀 세트는 삭제 전에 링크로 공유해 두세요.

**Q. Mac Safari도 지원하나요?**
v0.1은 **iPhone 전용**입니다. iPad·Mac은 지원하지 않습니다.

---

### 문제 해결

**확장 프로그램 목록에 TestPin이 안 보입니다.**
1. TestPin 앱을 한 번 실행합니다. (설치 후 한 번도 실행하지 않으면 확장이 등록되지 않을 수 있습니다.)
2. Safari를 완전히 종료한 뒤 다시 엽니다. (앱 전환기에서 위로 밀어 종료)
3. 그래도 안 보이면 **설정 앱 → 앱 → Safari → 확장 프로그램**에서 확인합니다.
4. 기기를 재시작합니다.

**팝업에 "TestPin 앱과 연결할 수 없습니다"가 뜹니다.**
앱을 한 번 실행한 뒤 다시 시도하세요.

**켰는데 좌표가 안 바뀝니다.**
- 앱의 마스터 스위치가 켜져 있는지 확인합니다.
- 적용 범위가 "지정 도메인만"이면 해당 도메인이 목록에 있는지 확인합니다.
- Safari 확장 설정에서 웹사이트 접근이 "허용"인지 확인합니다. ("하루 동안 허용"으로 되어 있으면 만료됐을 수 있습니다.)
- 페이지를 새로고침합니다.
- 앱 내 브라우저가 아니라 Safari에서 연 페이지인지 확인합니다.

**핀이 하나도 없다고 나옵니다.**
앱에서 핀을 하나 이상 추가하고 즐겨찾기에서 선택하세요.

---

### 문의

- App Store 페이지의 지원 링크
- GitHub 이슈

---

## Support (English)

**What TestPin does:** it replaces the location that web pages in Safari read through the browser Geolocation API (`getCurrentPosition`, `watchPosition`, Permissions API state) with a coordinate (a "pin") you choose in the app. It is installed before page scripts run.

**What it does not do:** it does not change the device or system GPS, does not affect other apps, and **IP-based location is not changed** — TestPin is not a VPN or proxy. It collects and transmits no data.

**Enable the extension:** Open Safari → tap **"aA"** to the left of the address bar (iOS 17) or the page menu / extensions icon (iOS 18+) → **Manage Extensions** → turn on **TestPin** → set website access to **Allow** (recommended: All Websites). Alternative path: Settings app → Apps → Safari → Extensions → TestPin.

**Quick start:** (1) Create a pin in the app by typing coordinates, tapping the map, or searching an address or place name. (2) Enable the extension and turn on the master switch. (3) Tap **Check** in the app to open the check page and confirm the Geolocation API returns your pin.

Check page: <https://hanariago.github.io/privacy-policy/testpin/check/>

**Common questions**

- *System GPS unchanged?* Expected. Only Safari web pages are affected.
- *IP location unchanged?* Expected. TestPin does not change your IP address. Sites that infer location from IP will still show your real region.
- *Some sites do not work?* A site's CSP may restrict extension scripts; in-app browsers (WKWebView) inside other apps are out of scope; and if scope is set to a domain list, domains not on the list receive your real location.
- *Native map apps?* Not supported. Safari web pages only.
- *Does it survive reload?* Yes. Switching pins in the toolbar popup also updates live `watchPosition` callbacks.
- *Sharing with teammates?* Share a pin set as a link or QR code. The pin data lives in the URL fragment (`#…`), so nothing is sent to any server.
- *Deleting the app?* Pins and settings are stored only in an on-device App Group container and are removed with the app.
- *Mac Safari?* v0.1 is iPhone only (iOS 17+).

**Troubleshooting:** If TestPin is missing from the extension list, launch the TestPin app once, fully quit and reopen Safari, then check Settings → Apps → Safari → Extensions. If the popup says it cannot reach the app, launch the app once and retry.

**Contact:** use the support link on the App Store page, or open a GitHub issue.

Last Updated: September 22, 2026
