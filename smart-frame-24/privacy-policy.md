# Privacy Policy for Smart Frame 24

**Effective Date:** May 29, 2026
**Last Updated:** May 29, 2026

This document is published in two languages.

- **English** is the primary language and the controlling version for any legal interpretation. See sections 1 - 16 below.
- **한국어** translation is provided for the convenience of Korean users. See section 17 onwards.

---

## 1. Introduction

Smart Frame 24 ("the App", "we", "our", or "us") is a digital photo frame application for Android, developed and operated by the publisher listed in section 16 below. This Privacy Policy explains what data the App accesses, how that data is processed, and the choices you have.

We designed Smart Frame 24 to do as little with your data as possible. The App does not run any backend server, does not include any analytics or advertising SDK, and does not transmit personal information to us or to any third party for marketing purposes.

## 2. Summary at a Glance

| Topic | Our position |
| --- | --- |
| Do we run a server that stores your data? | **No.** All processing happens on your device. |
| Do we sell or share your data? | **No.** Never. |
| Do we include analytics, crash reporting, or advertising SDKs? | **No.** Zero third-party trackers. |
| Do we use Google APIs? | **Yes**, only with your explicit consent and only with read-only scopes. |
| Do we collect your location? | **Only while the App is open**, and only to fetch local weather. |
| Do we charge anything? | **One-time purchase**, USD 9.99 (or local equivalent), processed by Google Play. |

## 3. Information the App Accesses

We group the data the App can access into four categories. None of this data is sent to a server we control.

### 3.1 Information you choose to provide

- **Photos and videos** that you select from your device gallery to display in the slideshow. They are read by the operating system and rendered on screen. They never leave your device.
- **Custom alarm sounds** (MP3 files) you optionally pick to play when an alarm fires. The picked file is copied into the App's private document directory so the alarm can keep playing even after the original file is moved. It is never uploaded.
- **Settings you toggle** (slideshow interval, language, alarm times and labels, brightness preferences, etc.). These are persisted on the device using Android's `AsyncStorage`.

### 3.2 Information accessed through Google APIs (only with your explicit sign-in)

If you choose to sign in with Google in the App's Settings screen, the App requests the following read-only OAuth scopes:

- **`calendar.readonly`** — to read your primary Google Calendar so today's events can appear in the top-left card and on the Calendar screen. The App never creates, modifies, or deletes events.
- **`drive.readonly`** — to read images inside a folder named `Photo` on your Google Drive (Premium feature). The App never creates, modifies, or deletes Drive files.
- **`userinfo.profile`** and **`userinfo.email`** — to display your Google display name, email, and profile photo on the Settings screen so you can confirm which account is signed in.

The data returned by these APIs is **kept only in device memory and a small device-side cache** for the duration of your usage. It is not transmitted to any server controlled by us.

You can revoke the App's access at any time at <https://myaccount.google.com/permissions>. Revoking access immediately stops the App from receiving any further data from Google.

### 3.3 Information used for local features

- **Approximate or precise location**, requested only **while the App is in the foreground** and only when you keep the Weather widget enabled. It is sent **directly to Open-Meteo** (`api.open-meteo.com`, `air-quality-api.open-meteo.com`) over HTTPS so the App can fetch the current temperature, weather code, and PM10 air quality. The App does not collect your location while it is in the background and does not store any location history.
- **Audio playback and vibration**, used to play the configured alarm sound and provide a tactile fallback when an alarm fires.

### 3.4 Information the App does NOT collect

The following items are **never** collected by us:

- No analytics SDK (Firebase Analytics, Google Analytics, Amplitude, etc.)
- No crash-reporting SDK (Crashlytics, Sentry, Bugsnag, etc.)
- No advertising identifier (no `AAID`, no `IDFA`, no ad networks)
- No microphone, camera, contacts, SMS, call log, or biometric data
- No background location, no precise location history
- No personal information beyond what you actively grant via Google sign-in or device permissions

## 4. How We Use the Information

The information described in section 3 is used solely for the following purposes:

1. To display the photos, videos, calendar events, weather, and alarms you have configured.
2. To authenticate your Google sign-in for Calendar and Drive read-only access.
3. To process your one-time in-app purchase and to verify the receipt with Google Play.
4. To remember your preferences across app launches.

