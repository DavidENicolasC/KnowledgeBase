_What does it protect against?_

Depending on the permissions and capabilities it is able to:

- Minimize impact of frontend compromise
- Prevent or reduce (accidential) exposure of local system interfaces and data
- Prevent or reduce possible privilege escalation from frontend to backend/system

_What does it **not** protect against?_

- Malicious or insecure Rust code
- Too lax scopes and configuration
- Incorrect scope checks in the command implementation
- Intentional bypasses from Rust code
- Basically anything which was written in the rust core of an application
- 0-days or unpatched 1-days in the system WebView
- Supply chain attacks or otherwise compromised developer systems