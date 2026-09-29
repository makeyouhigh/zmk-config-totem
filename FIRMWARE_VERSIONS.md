# TOTEM 동글 펌웨어

현재 버전: v1 — AC Minimize HID 직접 전송 (2026-09-29)

□ 기반: 2b33e8f958b899b76ce141c9ddaf1fe494aa2e43. 이 번호는 dongle 브랜치의 배포 번호입니다.

□ 기존 WINMINIMIZE와 X+C 콤보에서 Alt+Space → N을 제거하고 Consumer Usage 0x0206 한 개를 전송합니다. FULL 보고서를 명시했습니다. [사용법과 검증 한계](docs/hid-minimize.md).

□ 동글 중앙 장치 적용 대상입니다. 양쪽 키보드의 주변 역할, 화면, 전력 설정, 다른 키맵은 유지합니다. 설정 초기화는 필요하지 않습니다.

□ 검증: [GitHub Actions 36531027713](https://github.com/makeyouhigh/zmk-config-totem/actions/runs/36531027713)의 전체 빌드 및 산출물 통합 성공. 소스 커밋 e7994c2c416df1433d6df2eb086f6defb2d7c0ce. 중앙 장치의 FULL Consumer 보고서, 실제 전처리된 단일 0x0C0206 바인딩과 40ms 눌림·해제, UF2 내부 코드와 ZIP/블록/nRF52840 기종을 확인했습니다. Windows 실기기 최소화 동작은 미확인입니다.

□ ZIP SHA256: b41d535d76e2d12bbf8753cf5eb11fe70931ad35c605b1ab11ee72352ee49a1f. 동글 중앙 장치만 적용하면 되며 기존 주변 장치 펌웨어와 통신 형식은 유지됩니다.
