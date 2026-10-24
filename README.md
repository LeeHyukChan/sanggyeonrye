# 두 가족의 첫 만남 — 상견례 모바일 리플릿

상견례 자리에서 양가 부모님이 **QR을 찍으면 휴대폰으로 바로 열리는** 한 장짜리 웹페이지입니다.
종이 3단 리플릿과 같은 내용을 휴대폰 세로 화면에 맞춰 위에서 아래로 읽도록 옮겼습니다.

- 접속 주소: https://leehyukchan.github.io/sanggyeonrye/
- QR 이미지: [`qr.png`](qr.png) (위 주소로 연결)
- 기획안: [`docs/PLAN.md`](docs/PLAN.md)

## 폴더 구성

```
sanggyeonrye/
├── index.html      ← 페이지 전체 (HTML + CSS 한 파일)
├── images/         ← 사진 넣는 곳 (아래 파일 이름 그대로)
├── qr.png          ← 인쇄용 QR 코드
├── .nojekyll       ← GitHub Pages가 파일을 그대로 서비스하도록
├── docs/PLAN.md    ← 기획안
└── README.md
```

## 내용 채우기

1. `index.html`을 메모장이나 VS Code로 열고 `[대괄호]` 부분을 찾아 실제 내용으로 바꿉니다.
   (`Ctrl+F`로 `[` 검색 → 하나씩 수정)
2. 사진은 `images/` 폴더에 아래 이름으로 넣으면 자동으로 표시됩니다. 없으면 회색 자리 표시가 나옵니다.

   | 파일 이름 | 위치 | 권장 비율 |
   |---|---|---|
   | `cover.jpg` | 표지 아치형 사진 | 세로 3:4 |
   | `groom.jpg` | 신랑 소개 원형 사진 | 정사각형 |
   | `bride.jpg` | 신부 소개 원형 사진 | 정사각형 |
   | `story.jpg` | 우리의 이야기 아래 사진 | 가로 3:2 |

   휴대폰으로 빨리 열리도록 사진은 한 장에 **500KB 이하**(긴 변 1200px 정도)로 줄여서 넣는 걸 권장합니다.
3. 포인트 색은 `index.html` 위쪽 `--accent: #4F6B55;` 한 줄만 바꾸면 전체가 바뀝니다.
   - 더스티로즈 `#8A5A54` · 네이비 `#3F5872` · 브라운 `#6B5B3E`

## 배포 (GitHub Pages)

최초 1회만:

1. GitHub 저장소 → **Settings → Pages**
2. *Build and deployment* → Source: **Deploy from a branch**
3. Branch: **main** / 폴더: **/(root)** → Save
4. 1~2분 뒤 `https://leehyukchan.github.io/sanggyeonrye/` 로 접속 확인

이후에는 수정한 파일을 커밋·푸시하면 1~2분 안에 자동 반영됩니다.

```bash
git add .
git commit -m "내용 채우기"
git push
```

## 공개 범위 주의

GitHub Pages(무료)는 **주소를 아는 누구나 볼 수 있는 공개 페이지**입니다.
검색엔진에 노출되지 않도록 `noindex`를 넣어두었지만, 가족 성함·사진이 들어가므로
상견례가 끝나면 저장소를 Private으로 돌리거나 Pages를 꺼두는 걸 권장합니다.
