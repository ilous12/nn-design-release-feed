# nn.design 배포 채널

이 저장소는 nn.design 데스크톱 앱의 공개 배포 피드입니다. 설치 파일과 업데이트 메타데이터는 버전별로 관리되며, 앱은 이 피드를 통해 최신 버전을 확인합니다.

## 최신 설치 파일

- [최신 릴리스에서 설치 파일 받기](https://github.com/ilous12/nn-design-release-feed/releases/latest)
- [전체 릴리스 목록 보기](https://github.com/ilous12/nn-design-release-feed/releases)

운영체제에 맞는 파일을 선택해 설치하세요.

- macOS: `.dmg`
- Windows: `setup.exe`

## 업데이트 피드

- [최신 메타데이터](https://ilous12.github.io/nn-design-release-feed/stable/latest/metadata.json)
- [macOS 업데이트 피드](https://ilous12.github.io/nn-design-release-feed/stable/latest/latest-mac.yml)
- [Windows 업데이트 피드](https://ilous12.github.io/nn-design-release-feed/stable/latest/latest.yml)

## 배포 구조

이 저장소에는 앱이 참조하는 작은 메타데이터만 보관합니다. 용량이 큰 설치 파일, 런처 payload, 체크섬 파일은 각 버전의 GitHub Release asset으로 업로드됩니다.

```text
stable/
  latest/
    metadata.json
    latest-mac.yml
    latest.yml
    platforms/
  versions/
    <version>/
      metadata.json
      platforms/
```

## 무결성

릴리스 asset에는 SHA-256 체크섬이 함께 제공됩니다. 설치 파일을 직접 배포하거나 검증해야 하는 경우, 같은 릴리스에 포함된 `.sha256` 파일을 기준으로 확인하세요.

## 참고

이 저장소는 배포 자동화에 의해 갱신됩니다. 이슈 제보나 기능 요청은 제품 본 저장소에서 관리합니다.
