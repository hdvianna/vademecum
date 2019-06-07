# MySQL

## Enabling Long Query Log on Windows
1. Edit the file my.ini (usually on &lt;mysql instalation folder&gt;/bin)
2. Add the following lines  

<pre>
slow_query_log = 1
long_query_time = &lt;time limit in seconds for the query to be logged\&gt;
slow-query-log-file=&lt;path to the file log, use / instead of \&gt;
</pre>

Example:

<pre>
slow_query_log = 1
long_query_time = 2
slow-query-log-file=c:/mysql/logs/longquery.log
</pre>

## Showing Indices
Type `SHOW INDEXES FROM <table tame>;`

For example, `SHOW INDEXES FROM country;`

## Showing Table Structure
Type `SHOW CREATE TABLE <table tame>;`

For example, `SHOW CREATE TABLE country;`

## Safe export on Windows console

Type `mysqldump <database name> -h <host> -u <user> -r <file path> -p`

For example, `mysqldump blog -h mysql.blog.example.com -u ad_blog -r .\blog.dump.sql -p`

## Safe import on Windows console

On the MySQL console, first select the desired database. For example, `use blog;`

Then type `source <dump file path>;`. For example, `source blog.sql;`
