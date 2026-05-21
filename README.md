# 자소합체 Windows App

<p align="center">
  <img src="v0.1.0/Jasohapche.Windows/Assets/TrayIcon-B-active.png" alt="자소합체 Windows 트레이 아이콘" width="96">
</p>

<p align="center">
  <strong>분리된 한글 자모 파일명을 Windows에서 조용히 합쳐 주는 배포용 데스크톱 앱 패키지.</strong><br>
  macOS에서 복사한 파일, 압축 해제 파일, 클라우드 동기화 폴더의 깨진 한글 이름을 NFC로 정리합니다.
</p>

<p align="center">
  <a href="Jasohapche-Windows-v0.1.0.zip"><img alt="Download" src="https://img.shields.io/badge/download-v0.1.0-22C55E?style=flat-square"></a>
  <a href="https://dotnet.microsoft.com/download/dotnet/8.0"><img alt=".NET 8 Desktop Runtime" src="https://img.shields.io/badge/.NET%20Desktop%20Runtime-8.0-512BD4?style=flat-square&logo=dotnet&logoColor=white"></a>
  <a href="https://www.microsoft.com/windows"><img alt="Windows" src="https://img.shields.io/badge/platform-Windows%2010%2F11-0078D4?style=flat-square&logo=windows11&logoColor=white"></a>
  <a href="v0.1.0/README.md"><img alt="Package README" src="https://img.shields.io/badge/package-README-8B5CF6?style=flat-square"></a>
</p>

---

## 무엇을 내려받나요?

이 저장소는 **자소합체 Windows v0.1.0 실행 배포본**을 담고 있습니다. 개발 소스가 아니라, 사용자가 바로 압축을 풀고 실행할 수 있는 패키지 저장소입니다.

```text
한글.txt  →  한글.txt
```

| 항목 | 값 |
| --- | --- |
| 현재 버전 | `v0.1.0` |
| 다운로드 파일 | `Jasohapche-Windows-v0.1.0.zip` |
| 실행 파일 | `v0.1.0/Jasohapche.Windows/Jasohapche.Windows.exe` |
| 대상 런타임 | `.NET 8 / win-x64` |
| 필요 환경 | Windows 10/11 + .NET 8 Desktop Runtime |

> 소스 코드와 개발 문서는 [`yelixir-dev/jasohapche-windows`](https://github.com/yelixir-dev/jasohapche-windows) 저장소를 기준으로 합니다.

## 빠른 실행

1. 이 저장소에서 `Jasohapche-Windows-v0.1.0.zip`을 다운로드합니다.
2. 원하는 폴더에 압축을 풉니다.
3. 아래 실행 파일을 엽니다.

   ```text
   v0.1.0\Jasohapche.Windows\Jasohapche.Windows.exe
   ```

4. 필요한 감시 폴더를 추가합니다.
5. 바로 정리하려면 `지금 검사`를 누릅니다.
6. 창을 닫아도 앱은 시스템 트레이에서 계속 동작합니다.
7. 완전히 종료하려면 트레이 아이콘을 우클릭한 뒤 `종료`를 선택합니다.

## 요구 사항

- Windows 10/11
- [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0)

실행되지 않거나 Windows가 런타임을 요구하면 .NET 8 Desktop Runtime을 설치한 뒤 다시 실행해 주세요.

## 주요 기능

### 파일명 정규화

- 분리된 한글 자모 파일명/폴더명을 Windows 친화적인 NFC 형태로 정규화
- 같은 이름이 이미 있을 때 기존 파일을 덮어쓰지 않고 suffix 적용
  - 예: `파일.txt` → `파일 (1).txt`

### 감시와 수동 검사

- 바탕 화면 / 다운로드 폴더 기본 감시
- 감시 폴더 추가, 삭제, 열기
- 실시간 파일명 감시
- 수동 `지금 검사`

### 제외 규칙

| 유형 | 용도 |
| --- | --- |
| 확장자 제외 | `zip`, `tmp` 같은 파일 확장자 제외 |
| 파일명 제외 | 특정 파일명 패턴 제외 |
| 폴더명 제외 | `node_modules`, `.git` 같은 폴더 제외 |
| 경로 포함 제외 | 특정 경로 문자열이 포함된 항목 제외 |
| 숨김 항목 제외 | 숨김 속성 파일/폴더 제외 |

### 데스크톱 사용성

- 시스템 트레이 상주
- 최근 로그와 오늘 통계 표시
- Windows 시작 시 자동 실행 옵션
- `Dark` / `Carbon Light` 테마
- 활성/일시정지 상태별 트레이 아이콘 포함

## 포함 파일

```text
jasohapche-windows-app/
├── Jasohapche-Windows-v0.1.0.zip
├── README.md
└── v0.1.0/
    ├── README.md
    └── Jasohapche.Windows/
        ├── Jasohapche.Windows.exe
        ├── Jasohapche.Windows.dll
        ├── Jasohapche.Core.dll
        ├── Jasohapche.Windows.deps.json
        ├── Jasohapche.Windows.runtimeconfig.json
        └── Assets/
            ├── TrayIcon-A-active.ico
            ├── TrayIcon-A-paused.ico
            ├── TrayIcon-B-active.ico
            ├── TrayIcon-B-paused.ico
            └── ...
```

## 무결성 확인

다운로드한 zip이 이 저장소의 배포본과 같은지 확인하려면 SHA-256 값을 비교하세요.

```text
Jasohapche-Windows-v0.1.0.zip
SHA-256: 1de9624105a95ff3d4ef4e4555a9daf5c5499695d2ccc5a04ebd924cf61736bc
```

## 안전 안내

이 앱은 파일명과 폴더명을 실제로 변경합니다. 중요한 폴더에 사용하기 전에는 작은 테스트 폴더에서 먼저 동작을 확인해 주세요.

- 같은 이름이 이미 있으면 기존 파일을 덮어쓰지 않습니다.
- 접근할 수 없는 항목은 건너뛰고 로그에 남깁니다.
- 민감한 파일명이나 개인 경로가 포함된 로그는 공개적으로 공유하지 마세요.
- 최종 트레이/파일명 변경 동작은 Windows 환경에서 확인해야 합니다.

## 배포 메모

- 이 저장소는 사용자 다운로드용 패키지 저장소입니다.
- `v0.1.0/` 폴더 전체를 함께 보관해야 실행 파일과 아이콘 자산이 정상적으로 동작합니다.
- zip 내부에도 같은 `v0.1.0/` 폴더 구조가 포함되어 있습니다.

## 라이선스

현재 이 배포 저장소에는 별도 `LICENSE` 파일이 없습니다. 공개 재배포 전 라이선스 파일을 추가해야 합니다.
