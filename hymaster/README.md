# Hymaster — 법적·지원 페이지

Google Play Console과 App Store Connect에 등록하는 **공개 URL**입니다. 앱 레포(`uppinote20/hymaster`)는
private라 이 public 레포에서 정적 페이지로 서빙합니다. 손으로 작성한 HTML이며 생성기는 없습니다.

## URL

| 페이지 | URL | 용도 |
|--------|-----|------|
| 지원 | https://support-minsukkim.github.io/hymaster/ | Play 스토어 등록정보 · App Store 지원 URL |
| 개인정보 처리방침 | https://support-minsukkim.github.io/hymaster/privacy.html | Play 스토어 등록정보 · 앱 로그인 화면 링크 |
| 이용약관 | https://support-minsukkim.github.io/hymaster/terms.html | 앱 로그인 화면 링크 |
| 계정 삭제 | https://support-minsukkim.github.io/hymaster/account-deletion.html | Play 데이터 보안 → 계정 삭제 URL |

## 처리방침에 반영된 사실 (앱 변경 시 함께 갱신)

- 인증: Firebase Authentication 이메일/비밀번호만. 소셜 로그인 없음.
- 저장: 계정 정보만 Firebase Auth(Google, 국외)에 보관. `cloud_firestore` 의존성은 있으나 미사용 — 게시판·구성원 목록 등이 Firestore를 쓰기 시작하면 항목·위탁·국외 이전 표를 먼저 갱신.
- 광고·분석·크래시 SDK 없음. 권한은 INTERNET만. 외부 SNS 링크는 외부 앱/브라우저로 열기만 함.
- 계정 삭제: 앱 내 메뉴 → 정보 → 회원 탈퇴(비밀번호 재인증 후 즉시 삭제). 로그인 불가 시 이메일 요청(10일 내).
- 비밀번호 재설정 UI는 아직 없음(uppinote20/hymaster#9) — 추가되면 지원 페이지 FAQ 갱신.

운영: Minsuk Kim · support.minsukkim@gmail.com
