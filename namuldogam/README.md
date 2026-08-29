# 나물대사전 — 법적 페이지 (자동 생성)

Google Play Console과 App Store Connect에 사용하는 **공개 URL**(개인정보 처리방침 · 광고
개인정보 선택/신고 · 이용약관 · 기존 계정 삭제 안내)을 위해,
나물대사전 앱의 법적 문서를 정적 페이지로 호스팅합니다. 앱 레포는 private라 GitHub Pages를
못 쓰므로 이 별도 public 레포에서 서빙합니다.

> ⚠️ **이 HTML을 직접 수정하지 마세요.** 원천은 앱 레포(private)의 `src/content/legalContent.js`이며,
> `scripts/gen-legal-html.mjs`로 생성된 산출물입니다. `legal-source.json`의 SHA-256으로 원문
> drift를 검증합니다.

## 갱신 방법 (방침·약관 변경 시)

앱 레포에서:

```bash
# 1. src/content/legalContent.js 수정
# 2. 이 레포로 재생성
node scripts/gen-legal-html.mjs <이 레포 경로>/namuldogam
# 3. source hash·HTML·canonical·내부/외부 링크·이메일 감사
node scripts/assert-legal-site.mjs <이 레포 경로>/namuldogam src/content/legalContent.js
```

위 명령은 파일만 생성·검증하며 push 또는 Pages 배포를 하지 않습니다. 공개 반영은 서명된 앱,
스토어/AdMob 제출값과 함께 별도 승인된 cutover에서 수행합니다.

실제 공개일·앱 제출일에는 원천의 `effectiveDate`와 `effectiveDateLabel`을 함께 갱신한 뒤 다시
생성해야 합니다. auditor는 날짜 표기, 원천 SHA-256과 생성물의 일치를 함께 검사합니다.

현재 무료 로컬 보관 v1은 일기·위치 좌표/주소·사진을 담는 whole-file versioned JSON입니다.
지도 스냅샷 파일은 제외되며 좌표로 재생성될 수 있습니다. CRC는 손상 탐지 전용이고 암호화나
위변조 인증을 제공하지 않습니다.

## URL

| 페이지 | URL | 용도 |
|--------|-----|------|
| 기존 계정·데이터 삭제 | https://support-minsukkim.github.io/namuldogam/account-deletion.html | Play 데이터보안 계정삭제 링크 |
| 개인정보 처리방침 | https://support-minsukkim.github.io/namuldogam/privacy.html | Play 스토어 등록정보 처리방침 URL |
| 광고 개인정보 선택·신고 | https://support-minsukkim.github.io/namuldogam/privacy-choices.html | App Privacy 선택 URL·AdMob/지원 안내 |
| 이용약관 | https://support-minsukkim.github.io/namuldogam/terms.html | 참고 |

공개 배포 대상: main 브랜치 / namuldogam 디렉터리. 운영: Minsuk Kim · support.minsukkim@gmail.com
