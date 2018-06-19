---
title: Administrative Privileges From A Remote Location
layout: post
permalink: /blog/:year-:month-:day-:title.html
---

1) Go to the text file /etc/cups/cupsd.conf
2) Scroll down the file and put under the <Location/ admin> section:



 <Location /admin>
 Order deny,allow
 Encryption IfRequested
 Satisfy All
 AuthType Basic
 AuthClass System
 Deny All
 Allow 127.0.0.1
 </Location>


 <Location /admin>
 Order deny,allow
 Encryption IfRequested
 Satisfy All
 AuthType Basic
 AuthClass System
 Deny All
 Allow 127.0.0.1
 Allow 192.168.10.1
 </Location>