The App does not perform any profiling, ad targeting, or automated decision-making about you.

## 5. Google API Services User Data Policy ("Limited Use")

Smart Frame 24's use and transfer to any other app of information received from Google APIs will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the **Limited Use** requirements.

In plain language, this means:

- We use data from Google Calendar and Google Drive only to provide the user-facing features described in this policy.
- We do not transfer the data to others, except as necessary to provide or improve user-facing features that are prominent in the App and are in compliance with the Limited Use requirements.
- We do not use the data for serving advertisements.
- We do not allow humans to read the data, except (a) with your explicit consent for specific messages, (b) for security purposes, (c) to comply with applicable law, or (d) where the data has been aggregated and is used for internal operations in compliance with the Limited Use requirements.

## 6. In-App Purchases

Smart Frame 24 offers a single one-time purchase named **"Smart Frame 24 Premium"** at a suggested price of **USD 9.99** (or the local-currency equivalent set by Google Play in your region). Once unlocked, the entitlement is permanent for the Google account that completed the purchase and can be restored at any time from the Settings screen.

- All payment processing is performed entirely by **Google Play Billing**. We never see, store, or transmit your credit card number, billing address, or other payment credentials.
- The App uses **RevenueCat** (a purchase-orchestration SDK) to validate and synchronize the purchase entitlement. RevenueCat receives an anonymous user identifier generated on your device and the purchase receipt issued by Google Play. RevenueCat does not receive your name, email, or contact information from us. RevenueCat's privacy practices are described at <https://www.revenuecat.com/privacy>.
- Pricing, taxes, refund policy, and dispute handling are governed by Google Play's terms.

## 7. Permissions Used

Below is the list of Android permissions Smart Frame 24 may request and the exact reason for each one. The App requests every permission **only when it is needed** for the feature you are using.

| Permission | Purpose |
| --- | --- |
| `READ_MEDIA_IMAGES`, `READ_MEDIA_VIDEO` (Android 13+) / `READ_EXTERNAL_STORAGE` (older) | To display the photos and videos you pick from your device gallery in the slideshow. |
| `ACCESS_COARSE_LOCATION` / `ACCESS_FINE_LOCATION` | To fetch local weather and air quality. **Foreground only.** Background location is explicitly disabled. |
| `INTERNET`, `ACCESS_NETWORK_STATE` | To call Google APIs (Calendar, Drive), Open-Meteo (weather), RSS feeds (CNN, BBC, Yonhap), and Google Play Billing. |
| `VIBRATE` | To provide a tactile fallback when an alarm fires. |
| `WAKE_LOCK` (via `expo-keep-awake`) | To keep the screen on while the digital frame is running, only when you enable the keep-screen-on option. |
| `POST_NOTIFICATIONS` (Android 13+, optional) | Reserved for future scheduled-alarm reliability. The App currently does not post user-visible notifications. |

The App does **not** request the following sensitive permissions: contacts, SMS, call logs, microphone, camera, body sensors, accessibility services, device admin, or background location.

## 8. Data Storage and Security

- All user-controlled data (settings, picked photo URIs, alarm definitions, custom MP3 files, Drive cache, calendar cache) is stored **locally on your device** using Android's standard storage primitives (`AsyncStorage` for settings, the App's private document directory for files).
- **OAuth tokens** issued by Google are kept in the platform's encrypted secure storage (Android Keystore via `expo-secure-store`). They are never written to plaintext storage and never leave the device.
- Communication with third-party services (Google APIs, Open-Meteo, RSS sources, Google Play, RevenueCat) uses **HTTPS / TLS**. The single exception is the CNN Top Stories RSS feed, which CNN currently serves only over HTTP at `rss.cnn.com`; we use this feed solely to display public news headlines, and we do not transmit any user data to it.
- Because Smart Frame 24 does not run a backend server, there is no central database that could be breached on our side. Your data lives on your device and on the Google services you have chosen to connect.

## 9. Data Retention

We retain user-controlled data on your device until **you** decide to remove it. Specifically:

