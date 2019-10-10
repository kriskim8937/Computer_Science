```
spring.datasource.url=jdbc:mysql://localhost:3306/ssafyhrm?useUniCode=yes&characterEncoding=UTF-8&serverTimezone=Asia/Seoul
spring.datasource.username=ssafy
spring.datasource.password=ssafy

'chaelyn', 'CREATE DATABASE `chaelyn` 
/*!40100 DEFAULT CHARACTER SET utf8 */ /*!80016 DEFAULT ENCRYPTION=\'N\' */'

'books', 'CREATE TABLE `books`
 (\n  `isbn` varchar(50) NOT NULL,\n
   `title` varchar(100) NOT NULL,\n
     `author` varchar(50) NOT NULL,\n
       `publisher` varchar(50) NOT NULL,\n
         `price` int(8) NOT NULL,\n 
          `quantity` int(8) NOT NULL,\n
            PRIMARY KEY (`isbn`)\n) ENGINE=InnoDB DEFAULT CHARSET=utf8'

```
maven repository 


sql injection -> mssql -> Statement
id=safsdf&pass=asfsafas or 1=1

CallableStatement extends PrepareStatement extends Statement


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
