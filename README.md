# 🍽 오늘 뭐 먹지? — 팀 점심 메뉴 결정기

> 팀원들과 함께 쓰는 점심 메뉴 랜덤 뽑기 / 투표 / 기록 앱

![Static Badge](https://img.shields.io/badge/무료-100%25-green) ![Static Badge](https://img.shields.io/badge/설치-불필요-blue) ![Static Badge](https://img.shields.io/badge/Google_Sheets-연동-yellow)

---

## ✨ 기능

- 🎲 **랜덤 뽑기** — 슬롯머신처럼 돌아가다가 메뉴 결정
- 👍 **투표** — 팀원들이 원하는 메뉴에 투표, 1위 메뉴 표시
- 📋 **오늘의 메뉴 기록** — 날짜별로 뭐 먹었는지 기록
- 🍜 **메뉴 관리** — 팀원 누구나 메뉴 추가 / 삭제
- ☁️ **Google Sheets 실시간 동기화** — 팀원 전체가 같은 데이터 공유

---

## 🚀 시작하기

### 1단계 — Google Apps Script 설정

1. [Google Sheets](https://sheets.google.com) 에서 새 스프레드시트 생성
2. 상단 메뉴 **확장 프로그램 → Apps Script** 클릭
3. 기존 코드 전부 삭제 후 `apps-script.gs` 파일 내용 붙여넣기
4. 💾 저장 (Ctrl+S)

### 2단계 — 웹 앱 배포

1. 오른쪽 상단 **배포 → 새 배포** 클릭
2. 유형: **웹 앱** 선택
3. 다음 액세스 권한이 있는 사용자: **모든 사용자** 선택
4. **배포** 클릭
5. 생성된 **웹 앱 URL 복사**

### 3단계 — HTML 파일 연결

`index.html` 파일을 열고 아래 부분에 URL 붙여넣기:

```javascript
// 여기에 붙여넣기
const HARDCODED_URL = "https://script.google.com/macros/s/여기에붙여넣기/exec";
```

저장 후 팀원들에게 파일 공유 or GitHub Pages 링크 전송 🎉

---

## 🌐 GitHub Pages로 링크 공유하기 (권장)

파일 공유 대신 링크 하나로 팀원 전체가 접속할 수 있어요.

1. GitHub에서 새 Repository 생성 (Public)
2. `index.html` 파일 업로드
3. Settings → Pages → Branch: main → Save
4. 아래 링크 팀원들에게 공유:

```
https://[깃헙아이디].github.io/[저장소이름]
```

---

## 📁 파일 구성

```
📦 lunch-picker
 ┣ 📄 index.html        # 메인 앱 (이거 하나면 됩니다)
 ┣ 📄 apps-script.gs    # Google Apps Script 백엔드 코드
 ┗ 📄 README.md         # 이 파일
```

---

## 🛠 기술 스택

- **Frontend** — HTML / CSS / Vanilla JS (라이브러리 없음)
- **Backend** — Google Apps Script
- **DB** — Google Sheets
- **Font** — [HSSanTokki20](https://github.com/projectnoonnu/2405) (무료 상업용)
- **Hosting** — GitHub Pages (무료)

---

## ❓ FAQ

**Q. 설치해야 하나요?**  
A. 아니요! 파일 열기만 하면 바로 사용 가능해요.

**Q. 비용이 드나요?**  
A. 전부 무료예요. Google Sheets, GitHub Pages 모두 무료 플랜으로 충분합니다.

**Q. 팀원들도 메뉴를 추가할 수 있나요?**  
A. 네! 앱 하단 메뉴 관리 섹션에서 누구나 추가/삭제 가능해요.

**Q. 실시간으로 반영되나요?**  
A. 30초마다 자동 동기화돼요. 투표/메뉴 추가는 즉시 반영됩니다.
