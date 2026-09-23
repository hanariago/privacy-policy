# testpin-privacy-policy

## 개인정보처리방침 (Korean)

### TestPin (테스트핀) 개인정보처리방침

본 방침은 TestPin 앱 및 TestPin Safari 확장 프로그램(이하 "앱")의 개인정보 수집 및 이용에 관한 사항을 안내합니다.

TestPin은 웹 개발자·QA 담당자가 자신의 웹 서비스가 특정 좌표에서 어떻게 동작하는지 iPhone Safari에서 확인하기 위한 테스트 도구입니다.

#### 1. 수집하는 정보

앱은 **사용자의 개인정보를 일절 수집하지 않으며, 외부로 전송하지 않습니다.**

- 계정·로그인 기능이 없습니다.
- 앱 개발사가 운영하는 서버가 없습니다.
- 사용자 식별자, 기기 식별자, 사용 기록, 방문한 웹사이트 주소를 수집하거나 저장하지 않습니다.
- 앱은 **기기의 위치 권한을 요청하지 않으며**, 기기의 실제 위치를 읽지 않습니다.

#### 2. Safari 확장이 하는 일과 하지 않는 일

**하는 일**

- Safari에서 열린 웹페이지가 브라우저 위치 정보 API(`getCurrentPosition`, `watchPosition`, Permissions API 상태)로 읽는 위치를, 사용자가 앱에서 선택한 좌표("핀")로 대체합니다.
- 페이지 스크립트가 실행되기 전에 설치되므로, 적용 중에는 실제 위치가 해당 페이지로 전달되지 않습니다.

**하지 않는 일**

- 기기·시스템의 GPS 위치를 변경하지 않습니다.
- Safari 외의 다른 앱에 영향을 주지 않습니다.
- **IP 기반 위치는 바뀌지 않습니다.** 앱은 IP 주소를 변경하지 않으며, VPN·프록시 기능을 제공하지 않습니다.
- 사용자가 방문한 웹페이지의 내용을 읽거나 수집·전송하지 않습니다.

#### 3. 기기 내 저장

사용자가 만든 핀(이름, 위도, 경도, 정확도), 즐겨찾기, 적용 범위 설정(모든 사이트 / 지정 도메인 목록), 켜짐·꺼짐 상태는 **기기 내 App Group 컨테이너(UserDefaults)에만 저장**됩니다. 이 저장소는 TestPin 앱과 TestPin Safari 확장 프로그램이 공유하며, 외부로 전송되지 않습니다.

#### 4. 지도 검색 기능

주소·장소 이름으로 좌표를 찾는 검색 기능을 사용하면, **입력한 검색어가 Apple 지도 서비스로 전송**됩니다. 이는 Apple이 제공하는 서비스이며, 해당 처리는 Apple의 개인정보처리방침을 따릅니다. TestPin은 검색어를 저장하거나 기록하지 않으며, 앱 개발사의 서버로 전송하지 않습니다.

검색 기능을 사용하지 않고 좌표를 직접 입력하거나 지도에서 탭하여 핀을 만들면, 외부로 전송되는 데이터가 없습니다.

#### 5. 핀 세트 공유 링크

핀 세트를 링크 또는 QR 코드로 공유하면, 사용자가 선택한 핀 데이터가 **링크 주소의 프래그먼트(`#` 뒷부분)에 담깁니다.** URL 프래그먼트는 웹 표준상 서버로 전송되지 않으므로, 공유한 핀 데이터가 앱 개발사나 제3자의 서버에 저장되지 않습니다.

다만 링크 자체에는 사용자가 공유하기로 선택한 핀 정보(이름·좌표)가 들어 있으므로, 링크를 받은 사람은 그 내용을 볼 수 있습니다. 공유 대상은 사용자가 직접 선택해 주세요. 공유 링크에는 계정 정보, 기기 정보, 실제 위치가 포함되지 않습니다.

#### 6. 제3자 공유

앱 개발사는 사용자 데이터를 수집하지 않으므로, 제3자와 공유할 데이터가 없습니다.

