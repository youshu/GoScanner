GoScanner
=========

GO语言编写的TCP端口扫描器，本人的第一个GO程序。<br />
<br />
###使用命令：<br />
Scanner startIp [endIp] port thread<br />
<br />
###参数说明：<br />
startIp &nbsp;开始IP<br />
endIp &nbsp;结束IP,可选,不输入表示只扫描startIp<br />
port &nbsp;扫描端口,单个端口：3389；多个端口：1433,3389；连续端口：135-3389<br />
thread &nbsp;最大并发线程数,最高2048<br />
<br />
扫描结果保存在同目录下的 result.txt 中，每次启动都会清掉之前的内容。<br />
<br />
例子一:&nbsp;<br />
Scanner 58.96.172.22 58.96.172.220 80 512<br />
扫描58.96.172.22到58.96.172.220中的80端口，最大并发线程512。<br />
<br />
例子二：&nbsp;<br />
Scanner 58.96.172.22 58.96.172.220 21,5631 512<br />
扫描58.96.172.22到58.96.172.220中的21和5631端口，最大并发线程512。<br />
<br />
例子三：&nbsp;<br />
Scanner 58.96.172.22 58.96.172.220 1-520 512<br />
扫描58.96.172.22到58.96.172.220中的1到520端口，最大并发线程512。<br />
<br />
例子四：&nbsp;<br />
Scanner 58.96.172.22 1-520 512<br />
扫描58.96.172.22中的1到520端口，最大并发线程512。
