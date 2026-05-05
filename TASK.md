# TASK.md

## 현재 상태

- GitHub 저장소: https://github.com/soleme/aribahelp
- 배포 URL: https://ariba-gamma.vercel.app
- 현재 브랜치: `main`
- 최신 커밋: `2790f7d Add search term highlighting`
- Vercel GitHub 연동: 완료
- `main` 푸시 시 Vercel 자동 배포 생성 확인
- 참고: 마지막 확인 시점에 최신 자동 배포 `https://ariba-q4q0imvl6-soleme-2061s-projects.vercel.app`는 `Queued` 상태였고, 이전 production 배포는 `Ready` 상태였다.

## 내일 우선순위

1. Vercel 최신 자동 배포 상태 확인
   - `npx vercel ls ariba`
   - `https://ariba-gamma.vercel.app/prototype/` 접속 확인

2. 한글 산출물 페이지 품질 보강
   - 6개 산출물 페이지의 설명을 더 실무형으로 확장
   - 각 페이지의 예외 상황을 SAP Ariba 업무 기준으로 보강
   - 단계별 흐름과 관련 용어가 정확히 맞는지 확인

3. 용어 데이터 검수 시작
   - 117개 용어 한글명 검수
   - 유사 용어 정리: `Goods Receipt`, `Receipt`, `Receiving`
   - `검수 필요 / 검수 완료` 상태 분류

4. SAP 공식 출처 정확성 검수
   - 각 용어의 `source_url`이 해당 용어와 직접 관련 있는지 확인
   - 임시로 SAP Ariba Glossary에 몰아둔 항목을 더 정확한 문서로 교체

5. 디자인 QA
   - 모바일 화면 확인
   - 긴 영문 용어 카드 줄바꿈 확인
   - 자동차 이미지가 SAP Ariba 도움말 사이트에 적합한지 판단
   - 필요하면 조달/공급망 이미지로 교체

## 남은 작업

### 산출물 페이지

- [ ] 한글 산출물 페이지 품질 보강

### 용어 데이터

- [ ] 현재 117개 용어 한글명 검수
- [ ] 용어별 SAP 공식 출처 정확성 검수
- [ ] 실무 예시 보강
- [ ] 중복/유사 용어 정리
- [ ] `검수 필요 / 검수 완료` 상태 실제 분류

### 디자인 QA

- [ ] BMW M 스타일이 현재 용도에 적합한지 디자인 톤 검토
- [ ] 자동차 이미지 대신 조달/공급망 이미지로 교체 여부 결정
- [ ] 모바일 화면 QA
- [ ] 긴 영문 용어 카드 줄바꿈 QA

### 운영 방식

- [ ] 정적 HTML + CSV 유지 여부 결정
- [ ] React/Svelte 등 앱 전환 여부 결정
- [ ] Google Sheets 같은 외부 데이터 소스 연동 여부 결정
- [ ] 사내 위키/Confluence/Notion 이전 여부 결정

### 문서화

- [ ] 용어 추가 규칙 문서화
- [ ] 한글 번역 원칙 문서화
- [ ] 공식 출처 업데이트 기준 문서화
- [ ] 변경 이력 관리 방식 정리

## 완료된 주요 작업

- [x] 프로젝트 README 작성
- [x] 용어집 기획안 작성
- [x] 초기 용어 데이터 117개 구축
- [x] 메인 용어집 프로토타입 작성
- [x] 목표 기반 탐색 기능 추가
- [x] 업무 흐름 요약 섹션 추가
- [x] 공식 SAP 참조 산출물 카드 추가
- [x] 외부 SAP 링크를 내부 한글 산출물 페이지로 전환
- [x] 한글 산출물 페이지 6개 생성
- [x] 각 산출물 페이지에 자체 다이어그램 추가
- [x] 산출물 페이지에 관련 용어 바로가기 추가
- [x] 관련 용어 클릭 시 메인 용어 상세로 이동 기능 추가
- [x] URL 공유 기능 추가: `?term=purchase-order`, `?goal=invoice-flow`
- [x] 검색어 하이라이트 기능 추가
- [x] 목표 선택 상태를 URL에 반영
- [x] 산출물 페이지에서 메인 용어집으로 돌아갈 때 관련 필터 자동 적용
- [x] Vercel 배포 프로젝트 생성
- [x] GitHub main 푸시 시 Vercel 자동 배포 연결
