# Lab: DOM XSS in innerHTML sink using source location.search

*5/19/2026*

**Base URL:**
https://0a0500670386d205802821970042006f.web-security-academy.net/ 

**Vulnerable URL:**
https://0a0500670386d205802821970042006f.web-security-academy.net/ 

**Injected URL:**
https://0a2400ea03c77ef980bf037900820013.web-security-academy.net/?search=%3Cimg+src%3D%270%27+onerror%3D%27alert%28%29%27%3E 

**Note:**
``<img src='0' onerror='alert()'>``

The script above being entered into the search function allows the user to submit the alert() function in place of any javascript code they choose to send. The search bar in this lab blocks the typical ``<source> alert() </source>`` function using the location.search method in html. However, the script above searches for a nonexistent image, allowing the attacker to submit an onerror clause which contains javascript code. 