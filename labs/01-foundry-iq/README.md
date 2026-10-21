---
title: 01. Foundry IQ 지식 베이스 구축
duration_minutes:
last_updated: 2026-10-21
---

# 01. Foundry IQ 지식 베이스 구축

## 개요와 학습 목표

Zava의 HR·복리후생 질문에 답할 기본 지식 베이스를 만듭니다. PDF를 업로드하는 파일 지식 소스와 미리 구축된 검색 인덱스를 사용하는 소스를 각각 실습합니다.

- 클라우드 아키텍처 PDF를 파일 지식 소스로 업로드하고 질의합니다.
- `hrdocs`와 `healthdocs` 인덱스를 색인된 지식 소스로 연결합니다.
- 질문을 적절한 소스로 라우팅하고 인용 기반 답변을 확인합니다.

## 사전 요구사항

[환경 배포](../00-setup/README.md)를 마쳐야 합니다. Azure AI Search, Azure OpenAI의 `gpt-5.4`·`text-embedding-3-large` 배포와 두 검색 인덱스를 사용합니다. 저장소 루트의 `.env`와 준비한 Python 커널을 확인하세요.

## 소요 시간

<!-- TODO: 저자가 Part 1을 완주해 소요 시간을 확인하고 duration_minutes와 본문에 반영합니다. -->

## 실습 단계

| 실행 자료 | 내용 |
|---|---|
| [Part 1 노트북](../../notebooks/part1-standard-foundry-iq-kb.ipynb) | 환경 변수 로드, 파일 업로드, 파일 지식 베이스 질의, 두 인덱스를 연결한 지식 베이스 질의 |

노트북을 원래 위치에서 열고 셀을 위에서부터 실행합니다. 파일 업로드 셀은 기존 [실습 데이터](../../data/ai-search-data)를 사용합니다. 노트북을 다른 폴더로 복사하면 상대 경로가 달라집니다.

Copilot CLI 보너스는 선택 사항입니다. 진행하려면 [사이드퀘스트](../../notebooks/copilot-cli-sidequest.md)를 따르세요.

## 검증

파일 지식 베이스의 답변이 업로드한 PDF를 참조하는지 확인합니다. 이어서 색인된 소스의 답변·참조·활동 로그를 확인해 HR 문서와 건강 문서의 검색 결과를 추적합니다. 노트북의 소스 헌트에서 답변과 실제 근거를 대조하세요.

## 정리 (Clean-up)

다음 랩에서 같은 Search 서비스와 인덱스를 사용합니다. 전체 실습 후 [배포 정리](../00-setup/README.md#정리-clean-up)를 수행합니다. Copilot CLI를 연결했다면 [MCP 설정 정리](../../notebooks/copilot-cli-sidequest.md#5-실습-후-정리)도 수행하세요.

## 트러블슈팅

초기 배포나 환경 설정에 문제가 있으면 [배포 가이드](../00-setup/README.md)를 확인합니다.

<!-- TODO: Part 1에서 재현하고 해결한 추가 오류만 기록합니다. -->

## 이전·다음

[워크샵 홈](../../README.md) · [이전: 환경 배포](../00-setup/README.md) · [다음: Part 2. Web IQ](../02-web-iq/README.md)
