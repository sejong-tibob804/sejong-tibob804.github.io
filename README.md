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
