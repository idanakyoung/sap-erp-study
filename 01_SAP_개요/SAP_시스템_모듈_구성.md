# 🛠️ 2. SAP 시스템 모듈 구성

---

## a. R/3 모듈

| 🚩 모듈 (Module)    | 설명 (Description)                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------|
| **FI**              | Financial Accounting (재무회계) – 회계전표, 자금관리, 계정결산                                           |
| **CO**              | Controlling (관리회계) – 원가센터·이익센터 회계, 예산관리                                               |
| **SD**              | Sales & Distribution (영업·출하) – 수주, ATP, 배송, 대금청구                                           |
| **MM**              | Materials Management (자재관리) – 구매, 재고관리, 물류                                                 |
| **PP**              | Production Planning (생산계획) – MRP, 제조오더, 자원계획                                               |
| **QM**              | Quality Management (품질관리) – 검사계획, 검사실적                                                    |
| **PM**              | Plant Maintenance (설비관리) – 설비점검, 보전계획                                                     |
| **PS**              | Project System (프로젝트관리) – WBS, 예산·실적 관리                                                   |
| **TR**              | Treasury (중앙자금관리) – 현금·증권·환위험 관리                                                       |
| **RE**              | Real Estate Management (부동산) – 자산·임대 관리                                                     |
| **EC**              | Enterprise Controlling (연결회계) – 그룹 결산, 내부거래 조정                                          |
| **IM**              | Investment Management (투자관리) – 예산·펀드·프로그램 관리                                           |

---

## 🧩 b. ECC 모듈 확장 구성

| 📦 영역 (Area)      | 모듈 (Module)         | 설명 (Description)                                            |
|---------------------|-----------------------|---------------------------------------------------------------|
| **재무관리**        | FI / CO / FSCM        | FI: 재무회계 · CO: 관리회계 · FSCM: 금융공급망관리            |
| **리스크·준법**     | GRC / TRM             | GRC: 리스크·권한관리 · TRM: 자금·위험관리                     |
| **성과관리**        | EPM / BI / BW         | EPM: 성과관리 · BI/BW: 데이터웨어하우스·보고                  |
| **인사관리**        | HCM (HR)              | 인사·급여·타임관리                                            |
| **공급망관리**      | SCM / MM / PP         | SCM: 공급망관리 · MM: 자재관리 · PP: 생산계획                 |
| **영업관리**        | SD / LE / CRM         | SD: 영업·출하 · LE: 물류실행 · CRM: 고객관계관리              |
| **유지보수**        | PM / EHS / QM         | PM: 설비관리 · EHS: 환경·안전 · QM: 품질관리                |
| **프로젝트**        | PS / PLM              | PS: 프로젝트관리 · PLM: 제품수명주기관리                    |
| **기술·기반**       | BASIS / XI / SOLMAN   | BASIS: 시스템관리 · XI: 통합플랫폼 · SOLMAN: 솔루션관리      |

---

## 🔗 c. SAP ERP 협업 관점 (Collaboration)

| 내부 프로세스 (Core)     | 사용 모듈          | 외부·협업 프로세스 (Cross-Functional)   | 대응 모듈                      |
|--------------------------|--------------------|------------------------------------------|--------------------------------|
| 인사 행정 & 급여         | HCM (HR)           | 온라인 채용 (채용 플랫폼 ↔ SAP)          | Recruiting, SuccessFactors     |
| 자재 계획 & 실행         | MM / PP            | 공급망 계획 (벤더 ↔ SAP)                 | SCM, Ariba                     |
| 재무 분석 & 관리         | FI / TR / CO       | 금융 파트너 협업 (은행·ERP ↔ SAP)        | FSCM, Treasury                 |
| 설계 변경 & 제품 개발    | PM / PS / QM       | 협업 개발 (PLM ↔ CAD/PLATFORM)           | PLM, SAP Innovation            |
| 주문 & 배송 실행        | SD / LE            | 고객 포털 연계 (e-Commerce ↔ SAP)        | SAP Commerce Cloud             |
| 마케팅 캠페인 관리       | CRM                | 캠페인 플랫폼 통합 (Marketo, Salesforce) | SAP Marketing Cloud            |

---

🔍 **Tip**:  
- 각 모듈 앞에 **아이콘**(예: 💰, 🚚 등)을 추가하면 시각적으로 한눈에 구분됩니다.  
- Notion이나 Confluence에도 **표** 그대로 붙여쓰면 편리합니다.  