- Picked photos and videos are forgotten when you remove them in Settings or clear app data.
- Custom MP3 alarm sounds are deleted when you remove the corresponding alarm or clear app data.
- Google Drive and Calendar caches are purged when you sign out or clear app data.
- All persisted settings are erased when you uninstall the App or clear its app data in system Settings.

We do not retain any user data on servers we operate, because we do not operate any.

## 10. Your Rights and Choices

Regardless of where you live, you have the following practical controls:

- **Revoke Google access** at <https://myaccount.google.com/permissions>.
- **Disable location** for Smart Frame 24 in your device's system settings; the App will continue to work without weather.
- **Remove individual photos / alarms / MP3 files** in the App's Settings screen.
- **Uninstall the App** to delete every piece of data the App ever stored on your device.

If you reside in the European Economic Area, the United Kingdom, or California, you may additionally have the rights to access, correct, delete, port, and restrict processing of personal information about you. Because we do not operate a backend server and we do not store personal information ourselves, the easiest way to exercise these rights is to use the controls listed above and, where applicable, contact Google for data Google holds on your behalf. You can also contact us using the information in section 16.

## 11. Children's Privacy

Smart Frame 24 is a general-audience product. It is not directed to children under 13 (or under 14 / 15 / 16 depending on your local age threshold). We do not knowingly collect personal information from children. If you believe a child has provided personal information to the App, please contact us so we can help you remove it.

## 12. Third-Party Services

The App relies on the following third-party services. Each one is invoked only when you use a feature that needs it.

| Service | Purpose | Provider's privacy policy |
| --- | --- | --- |
| Google Sign-In, Google Calendar API, Google Drive API | Authentication and read-only data | <https://policies.google.com/privacy> |
| Google Play Billing | Process the in-app purchase | <https://policies.google.com/privacy> |
| RevenueCat | Validate and synchronize the in-app purchase entitlement | <https://www.revenuecat.com/privacy> |
| Open-Meteo | Current weather and air quality | <https://open-meteo.com/en/terms> |
| CNN, BBC, Yonhap News RSS feeds | Public news headlines (read-only, anonymous) | Provided by each respective publisher |

We are not responsible for the privacy practices of these third parties, and we encourage you to review their policies.

## 13. International Data Transfers

Because the App processes data on your device and on Google's services, the location of any data you generate is determined by Google's regional infrastructure and by your own device. We do not perform any additional cross-border transfer ourselves.

## 14. Changes to This Privacy Policy

We may update this Privacy Policy when the App's features change or when applicable law requires it. When we do, we will update the **Last Updated** date at the top of this document and, for material changes, post a notice in the App's Settings screen. Your continued use of the App after the change becomes effective constitutes acceptance of the updated policy.

## 15. Children Under Local Age Threshold and Parental Consent

If you are below the digital-consent age threshold in your jurisdiction (for example, 14 in South Korea, 16 in much of the European Union), please do not use Smart Frame 24 without the consent of a parent or legal guardian.

## 16. Contact Us

If you have any questions about this Privacy Policy, the App's data handling, or want to exercise the rights described in section 10, please contact us at:

- **Email:** smartframe24@example.com
- **Publisher:** Smart Frame 24 (publisher legal name to be inserted before public release)
- **Address:** (to be inserted before public release)

We aim to respond within 14 days.

---

## 17. 한국어 번역본 (Korean translation)

> 이 한국어 번역본은 한국 사용자의 편의를 위해 제공되며, 법적 해석상 차이가
> 발생하는 경우에는 위 영어 원문(섹션 1 ~ 16)이 우선합니다.

**시행일:** 2026년 5월 29일
**최종 업데이트:** 2026년 5월 29일

### 17.1 서문

Smart Frame 24(이하 "본 앱")는 안드로이드용 디지털 액자 애플리케이션이며,
아래 17.16 항에 명시된 발행자가 개발 · 운영합니다. 본 개인정보처리방침은 본
앱이 어떤 데이터를 어떻게 처리하는지, 그리고 사용자가 어떤 권리를 가지는지를
설명합니다.

본 앱은 데이터를 가능한 한 사용하지 않도록 설계되었습니다. 별도의 백엔드
서버를 운영하지 않으며, 분석 · 광고 SDK 도 일절 포함하지 않으며, 마케팅
목적으로 개인정보를 외부로 전송하지 않습니다.

