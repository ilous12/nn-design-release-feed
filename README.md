# Design For AIR 시작 가이드

Design For AIR는 nn.design 배포판의 데스크톱 앱입니다. 처음 사용하는 사람도 설치 후 바로 디자인을 열고, 리믹스하고, 사내 작업 환경에 맞게 설정할 수 있도록 이 배포 채널을 운영합니다.

## 설치

1. [최신 릴리스에서 설치 파일 받기](https://github.com/ilous12/nn-design-release-feed/releases/latest)를 엽니다.
2. macOS 사용자는 `.dmg` 파일을 내려받아 Applications 폴더로 이동합니다.
3. 앱을 처음 열 때 보안 확인이 나오면 조직에서 배포한 앱인지 확인한 뒤 실행합니다.
4. 업데이트는 앱이 이 배포 피드의 `metadata.json`을 읽어 자동으로 확인합니다.

## 가이드

- **열기**: 앱을 실행한 뒤 기존 프로젝트 폴더나 디자인 작업 폴더를 엽니다. 처음에는 샘플 또는 사내 템플릿으로 시작하는 것이 좋습니다.
- **리믹스**: 생성된 화면을 그대로 쓰기보다 목적, 사용자, 플랫폼을 바꿔 다시 요청합니다. 예: "사내 관리자 화면으로 리믹스", "모바일 우선으로 재구성".
- **설정**: 사용할 AI 에이전트, API 키, 언어, 디자인 시스템을 조직 정책에 맞게 조정합니다. 민감한 프로젝트에서는 허용된 에이전트만 사용합니다.

## 업데이트 피드

- [최신 메타데이터](https://ilous12.github.io/nn-design-release-feed/stable/latest/metadata.json)
- [macOS arm64 manifest](https://ilous12.github.io/nn-design-release-feed/stable/latest/platforms/mac_arm64.json)

## 배포 구조

이 저장소에는 앱이 참조하는 작은 메타데이터만 보관합니다. 용량이 큰 설치 파일, 런처 payload, 체크섬 파일은 각 버전의 GitHub Release asset으로 업로드됩니다.

```text
stable/
  latest/
    metadata.json
    platforms/
  versions/
    <version>/
      metadata.json
      platforms/
```

## 검증

릴리스 asset에는 SHA-256 체크섬이 함께 제공됩니다. 설치 파일을 직접 배포하거나 검증해야 하는 경우, 같은 릴리스에 포함된 `.sha256` 파일을 기준으로 확인하세요.
