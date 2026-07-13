# design for air 시작 가이드

design for air는 nn.design 배포판의 데스크톱 앱입니다. 회사 기준으로 AI 디자인 작업을 운영하고, Codex, Claude Code, Gemini CLI 같은 로컬 CLI와 사내 승인 모델을 연결해 비용, 데이터, 실행 환경을 통제합니다.

## 설치

[최신 릴리스](https://github.com/ilous12/nn-design-release-feed/releases/latest)에서 운영체제에 맞는 설치 파일을 받아 실행하면 됩니다. macOS와 Windows를 같은 배포 흐름에서 안내합니다.

## 활용 컨셉

- **플랫폼 비종속**: Claude Design 같은 특정 플랫폼의 사용량, 모델, 저장 방식에 업무가 묶이지 않도록 운영합니다.
- **로컬 CLI 우선**: Codex, Claude Code, Gemini CLI, 로컬 모델을 회사 정책 안에서 연결해 API 방식만 고집하지 않습니다.
- **데이터 통제**: 디자인 파일, 프롬프트, 결과물, 프로젝트 컨텍스트를 로컬 또는 사내 승인 경로에서 관리합니다.
- **회사 맞춤 시스템**: 사내 서비스 UI, 브랜드 톤, 컴포넌트 규칙, 개발팀 산출물 형식에 맞게 nn.design 전용 시스템으로 운영합니다.
- **검증 가능한 운영**: 생성 결과를 검토, 수정, 재사용하고 에이전트 권한, 로그, 품질 기준을 관리합니다.

## 가이드

- **열기**: 프로젝트 폴더, 디자인 시스템, 사내 템플릿을 열어 컨텍스트를 고정합니다.
- **리믹스**: AIR 서비스 톤, 모바일 우선, 관리자 업무 흐름, 개발 전달물 기준으로 다시 요청합니다.
- **설정**: Codex, Claude Code, Gemini CLI, 로컬 모델, BYOK, 사내 API 키를 보안 정책과 비용 기준에 맞춥니다.

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

