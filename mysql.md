# MySQL

## Enabling Long Query Log on Windows
1. Edit de file my.ini (usually on <mysql instalation folder>/bin)
2. Add the following lines  

<pre>
slow_query_log = 1
long_query_time = <time limit for the query to be logged>
slow-query-log-file=<path to the file log, use / instead of \>
</pre>

Example:

<pre>
``slow_query_log = 1``
``long_query_time = 2``
``slow-query-log-file=c:/mysql/logs/longquery.log``
</pre>
