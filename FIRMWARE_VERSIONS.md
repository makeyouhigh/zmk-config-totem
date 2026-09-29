# TOTEM-PLA 동글 없는 펌웨어

현재 버전: v2 — AC Minimize HID 직접 전송 (2026-09-29)

□ 기존 WINMINIMIZE와 X+C 콤보에서 Alt+Space → N을 제거하고 Consumer Usage 0x0206 한 개를 전송합니다. FULL 보고서를 명시했습니다. [사용법과 검증 한계](docs/hid-minimize.md).

□ 왼쪽 중앙 장치 적용 대상입니다. 오른쪽 동작, TOTEM-PLA 이름, 연결 역할, 절전, 다른 키맵은 유지합니다. 설정 초기화는 필요하지 않습니다.

□ 빌드와 산출물 검증: 진행 전. Windows 실기기 최소화 동작: 미확인.

# 이전 버전 v1

□ 기반: dongle 브랜치의 2b33e8f958b899b76ce141c9ddaf1fe494aa2e43. 새 브랜치는 codex/no-dongle입니다. 기존 dongle/master 브랜치는 변경하지 않았습니다.

□ 연결: 오른쪽 → BLE → 왼쪽 → BLE 또는 USB → PC. 왼쪽이 중앙 장치이며 블루투스·USB 이름은 TOTEM-PLA입니다. 중앙 장치가 연결하는 키보드 주변 장치는 오른쪽 한 개입니다.

□ 동글 전용 화면, Raw HID, KeyPeek 모듈과 동글 빌드/실드/이전 오버레이를 제거했습니다. 키맵·콤보·매크로·레이어·마우스 키와 양쪽 실제 키 스캔/핀 배치, 충전 설정, 1시간 절전 설정은 dongle 브랜치를 유지합니다. 중앙 장치의 배터리 수신 설정은 왼쪽에만 적용합니다.

□ 파일: totem-no-dongle-left-v1.uf2, totem-no-dongle-right-v1.uf2. 설정 초기화 파일은 totem-no-dongle-settings-reset-v1.uf2입니다. 동글용으로 페어링된 기기를 전환할 때는 양쪽의 저장 설정을 초기화한 뒤 새 구성으로 연결합니다.

□ 검증: [GitHub Actions 36519243720](https://github.com/makeyouhigh/zmk-config-totem/actions/runs/36519243720)에서 세 대상 빌드와 산출물 통합 성공. 빌드 소스는 dc8b208133c85d700f148514c467594828834891입니다.

□ 빌드된 설정에서 왼쪽 중앙 역할·오른쪽 주변 역할, 왼쪽 BLE/USB 출력, TOTEM-PLA 이름, 오른쪽 1대 연결, 절전 설정을 확인했습니다. 기존 키맵과 양쪽 핀 배치 파일의 Git 해시가 기반과 동일합니다. 다운로드 ZIP의 SHA256 일치, 세 UF2의 블록·nRF52840 식별자·주소 범위를 확인했습니다. 실제 키보드 적용과 연결 동작은 아직 확인하지 않았습니다.
