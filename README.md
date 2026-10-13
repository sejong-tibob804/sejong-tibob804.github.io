# sejong-tibob804.github.io

GitHub 계정 루트 페이지. 게시 주소는 https://sejong-tibob804.github.io/ 다.

## 왜 이 저장소가 필요한가

`app-ads.txt` 때문이다. AdMob 은 Play 등록정보의 **「웹사이트」** 칸에 적힌 주소에서
**경로를 버리고 도메인만** 떼어내 `app-ads.txt` 를 찾는다.

```
Play 웹사이트:  https://sejong-tibob804.github.io/penguin-privacy/
AdMob 이 보는 곳: https://sejong-tibob804.github.io/app-ads.txt
```

그래서 `penguin-privacy` 레포 안에 넣으면 소용이 없고, 계정 루트를 서빙하는
`<계정명>.github.io` 레포가 따로 있어야 한다. 그게 여기다.

## app-ads.txt 는 앱마다 늘지 않는다

파일 한 줄은 "이 계정이 내 광고 지면을 팔 권한이 있다" 는 선언이지 앱 목록이 아니다.
게임을 몇 개를 내든 **같은 AdMob 계정이면 한 줄 그대로**다. 줄이 느는 건 광고
네트워크를 더할 때뿐이다(Unity Ads, AppLovin 등).

고칠 일이 있으면 AdMob → 앱 → app-ads.txt 안내에 적힌 줄을 그대로 복사해 넣는다.

## 게임별 폴더

게임마다 개인정보처리방침과 업데이트 확인 파일을 `/<게임>/` 폴더에 둔다 (펭귄은 예전부터 쓰던 `penguin-privacy` 레포 그대로).

| 폴더 | 내용 |
|---|---|
| `fallingdash/index.html` | Falling Dash 개인정보처리방침 (한·영·일). 고치면 문서 안의 시행일·최종 수정일도 올린다 |
| `fallingdash/version.json` | 게임이 켜질 때 읽는 버전 정보 (아래) |

`version.json`:

- `latest`: 최신 버전 코드 (안드로이드 versionCode). 게임 버전이 이보다 낮으면 "새 버전이 있어요" 안내를 버전마다 한 번.
- `min`: 이보다 낮은 버전은 업데이트해야만 계속할 수 있다 (저장 방식이 바뀌는 큰 업데이트 때만).
- `store`: [업데이트] 버튼이 여는 주소.
- `message`: 업데이트 안내에 덧붙일 말 (`null`, 글자, 또는 `{"ko": …, "en": …, "ja": …}`).
- `notice`: 공지 (`null` 또는 `{"id": "고유값", "ko": …, "en": …, "ja": …}`). `id` 마다 한 번만 보인다.