#### 7. 광고 및 분석

앱은 광고 SDK, 분석 SDK, 추적 코드를 일절 포함하지 않습니다. 앱 내 구매(IAP)도 없습니다.

#### 8. 데이터 보안

모든 데이터는 기기 내에만 저장되며, iOS의 앱 샌드박스와 App Group 접근 제어로 보호됩니다. 앱을 삭제하면 저장된 핀과 설정도 함께 삭제됩니다.

#### 9. 아동의 개인정보

앱은 어떤 사용자로부터도 개인정보를 수집하지 않으며, 아동으로부터 개인정보를 수집하지 않습니다. 연령 등급은 4+입니다.

#### 10. 방침 변경

본 방침이 변경되는 경우, 이 페이지를 통해 변경 내용과 최종 수정일을 공지합니다.

#### 11. 문의

개인정보 관련 문의는 App Store 페이지의 지원 링크 또는 GitHub 이슈를 이용해 주세요.

최종 수정일: 2026년 9월 22일

---

## Privacy Policy (English)

### Privacy Policy for TestPin (테스트핀)

This policy describes how the TestPin app and the TestPin Safari extension (the "app") handle your information.

TestPin is a testing tool for web developers and QA testers who need to check how their web service behaves at specific coordinates in Safari on iPhone.

#### 1. Data Collection

The app **collects no personal information and transmits nothing externally.**

- There are no accounts and no sign-in.
- The developer operates no servers.
- No user identifiers, device identifiers, usage logs, or browsing history are collected or stored.
- The app **does not request the device location permission** and never reads your actual location.

#### 2. What the Safari Extension Does and Does Not Do

**What it does**

- It replaces the location that web pages open in Safari read through the browser Geolocation API (`getCurrentPosition`, `watchPosition`, Permissions API state) with a coordinate (a "pin") you chose in the app.
- It is installed before page scripts run, so while it is active your real location is never handed to the page.

**What it does not do**

- It does not change the device or system GPS location.
- It does not affect apps other than Safari.
- **IP-based location is not changed.** The app does not change your IP address and provides no VPN or proxy functionality.
- It does not read, collect, or transmit the content of the pages you visit.

#### 3. On-Device Storage

The pins you create (name, latitude, longitude, accuracy), your favorites, the scope setting (all sites / specified domains), and the on-off state are stored **only in an App Group container (UserDefaults) on your device.** This storage is shared between the TestPin app and the TestPin Safari extension and is never transmitted externally.

#### 4. Map Search

When you search for an address or place name to find a coordinate, **the search text you type is sent to Apple Maps.** That is a service provided by Apple and is governed by Apple's privacy policy. TestPin does not store or log your search queries and does not send them to any server operated by the developer.

If you do not use search — entering coordinates directly or tapping on the map instead — no data leaves your device.

#### 5. Pin Set Share Links

When you share a pin set as a link or QR code, the pin data you selected is encoded **in the fragment of the link (the part after `#`).** By web standard, URL fragments are not sent to servers, so shared pin data is never stored on a server run by the developer or by any third party.

The link itself does contain the pin information (names and coordinates) you chose to share, so anyone who receives the link can read it. Please choose your recipients accordingly. Share links contain no account information, no device information, and not your real location.

#### 6. Third-Party Sharing

The developer collects no user data, so there is no data to share with third parties.

#### 7. Advertising and Analytics

The app contains no advertising SDKs, analytics SDKs, or tracking code of any kind. There are no in-app purchases.

#### 8. Data Security

All data is stored on your device only and is protected by the iOS app sandbox and App Group access control. Deleting the app also deletes your stored pins and settings.

#### 9. Children's Privacy

The app collects no personal information from any user, including children. Its age rating is 4+.

#### 10. Changes to This Policy

If this policy changes, the change and the new last-updated date will be posted on this page.

#### 11. Contact

For privacy-related questions, please use the support link on the App Store page or open a GitHub issue.

Last Updated: September 22, 2026
