---
id: community-20260820-001
title: Initialize Organization Governance
status: completed
created_at: 2026-08-20T12:05:00+09:00
updated_at: 2026-08-20T12:05:00+09:00
owners:
  - organization
initiative: foundation-multirepo-bootstrap
depends_on: []
supersedes: []
affected_repos:
  - .github
  - roadmap
  - gateway
  - conformance
  - dashboard
  - cloud
---

# Initialize Organization Governance

## 목적

모든 Native AI Gateway 저장소에 공통 기여, 보안, 거버넌스 및 GitHub 협업 진입점을 제공한다.

## 범위

- Organization profile
- Community contribution policy
- Governance, security, and support policy
- Pull request template
- Plan and bug issue forms
- Plan validation workflow template
- Organization policy plan log

## 제외 범위

- Product repository implementation policy의 세부 내용
- Branch ruleset 강제 적용
- Production credential과 infrastructure
- 자동 cross-repository 문서 push

## 정책 및 Rollout

공통 GitHub UI 정책은 이 저장소가 제공한다. 각 제품 저장소는 clone만으로 Agent와 사람이 읽을 수 있도록 로컬 `AGENTS.md`, `CONTRIBUTING.md`, `plans/`를 별도로 유지한다.

## 보안 영향

이 저장소는 공개이므로 비공개 가격, credential, 고객 데이터, 취약점 세부 정보를 포함하지 않는다.

## 검증 계획

- Community file 경로와 YAML 형식 확인
- Public visibility 확인
- 제품 저장소의 clone-local 지침 존재 확인

## 완료 조건

- [x] 공통 contribution, governance, security 문서 작성
- [x] PR 및 Issue template 작성
- [x] 공개 Organization profile 작성
- [x] 저장소가 public으로 생성 및 push됨

## 검증 증거

- Repository: `https://github.com/nativegatewayhq/.github`
- Initial commit: `c2df945`
- Public visibility와 `main` default branch를 GitHub CLI로 검증함.
- 모든 초기 저장소에 `plan`, `initiative`, `security`, `billing` 공통 라벨을 생성함.

## 후속 작업

- Organization ruleset
- Private vulnerability reporting 활성화
- Workflow policy 강화
