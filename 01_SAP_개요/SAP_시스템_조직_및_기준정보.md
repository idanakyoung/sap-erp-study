# 🏢 3. ERP 조직 및 기준정보

---

## 🏗️ a. 전사적 조직구조 (Organization Structure)

---

### 🔍 조직구조  
> **Definition:** 각 모듈들의 조직구조와 관련된 코드들의 총칭이며, **Client** 단위로 관리됩니다.  

---

### 🔗 Assignment  
> **Definition:** 특정 조직구조 관련 코드가 다른 코드와 **연결관계**를 갖도록 설정하는 것.  

---

### 🛠️ 조직구조 모델링 (Enterprise Modeling)  
> 회사의 실제 조직 구조를 SAP가 제공하는 표준 모델과 **매핑**하여,  
> - ✅ 업무 프로세스 설계  
> - ✅ 산출되는 **내/외부 정보** 종류 결정  
> - ✅ ERP 시스템 분산 방식 결정  

---

### 🏢 주요 조직 단위

- **Client (클라이언트)**  
  - ERP 시스템 내에서 **최상위 독립 조직**  
  - 고유의 데이터·기준정보를 보관하는 논리적 단위  

- **Company Code (회사코드)**  
  - **법인 단위** 회계 실체  
  - 외부 공표용 재무제표(대차대조표·손익계산서) 산출  

- **Plant (플랜트)**  
  - 제품·서비스의 **생산·조달·공급**이 이루어지는 물류 단위  
  - 재고·자재 요구량·생산조직 관리  
  - 본사, 지사, 물류센터, 영업법인 등 포함  
  - 하나의 영업영역이 다수의 플랜트에, 하나의 플랜트가 다수의 영업영역에 연결 가능  

- **Storage Location (저장창고)**  
  - 플랜트 내 **재고 관리** 단위 (창고·보관실 등)  
  - 재고관리·재고실사·자재입출고·자재이전 수행  

- **Shipping Point (출하지점)**  
  - **출하처리** 담당 조직 단위  
  - 물리적 장소 또는 가상 조직으로 설정  
  - 하나의 출하지점에서 여러 플랜트 출하 가능  

- **Transportation Planning Point (운송계획지점)**  
  - 선적 문서 **구성·운송 실행** 담당 조직 단위  

---

## 📦 b. 전사적 기준정보 (Master Data & Transaction)

### 📑 Master Data (기준정보)

> **Master Data**  
> 기업 비즈니스 프로세스를 진행함에 있어서 기본적으로 필요한 데이터로, 장기간 유지·보수해야 하는 데이터  
> 프로세스에 의해 변화하지 않으며, 기업 경영 전반에 걸친 관리활동을 지원  
> 동일 고객의 중복 관리를 배제하고, 신규 고객 등록 및 고객 변경을 전사적으로 통합 관리  
> 모든 프로세스(Transaction)의 기반(Base)이므로, **정확한 기준정보 관리**가 가장 중요  

| 📌 모듈 (Module) | 🔖 Master Data 객체                               | 설명                                                         |
|------------------|---------------------------------------------------|--------------------------------------------------------------|
| **SD**           | Customer Master                                   | 고객 정보 (주소, 결제조건, 그룹 등)                          |
|                  | Condition Master                                  | 가격·할인·세금·운임 조건                                     |
|                  | Material Master (Sales view)                      | 판매 관련 자재 정보                                         |
| **MM**           | Vendor Master                                     | 공급업체 정보 (납품조건, 지불조건 등)                         |
|                  | Source List / Purchasing Info Record              | 자재별 벤더 정보, Quota Arrangement                          |
|                  | Material Master (MM view)                         | 자재 기본·플랜트·저장소별 정보                              |
| **PP**           | Material Master (MRP view)                        | 자재 MRP 파라미터                                           |
|                  | Work Center                                       | 생산 설비·자원 정보                                         |
|                  | Routing / BOM / Product Group                     | 공정·BOM·제품군 정보                                        |
| **FI & CO**      | Chart of Accounts (CoA)                           | 계정 체계 정보                                               |
|                  | Cost Center / Profit Center                       | 비용·수익 센터 관리                                         |
|                  | Activity Type                                     | 활동 유형별 원가 배부                                       |
|                  | Internal Order                                    | 내부 주문별 원가 추적                                       |
| **QM**           | Inspection Plan                                   | 검사 계획                                                   |
|                  | Quality Info Record                               | 품질 결과 기록                                               |

> 💡 Master Data는 기업의 모든 프로세스 기반이므로 **정확한 관리**가 필수입니다.

---

### 🔄 Transaction (거래)

| 🔧 개념               | 설명                                                         |
|----------------------|--------------------------------------------------------------|
| **Transaction**      | 비즈니스 업무 단위. 여러 화면/프로그램으로 구성             |
| **Transactional Data** | 실제 거래 발생 시 생성되는 데이터                         |
| **Transaction Code** | SAP GUI 메뉴 또는 커맨드 필드에서 사용되는 단축 코드 (예: VA01, ME21N) |

---

✨ **Tip**  
- 조직구조: Client → Company Code → Plant → Storage Location 순  
- 물류 프로세스: Shipping Point·Transportation Planning Point 별도 관리  
- Master Data Governance(MDG)로 중앙 집중 관리 가능  

