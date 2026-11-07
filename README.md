# 모아배달 광고 랜딩페이지

Google Ads 광고 → 이 페이지 → "오픈채팅 참여" 버튼 → 카카오톡 오픈채팅 으로 이어지는 랜딩페이지입니다.
버튼 클릭은 Google Ads 전환으로 기록됩니다.

- 공개 주소: https://ggcheese0927.github.io/moa-landing/
- 파일: `index.html` 하나 (GitHub Pages로 배포)

## Google 태그 ID / 전환 라벨 바꾸기

`index.html` **10~11번째 줄**의 두 값만 바꾸면 됩니다.

```js
var GOOGLE_TAG_ID    = "AW-XXXXXXXXXX";          // Google 태그 ID (AW-로 시작)
var CONVERSION_LABEL = "XXXXXXXXXXXXXXXXXXXX";   // 전환 라벨
```

Google Ads 전환 액션의 이벤트 스니펫에 있는 `send_to: 'AW-123456789/AbCdEfGhIj'`에서
`/` 앞부분이 태그 ID, 뒷부분이 전환 라벨입니다.

X로 채워진 placeholder 상태에서는 태그를 불러오지 않고, 버튼은 곧바로 오픈채팅으로 이동합니다.

## 재배포

**GitHub 웹에서 (가장 쉬움)**
1. https://github.com/ggcheese0927/moa-landing/blob/main/index.html 접속
2. 오른쪽 위 연필(✏️) 아이콘 → 값 수정 → **Commit changes**
3. 1~2분 뒤 공개 주소에 반영됩니다.

**내 PC에서**
```bash
cd "C:\Users\ggche\OneDrive\Desktop\모아배달\landing"
git add index.html
git commit -m "Set Google Ads tag ID and conversion label"
git push
```
