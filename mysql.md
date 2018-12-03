# MySQL

## Enabling Long Query Log on Windows
1. Edit the file my.ini (usually on <mysql instalation folder>/bin)
2. Add the following lines  

<pre>
slow_query_log = 1
long_query_time = &lt;time limit for the query to be logged\&gt;
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
