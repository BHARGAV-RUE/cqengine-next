# Security Policy

## Supported Versions

| Version | Supported          |
|---------|--------------------|
| 1.0.x   | ✅ Yes              |
| < 1.0   | ❌ No (pre-release) |

## Reporting a Vulnerability

If you discover a security vulnerability in this project, **please report it responsibly**. Do **not** open a public GitHub issue.

### How to Report

1. **GitHub Private Vulnerability Reporting (Preferred)**
   - Go to the [Security Advisories](https://github.com/MSaifAsif/cqengine-next/security/advisories) page
   - Click **"Report a vulnerability"**
   - Fill in the details and submit

2. **Email**
   - Send an email to **saifasifmirza@gmail.com**
   - Include `[SECURITY]` in the subject line
   - Provide as much detail as possible (see below)

### What to Include

When reporting a vulnerability, please include:

- **Description** of the vulnerability
- **Steps to reproduce** or a proof-of-concept
- **Affected version(s)**
- **Impact assessment** (what an attacker could do)
- **Suggested fix** (if you have one)

### What to Expect

- **Acknowledgment** within **48 hours** of your report
- **Initial assessment** within **7 days**
- We will work with you to understand and validate the issue
- A fix will be developed privately and released as a patch version
- You will be credited in the release notes (unless you prefer anonymity)

### Disclosure Policy

- Please allow us a reasonable amount of time to address the issue before public disclosure
- We aim to release a fix within **30 days** of a confirmed vulnerability
- We will coordinate with you on the disclosure timeline
- We follow [responsible disclosure](https://en.wikipedia.org/wiki/Responsible_disclosure) practices

## Security Best Practices for Users

When using CQEngine in your projects:

- **Keep dependencies updated** — Always use the latest patch version
- **Validate serialized data** — If using disk/off-heap persistence with `KryoSerializer`, be aware that deserialization of untrusted data can be dangerous
- **Restrict file permissions** — When using `DiskPersistence` or `SQLitePersistence`, ensure database files have appropriate filesystem permissions
- **Use parameterized queries** — When using the SQL/CQN string-based query parsers, avoid constructing queries from untrusted user input to prevent injection

## Dependency Monitoring

This project monitors dependencies for known CVEs. If a vulnerability is found in a transitive dependency, we will release a patch version with the updated dependency as soon as possible.

Current key dependencies and their security posture:

| Dependency         | Version   | CVE Status |
|--------------------|-----------|------------|
| sqlite-jdbc        | 3.45.0.0  | ✅ Clean    |
| kryo               | 5.0.0-RC1 | ✅ Clean    |
| javassist          | 3.30.2-GA | ✅ Clean    |
| antlr4-runtime     | 4.10.1    | ✅ Clean    |
| concurrent-trees   | 2.6.1     | ✅ Clean    |

*Last audited: March 2026*
