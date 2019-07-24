# StressTest-Mysql 壓力測試-Mysql


下載官方的mysql會自帶mysqlslap，建議使用mariadb
<pre>https://mariadb.org/download/</pre>
mysqlslap參數說明
<pre>https://mariadb.com/kb/en/library/mysqlslap/</pre>
### 使用mysqlslap Example
<pre><code>mysqlslap --user=帳號 --password=密碼 --host=127.0.0.1 --port 3306 --concurrency=50000 --iterations=1 --auto-generate-sql --auto-generate-sql-load-type=mixed --auto-generate-sql-add-autoincrement --engine=innodb --number-of-queries=50000
</code></pre>
### 參數說明
<pre>--concurrency=num:要模擬查詢運行的客戶端數。
--iterations=num:運行測試的次數。
--auto-generate-sql:在文件中未提供或通過命令選項提供時，會自動生成SQL語句。
--auto-generate-sql-load-type=name:指定測試負載類型。允許值為read（掃描表），write（插入表格），key（讀取主鍵），update（更新主鍵）或mixed（半插入，半掃描選擇）。默認值是混合的。
--auto-generate-sql-add-autoincrement:將AUTO_INCREMENT列添加到自動生成的表中。
--engine=name:用逗號分隔的存儲引擎列表，用於創建表。對每個引擎運行測試。
--number-of-queries=num:將每個客戶端限制為大約此數量的查詢。
</pre>
