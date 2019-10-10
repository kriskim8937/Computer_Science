## Oracle
- Introduction
  - 데이터 베이스
  - 관계형 데이터 베이스 관리 시스템 (RDBMS)
  - sql 개요
- 데이터 검색
- 데이터 검색2
- 테이블 생성 및 데이터 입력, 수정 삭제
- Object
- 고급 SQL
- PL/SQL
## JDBC
- JDBC 기본 API
- Tomcat 설치
- 팀별 실습 (기본 api)활용 


## Oracle
### introduction / 데이터 베이스 및 RDBMS의 기본 개념 파악, SQL 기본 명령어
#### 데이터 베이스
- 데이터 베이스란 Intefrated data, Stored data, Operational data, Shared data 4가지 의미
- 데이터 베이스는 Real-time accessibility, Countinous evolution, Concurrent sharing, Content reference 해야한다.
- 데이터 베이스 구성요소 3가지
  - Entity - 학생
  - Attribute  - 학번, 이름 ,학년, 성적 등 
  - Relationship : 개체 간, 개체와 속성간의 관계
### RDBMS
- 데이터베이스 관리 시스템은 파일 시스템이 갖는 단저임 '데이터의 종속성 및 중복성' 문제를 해결하기 위해 제안된 

## select 실행순서 FWGHSO
1. FROM 절에서 테이블의 목록을 가져옴
2. WHERE 절에서 검색 조건에 불일치 하는 행 제외
3. GROUP BY 절에서 명시된 행의 값을 그룹화
4. HAVING 절이 GROUP BY 절의 결과 행 중 검색 조건에 불일치 하는 행 제외
5. SELECT 절에서 명시된 열을 정리 
6. ORDER BY 절에서 열을 기준으로 출력할 대상을 정렬 후 출력

## select 작성순서 SFWGHO
1. SELECT
2. FROM
3. WHERE 
4. GROUP BY
5. HAVING
6. ORDER BY
## SQL 명령어 종류
- 정보처리기사, 기업 필기 시험 
### DML 
- 새로운 행을 입력하거나, 기존의 행을 수정하거나 원치 않는 데이터를 삭제 하는 등 데이터 조작에 관한 명령어
- INSERT
- UPDATE
- DELETE
- MERGE
### DDL
- 구조를 만든다거나, 구조변경, 삭제 등 데이터 구조에 관한 명령어
- CREATE
- ALTER
- DROP
- RENAME
- TRUNCATE
- COMMENT
### TCL
- 논리적인 작업의 단위로 DML에 의해 조작된 결과를 다루는 명령어
- COMMIT
- ROLLBACK
- SAVEPOINT
### DCL
- 데이터 베이스에 접근하고 객체들은 사용하도록 권한을 주고 받는 명령어
- GRANT
- REVOKE 
