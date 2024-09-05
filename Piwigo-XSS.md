## In Piwigo v14.5.0, I found XSS Vulnerability in function Add Album </br>
Piwigo v14.5.0: [https://github.com/Piwigo/Piwigo] </br>

## Reproduce bug:</br>
Step 1: Login with admin account and go to Add Album function.

![Alt text](test1.png)

Step 2: Add album with payload XSS in album name

![Alt text](test2.png)

Burp request add album
![Alt text](test3.png)

Step 3: Payload trigger
![Alt text](test4.png)

Payload trigger in dashboard
![Alt text](test5.png)

Burp request access to dashboard
![Alt text](test6.png)

