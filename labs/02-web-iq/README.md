---
title: 02. Web IQ 웹 검색 결합
duration_minutes:
last_updated: 2026-10-21
---

# 02. Web IQ 웹 검색 결합

## 개요와 학습 목표

Zava의 건강 복리후생을 최신 업계 벤치마크와 비교합니다. 내부 건강 문서만으로 답할 수 없는 질문에 웹 검색 근거를 추가합니다.

- Web IQ의 MCP 지식 소스를 연결합니다.
- HR 문서·건강 문서·웹의 3개 소스로 지식 베이스를 구성합니다.
- 내부 문서와 웹페이지의 인용을 한 답변에서 확인합니다.

## 사전 요구사항

[Part 1](../01-foundry-iq/README.md)을 마친 환경과 두 검색 인덱스를 사용합니다. Web IQ에 접근할 수 있는 키를 준비하고, 저장소 루트의 `.env`에 `WEB_IQ_KEY`를 설정해야 합니다. 키는 저장소나 공유 로그에 넣지 마세요.

## 소요 시간

<!-- TODO: 저자가 Part 2를 완주해 소요 시간을 확인하고 duration_minutes와 본문에 반영합니다. -->

## 실습 단계

| 실행 자료 | 내용 |
|---|---|
| [Part 2 노트북](../../notebooks/part2-search-mcp-kb.ipynb) | 환경 변수 로드, Web IQ MCP 소스와 두 인덱스 소스 구성, 지식 베이스 생성, 내부·웹 복합 질문 |

노트북을 원래 위치에서 열고 셀을 위에서부터 실행합니다. 선택 사항인 Copilot CLI 보너스는 [사이드퀘스트](../../notebooks/copilot-cli-sidequest.md)의 설정을 사용합니다.

## 검증

건강 플랜 질문의 근거는 내부 건강 문서에서, 업계 벤치마크 질문의 근거는 웹페이지에서 나오는지 확인합니다. 참조와 활동 로그에 웹 소스 결과가 있어야 하며, 소스 오류가 있는 부분 응답은 성공으로 판단하지 않습니다.

## 정리 (Clean-up)

이후 랩에서 같은 배포를 사용합니다. 전체 실습 후 [배포 정리](../00-setup/README.md#정리-clean-up)를 수행합니다. 보너스를 진행했다면 [Copilot CLI의 MCP 설정](../../notebooks/copilot-cli-sidequest.md#5-실습-후-정리)도 제거하세요.

## 트러블슈팅

`401 Unauthorized` 또는 `auth_invalid_api_key`가 발생하면 [Web IQ 인증 오류 안내](../00-setup/README.md#external-source-auth)를 확인합니다. 키를 갱신한 뒤에는 커널을 다시 시작하고 지식 소스 생성 셀부터 실행해 저장된 인증 헤더도 갱신합니다.

## 이전·다음

[워크샵 홈](../../README.md) · [이전: Part 1. Foundry IQ](../01-foundry-iq/README.md) · [다음: Part 3. Fabric IQ](../03-fabric-iq/README.md)
