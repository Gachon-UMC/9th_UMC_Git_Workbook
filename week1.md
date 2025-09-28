# DB 조인과 관련 개념 정리

## 1. DB 조인이란?
- 두 개 이상의 테이블을 연결하여 하나의 테이블로 만드는 것  
- 배경: 테이블 두 개 이상을 참조해 검색해야 할 필요성  
- 테이블 분리 이유: 데이터 중복 최소화, 데이터 일관성 유지  

---

## 2. Join 종류들

- **Inner Join**  
  두 테이블에서 공통된 필드를 반환 (집합의 교집합)

- **Left Outer Join**  
  왼쪽 테이블의 모든 행을 포함하고, 오른쪽 테이블에서 일치하는 행만 반환  
  → 일치하지 않으면 오른쪽 컬럼은 `NULL`

- **Right Outer Join**  
  Left Outer Join의 반대.  
  오른쪽 테이블의 모든 행을 포함하고, 왼쪽 테이블에서 일치하는 행만 반환  
  → 일치하지 않으면 왼쪽 컬럼은 `NULL`

- **Full Outer Join**  
  Left Outer Join + Right Outer Join의 결과 (집합의 합집합)  
  → 일치하지 않으면 `NULL`로 채워짐  

---

## 3. Join vs SubQuery
- **Join**: 성능과 가독성 측면에서 우수  
- **SubQuery**: 특정 조건 기반 검색, 복잡한 조건 처리에 유리  
- 개인적인 결론: 대부분의 경우 **Join**이 직관적이고 효과적  

---

## 4. 트랜잭션(Transaction)이란?
- 데이터베이스 상태를 변화시키는 작업들의 **논리적 단위**  
- 트랜잭션은 **모두 성공(All) 또는 모두 실패(Nothing)** 해야 함  
- 실패 시 이전 상태로 복구됨  

### ACID 특징
1. **원자성(Atomicity)**: 전부 성공하거나 전부 실패  
2. **일관성(Consistency)**: 성공 시 데이터 일관성 유지  
3. **격리성(Isolation)**: 여러 트랜잭션은 서로 간섭하지 않음  
4. **영속성(Durability)**: 성공 시 결과는 영구적으로 보존  

---

## 5. Join에서 ON vs WHERE

- **ON**: 조인 시, 테이블을 연결할 행을 결정  
- **WHERE**: 조인 후 결과에서 조건을 걸어 필터링  

---

## 6. 페이징(Paging)

대량 데이터를 한 번에 가져오지 않고 일정 단위로 나누어 조회하는 기법  

```sql
-- OFFSET 기반 페이징
SELECT * FROM mission
ORDER BY mission_id DESC
LIMIT y OFFSET (x - 1) * y;

-- Cursor 기반 페이징
SELECT * FROM mission
WHERE 정렬 기준 > 마지막 페이지 마지막 데이터 값
ORDER BY 정렬 기준
LIMIT 페이지크기;

-- 커버링 인덱스 기반 페이징
SELECT * FROM review AS r
WHERE r.star < ? 
   OR (r.star = ? AND r.review_id < ?)  -- 예: 4 / 4 / 733
ORDER BY r.star DESC, r.review_id DESC
LIMIT 15;