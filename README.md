# 자소합체 Windows

분리된 한글 자모 파일명을 Windows에서 조용히 합쳐 주는 데스크톱 앱입니다.
macOS에서 복사한 파일, 압축 해제 파일, 클라우드 동기화 폴더 등에서 한글 파일명이 깨져 보일 때 사용합니다.

```text
한글.txt  →  한글.txt
```

## 다운로드 / 실행

현재 배포 버전: `v0.1.0`

다운로드 파일:

```text
Jasohapche-Windows-v0.1.0.zip
```

1. `Jasohapche-Windows-v0.1.0.zip`을 다운로드합니다.
2. 원하는 폴더에 압축을 풉니다.
3. `v0.1.0\Jasohapche.Windows\Jasohapche.Windows.exe`를 실행합니다.
4. 필요한 감시 폴더를 추가합니다.
5. 바로 정리하려면 `지금 검사`를 누릅니다.
6. 창을 닫아도 앱은 시스템 트레이에서 계속 동작합니다.
7. 완전히 종료하려면 트레이 아이콘을 우클릭한 뒤 `종료`를 선택합니다.

## 요구 사항

- Windows 10/11
- [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0)

실행되지 않으면 .NET 8 Desktop Runtime을 설치한 뒤 다시 실행해 주세요.

## 주요 기능

- 바탕 화면 / 다운로드 폴더 기본 감시
- 감시 폴더 추가, 삭제, 열기
- 실시간 파일명 감시
- 수동 `지금 검사`
- 한글 파일명 NFC 정규화
- 이름 충돌 시 덮어쓰기 방지
  - 예: `파일.txt`가 이미 있으면 `파일 (1).txt`
- 제외 규칙 설정
  - 확장자, 파일명, 폴더명, 경로, 숨김 항목
- 최근 로그와 오늘 통계 표시
- Windows 시작 시 자동 실행 옵션
- 시스템 트레이 상주

## 안전 안내

이 앱은 파일명과 폴더명을 실제로 변경합니다.
중요한 폴더에 사용하기 전에는 작은 테스트 폴더에서 먼저 동작을 확인해 주세요.

- 같은 이름이 이미 있으면 기존 파일을 덮어쓰지 않습니다.
- 접근할 수 없는 항목은 건너뛰고 로그에 남깁니다.
- 민감한 파일명이 포함된 로그는 공개적으로 공유하지 마세요.

## 포함 파일

```text
v0.1.0/
└─ Jasohapche.Windows/
   ├─ Jasohapche.Windows.exe
   ├─ Jasohapche.Windows.dll
   ├─ Jasohapche.Core.dll
   ├─ *.json
   └─ Assets/
      └─ TrayIcon-*.*
```
