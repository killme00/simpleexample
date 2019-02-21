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

## SQL Server 통계

[SQL Server Statistics Basics](https://www.red-gate.com/simple-talk/sql/performance/sql-server-statistics-basics/)

### 통계 이름, 컬럼 조회
```
select s.stats_id StatsID,
  s.name StatsName,
  sc.stats_column_id StatsColID,
  c.name ColumnName
from sys.stats s
inner join sys.stats_columns sc
  on s.object_id = sc.object_id and s.stats_id = sc.stats_id
inner join sys.columns c
  on sc.object_id = c.object_id and sc.column_id = c.column_id
where object_name(s.object_id) = 'awsales'
order by s.stats_id, sc.column_id;
```

### 통계 정보
```
DBCC SHOW_STATISTICS (테이블명, 통계항목명);
```

### 실행계획 Query 조회
```
select
  decp.refcounts,
  decp.usecounts,
  decp.size_in_bytes,
  decp.cacheobjtype,
  decp.objtype,
  decp.plan_handle,
  t.text
from sys.dm_exec_cached_plans as decp
CROSS APPLY sys.dm_exec_sql_text(decp.plan_handle) t
WHERE t.text like 'SELECT soh.SalesOrderNumber,%';
```
## Powershell
### powershell에서 SQL Server Authentication 으로 접속

```
System.Reflection.Assembly]::LoadWithPartialName('Microsoft.SqlServer.SMO') | out-null 
$srv = new-object ('Microsoft.SqlServer.Management.Smo.Server') "168.154.244.53"  

# This sets the connection to mixed-mode authentication 
$srv.ConnectionContext.LoginSecure=$false; 

# This sets the login name 
$srv.ConnectionContext.set_Login("sas_admin"); 

# This sets the password 
$srv.ConnectionContext.set_Password("Passw0rd!")  ;

$srv.Databases | Select name

$db = New-Object("Microsoft.sqlServer.Management.Smo.Database") ($srv, "sas");
$ds = $db.ExecuteWithResults("select TOP 5 CUS_NM from CUSMST110");

$table = $ds.tables[0]

foreach ($item in $table) {
	Write-Output $item.CUS_NM
}
```

#### 참조
[Connect to SQL Server via Windows PowerShell with SQL Server authentication](https://www.mssqltips.com/sqlservertip/1947/connect-to-sql-server-via-windows-powershell-with-sql-server-authentication/)
