# SAP Ariba 용어집 기획안

## 1. 목적

SAP Ariba 용어집은 SAP Ariba와 SAP Business Network를 처음 접하는 사용자가 구매, 소싱, 계약, 송장, 공급업체 협업 업무에서 등장하는 용어를 빠르게 이해하도록 돕는 도구다.

핵심 방향은 다음과 같다.

- 공식 용어와 실무 표현을 함께 보여준다.
- 용어를 가나다순뿐 아니라 업무 흐름 기준으로도 찾을 수 있게 한다.
- 용어 상세에서 "어느 화면/업무 단계에서 나오는 말인지"를 설명한다.
- 출처를 명확히 남겨 나중에 정의가 바뀌었을 때 검수할 수 있게 한다.

## 2. 자료 수집 원칙

### 1차 출처

1차 출처는 SAP 공식 문서로 제한한다.

- SAP Ariba Glossary  
  https://help.sap.com/docs/ariba/sap-ariba-glossary/sap-ariba-glossary  
  공식 용어 정의의 기준 문서다. 검색 시점 기준 SAP Help Portal에 Version 2602로 노출된다.

- SAP Business Network for Procurement 문서  
  https://help.sap.com/docs/business-network-for-procurement/introduction-to-business-network/about-sap-business-network  
  구매자와 공급업체가 네트워크에서 협업하는 개념을 설명하는 기준 자료다.

- SAP Learning - SAP Business Network  
  https://learning.sap.com/products/intelligent-spend-management/business-network  
  초심자용 설명과 학습 경로를 정리할 때 사용한다.

- SAP Ariba Buying and Invoicing 문서  
  구매요청, 발주, 입고, 송장, 정산 흐름의 상세 용어를 확인할 때 사용한다.

- SAP Ariba Sourcing, Contracts 문서  
  이벤트, 입찰, 계약 워크스페이스, 계약 준수 관련 용어를 확인할 때 사용한다.

### 2차 출처

2차 출처는 공식 정의를 대체하지 않고 실무 표현을 보강하는 용도로만 사용한다.

- 내부 구매 프로세스 문서
- 사내 SAP Ariba 교육 자료
- 실제 화면 캡처와 메뉴명
- 현업이 쓰는 한글 표현
- 운영 이슈와 FAQ

## 3. v1 범위

v1은 "핵심 용어 50개"를 목표로 한다. 처음부터 SAP Ariba 전체 용어를 모두 다루지 않는다.

### 포함 영역

- 공통 / 시스템 개념
- SAP Business Network / 공급업체 협업
- Sourcing / 소싱
- Contracts / 계약
- Buying / 구매
- Receiving / 입고
- Invoicing / 송장
- Approval / 승인

### 제외 또는 후순위

- 고급 관리자 설정
- 통합 기술 상세
- API, cXML 전체 명세
- 국가별 세금 규칙
- 회사별 커스터마이징 명칭

## 4. 용어 데이터 구조

용어 하나는 다음 필드를 가진다.

| 필드 | 설명 |
| --- | --- |
| `id` | 내부 식별자 |
| `english_term` | 영문 공식 또는 일반 용어 |
| `korean_term` | 권장 한글 용어 |
| `abbreviation` | 약어 |
| `category` | 공통, 소싱, 계약, 구매, 송장 등 |
| `workflow_stage` | 업무 흐름 단계 |
| `plain_description` | 초심자용 쉬운 설명 |
| `business_example` | 실무 예시 |
| `related_terms` | 관련 용어 |
| `source_url` | 공식 또는 내부 출처 |
| `screen_hint` | 등장 가능성이 높은 화면/메뉴 |
| `level` | 기본, 실무, 고급 |
| `review_status` | 초안, 검수 필요, 검수 완료 |

## 5. 화면 구성

### 기본 레이아웃

화면은 세 영역으로 구성한다.

- 상단: 전체 검색, 보기 전환, 검수 상태 필터
- 좌측: 카테고리와 업무 흐름 필터
- 중앙: 용어 리스트
- 우측: 선택한 용어 상세

### 주요 화면

1. 용어 검색 화면
   - 검색창
   - 카테고리 필터
   - 업무 단계 필터
   - 난이도 필터
   - 용어 카드 목록

2. 용어 상세 화면
   - 영문명
   - 한글명
   - 약어
   - 쉬운 설명
   - 실무 예시
   - 관련 화면
   - 관련 용어
   - 공식 출처 링크
   - 검수 상태

3. 업무 흐름 화면
   - 소싱 -> 계약 -> 구매요청 -> 발주 -> 입고 -> 송장 -> 지급 순서로 용어를 배치
   - 신규 사용자가 프로세스를 따라가며 용어를 익히는 용도

4. 관리자 화면
   - 용어 추가/수정
   - 출처 관리
   - 검수 상태 변경
   - 내부 표현과 공식 표현의 매핑 관리

## 6. 설명 톤

공식 정의를 그대로 번역하기보다, 사용자가 바로 이해할 수 있는 설명을 우선한다. 단, 공식 정의와 충돌하면 공식 정의를 기준으로 수정한다.

예:

- 나쁜 설명: "구매요청은 구매 요청을 나타내는 문서다."
- 좋은 설명: "사용자가 물품이나 서비스를 구매하기 전에 내부 승인을 받기 위해 생성하는 문서다. 승인 후 발주로 이어질 수 있다."

## 7. 초기 작업 순서

