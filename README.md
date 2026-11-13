# THE NINTH ARENA

## 로컬 AI 대전

`index.html`을 브라우저에서 열고 재생 아이콘을 누르면 됩니다. Firebase 설정 전에도 플레이할 수 있습니다.

## GitHub Pages와 Firebase로 친구 대전 열기

1. Firebase 콘솔에서 프로젝트를 만들거나 기존 프로젝트를 열고 **프로젝트 설정 → 내 앱**에서 웹 앱을 등록합니다. **Authentication → Sign-in method**에서 **익명**을 사용 설정합니다.
2. **Realtime Database**를 잠금 모드로 만든 뒤 **Rules**에 `database.rules.json` 내용을 붙여 게시합니다. 기존 앱이 사용하는 데이터베이스라면 기존 규칙을 유지하면서 `ninthRooms` 규칙을 병합합니다.
3. 이 폴더의 `firebase-config.js`에는 `card-game-29135` 웹 앱 설정과 싱가포르 Realtime Database 주소가 입력되어 있습니다.
4. `index.html`, `firebase-config.js`, `.nojekyll`을 GitHub 저장소의 게시 폴더에 올립니다. 저장소 루트에 올렸다면 **Settings → Pages → Deploy from a branch → main → /(root)**에서 게시합니다. Firebase Authentication의 **Settings → Authorized domains**에 Pages 주소의 호스트명(예: `example.github.io`)을 등록합니다.
5. 두 사람이 각자 Pages 주소를 엽니다. 중앙의 교차 칼 아이콘으로 한 사람이 방을 만들고, 다른 사람이 6자리 코드나 초대 링크로 입장합니다. 서로 다른 Wi‑Fi에서도 대전할 수 있습니다.

- [Firebase 웹 앱 설정](https://firebase.google.com/docs/web/setup)
- [Firebase 익명 로그인](https://firebase.google.com/docs/auth/web/anonymous-auth)
- [Firebase Realtime Database 설정](https://firebase.google.com/docs/database/web/start)
- [GitHub Pages 게시 브랜치 설정](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## 효과음

제공된 MP3 10개를 짧은 모노 클립으로 압축해 `index.html`에 포함했습니다. 게임을 시작하면 효과음이 켜지고, 우측 상단 스피커로 끄거나 다시 켤 수 있습니다. 대전 시작·연장, 카드 배치, 캐릭터 공격·특수 능력, 포탑·코어 파괴, 승패에 따라 다른 소리가 나옵니다.

## 플레이

- 아이폰 세로에서는 내 코어가 아래, 상대 코어가 위에 있습니다. 두 공격로는 화면 왼쪽과 오른쪽에 놓이며 내 유닛은 위로 전진합니다. 가로에서는 내 코어가 왼쪽입니다.
- 카드를 눌러 선택하고 아군 쪽 경로 또는 지정 대상을 누르세요. 아이폰에서 길게 누르거나 맥북에서 커서를 올리면 카드 설명이 나옵니다.
- 방장 브라우저가 전투를 계산하므로 대전이 끝날 때까지 방장 탭을 전면에 둡니다. 참가자는 같은 브라우저의 같은 탭에서 45초 이내에 돌아올 수 있습니다. 방장이 페이지를 닫거나 새로고침하면 진행 중인 경기를 이어갈 수 없습니다. 이 구성은 친구 방을 위한 것이며 전투 결과는 방장 브라우저가 결정합니다.
- GitHub Pages에 공개할 때는 기존 캐릭터의 공개 사용 권한과 SCP 원문 표기 및 라이선스를 확인하세요.