### 17.2 핵심 요약

| 항목 | 입장 |
| --- | --- |
| 데이터를 저장하는 자체 서버를 운영하나요? | **아니요.** 모든 처리는 사용자의 기기 안에서 이루어집니다. |
| 데이터를 판매·공유하나요? | **아니요.** 어떤 경우에도 그렇지 않습니다. |
| 분석 · 충돌 보고 · 광고 SDK 가 포함되어 있나요? | **아니요.** 외부 트래커가 0 개입니다. |
| Google API 를 사용하나요? | **예.** 사용자의 명시적 동의를 받은 경우에만, 그리고 읽기 전용 권한만 사용합니다. |
| 위치 정보를 수집하나요? | **앱이 화면에 떠 있을 때만**, 그리고 현재 날씨를 가져오기 위해서만 사용합니다. |
| 결제가 있나요? | **1회성 정품 구매**, 9.99 USD (또는 지역 통화 환산액). Google Play 결제 시스템으로 처리됩니다. |

### 17.3 본 앱이 접근하는 정보

본 앱이 접근할 수 있는 정보는 네 가지로 나뉘며, 어느 항목도 우리가 통제하는
서버로 전송되지 않습니다.

#### 17.3.1 사용자가 직접 제공하는 정보

- 슬라이드쇼에 표시하기 위해 갤러리에서 직접 선택한 **사진 / 동영상**. 운영
  체제가 읽어와 화면에 표시할 뿐, 기기 밖으로 나가지 않습니다.
- 알람 발동 시 재생하도록 직접 선택한 **사용자 지정 MP3 파일**. 알람이 안정적
  으로 재생되도록 본 앱의 비공개 문서 디렉터리에 복사하며, 외부 업로드는
  하지 않습니다.
- 사용자가 토글한 **설정 값**(슬라이드 간격, 언어, 알람 시각/라벨, 밝기 옵션
  등). 안드로이드 `AsyncStorage` 를 사용해 기기 내부에 저장됩니다.

#### 17.3.2 Google API 를 통해 접근하는 정보 (사용자가 명시적으로 로그인한 경우에만)

설정 화면에서 사용자가 Google 로그인을 선택하면, 본 앱은 다음의 **읽기 전용
OAuth 권한**을 요청합니다.

- **`calendar.readonly`** — 메인 화면 좌상단 카드와 캘린더 화면에 오늘 일정을
  표시하기 위해 기본 Google 캘린더를 읽습니다. 일정의 생성·수정·삭제는 일절
  하지 않습니다.
- **`drive.readonly`** — Google Drive 의 `Photo` 폴더 내부 이미지를 읽어 액자
  슬라이드에 표시합니다(정품 기능). 파일의 생성·수정·삭제는 일절 하지
  않습니다.
- **`userinfo.profile`**, **`userinfo.email`** — 어느 Google 계정으로 로그인했
  는지 사용자 본인이 확인할 수 있도록 표시 이름, 이메일, 프로필 사진을
  설정 화면에 보여 주기 위해 사용합니다.

위 API 가 반환한 데이터는 **사용 시점의 기기 메모리와 작은 기기 측 캐시에만**
보관되며, 우리가 운영하는 어떤 서버로도 전송되지 않습니다.

언제든 <https://myaccount.google.com/permissions> 에서 본 앱의 접근 권한을
철회할 수 있습니다. 권한이 철회되면 본 앱은 즉시 Google 로부터 추가 데이터를
받지 않게 됩니다.

#### 17.3.3 로컬 기능을 위해 사용되는 정보

- **대략적 또는 정확한 위치 정보**. 날씨 위젯이 켜져 있고 본 앱이 **포그라운
  드(앱이 화면에 떠 있는 상태)** 일 때만 요청됩니다. 위치 값은 HTTPS 로 곧장
  Open-Meteo (`api.open-meteo.com`, `air-quality-api.open-meteo.com`) 에 전송
  되어 현재 기온·날씨 코드·PM10 공기질을 받아오는 데에만 사용됩니다. 백그라운
  드에서는 위치를 수집하지 않으며, 위치 이력도 보관하지 않습니다.
