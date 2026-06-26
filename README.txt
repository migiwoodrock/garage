GARAGE — PWA 설치 가이드
================================
앱 이름: GARAGE   |   아이콘: 직접 주신 바이크 엠블럼
(이전에 저장하신 정비 데이터 — PCX125·S1000RR 내역 — 그대로 들어있습니다)

[ 폴더 구성 ]
  index.html              ← 앱 본체 (정비이력 + 데이터 내장)
  manifest.webmanifest    ← 앱 이름/아이콘/색상
  service-worker.js       ← 오프라인 실행 + 설치 가능
  icons/                  ← 엠블럼 아이콘 (192/512/maskable/apple-touch/favicon)

────────────────────────────────
[ GitHub Pages 로 올리기 (무료) ]
1. github.com 가입/로그인 → New repository → 이름 예: garage → Public → Create
2. "uploading an existing file" → 이 폴더 안의 항목 전부 업로드
   (index.html, manifest.webmanifest, service-worker.js, icons 폴더가 최상단에 오게)
   → Commit
3. Settings → Pages → Branch: main / 폴더: /(root) → Save
4. 잠시 뒤 https://<아이디>.github.io/garage/ 주소 생성

────────────────────────────────
[ 아이폰 설치 ]  Safari 로 위 주소 열기 → 공유 → "홈 화면에 추가"
[ 윈도우 설치 ] 크롬으로 위 주소 열기 → 주소창 "설치"(⊕) 클릭

→ 양쪽 다 바이크 엠블럼 아이콘으로 앱처럼 깔립니다.

────────────────────────────────
[ 데이터 ]
설치 후엔 기기 안(localStorage)에 자동 저장 → 닫았다 켜도 유지.
(처음 실행 땐 index.html 에 내장된 데이터로 시작, 이후엔 내 편집이 우선)
다른 기기로 옮길 땐 앱 안 "💾 저장"으로 파일 내보내 옮기면 됨.

[ 아이콘/이름 바꾸려면 ]
- 이름: manifest.webmanifest 의 "name"/"short_name" 수정
- 아이콘: icons/ 안 png 들을 같은 이름으로 교체 (정사각형 이미지 주시면 만들어 드림)
- 바꾼 뒤엔 앱 삭제 후 다시 "홈 화면에 추가" 해야 새 아이콘 반영
