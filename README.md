# 벤케이 외전 한국어 패치 v1.0.0

PC Engine 일본판 『弁慶外伝』용 비공식 한국어 패치입니다.

## 다운로드

비공개 저장소입니다. 접근 권한이 있는 GitHub 계정으로 로그인해야 파일을 받을 수 있습니다.

[v1.0.0 릴리즈](https://github.com/kilk96/benkei-gaiden-korean-patch/releases/tag/v1.0.0)에서 [Benkei_Gaiden_KO_v1.0.0.zip](https://github.com/kilk96/benkei-gaiden-korean-patch/releases/download/v1.0.0/Benkei_Gaiden_KO_v1.0.0.zip)을 받아 주세요. 압축을 풀고 `Benkei_Gaiden_KO_v1.0.0.xdelta`를 사용해 주세요. 패치와 안내문·화면 자료를 포함하며 원본 게임 파일은 직접 준비해 주세요.

## 적용 방법

1. 보유한 일본판 원본과 세이브를 백업하고, 아래 지원 원본의 파일 크기와 SHA-256을 확인해 주세요.
2. [xdelta3 3.2.0](https://github.com/jmacd/xdelta/releases/tag/v3.2.0) 또는 3.2 형식을 지원하는 패처에서 원본과 `Benkei_Gaiden_KO_v1.0.0.xdelta`를 선택해 주세요. 이 패치는 원본 파일 전체를 검사하는 3.2 검증 형식을 사용합니다.
3. 결과를 원본과 다른 이름인 `Benkei_Gaiden_KO_v1.0.0.pce`로 저장하고 결과 SHA-256을 확인해 주세요. 패치는 아래 해시의 원본에 적용합니다.
4. 결과 `.pce`를 PC Engine 에뮬레이터에서 실행해 주세요. 확인한 환경은 Mesen 2.2.1입니다.

명령줄로 적용할 때는 원본·패치·xdelta3를 같은 폴더에 두고 다음처럼 실행합니다.

```powershell
.\xdelta3.exe -d -s 'Benkei Gaiden (J).pce' 'Benkei_Gaiden_KO_v1.0.0.xdelta' 'Benkei_Gaiden_KO_v1.0.0.pce'
```

## 한글판 화면

1. 첫 대화 — 한글 대사와 줄 배치

![첫 대화](https://github.com/kilk96/benkei-gaiden-korean-patch/releases/download/v1.0.0/01-dialogue.png)

2. 필드 메뉴 — 한글 항목과 선택 표시

![필드 메뉴](https://github.com/kilk96/benkei-gaiden-korean-patch/releases/download/v1.0.0/02-menu.png)

3. 일반 전투 — 인물·적 이름과 전투 명령

![일반 전투](https://github.com/kilk96/benkei-gaiden-korean-patch/releases/download/v1.0.0/03-battle.png)

4. 능력 메뉴 — 초상화와 능력치·장비

![능력 메뉴](https://github.com/kilk96/benkei-gaiden-korean-patch/releases/download/v1.0.0/04-status.png)

## 번역·확인 범위

- 확인한 문구 목록1218항목을 기준으로 대사·메뉴·아이템/법술/적 이름·시스템·저장 안내에 한글을 적용했습니다. 원작 크레디트 인명·법인명과 비밀번호 입력 문자 등은 원어를 유지합니다.
- 사용자 엔딩 확인을 완료했습니다.
- 최신 수정인 `제호 디자인`은 실제 크레디트 장면에서 폭·글자 픽셀·원작 인명 보존을 확인했습니다. 대화·메뉴와 글꼴/조사/숫자 등 대표 검사를 함께 통과했습니다.
- 긴 대사 복사 정지, 상점/대사 잔상, 프롤로그 글자 손상, 이동 목록 넘침, 긴 이름과 커서 겹침을 수정했습니다.

## 실행과 저장

게임 내 `백업`은 저장, `여정록`은 비밀번호를 뜻합니다. 원본의 저장·비밀번호 형식을 유지합니다. 에뮬레이터의 순간 저장은 빌드에 따라 호환이 달라질 수 있으므로 기존 자료를 보존해 주세요. 원본판·다른 한글 빌드와의 순간 저장 교차 사용 및 후반 모든 저장 조합은 전수 확인하지 않았습니다.

## 알려진 제한

- 상태창·아이템 목록·장비창은 원본보다4~6프레임(약0.1초 이내) 늦게 완성될 수 있습니다. 대사는 한글 문장 폭에 따라 표시 시간이 길어질 수 있습니다.
- 원작 크레디트 인명·일부 보존 표기는 일본어입니다. 일행 목록의 죽음 상태는 공간에 맞춰 `사`로 표시합니다.
- 전체 분기·모든 특수/중첩창·최장 비밀번호·실기 환경은 전수 확인하지 않았습니다. 알려진 경미 항목으로 일부 문구의 줄 앞 공백이 있습니다.

## 지원 원본과 파일 확인

| 항목 | 값 |
|---|---|
| 기종·판본 | PC Engine HuCard 일본판 |
| 원본 파일명 예 | `Benkei Gaiden (J).pce` |
| 원본 형식 | `.pce`, 512바이트 헤더 포함 |
| 원본 크기 | 393728바이트 |
| 원본 SHA-256 | `e2bfb344b356cbbb4f32d7e9e992e392c4b7b636deb7dd601effdd0b488048de` |
| 결과 크기 | 1049088바이트(헤더 포함) |
| 결과 SHA-256 | `4bbe01b236bd8b5682b466f346265bff591e4191360a31584d41baecc2b15bb5` |

게임 데이터 영역은384KiB에서1MiB로 확장됩니다. 헤더를 제거하거나 다른 판본에 적용하지 말고 위 파일 크기·해시를 기준으로 확인해 주세요. 패치 무결성 검사와 별도로 다음 명령으로 파일 해시를 확인할 수 있습니다.

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '확인할파일.pce'
```

압축 파일 안의 `manifest.json`에는 원본·결과·패치 해시와 적용 검증 결과가, `SHA256SUMS.txt`에는 포함 파일 해시가 있습니다.

## 문제 제보

패치 버전, 에뮬레이터 이름·버전, 발생 장소와 직전 조작, 문제 화면을 함께 알려 주세요. 원본·패치 적용 완료 게임 파일은 첨부하지 말아 주세요.

## 권리와 글꼴

원작사와 관계없는 팬 번역이며 게임의 권리는 각 권리자에게 있습니다. 한글 글꼴은 [갈무리](https://github.com/quiple/galmuri)의 Galmuri14와 이름 표시용 Galmuri11을 사용합니다. 글꼴 저작권·SIL Open Font License 1.1 전문은 `FONT-LICENSE.txt`에 포함했습니다.