- **오디오 재생 및 진동**. 사용자가 설정한 알람음을 재생하고, 알람 발동 시
  진동 보조를 제공하기 위해 사용됩니다.

#### 17.3.4 본 앱이 수집하지 않는 정보

다음은 **절대로** 수집하지 않습니다.

- 분석 SDK (Firebase Analytics, Google Analytics, Amplitude 등 일체)
- 충돌 보고 SDK (Crashlytics, Sentry, Bugsnag 등 일체)
- 광고 식별자 (`AAID`, `IDFA`, 광고 네트워크 일체)
- 마이크, 카메라, 연락처, 문자, 통화 기록, 생체 정보
- 백그라운드 위치, 정확한 위치 이력
- Google 로그인 또는 기기 권한을 통해 사용자가 직접 부여한 정보 외의 개인
  정보

### 17.4 정보의 이용 목적

위 17.3 의 정보는 다음 목적으로만 이용됩니다.

1. 사용자가 설정한 사진·동영상·캘린더 일정·날씨·알람을 화면에 표시하기 위해
2. Google 캘린더 / Drive 읽기 권한을 얻기 위한 사용자 인증을 위해
3. 1회성 인앱 결제를 처리하고 영수증을 Google Play 와 검증하기 위해
4. 사용자의 환경설정을 다음 실행 시에도 기억하기 위해

본 앱은 사용자에 대한 프로파일링, 광고 타게팅, 자동화된 의사결정을 일절
수행하지 않습니다.

### 17.5 Google API 서비스 사용자 데이터 정책 ("Limited Use")

본 앱은 Google API 로부터 받은 정보의 이용과 다른 앱으로의 전송에 있어
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy)
의 **Limited Use** 요건을 준수합니다.

쉽게 풀어 쓰면 다음과 같습니다.

- Google 캘린더 / Drive 데이터를 본 정책에서 설명한 사용자 대상 기능을 제공
  하는 용도로만 사용합니다.
- 사용자에게 명확하게 노출되는 기능을 제공하거나 개선하기 위해 필요한 경우와
  Limited Use 요건을 준수하는 경우를 제외하고는 데이터를 제3자에게 전송하지
  않습니다.
- 데이터를 광고 송출 목적으로 사용하지 않습니다.
- (a) 사용자의 명시적 동의가 있는 경우, (b) 보안 목적, (c) 관련 법령 준수,
  (d) Limited Use 요건을 준수하는 내부 운영 목적의 집계된 데이터 사용을
  제외하고는 사람이 데이터를 열람하지 않습니다.

### 17.6 인앱 결제

본 앱은 **"Smart Frame 24 Premium"** 이라는 **1회성 정품 구매** 한 가지를
제공하며, 권장 가격은 **9.99 USD** (또는 Google Play 가 사용자 지역에 맞춰
설정한 현지 통화 환산액) 입니다. 결제가 완료된 Google 계정에 대해 권한이
영구적으로 부여되며, 설정 화면에서 언제든 [구매 복원] 으로 복구할 수
있습니다.

- 모든 결제 처리는 **Google Play 결제 시스템** 이 단독으로 수행합니다. 본 앱
  은 사용자의 카드 번호, 청구 주소, 그 밖의 결제 자격 증명을 보거나, 저장하거
  나, 전송하지 않습니다.
- 본 앱은 결제 권한 검증 · 동기화를 위해 결제 오케스트레이션 SDK 인 **Revenue
  Cat** 을 사용합니다. RevenueCat 은 사용자의 기기에서 생성된 익명 사용자
  식별자와 Google Play 가 발급한 결제 영수증만을 받습니다. 우리는 사용자의
  이름·이메일·연락처를 RevenueCat 에 전달하지 않습니다. RevenueCat 의 개인
  정보 처리 방침은 <https://www.revenuecat.com/privacy> 에서 확인할 수
  있습니다.
- 가격, 세금, 환불 정책, 분쟁 처리는 Google Play 약관을 따릅니다.

### 17.7 사용 권한

본 앱이 요청할 수 있는 안드로이드 권한과 그 정확한 사용 목적은 다음과
같습니다. 모든 권한은 해당 기능을 사용하는 시점에만 요청됩니다.

