# 📄 **DataBase Modeling**

<p align="center">
    <img style="width: 90%" src="images/DATABASE.png" alt="DATABASE">
</p></br>

## **DataBase Modeling 프로세스**

1. 업무 프로세스 분석
2. 개념적 모델링 -> ERD 생성
3. 논리적 모델링
4. 물리적 모델링
   <br/><br/>

## **개념적 데이터베이스 모델링**

- **개체 (Entity)** : 사용자와 관계가 있는 주요 객체 (데이터로 관리)

  - 영속적으로 존재
  - 새로 식별이 가능한 데이터 요소를 가짐
  - Attibute(속성)을 가짐

- **속성 (Attribute)** : 저장할 필요가 있는 실체에 관한 정보

  - 개체의 성질, 분류, 수량, 상태, 특성 등을 나타내는 세부사항
  - 개체에 포함되는 속성의 개수는 10개 내외가 바람직
  - 최종 DB 모델링 단계를 통해 <u>**테이블의 컬럼**</u>으로 활용

- **관계 (Relationship)** : 두 Entity 간의 업무적인 연관성 또는 관련 사실
  <br/><br/>

### **키(key)**

- **식별자** : 한 개체(Entity) 내에서 인스턴스를 구분할 수 있는 단일 속성 또는 속성 그룹
- **후보 키 (Candidate Key)** : 개체 내에서 가각의 인스턴스를 구분할 수 있는 속성 (기본 키가 될 수 있음)
- **기본 키 (Primary Key)** : 개체에서 각 인스턴스를 유일하게 식별하는데 적합한 키
- **대체 키 (Alternate Key)** : 후보 키 중에서 기본 키로 선정되지 않은 키
- **복합 키 (Composite Key)** : 하나의 속성으로 기본 키가 될 수 없는 경우 여러 키를 묶어 식별자로 사용
- **대리 키 (Surrogate Key)** : 식별자가 너무 길거나 여러 개의 속성으로 구성되어 있는 경우 인위적으로 추가한 키
  <br/><br/>

### **차수**

- **1 : 1** -> 두 Entity의 레코드가 하나씩 대응
- **1 : N** -> 부모 Entity의 하나의 레코드가 자식 Entity의 여러 레코드에 대응
- **N : M** -> 양 Entity 간 여러 개의 레코드가 관계를 맺을 수 있음
  <br/><br/>

## **논리적 데이터베이스 모델링**

&nbsp;&nbsp;개념적 데이터베이스 모델링 단계에서 정의된 ER-Diagram을 Mapping Rule을 적용하여 관계형 데이터베이스 이론에 입각한 스키마(Schema)를 설계하는 단계와 이를 이용하여 정규화하는 단계로 구성
<br/><br/>

### **Mapping Rule**

- Entity -> Table
- Attribute -> Column
- 식별자 -> Primary Key
- 관계 -> 참조키 or 중계 Table
  <br/><br/>

### **정규화 (Normalization)**

&nbsp;&nbsp;관계형 데이터베이스 설계에서 <u>**중복을 최소화**</u>하게 데이터를 구조화하는 프로세스
<br/>

- 데이터베이스 변경시 이상현상 제거
- 데이터베이스 구조 확장시 재 디자인 최소화
- 사용자에게 데이터 모델을 더욱 의미있게 작성하도록 함
- 다양한 질의 지원
  <br/><br/>

### **제 1 정규화 (Atmoic Columns)**

<br/><br/>

### **제 2 정규화 (부분함수 종속 제거)**

<br/><br/>

### **제 3 정규화 (이행적 함수 종속 제거)**

<br/><br/>

## **물리적 데이터베이스 모델링**

&nbsp;&nbsp;논리적 데이터베이스 모델링 단계에서 얻어진 데이터베이스 스키마를 좀 더 효율적으로 구현하기 위한 작업으로 DBMS 특성에 맞게 실제 데이터베이스 내의 개체들을 정의하는 단계. 상황에 따라 역정규화 실행.
<br/><br/>

### **역정규화 (Denormalization)**

- 시스템 성능을 고려하여 기존 설계를 재구성하는 것
- 정규화에 위배되는 행위
- 테이블의 재구성
  <br/><br/>
