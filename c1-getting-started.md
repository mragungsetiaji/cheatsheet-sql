# Chapter 1: Pengenalan mengenai SQL

Napaktilas SQL dari dulu hingga sekarang:

|Version |Short Name| Standard| Release Date|
|---|----|---|---|
| 1986 |SQL-86 |ANSI X3.135-1986, ISO 9075:1987 |1986-01-01| 
| 1989 |SQL-89 |ANSI X3.135-1989, ISO/IEC 9075:1989 |1989-01-01| 
| 1992 |SQL-92 |ISO/IEC 9075:1992 |1992-01-01 |
| 1999 |SQL:1999 |ISO/IEC 9075:1999 |1999-12-16| 
| 2003 |SQL:2003 |ISO/IEC 9075:2003 |2003-12-15 |
| 2006 |SQL:2006 |ISO/IEC 9075:2006 |2006-06-01 |
| 2008 |SQL:2008 |ISO/IEC 9075:2008 |2008-07-15 |
| 2011 |SQL:2011 |ISO/IEC 9075:2011 |2011-12-15 |
| 2016 |SQL:2016 |ISO/IEC 9075:2016 |2016-12-01 |

## Sub Chapter 1.1: Sekilas tentang SQL
Structured Query Language atau SQL adalah bahasa programming khusus yang didesign untuk menanggani data dalam sebuah Relational Database Management System atau RDBMS. Bahasa seperti SQL bisa juga digunakan dalam Relational Data Stream Management Systems (RDSMS) atau di database "not-only SQL" (NoSQL).

SQL terbagi menjadi 3 sub-bahasa:
1. `Data Deﬁnition Language` atau DDL digunakan untuk membuat dan memodifikasi struktur dari database.
2. `Data Manipulation Language` atau DML digunakan untuk melakukan operasi Read, Insert, Update dan Delete pada data dalam database. 
3. `Data Control Language` atau DCL digunakan untuk mengontrol access dari data yang ada dalam database.

### SQL menurut Wikipedia
Core dari operasi DML adalah Create, Read, Update dan Delete (CRUD for short) yang dilakukan dengan menggunakan query INSERT, SELECT, UPDATE dan DELETE. Aada juga query MERGE yaitu melakukan ketiga operasi tersebut (INSERT, UPDATE, DELETE). https://en.wikipedia.org/wiki/SQL

### CRUD menurut Wikipedia
Banyak dari database SQL diimplementasikan sebagai client/server systems, istilah "SQL Server" mendeskripsikan sebuah database. Di waktu yang sama, Microsoft membuat database yang dikasih nama "SQL Server" yang menggunakan *logat* tersendiri dari SQL. https://en.wikipedia.org/wiki/Create,_read,_update_and_delete

# Chapter 2: Identiﬁer
Topic ini membahas tentang identifiers, seperti syntax untuk penamaan dari tables, columns, dan object database yang lain. Biar cocok dalam penggunaanya, untuk contoh penerapan akan diusahakan mengcover semua variasi yang digunakan oleh implementasi SQL yang berbeda.

## Sub Chapter 2.1: Unquoted identiﬁers
Unquoted identiﬁers bisa menggunakan huruf (a-z), angka (0-9), dan underscore (_), dan harus diawali dengan huruf.

Berdasarkan jenis dari implementasi SQL, dan/atau pengaturan databasenya, karakter yang lain mungkin aja diijinin, beberapa bahkan menjadi karakter pertama seperti:

- **MS SQL**: @, $, #, dan unicode yang lainnya
    https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-identifiers?view=sql-server-2017
- **MySQL**: $ 
    https://dev.mysql.com/doc/refman/5.7/en/identifiers.html
- **Oracle**: $, #, dan karakter lain
    https://docs.oracle.com/database/121/SQLRF/sql_elements008.htm#SQLRF00223
- **PostgreSQL**: $, dan lain-lain
    https://www.postgresql.org/docs/current/static/sql-syntax-lexical.html


Unquoted identiﬁers itu case-insensitive. Bagaimanapun juga aturan lebih lanjut berdasarkan pada masing-masing Implementasi SQL:
- **MS SQL**: Case-preserving, sensitivity didefinisikan dengan character set databasenya, jadi bisa case-sensitive.
- **MySQL**: Case-preserving, sensitivity tergantung pada pengaturan database dan file systemnya.
- **Oracle**: dikonversi ke uppercase, kemudian dihandle seperti quoted identiﬁer.
- **PostgreSQL**: dikonversi ke lowercase, kemudian dihandle seperti quoted identiﬁer.
- **SQLite**: Case-preserving; case insensitivity hanya jika untuk karakter ASCII. 

# Chapter 3: Data Types 
## Sub Chapter 3.1: DECIMAL dan NUMERIC
DECIMAL dan NUMERIC adalah fungsi yang ekuivalen.

Syntax:
```sql
DECIMAL ( precision [ , scale] ) 
NUMERIC ( precision [ , scale] )
```
Contoh:
```sql
SELECT CAST(123 AS DECIMAL(5,2)) --returns 123.00 
SELECT CAST(12345.12 AS NUMERIC(10,5)) --returns 12345.12000 
```

## Sub Chapter 3.2: FLOAT dan REAL
Data type pada data numeric sebagai floating point.

```sql
SELECT CAST( PI() AS FLOAT) --returns 3.14159265358979 
SELECT CAST( PI() AS REAL) --returns 3.141593
```

## Sub Chapter 3.3: Integers
Data type number menggunakan data integer.

|Data type |Range| Storage|
|---|---|---|
|bigint| -2^63 (-9,223,372,036,854,775,808) to 2^63-1 (9,223,372,036,854,775,807)| 8 Bytes |
|int| -2^31 (-2,147,483,648) to 2^31-1 (2,147,483,647) |4 Bytes|
|smallint| -2^15 (-32,768) to 2^15-1 (32,767)| 2 Bytes 
|tinyint| 0 to 255| 1 Bytes|

## Sub Chapter 3.4: MONEY dan SMALLMONEY
Data types tersebut merepresentasikan currency values.

|Data type |Range |Storage|
|---|---|---|
|money |-922,337,203,685,477.5808 to 922,337,203,685,477.5807| 8 bytes|
|smallmoney| -214,748.3648 to 214,748.3647 |4 bytes|  

## Sub Chapter 3.5: BINARY dan VARBINARY
Data types Binary merupakan fixed length.

Syntax:
```sql
BINARY [ ( n_bytes ) ] 
VARBINARY [ ( n_bytes | max ) ]
```
n_bytes bisa jadi sembarang angka dari 1 to 8000 bytes. 
max mengindikasikan bahwa maximum storage space adalah 2^31-1.

Contoh:
```sql
SELECT CAST(12345 AS BINARY(10)) -- 0x00000000000000003039 
SELECT CAST(12345 AS VARBINARY(10)) -- 0x00003039 
```

## Sub Chapter 3.6: CHAR dan VARCHAR
String data types of either ﬁxed length or variable length.

Syntax:
```sql
CHAR [ ( n_chars ) ] VARCHAR [ ( n_chars ) ]
```

Contoh:
```sql
SELECT CAST('ABC' AS CHAR(10)) -- 'ABC       ' (padded with spaces on the right) 
SELECT CAST('ABC' AS VARCHAR(10)) -- 'ABC' (no padding due to variable character) 
SELECT CAST('ABCDEFGHIJKLMNOPQRSTUVWXYZ' AS CHAR(10))  -- 'ABCDEFGHIJ' (truncated to 10 characters)