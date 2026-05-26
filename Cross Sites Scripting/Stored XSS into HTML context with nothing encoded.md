# Lab: Stored XSS into HTML context with nothing encoded

*5/14/2026*

**Base URL:**
https://0a7c00d0040e88ee80d10359002c005f.web-security-academy.net/ 

**Vulnerable URL:**
https://0a7c00d0040e88ee80d10359002c005f.web-security-academy.net/post?postId=6 

**Injected URL:**
https://0a7c00d0040e88ee80d10359002c005f.web-security-academy.net/post?postId=6 

**Note:**
``<script> alert(“Injected Successfully”) </script>``

There is no difference between the vulnerable and injected url in this, because stored XSS is done within a field of the website itself. In this case, the comments section had a vulnerability allowing any posted comment to contain javascript code that activates to anyone connecting to that webpage. This one is especially dangerous because it activates any time someone connects to the site because it is stored in the comments section, but on the victims browser. 