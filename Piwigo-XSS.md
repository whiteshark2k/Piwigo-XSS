## In Piwigo v14.5.0, I found XSS Vulnerability in function Add Album </br>
Piwigo v14.5.0: [https://github.com/Piwigo/Piwigo] </br>

## Reproduce bug:</br>
Step 1: Login with admin account and go to Album List Management function.</br>
Can access to URL: http://localhost:8088/piwigo/admin.php?page=cat_list
![Alt text](test1.png)

Step 2: Add album with payload XSS in album name

![Alt text](test2.png)

Burp request add album</br>
Manipulate Param: virtual_name=test%3Cscript%3Ealert%28%27XSS%27%29%3C%2Fscript%3E
![Alt text](test3.png)

Step 3: Payload trigger
![Alt text](test4.png)

Use webmaster account visit dashboard, payload trigger successful.
![Alt text](test5.png)

Burp request access to dashboard
![Alt text](test6.png)

