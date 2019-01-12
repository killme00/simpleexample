# SQL SERVER 데이터베이스

## 메타 정보 조회
```
-- 데이터베이스 목록
select name from sys.databases;

-- 데이터베이스 선택
use sqlDB;

-- 테이블 목록
select name, id from sysobjects
where xtype = 'U'
;

-- 컬럼 목록
select TABLE_CATALOG, TABLE_SCHEMA, TABLE_NAME, COLUMN_NAME
from INFORMATION_SCHEMA.COLUMNS
where table_name = 'person';

-- 컬럼 상세
select
	OBJECT_SCHEMA_NAME(c.object_id) SchemeName
	,o.name as table_name
	,c.name as column_name
	,t.name as data_type
	,t.max_length as length_size
	,t.precision as Precision
from sys.columns c
inner join sys.objects o on o.object_id = c.object_id
left outer join sys.types t on t.user_type_id = c.user_type_id
where o.type = 'U'
	and o.name = 'person'
order by o.name, c.name;
```
