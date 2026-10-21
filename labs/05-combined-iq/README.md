---
title: 05. Work IQ 없는 통합 검색
duration_minutes:
last_updated: 2026-10-21
---

# 05. Work IQ 없는 통합 검색

## 개요와 학습 목표

Zava의 여름 세일 준비 상황을 사내 정책·제품 재고·웹 벤치마크로 점검합니다. Work IQ를 제외하고 Foundry IQ·Fabric IQ·Web IQ의 4개 지식 소스를 결합합니다.

- HR 문서·건강 문서·Fabric·웹을 하나의 지식 베이스로 연결합니다.
- 하나의 복합 질문으로 네 지식 소스의 결과와 인용을 확인합니다.

## 사전 요구사항

[Part 1](../01-foundry-iq/README.md)의 검색 인덱스, [Part 2](../02-web-iq/README.md)의 Web IQ 키, [Part 3](../03-fabric-iq/README.md)의 Fabric 데이터와 사용자 접근 권한을 사용합니다. Work IQ의 인증·결제 설정은 필요하지 않습니다.

## 소요 시간

<!-- TODO: 저자가 Part 5를 완주해 소요 시간을 확인하고 duration_minutes와 본문에 반영합니다. -->

## 실습 단계

| 실행 자료 | 내용 |
|---|---|
| [Part 5 노트북](../../notebooks/part5-except-workiq-kb.ipynb) | 환경 변수 로드, Fabric 로그인, 네 지식 소스 구성, 단일 복합 질문과 통합 답변 |

노트북을 원래 위치에서 열고 셀을 위에서부터 실행합니다. Work IQ를 사용할 수 없어 Part 4를 건너뛴 경우에도 이 랩을 진행할 수 있습니다.

## 검증

HR 문서·건강 문서·Fabric·웹의 네 소스 결과와 인용을 확인합니다. Fabric의 `HAND TOOLS` 재고 집계 기준은 총 `stockLevel` 1,635입니다. Fabric이나 Web IQ 조회가 실패했는데 문서 답변만 표시되는 결과는 전체 성공으로 판단하지 않습니다.

## 정리 (Clean-up)

Part 6을 진행한다면 같은 배포를 유지합니다. 이 랩에서 마치는 경우에는 [배포 정리](../00-setup/README.md#정리-clean-up)를 수행합니다.

## 트러블슈팅

Fabric 조회 문제는 [Ontology 바인딩 안내](../00-setup/README.md#ontology-bindings), Web IQ 인증 문제는 [소스 인증 오류 안내](../00-setup/README.md#external-source-auth)를 확인합니다.

## 이전·다음

[워크샵 홈](../../README.md) · [이전: Part 4. Work IQ](../04-work-iq/README.md) · [다음: Part 6. 전체 IQ 통합](../06-all-iq/README.md)

Part 4를 건너뛰었다면 [Part 3](../03-fabric-iq/README.md)이 선행 랩입니다. Part 6을 진행하려면 먼저 Part 4의 Work IQ 설정과 메일 준비를 마치세요.
