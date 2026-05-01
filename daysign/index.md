# daysign-privacy-policy

## 개인정보처리방침 (Korean)

### Daysign 개인정보처리방침

본 방침은 Daysign 앱(이하 "앱")의 개인정보 수집 및 이용에 관한 사항을 안내합니다.

1. **수집하는 정보**
   앱은 사용자의 개인정보를 외부 서버로 수집하거나 전송하지 않습니다. 앱에서 입력한 모든 데이터(디데이 제목, 날짜, 메모, 이모지, 사진)는 사용자의 iPhone에만 저장됩니다.

2. **iCloud 동기화 (CloudKit)**
   사용자의 Apple ID로 로그인된 경우, 앱은 SwiftData + CloudKit을 통해 사용자 본인의 iCloud 비공개 데이터베이스에 디데이 데이터를 자동 동기화합니다. 이 데이터는 Apple의 iCloud 인프라에만 저장되며 개발자를 포함한 제3자는 접근할 수 없습니다. iCloud 동기화는 iPhone 설정 → [사용자 이름] → iCloud → iCloud 사용 앱에서 비활성화할 수 있습니다.

3. **사진 및 카메라**
   앱은 사용자의 허가 하에 디데이에 사진을 첨부하기 위해 사진 라이브러리 및 카메라에 접근합니다. 선택한 사진은 앱 내부와 사용자의 iCloud(동기화 활성 시)에만 저장되며 외부 서버로 전송되지 않습니다. 권한은 언제든지 iPhone 설정 → 개인정보 보호 및 보안 → 사진 / 카메라에서 해제할 수 있습니다.

4. **알림**
   사용자의 허가 하에 디데이 임박 시 로컬 알림을 발송합니다. 알림은 기기 내에서만 생성되며 외부 서버를 거치지 않습니다.

5. **Apple Watch 연동**
   앱은 WatchConnectivity 프레임워크를 통해 페어링된 Apple Watch와 디데이 데이터를 동기화합니다. 이 통신은 iPhone과 Watch 간 직접 이루어지며 외부 서버로 전송되지 않습니다.

6. **위젯 및 App Group**
   앱은 홈 화면 위젯, 잠금 화면 위젯, StandBy 위젯, Apple Watch 컴플리케이션에 디데이 정보를 표시합니다. 이를 위해 App Group(`group.com.hanariago.daysign`) 공유 컨테이너에 데이터를 캐싱하며, 이 데이터는 사용자의 기기 내에서만 접근됩니다.

7. **데이터 보안**
   모든 데이터는 기기 내 SwiftData, UserDefaults, App Group 컨테이너에 저장되며, iCloud 동기화 시 Apple의 암호화된 인프라를 통해 전송됩니다. 외부 서버로의 전송, 제3자 공유, 광고 목적 사용은 일절 없습니다.

8. **문의**
   개인정보 관련 문의는 앱 스토어 지원 페이지를 이용해 주세요.

시행일: 2026년 5월 1일

---

## Privacy Policy (English)

### Privacy Policy for Daysign

This policy describes how the Daysign app handles your information.

1. **Data Collection**
   Daysign does not collect, transmit, or store any personal information on external servers. All data you enter (D-day titles, dates, notes, emojis, photos) is stored exclusively on your iPhone.

2. **iCloud Sync (CloudKit)**
   When you are signed in to your Apple ID, Daysign automatically syncs your D-day data to your own iCloud private database via SwiftData and CloudKit. This data is stored only within Apple's iCloud infrastructure and is inaccessible to the developer or any third party. You can disable iCloud sync at any time via iPhone Settings → [Your Name] → iCloud → Apps Using iCloud.

3. **Photos & Camera**
   With your permission, Daysign accesses your photo library and camera so you can attach photos to a D-day. Selected photos are stored only on your device and in your iCloud (when sync is enabled), and are never transmitted to external servers. You can revoke these permissions at any time via iPhone Settings → Privacy & Security → Photos / Camera.

4. **Notifications**
   With your permission, Daysign sends local notifications as a D-day approaches. These notifications are generated entirely on-device and do not involve any external servers.

5. **Apple Watch Integration**
   Daysign syncs D-day data with a paired Apple Watch via the WatchConnectivity framework. This communication happens directly between your iPhone and Watch and is not transmitted to any external servers.

6. **Widgets & App Group**
   Daysign displays D-day information in Home Screen widgets, Lock Screen widgets, StandBy widgets, and Apple Watch complications. To support this, data is cached in a shared App Group container (`group.com.hanariago.daysign`), which is only accessible on your device.

7. **Data Security**
   All data is stored locally using SwiftData, UserDefaults, and an App Group container. When iCloud sync is enabled, data is transmitted through Apple's encrypted infrastructure. We do not share your data with third parties, use it for advertising, or transmit it anywhere outside your device or iCloud.

8. **Contact**
   For privacy-related questions, please use the support link on the App Store page.

Effective Date: May 1, 2026
