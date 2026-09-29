# TOTEM-PLA — 동글 없는 구성 v1

동글용 최신 키맵을 유지하며 키보드 두 쪽만으로 사용하는 브랜치입니다.

□ 브랜치: `codex/no-dongle`

□ 연결: 오른쪽 → BLE → 왼쪽 → BLE 또는 USB → PC. PC와 연결할 쪽은 왼쪽이며, 블루투스 장치 이름은 `TOTEM-PLA`입니다.

□ 기반: [dongle 브랜치](https://github.com/makeyouhigh/zmk-config-totem/tree/dongle)의 `2b33e8f958b899b76ce141c9ddaf1fe494aa2e43`. 기존 키맵과 콤보·매크로·레이어·마우스 키를 유지합니다. 동글 화면과 동글 전용 모듈은 포함하지 않습니다.

## 펌웨어

[Actions](https://github.com/makeyouhigh/zmk-config-totem/actions)에서 이 브랜치의 성공한 빌드를 선택하고 `firmware-totem-no-dongle-v1`을 내려받습니다.

| 적용 대상 | 파일 |
| --- | --- |
| 왼쪽 | `totem-no-dongle-left-v1.uf2` |
| 오른쪽 | `totem-no-dongle-right-v1.uf2` |
| 기존 설정 초기화 | `totem-no-dongle-settings-reset-v1.uf2` |

양쪽을 각각 USB에 연결하고 리셋을 두 번 눌러 나타난 드라이브에 해당 UF2를 복사합니다.

동글용 펌웨어를 쓰던 키보드라면 처음 전환할 때 양쪽에 설정 초기화 UF2를 적용한 다음 각각 왼쪽/오른쪽 UF2를 적용합니다. 초기화는 페어링·출력 선택 등 저장 설정을 지웁니다. 기존 동글은 분리하고 양쪽 전원을 다시 켠 뒤 PC에서 TOTEM-PLA를 페어링합니다. 이후 같은 구성의 일반 업데이트마다 초기화할 필요는 없습니다. PC에 이전 TOTEM 등록이 남아 연결이 안 되면 그 등록도 삭제하고 다시 페어링합니다. [1](https://zmk.dev/docs/troubleshooting/connection-issues)

기존 키맵의 `SYS` 레이어에는 블루투스 프로필 0~4 선택, 현재 프로필 연결 삭제, USB/BLE 출력 전환이 있습니다.

[버전 및 검증 기록](FIRMWARE_VERSIONS.md) · [하드웨어/조립 안내](https://github.com/GEIGEIGEIST/TOTEM)

![TOTEM 배열](docs/images/TOTEM_layout.svg)