| 권한 | 사용 목적 |
| --- | --- |
| `READ_MEDIA_IMAGES`, `READ_MEDIA_VIDEO` (Android 13+) / `READ_EXTERNAL_STORAGE` (이전 버전) | 사용자가 직접 고른 사진·동영상을 슬라이드에 표시 |
| `ACCESS_COARSE_LOCATION` / `ACCESS_FINE_LOCATION` | 현재 위치의 날씨·공기질을 가져오기 위해. **포그라운드에서만 사용**, 백그라운드 위치는 명시적으로 비활성화 |
| `INTERNET`, `ACCESS_NETWORK_STATE` | Google API (캘린더, Drive), Open-Meteo (날씨), RSS 피드 (CNN, BBC, 연합뉴스), Google Play 결제 호출 |
| `VIBRATE` | 알람 발동 시 진동 보조 제공 |
| `WAKE_LOCK` (`expo-keep-awake` 경유) | 화면 꺼짐 방지 옵션을 사용자가 켰을 때만 화면을 켠 상태로 유지 |
| `POST_NOTIFICATIONS` (Android 13+, 선택) | 향후 예약 알람 안정성을 위해 예약된 권한. 현재는 사용자에게 보이는 알림을 게시하지 않음 |

본 앱은 다음의 민감 권한을 **요청하지 않습니다**: 연락처, 문자, 통화 기록,
마이크, 카메라, 신체 센서, 접근성 서비스, 디바이스 관리자, 백그라운드 위치.

### 17.8 데이터 저장 및 보안

- 사용자가 직접 통제하는 모든 데이터(설정 값, 선택한 사진 URI, 알람 정의,
  사용자 지정 MP3, Drive 캐시, 캘린더 캐시) 는 안드로이드 표준 저장소
  프리미티브 (`AsyncStorage`, 비공개 문서 디렉터리) 를 사용해 **기기 내부에**
  보관됩니다.
- Google 이 발급한 **OAuth 토큰**은 플랫폼의 암호화된 보안 저장소(Android
  Keystore, `expo-secure-store`) 에 저장됩니다. 평문 저장이나 외부 전송은
  일절 없습니다.
- 외부 서비스(Google API, Open-Meteo, RSS 소스, Google Play, RevenueCat)
  와의 통신은 **HTTPS / TLS** 를 사용합니다. 단 한 가지 예외는 CNN Top
  Stories RSS 피드로, CNN 이 현재 `rss.cnn.com` 에서 HTTP 로만 제공하는 공개
  뉴스 헤드라인 피드입니다. 본 앱은 이 피드를 헤드라인 표시 용도로만 사용
  하며, 어떠한 사용자 데이터도 이 도메인으로 전송하지 않습니다.
- 본 앱은 백엔드 서버를 운영하지 않으므로, 우리 측에서 침해될 수 있는 중앙
  데이터베이스가 존재하지 않습니다. 데이터는 사용자의 기기와 사용자가
  직접 연결한 Google 서비스 안에서만 존재합니다.

### 17.9 데이터 보유 기간

사용자가 직접 통제하는 데이터는 **사용자가 삭제하기로 결정할 때까지** 기기에
보관됩니다. 구체적으로:

- 선택한 사진·동영상은 설정에서 삭제하거나 앱 데이터를 지우면 사라집니다.
- 사용자 지정 MP3 알람음은 해당 알람을 삭제하거나 앱 데이터를 지우면 함께
  삭제됩니다.
- Google Drive / 캘린더 캐시는 로그아웃하거나 앱 데이터를 지우면 비워집니다.
- 모든 영구 저장 설정은 앱을 삭제하거나 시스템 설정에서 앱 데이터를 지우면
  사라집니다.

우리가 운영하는 서버는 존재하지 않으므로, 서버 측에 보관된 사용자 데이터도
존재하지 않습니다.

### 17.10 사용자의 권리와 선택

사용자는 거주 지역과 무관하게 다음과 같은 실질적 통제권을 갖습니다.

- <https://myaccount.google.com/permissions> 에서 **Google 접근 권한 철회**
- 시스템 설정에서 본 앱의 **위치 권한 비활성화** (날씨 위젯만 비활성화되고
  나머지 기능은 정상 동작)
