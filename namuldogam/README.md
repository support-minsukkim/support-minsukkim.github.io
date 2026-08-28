# 나물대사전 — 법적 페이지 (자동 생성)

Google Play Console이 요구하는 **공개 URL**(개인정보처리방침 · 계정 삭제 안내)을 위해,
나물대사전 앱의 법적 문서를 정적 페이지로 호스팅합니다. 앱 레포는 private라 GitHub Pages를
못 쓰므로 이 별도 public 레포에서 서빙합니다.

> ⚠️ **이 HTML을 직접 수정하지 마세요.** 원천은 앱 레포(private)의 `src/content/legalContent.js`이며,
> `scripts/gen-legal-html.mjs`로 생성된 산출물입니다.

## 갱신 방법 (방침·약관 변경 시)

앱 레포에서:

```bash
# 1. src/content/legalContent.js 수정
# 2. 이 레포로 재생성
node scripts/gen-legal-html.mjs <이 레포 경로>
# 3. 이 레포에서 커밋 + push (main) → GitHub Pages 자동 재배포
```

## URL

| 페이지 | URL | 용도 |
|--------|-----|------|
| 계정·데이터 삭제 | https://support-minsukkim.github.io/namuldogam/account-deletion.html | Play 데이터보안 계정삭제 링크 |
| 개인정보 처리방침 | https://support-minsukkim.github.io/namuldogam/privacy.html | Play 스토어 등록정보 처리방침 URL |
| 이용약관 | https://support-minsukkim.github.io/namuldogam/terms.html | 참고 |

배포: main 브랜치 / namuldogam 디렉터리. 운영: Minsuk Kim · support.minsukkim@gmail.com
