---
title: 03. Fabric IQ 구조화 데이터 연결
duration_minutes:
last_updated: 2026-10-21
---

# 03. Fabric IQ 구조화 데이터 연결

## 개요와 학습 목표

Zava DIY의 제품·재고 데이터를 사내 정책 문서와 함께 조회합니다. Fabric IQ의 온톨로지 지식 소스로 구조화된 운영 데이터를 연결합니다.

- Fabric 온톨로지를 지식 소스로 추가합니다.
- HR 문서·건강 문서·Fabric의 3개 소스로 지식 베이스를 구성합니다.
- 재고 현황과 예산 에스컬레이션 정책의 근거를 함께 확인합니다.

## 사전 요구사항

[환경 배포](../00-setup/README.md)에서 Fabric 용량·워크스페이스·Lakehouse·Ontology 구성을 마쳐야 합니다. [Part 1](../01-foundry-iq/README.md)의 검색 인덱스와 환경 설정을 재사용합니다. Fabric 데이터에 접근할 수 있는 사용자로 노트북의 로그인 절차를 진행합니다.

## 소요 시간

<!-- TODO: 저자가 Part 3을 완주해 소요 시간을 확인하고 duration_minutes와 본문에 반영합니다. -->

## 실습 단계

| 실행 자료 | 내용 |
|---|---|
| [Part 3 노트북](../../notebooks/part3-fabric-iq-to-kb.ipynb) | 환경 변수 로드, Fabric 로그인, 온톨로지와 인덱스 소스 구성, 재고·정책 복합 질문 |

노트북을 원래 위치에서 열고 셀을 위에서부터 실행합니다. 활동 로그와 소스 헌트에서 구조화된 데이터 조회와 문서 검색을 구분해 확인합니다.

## 검증

Fabric 참조와 오류 없는 `fabricOntology` 활동이 있어야 합니다. 워크샵 데이터의 `HAND TOOLS` 재고 집계 기준은 총 `stockLevel` 1,635입니다. HR 문서 검색이나 답변 합성만 성공하고 Fabric 조회가 실패한 결과는 성공으로 판단하지 않습니다.

## 정리 (Clean-up)

Part 5와 Part 6에서 같은 Fabric 데이터를 사용합니다. 랩 사이에는 배포를 삭제하지 않고, 전체 실습 후 [배포 정리](../00-setup/README.md#정리-clean-up)를 수행합니다.

## 트러블슈팅

Ontology는 있지만 데이터 원본이 없다는 오류가 발생하면 [기존 바인딩 검증 및 복구](../00-setup/README.md#ontology-bindings)를 따르세요. 기존 Ontology ID를 유지하는 복구와 실제 데이터 조회 검증은 서로 다른 단계입니다.

## 이전·다음

[워크샵 홈](../../README.md) · [이전: Part 2. Web IQ](../02-web-iq/README.md) · [다음: Part 4. Work IQ](../04-work-iq/README.md)

Work IQ를 준비하지 않았다면 [Part 5](../05-combined-iq/README.md)로 진행할 수 있습니다.
