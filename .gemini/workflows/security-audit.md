---
name: security-audit
description: Run a mandatory security audit on the current implementation
---
1. Activate `security-analyst` to audit all auth, payment, and data handling code.
2. If vulnerabilities are found, activate `code-analyst` to plan remediation.
3. Do not proceed to deployment until `security-analyst` provides a ✅ verdict.
