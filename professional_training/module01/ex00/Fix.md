# Vulnerability Remediation

## Root Cause
The vulnerability exists because user input is concatenated directly into the `render_template_string()` function, causing the Jinja2 engine to evaluate it as executable code rather than plain text.

## Secure Implementation
To fix this vulnerability, the application should separate the template structure from the user data:

1. **Use `render_template`:** Replace `render_template_string` with `render_template` to load static, predefined HTML files.
2. **Pass Context Variables:** Pass user input as parameters (variables) to the template. Jinja2 automatically escapes variables, neutralizing any malicious template syntax.

**Example:**
```python
# Insecure (Vulnerable to SSTI)
# return render_template_string("Hello " + request.args.get('name'))

# Secure (Mitigated)
# return render_template("index.html", name=request.args.get('name'))
