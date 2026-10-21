---
title: 06. 전체 IQ 통합 검색
duration_minutes:
last_updated: 2026-10-21
---

# 06. 전체 IQ 통합 검색

## 개요와 학습 목표

Fabric의 재고 위험, Microsoft 365 업무 메일, 사내 정책, 건강 복리후생, 웹 벤치마크를 함께 조회합니다. 네 가지 IQ의 다섯 지식 소스를 한 지식 베이스로 연결하는 마지막 랩입니다.

- HR 문서·건강 문서·Fabric·Work IQ·웹을 결합합니다.
- 단일 retrieval request에서 질문 계획, 소스 조회, 참조와 답변 합성을 확인합니다.

## 사전 요구사항

[Part 1](../01-foundry-iq/README.md)의 검색 인덱스, [Part 2](../02-web-iq/README.md)의 Web IQ 키, [Part 3](../03-fabric-iq/README.md)의 Fabric 설정을 사용합니다. [Part 4](../04-work-iq/README.md)에서 Search 연결과 Work IQ 환경 변수 4개를 준비하고 사용자 접근 권한을 확인해야 합니다.

Part 4에서 같은 메일함에 데모 이메일 3통을 준비했다면 다시 보낼 필요가 없습니다. 아직 준비하지 않았다면 Part 4 노트북의 메일 준비 셀부터 진행합니다.

## 소요 시간

<!-- TODO: 저자가 Part 6을 완주해 소요 시간을 확인하고 duration_minutes와 본문에 반영합니다. -->

## 실습 단계

| 실행 자료 | 내용 |
|---|---|
| [Part 6 노트북](../../notebooks/part6-work-iq-fabric-iq-to-kb.ipynb) | Azure 로그인, 환경 변수 로드, Work IQ·Fabric 로그인, 다섯 소스 구성, 단일 요청 기반 통합 검색 |

노트북을 원래 위치에서 열고 셀을 위에서부터 실행합니다. 같은 환경의 Part 4에서 Azure 로그인을 마쳤다면 노트북 안내에 따라 로그인 단계를 건너뛸 수 있습니다.

## 검증

하나의 retrieval request에 대한 계획과 활동 로그를 확인하고 다섯 지식 소스의 결과·참조를 대조합니다. Fabric 조회 오류가 없고 `workIQ`와 웹 참조가 포함되어야 합니다. Fabric의 `HAND TOOLS` 재고 집계 기준은 총 `stockLevel` 1,635입니다.

어느 소스라도 실패하거나 필요한 참조가 누락된 부분 응답은 전체 성공으로 판단하지 않습니다. 노트북의 마지막 미션 완료 항목과 실제 결과를 대조하세요.

## 정리 (Clean-up)

전체 실습을 마쳤다면 [배포 정리](../00-setup/README.md#정리-clean-up)를 수행합니다. Part 1/2의 Copilot CLI 보너스를 진행했다면 [MCP 설정](../../notebooks/copilot-cli-sidequest.md#5-실습-후-정리)도 제거합니다.

<!-- TODO: 데모 메일, Entra 앱 등록과 Work IQ 결제 정책의 정리 범위는 Part 4와 함께 저자가 확인합니다. -->

## 트러블슈팅

Fabric 문제는 [Ontology 바인딩 안내](../00-setup/README.md#ontology-bindings), Web IQ·Work IQ 문제는 [소스 인증 오류 안내](../00-setup/README.md#external-source-auth)를 확인합니다. Work IQ 설정이 누락됐다면 [Part 4의 시작 준비](../../notebooks/part4-work-iq-to-kb.ipynb#시작-준비-search-관리-id-연결)로 돌아갑니다.

## 이전·다음

[이전: Part 5. 통합 검색](../05-combined-iq/README.md) · [완료: 워크샵 홈](../../README.md)
