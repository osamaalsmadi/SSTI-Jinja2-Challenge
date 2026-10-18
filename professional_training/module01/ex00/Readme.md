# Server-Side Template Injection (SSTI) Report

## Description
The web application is vulnerable to a Server-Side Template Injection (SSTI) flaw due to the insecure handling of user input within the Jinja2 template engine.

## Discovery
The vulnerability was identified by inputting a basic template expression `{{ 7*7 }}`. The server evaluated the expression and returned `49`, confirming the presence of SSTI.

## Exploitation
The flaw was successfully exploited to bypass the template sandbox and achieve Remote Code Execution (RCE). By accessing Python's underlying OS modules, it was possible to read sensitive system files, such as `/etc/passwd`.