- 설정 화면에서 **개별 사진 / 알람 / MP3 파일 삭제**
- **앱 삭제** 시, 본 앱이 기기에 남긴 모든 데이터가 함께 삭제됨

대한민국 사용자는 **개인정보 보호법** 에 따라 개인정보의 열람·정정·삭제·처리
정지를 요구할 권리를 갖습니다. 본 앱은 자체 서버를 운영하지 않고 개인 정보를
직접 보관하지 않으므로, 위에 안내된 통제 수단을 통해 권리를 가장 빠르게
행사할 수 있습니다. EU/EEA, 영국, 캘리포니아 거주 사용자는 GDPR / UK GDPR /
CCPA 에 따른 추가 권리를 가질 수 있습니다. 그 경우에도 위의 직접 통제 수단을
가장 먼저 사용해 주시고, 필요 시 17.16 항의 연락처로 문의해 주세요.

### 17.11 아동의 개인정보 보호

본 앱은 일반 이용자 대상 제품으로, 만 14 세 미만 아동을 대상으로 하지
않습니다. 우리는 아동의 개인정보를 알면서 수집하지 않습니다. 아동이 본 앱에
개인정보를 제공한 사실을 알게 된 경우, 17.16 항의 연락처로 알려 주시면 삭제
조치를 도와드리겠습니다.

### 17.12 제3자 서비스

본 앱은 다음의 제3자 서비스에 의존하며, 각 서비스는 해당 기능을 사용할 때만
호출됩니다.

| 서비스 | 사용 목적 | 제공자 개인정보 처리 방침 |
| --- | --- | --- |
| Google 로그인, Google Calendar API, Google Drive API | 인증 및 읽기 전용 데이터 | <https://policies.google.com/privacy> |
| Google Play 결제 시스템 | 인앱 결제 처리 | <https://policies.google.com/privacy> |
| RevenueCat | 인앱 결제 권한 검증 · 동기화 | <https://www.revenuecat.com/privacy> |
| Open-Meteo | 현재 날씨 및 공기질 | <https://open-meteo.com/en/terms> |
| CNN, BBC, 연합뉴스 RSS | 공개 뉴스 헤드라인 (읽기 전용, 익명) | 각 발행처의 정책에 따름 |

위 제3자의 개인정보 처리 관행에 대해서는 우리가 책임지지 않으며, 각자의
정책을 확인하시기 바랍니다.

### 17.13 국외 데이터 이전

본 앱이 데이터를 사용자의 기기와 Google 서비스 안에서만 처리하므로, 사용자가
생성한 데이터의 위치는 Google 의 지역별 인프라와 사용자 본인의 기기에 따라
정해집니다. 우리는 추가적인 국외 이전을 자체적으로 수행하지 않습니다.

### 17.14 본 방침의 변경

본 앱의 기능이 변경되거나 관련 법령이 요구하는 경우, 본 방침을 갱신할 수
있습니다. 갱신 시 문서 상단의 **최종 업데이트** 일자를 갱신하며, 중대한 변경
의 경우 앱 설정 화면에 별도 안내를 게시합니다. 변경 사항이 효력을 발생한
이후에도 본 앱을 계속 사용하시면 갱신된 방침에 동의하신 것으로 간주합니다.

### 17.15 만 14 세 미만 사용자와 보호자 동의

대한민국 거주 사용자가 만 14 세 미만이라면 보호자(법정대리인) 의 동의 없이
본 앱을 사용하지 마시기 바랍니다. 다른 국가의 디지털 동의 연령 기준 (예: EU
대부분 16 세) 도 동일하게 적용됩니다.

### 17.16 문의처

본 개인정보처리방침, 본 앱의 데이터 처리, 또는 17.10 항에 안내된 권리의 행사
에 관한 문의는 다음 주소로 보내주시면 됩니다.

- **이메일:** smartframe24@example.com
- **발행자:** Smart Frame 24 (출시 직전에 발행자 법적 명칭으로 갱신 예정)
- **주소:** (출시 직전에 추가 예정)

가능한 한 14 일 이내에 답변드립니다.
