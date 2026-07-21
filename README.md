# 메디힘 경영정보센터 — 로고·폴드6 최적화본

정적 GitHub Pages용 메디힘 경영정보 대시보드입니다.

## LNB 바로가기

- 성과 현황: `https://medihimdash.com`
- 당월 비용: `https://spend.medihimdash.com`
- 디딤돌 신청: `https://medihim.github.io/govfund/index.html` (새 창 열기)

## 브랜드 적용

- 시스템 주색을 메디힘 브랜드 컬러 `#16A2B5`로 변경
- 밝은 사이드바에 메디힘·IPPEO 로고를 별도 배경 박스 없이 나란히 배치
- 데스크톱 LNB와 모바일 드로어에서 동일한 비율로 축소
- 로고 원본은 `assets/medihim-logo-brandcolor.png`, `assets/ippeo-logo-ko.png`에 저장
- 이뻐 로고는 일본어 표기를 제외한 한글 전용 이미지이며, 원본 비율을 유지해 표시

## 접속 비밀번호

- `5153370`

비밀번호 원문은 HTML에 직접 저장하지 않고 SHA-256 해시로 비교합니다.

## 보안 적용 내용

- 최초 접속 시 전체 화면 비밀번호 입력
- 인증 전 본문 숨김
- 인증 상태는 `sessionStorage`에만 유지
- 브라우저 탭 또는 세션 종료 후 재인증
- 5회 연속 오류 시 30초 입력 제한
- 비밀번호 표시·숨김 기능
- 접속 후 `잠금` 버튼 제공
- 검색엔진 색인 방지용 `noindex` 메타 적용

## 중요한 한계

GitHub Pages는 정적 호스팅이므로 이 방식은 **최소한의 접근 제한**입니다.
HTML·JavaScript가 브라우저에 전달되기 때문에 전문적인 사용자 인증이나 기밀정보 보호 수단은 아닙니다.

다음 정보는 게시하지 않는 것을 권장합니다.

- 개인정보
- 급여 및 인사평가
- 계약서 원문
- 계좌정보
- 협상 중인 조건
- 영업비밀
- 병원 또는 환자 식별정보

실질적인 접근통제가 필요하면 Cloudflare Access, 별도 로그인 서버, 사내 Google Workspace 인증 등의 서버 측 인증이 필요합니다.

## GitHub Pages 배포

1. 새 GitHub 저장소 생성
2. `index.html`, `assets` 폴더, `.nojekyll`, `README.md` 업로드
3. `Settings → Pages`
4. `Deploy from a branch`
5. `main / root` 선택
