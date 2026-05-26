# Lab: Reflected XSS into HTML context with nothing encoded

*5/14/2026*

**Base URL:**
https://0a0c0032044955ed803d1778001000f5.web-security-academy.net/ 

**Vulnerable URL:**
https://0a0c0032044955ed803d1778001000f5.web-security-academy.net/?search= 

**Injected URL:**
https://0a0c0032044955ed803d1778001000f5.web-security-academy.net/?search=%3Cscript%3Ealert(%22Insecure%22)%3C/script%3E 

**Note:**
``https://0a0c0032044955ed803d1778001000f5.web-security-academy.net/?search=<script>alert(“Insecure”)</script>`` 

Above is what the actual injected url looks like. The lab demonstrated a reflected cross site scripting attack, a way of injecting javascript code into a url that allows it to be performed upon connecting to that url. The code above just did an “alert(‘insecure’)” function, but in theory any javascript code can be put between those functions. The ``<script>`` at the beginning and ``</script>`` at the end identify the beginning and end of the code and force the html behind it to assume everything between that is javascript code that needs to be executed, the same way it does in the inspect element field. The limitation to this is that it needs to be done on the search function or onto another field, anything that sends a request that says something like ``page=`` or ``search=``.
