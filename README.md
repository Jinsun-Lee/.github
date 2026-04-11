# .github
GitHub 특수 레포. 같은 소유자(개인 또는 조직)의 다른 레포들이 community health files 를 가지지 않을 때 **public 레포**에 fallback 으로 사용된다.

## 포함 파일
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md): 행동 강령
- [CONTRIBUTING.md](CONTRIBUTING.md): 기여 가이드
- [SECURITY.md](SECURITY.md): 보안 취약점 신고 절차
- [SUPPORT.md](SUPPORT.md): 지원 채널 안내
- [PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md): PR 작성 시 기본 본문
- [ISSUE_TEMPLATE/](ISSUE_TEMPLATE/): 이슈 생성 시 뜨는 양식
- [CODEOWNERS](CODEOWNERS): 리뷰어 자동 지정 (fallback 미적용, 참고용)
- [FUNDING.yml](FUNDING.yml): 스폰서 버튼 설정 (fallback 미적용, 참고용)

<br>

## fallback 동작
이 레포의 파일은 같은 소유자의 다른 레포가 해당 파일을 가지지 않을 때 GitHub UI 에 자동으로 표시된다. 각 레포가 자체 파일을 가지면 그 파일이 우선한다.

<br>

## fallback 적용 대상
- `CODE_OF_CONDUCT.md`
- `CONTRIBUTING.md`
- `SECURITY.md`
- `SUPPORT.md`
- `PULL_REQUEST_TEMPLATE.md`
- `ISSUE_TEMPLATE/`

<br>

## fallback 미적용
- `CODEOWNERS`: 각 레포에 직접 둬야 동작한다.
- `FUNDING.yml`: 각 레포에 직접 둬야 동작한다.

<br>

## 소유자별 동작
- **개인 계정**: 해당 사용자의 모든 public 레포에 fallback
- **조직 계정**: 해당 조직의 모든 public 레포에 fallback

<br>

## 조직으로 옮기는 방법
GitHub UI 에서 이 레포를 조직으로 fork 한다. Fork 시 레포 이름을 반드시 `.github` 로 유지한다.

또는 `gh` CLI 사용:
```bash
gh repo fork Jinsun-Lee/.github --org my-org --fork-name .github
```

<br>

fork 후 조직의 public 레포들에 자동으로 fallback 이 적용된다. 별도 설정은 필요 없다.