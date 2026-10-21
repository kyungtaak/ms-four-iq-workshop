---
title: 04. Work IQ 업무 맥락 연결
duration_minutes:
last_updated: 2026-10-21
---

# 04. Work IQ 업무 맥락 연결

## 개요와 학습 목표

시애틀 매장의 재고 부족을 다룬 업무 메일과 사내 정책을 함께 조회합니다. 로그인한 사용자의 Microsoft 365 데이터에 접근하는 Work IQ 지식 소스를 추가합니다.

- 사용자 위임 인증으로 Work IQ를 연결합니다.
- HR 문서·건강 문서·Work IQ의 3개 소스로 지식 베이스를 구성합니다.
- 받은 편지함의 업무 맥락과 정책 문서의 근거를 함께 확인합니다.

## 사전 요구사항

[배포 가이드](../00-setup/README.md)의 Work IQ 결제 정책, 실습 사용자 포함, 테넌트 활성화, 연결 앱과 로그인 앱 등록을 마쳐야 합니다. [Part 1](../01-foundry-iq/README.md)의 검색 인덱스와 배포 환경도 사용합니다.

노트북 시작 준비에서 Search 관리 ID의 Federated Credential을 연결합니다. 사용자 로그인은 디바이스 코드 흐름을 사용하므로 로그인 앱의 `Allow public client flows`를 허용해야 합니다.

데모 메일 생성은 본인의 Microsoft 365 계정과 Microsoft Graph의 `User.Read`·`Mail.Send` 위임 권한을 사용합니다. 테넌트 정책에 따라 관리자 동의가 필요합니다.

## 소요 시간

<!-- TODO: 저자가 Part 4를 완주해 소요 시간을 확인하고 duration_minutes와 본문에 반영합니다. -->

## 실습 단계

| 실행 자료 | 내용 |
|---|---|
| [Part 4 노트북](../../notebooks/part4-work-iq-to-kb.ipynb) | Search 관리 ID 연결, 환경 변수 설정, 사용자 로그인, 본인 메일함에 데모 메일 준비, 업무·정책 복합 질문 |

노트북을 원래 위치에서 열고 셀을 위에서부터 실행합니다. Part 6은 여기서 준비한 연결 설정과 메일을 재사용합니다.

## 검증

조회 결과에 `workIQ` 참조가 있고 활동 로그에 Work IQ 소스 오류가 없는지 확인합니다. 받은 편지함의 재고 부족 메일과 HR 정책의 근거를 함께 대조하세요. 다른 소스의 답변만 있는 부분 응답은 성공으로 판단하지 않습니다.

데모 메일 전송을 건너뛰었다면 실제 받은 편지함의 자료로 조회를 확인하되, 메일 준비 단계까지 검증한 것으로 기록하지 않습니다.

## 정리 (Clean-up)

Part 6에서 같은 Work IQ 연결과 메일을 사용합니다. 전체 실습 후 [배포 정리](../00-setup/README.md#정리-clean-up)를 수행합니다.

<!-- TODO: 데모 메일, Entra 앱 등록과 Work IQ 결제 정책의 정리 책임·절차를 저자가 확인합니다. azd down의 정리 범위로 간주하지 않습니다. -->

## 트러블슈팅

결제 권한, 관리자 동의, 디바이스 코드 로그인, Federated Credential 오류는 [Work IQ 설정 안내](../00-setup/README.md#노트북-연결-및-검증)와 [소스 인증 오류 안내](../00-setup/README.md#external-source-auth)를 확인합니다. Azure 로그인 성공만으로 Work IQ 사용자 권한이 준비된 것은 아닙니다.

## 이전·다음

[워크샵 홈](../../README.md) · [이전: Part 3. Fabric IQ](../03-fabric-iq/README.md) · [다음: Part 5. 통합 검색](../05-combined-iq/README.md)

Work IQ 연결을 마쳤다면 [Part 6](../06-all-iq/README.md)으로 바로 진행할 수도 있습니다.
