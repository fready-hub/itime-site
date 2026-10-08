# 아이타임 공개 페이지 (itime.rapa.world)

앱 **아이타임**(`world.rapa.itime`)의 소개·사용 설명서·개인정보처리방침. 이 폴더가 원본이고,
공개 저장소(GitHub Pages)로 그대로 게시한다 — 비공개 저장소(`fready-hub/itime`)는 Pages 를 쓸 수 없다.

| 경로 | 내용 |
|---|---|
| `/` (`index.html`) | 랜딩(서비스 소개) |
| `/manual/` | 사용 설명서 |
| `/privacy.html` (`/privacy`) | 개인정보처리방침 — 스토어 "개인정보처리방침" 칸 |
| `/account-deletion.html` | 데이터 삭제 안내 |
| `/404.html` | 오타 대응 |

앱의 설정 화면은 `https://itime.rapa.world/privacy` 와 `/manual` 로 연결한다(`lib/features/settings/settings_screen.dart`).

## 게시
- 공개 저장소 [`fready-hub/itime-site`](https://github.com/fready-hub/itime-site) 로 **파일별 복사**해 push 한다(GitHub Pages, `main` 루트).
- ⚠️ 공개 저장소의 `CNAME` 은 GitHub 이 만든다 — 원본에 두지 않고, 통째로 덮거나 `rsync --delete` 하지 않는다(공통 DOMAIN.md).
- 커스텀 도메인·DNS 는 공통 세션이 붙인다.

## 고칠 때

**앱이 실제로 하는 일과 어긋나면 안 된다.** 다음이 바뀌면 같이 고친다.

| 바뀌는 것 | 고칠 곳 |
|---|---|
| 광고·SDK·권한 | `privacy.html` 1-다, 3 · `manual/` 8, 9 |
| 입력받는 항목 | `privacy.html` 1-가 |
| 알림 동작(부팅 후 재예약, 하루 전 알림 등) | `manual/` 4, 9 |
| 화면 | `img/*.webp` 는 `SHOTS=1 flutter test test/features` 결과에서 만든다 |

수정하면 시행일과 `<footer>` 날짜를 함께 갱신한다.

## 아직 없는 것
- `app-ads.txt` — AdMob 게시자 ID 가 정해지면 그 내용으로 만든다. **빈 파일을 미리 두지 않는다**(공통 DOMAIN.md).
- 스토어 링크 — 출시 후 랜딩의 "스토어 출시 준비 중" 배지를 바꾼다.