1. 핵심 용어 50개 후보 작성
2. SAP 공식 출처 링크 연결
3. 쉬운 설명과 실무 예시 작성
4. 화면 프로토타입으로 검색/필터 구조 검증
5. 현업 용어 검수
6. 공식 정의 검수
7. 실제 앱 또는 문서 형태 결정

## 8. 결정된 기본 방향

- v1은 문서와 정적 프로토타입으로 시작한다.
- 용어 데이터는 CSV로 관리한다.
- 화면은 검색 중심으로 구성한다.
- 카테고리와 업무 흐름을 동시에 제공한다.
- SAP 공식 출처는 모든 용어에 연결하는 것을 원칙으로 한다.

## 9. 검수 기준

용어는 다음 기준을 통과해야 `검수 완료`로 바꾼다.

### 공식성

- `english_term`이 SAP 공식 문서 또는 제품 화면에서 확인되는 표현인지 확인한다.
- `source_url`이 SAP Help Portal, SAP Learning, SAP Community의 공식 문서 또는 내부 승인 자료인지 확인한다.
- SAP Ariba에서 SAP Business Network로 명칭이 바뀐 영역은 최신 명칭과 과거 명칭을 함께 확인한다.

### 한글 표현

- `korean_term`은 사내에서 실제로 쓰는 표현을 우선하되, 공식 번역과 충돌하면 비고나 설명으로 차이를 남긴다.
- 같은 개념에 대해 `구매요청`, `구매 요청`, `PR`처럼 여러 표현이 섞이지 않도록 대표 표현을 정한다.
- 약어는 `abbreviation`에만 넣고, 한글명에는 반복해서 넣지 않는다.

### 설명 품질

- `plain_description`은 초심자가 읽어도 업무상 의미를 이해할 수 있어야 한다.
- 설명 안에서 다른 어려운 용어를 쓸 경우 `related_terms`에 연결한다.
- 공식 정의를 그대로 번역하지 않고, 실제 업무 맥락을 설명한다.

### 실무 예시

- `business_example`은 한 문장으로 실제 사용 상황을 보여준다.
- 특정 회사의 비밀 정보, 내부 조직명, 공급업체명, 금액은 넣지 않는다.
- 구매요청, 발주, 입고, 송장처럼 흐름이 있는 용어는 앞뒤 단계가 드러나게 작성한다.

### 화면 힌트

- `screen_hint`는 정확한 메뉴명이 확정되지 않았으면 넓은 위치를 적는다.
- 회사별 커스터마이징 화면명은 내부 검수 후 별도 필드로 분리할 수 있다.

### 검수 상태

- `초안`: 용어 후보만 들어간 상태
- `검수 필요`: 설명과 출처가 있으나 공식/현업 검수가 끝나지 않은 상태
- `검수 완료`: 공식 출처, 한글 표현, 실무 예시, 관련 용어를 모두 확인한 상태

## 10. 다음 구현 후보

현재 프로토타입 이후의 구현 후보는 다음과 같다.

- CSV를 JSON으로 변환하는 빌드 스크립트
- 용어 추가/수정용 관리자 화면
- 검수 상태별 작업 목록
- 업무 흐름 다이어그램 보기
- 내부 화면 캡처와 용어 상세 연결
- Markdown/PDF 용어집 자동 생성

## 11. 공식 워크플로우 참조

프로토타입의 업무 흐름도는 아래 SAP 공식 문서를 기준으로 자체 요약한다. 공식 문서 안에는 SAP가 제공하는 프로세스 다이어그램 또는 예시 승인 흐름 그림이 포함된 항목이 있다.

| 영역 | 공식 참조 | 용도 |
| --- | --- | --- |
| 구매요청 워크플로우 | https://help.sap.com/docs/buying-invoicing/purchasing-guide-for-procurement-professionals/about-workflow-of-purchase-requisitions-8b3f5dbe7a7b4427a1039a46dfe475d3 | PR 생성, 승인, PO 생성, 입고, 지급 요청 흐름 |
| 발주 프로세스 | https://help.sap.com/docs/buying-invoicing/purchasing-guide-for-procurement-professionals/purchase-order-process-6b32ab8fc1da1014bbcef40b7787d981 | 승인된 PR이 PO로 생성되고 공급업체에 전달되는 흐름 |
| 소싱 이벤트 프로세스 | https://help.sap.com/docs/strategic-sourcing/event-management/sap-ariba-sourcing-event-process-7c23b02f71ea1014ac1cc01462d30873 | 이벤트 생성, 공급업체 응답, 평가, 선정 흐름 |
| Guided Buying 승인 흐름 | https://help.sap.com/docs/buying-invoicing/guided-buying-administration/approval-flows-in-guided-buying-f75adff652ab4a658d7173a2b7e39495 | 승인 규칙과 승인 흐름 예시 |
| 입고 기준 송장 검증 | https://help.sap.com/docs/buying-invoicing/invoicing-and-payment-process-guide/workflow-for-goods-receipt-based-invoice-verification-in-sap-ariba-buying-and-invoicing-aede7515ef3148f5a0f96e05d8670438 | 입고, 송장, IR 생성, 검증 흐름 |
| 주문 확인과 출하 통지 제어 키 | https://help.sap.com/docs/business-network-for-supply-chain/business-network-buyer-administration/order-confirmation-and-ship-notice-control-keys | 공급업체 주문 확인과 출하 통지 생성 제어 |

공식 그림은 저작권과 문서 버전 관리를 위해 프로토타입에 직접 복제하지 않는다. 화면에는 출처 카드와 자체 요약 다이어그램을 함께 제공한다.
