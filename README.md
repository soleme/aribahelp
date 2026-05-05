# SAP Ariba Glossary

SAP Ariba 용어집을 만들기 위한 초기 작업 공간입니다.

목표는 단순한 영한 용어 목록이 아니라, SAP Ariba를 처음 접하는 사용자가 업무 흐름 안에서 용어를 이해할 수 있는 자료와 화면 구조를 만드는 것입니다.

## 현재 산출물

- `docs/glossary-product-plan.md`: 자료 출처, 정보 구조, 화면 구성, v1 범위 결정안
- `data/glossary-seed.csv`: v1 초안에 넣을 핵심 용어 후보 117개
- `prototype/index.html`: 검색/필터/상세 패널 중심의 정적 화면 프로토타입

현재 프로토타입은 검은 캔버스, 대문자 헤드라인, 1px 헤어라인, 각진 버튼/카드, 트리컬러 스트라이프, 풀블리드 이미지 밴드를 사용하는 BMW M 스타일 레퍼런스 기반의 시각 방향으로 구성되어 있습니다.

프로토타입에는 목표 기반 탐색 기능이 있습니다. 사용자는 `신규 사용자 온보딩`, `구매요청에서 발주까지`, `입고와 송장 대사 이해`, `공급업체 협업 준비`, `소싱과 계약 연결` 같은 목표를 선택해 관련 용어 묶음만 볼 수 있습니다.

업무 흐름 섹션에는 자체 요약 워크플로우와 SAP Help Portal의 공식 프로세스 문서 링크를 함께 제공합니다.

공식 SAP 문서 링크는 메인 화면에서 바로 외부 이동하지 않고, `prototype/artifacts/`의 한글 산출물 상세 페이지 하단 출처로 제공합니다.

## 프로토타입 실행

프로토타입은 CSV를 브라우저에서 불러오므로 로컬 서버로 여는 것이 안정적입니다.

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

그 다음 브라우저에서 `http://127.0.0.1:4173/prototype/`를 엽니다.

## v1 방향

- 대상 사용자: SAP Ariba 신규 사용자, 구매/정산 담당자, 공급업체 온보딩 담당자
- 범위: 공통, 소싱, 계약, 구매, 입고, 송장, 공급업체 네트워크
- 기준 출처: SAP Help Portal과 SAP Learning의 공식 문서
- 설명 방식: 공식 정의 요약 + 쉬운 설명 + 실무 예시 + 관련 용어

## 주요 공식 출처

- SAP Ariba Glossary: https://help.sap.com/docs/ariba/sap-ariba-glossary/sap-ariba-glossary
- SAP Business Network 개요: https://help.sap.com/docs/business-network-for-procurement/introduction-to-business-network/about-sap-business-network
- SAP Learning - SAP Business Network: https://learning.sap.com/products/intelligent-spend-management/business-network
