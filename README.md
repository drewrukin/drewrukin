# Andrew Rukin (Андрей Рукин)

**Security researcher · Open source contributor · LLM security review tooling**

I work across software security research, source code analysis, and open-source engineering. Alongside finding and helping resolve vulnerabilities, I develop practical tools and methodologies that make security review more systematic and reproducible.

Each record below credits my contribution as a finder or reporter. Credits may be shared with other researchers.

[Browse indexed credits on CIRCL Vulnerability-Lookup](https://cve.circl.lu/credits/?q=Rukin).

| Project | Advisory | Finding |
| :--- | :--- | :--- |
| **Ranger** | [CVE-2026-40920](https://www.cve.org/CVERecord?id=CVE-2026-40920) | Privilege escalation through URL parameters |
|  | [CVE-2026-42537](https://www.cve.org/CVERecord?id=CVE-2026-42537) | Code execution through JDBC URL injection |
|  | [CVE-2026-44416](https://www.cve.org/CVERecord?id=CVE-2026-44416) | Code execution through arbitrary class instantiation |
|  | [CVE-2026-55814](https://www.cve.org/CVERecord?id=CVE-2026-55814) | Unauthenticated access to plugin download APIs |
|  | [CVE-2026-65942](https://www.cve.org/CVERecord?id=CVE-2026-65942) | Missing TLS hostname verification |
|  | [CVE-2026-65948](https://www.cve.org/CVERecord?id=CVE-2026-65948) | Missing brute-force protection in UnixAuth |
|  | [CVE-2026-65945](https://www.cve.org/CVERecord?id=CVE-2026-65945) | Replayable JWT bearer tokens in logs |
| **Airflow** | [CVE-2026-49487](https://www.cve.org/CVERecord?id=CVE-2026-49487) | Task-instance API exposes deferred trigger secrets |
|  | [CVE-2026-49486](https://www.cve.org/CVERecord?id=CVE-2026-49486) | FTPS data channel lacks encryption |
|  | [CVE-2026-65017](https://www.cve.org/CVERecord?id=CVE-2026-65017) | Config API exposes a team's Celery broker secret |
|  | [CVE-2026-68076](https://www.cve.org/CVERecord?id=CVE-2026-68076) | Connection test API crosses team boundaries |
|  | [CVE-2026-86843](https://www.cve.org/CVERecord?id=CVE-2026-86843) | SQL injection in the Teradata provider example DAG |
| **HBase** | [CVE-2026-49326](https://www.cve.org/CVERecord?id=CVE-2026-49326) | Missing scanner ownership checks in the Thrift service |
| **Hive** | [CVE-2026-53561](https://www.cve.org/CVERecord?id=CVE-2026-53561) | Forged SAML bearer tokens allow user impersonation |
| **Impala** | [CVE-2026-56207](https://www.cve.org/CVERecord?id=CVE-2026-56207) | SAML authentication bypass through forged bearer tokens |
|  | [CVE-2026-57866](https://www.cve.org/CVERecord?id=CVE-2026-57866) | SSRF exposes credentials through the AI endpoint |
| **FreeIPA** | [CVE-2026-14612](https://www.cve.org/CVERecord?id=CVE-2026-14612) | Off-by-one buffer overflows during OAuth2 device authorization |
|  | [CVE-2026-19550](https://www.cve.org/CVERecord?id=CVE-2026-19550) | Insufficient authorization for privileged trust refresh operations |
| **389 Directory Server** | [CVE-2026-14969](https://www.cve.org/CVERecord?id=CVE-2026-14969) | Static initialization vector in attribute encryption |
|  | [CVE-2026-15041](https://www.cve.org/CVERecord?id=CVE-2026-15041) | Non-constant-time PBKDF2 password comparison |
|  | [CVE-2026-18651](https://www.cve.org/CVERecord?id=CVE-2026-18651) | Failed SASL bind retains access as a locked account |
|  | [CVE-2026-19404](https://www.cve.org/CVERecord?id=CVE-2026-19404) | Anonymous access to CleanAllRUV replication maintenance |
|  | [CVE-2026-19843](https://www.cve.org/CVERecord?id=CVE-2026-19843) | Command injection in the Cockpit LDAP editor |

**Additional published advisory:** [GHSA-h6wx-5586-3jg7](https://github.com/andreax79/airflow-code-editor/security/advisories/GHSA-h6wx-5586-3jg7) — authorization bypass in `airflow-code-editor` allows users with read-only DAG access to modify DAG files.

### Upstream contributions

I also contribute fixes and regression coverage directly to the projects I review.

| Project | Contribution | Status |
| :--- | :--- | :--- |
| Apache Airflow | [Keep sensitive edge worker workloads out of logs](https://github.com/apache/airflow/pull/68355) | Merged |
| Apache Hadoop / HDFS | [Mask delegation tokens in WebHDFS client logs](https://github.com/apache/hadoop/pull/8565) | Merged |
| 389 Directory Server | [Reject mismatched certificate names in dynamic certificate requests](https://github.com/389ds/389-ds-base/pull/7680) | Merged |
| 389 Directory Server | [Check password history for every value in a multi-password change](https://github.com/389ds/389-ds-base/pull/7888) | Merged |

### Tools & methodology

- **[LLM Code Security Review](https://github.com/drewrukin/llm-code-security-review)** — a methodology for reviewing source code security with an LLM.
- **[Security Review MCP Server](https://github.com/drewrukin/llm-code-security-review-mcp)** — an MCP server for running LLM source code security reviews.
- **[Dependency-Track MCP](https://github.com/drewrukin/dtrack-mcp)** — vulnerability triage tooling with alias deduplication, cross-project discovery, and triage carry-over between versions.

---

Interested in application security research, source code review, or practical LLM audit workflows? Explore the projects above and their public discussions.

<sub>Selected public work · Updated September 2026</sub>
