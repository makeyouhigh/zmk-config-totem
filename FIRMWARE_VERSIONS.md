# TOTEM-PLA 동글 없는 펌웨어

현재 버전: v1

□ 기반: dongle 브랜치의 2b33e8f958b899b76ce141c9ddaf1fe494aa2e43. 새 브랜치는 codex/no-dongle입니다. 기존 dongle/master 브랜치는 변경하지 않습니다.

□ 연결: 오른쪽 → BLE → 왼쪽 → BLE 또는 USB → PC. 왼쪽이 중앙 장치이며 블루투스 이름은 TOTEM-PLA입니다. 중앙 장치가 연결하는 키보드 주변 장치는 오른쪽 한 개입니다.

□ 동글 전용 화면, Raw HID, KeyPeek 모듈과 동글 빌드/실드/이전 오버레이를 제거했습니다. 키맵·콤보·매크로·레이어·마우스 키와 양쪽 실제 키 스캔/핀 배치, 충전 설정, 1시간 절전 설정은 dongle 브랜치를 유지합니다. 중앙 장치의 배터리 수신 설정은 왼쪽에만 적용합니다.

□ 파일: totem-no-dongle-left-v1.uf2, totem-no-dongle-right-v1.uf2. 설정 초기화 파일은 totem-no-dongle-settings-reset-v1.uf2입니다. 동글용으로 페어링된 기기를 전환할 때는 기존 페어링을 초기화한 뒤 새 구성으로 연결합니다.

□ 빌드 및 산출물 검증은 완료 후 기록합니다. 실제 키보드 적용은 확인 전입니다.
