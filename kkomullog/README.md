# 꼬물록 (Kkomullog) — 법적·지원 페이지

Google Play Console과 App Store Connect에 등록하는 **공개 URL**입니다. 앱 레포(`minheeverse/bloomday`)는
private라 이 public 레포에서 정적 페이지로 서빙합니다. 손으로 작성한 HTML이며 생성기는 없습니다.

## URL

| 페이지 | URL | 용도 |
|--------|-----|------|
| 지원 | https://support-minsukkim.github.io/kkomullog/ | Play 스토어 등록정보 · App Store 지원 URL |
| 개인정보 처리방침 | https://support-minsukkim.github.io/kkomullog/privacy.html | Play 스토어 등록정보 · App Store 개인정보 처리방침 URL |
| 이용약관 | https://support-minsukkim.github.io/kkomullog/terms.html | 참고 |
| 계정·데이터 삭제 | https://support-minsukkim.github.io/kkomullog/account-deletion.html | Play 데이터 보안 → 계정 삭제 URL |

## 처리방침에 반영된 사실 (앱 변경 시 함께 갱신)

- 인증: Supabase Auth 이메일 + Sign in with Apple(iOS). Google 로그인 없음.
- 저장: Supabase(Seoul ap-northeast-2) DB·Storage(체크리스트 사진). 동기화: PowerSync Cloud(국외 리전) → 국외 이전 고지.
- 민감정보: 마음 셀프체크 PHQ-9 응답(별도 동의).
- 광고·분석·크래시 SDK 없음. 알림은 로컬. 위치·연락처 미수집.
- 계정 삭제는 앱 내 버튼 없음 → 이메일 요청 절차(10일 내 처리).

운영: Minsuk Kim · support.minsukkim@gmail.com
