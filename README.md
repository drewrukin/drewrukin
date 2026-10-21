# Andrew Rukin (Андрей Рукин)

**Security researcher · Open source contributor · LLM security review tooling**

I work across software security research, source code analysis, and open-source engineering. Alongside finding and helping resolve vulnerabilities, I develop practical tools and methodologies that make security review more systematic and reproducible.

Each record below credits my contribution as a finder or reporter.

*Only disclosed vulnerabilities cleared for publication are included. The table describes how the affected versions behave; published issues have already been fixed. Never postpone updates. :0)*

| Project | Advisory | Finding |
| :--- | :--- | :--- |
| **Apache Ranger** | [CVE-2026-40920](https://www.cve.org/CVERecord?id=CVE-2026-40920) | **Any domain user can become the KMS Key Admin with a single URL parameter.** |
|  | [CVE-2026-42537](https://www.cve.org/CVERecord?id=CVE-2026-42537) | **A routine JDBC connection test gives any Ranger user a shell on the Ranger Admin server.** |
|  | [CVE-2026-44416](https://www.cve.org/CVERecord?id=CVE-2026-44416) | **A user-supplied Java class name turns configuration validation into code execution on Ranger Admin.** |
|  | [CVE-2026-55814](https://www.cve.org/CVERecord?id=CVE-2026-55814) | Plugin download APIs expose data without authentication |
|  | [CVE-2026-65942](https://www.cve.org/CVERecord?id=CVE-2026-65942) | Ranger clients accept TLS certificates issued for other hostnames |
|  | [CVE-2026-65948](https://www.cve.org/CVERecord?id=CVE-2026-65948) | UnixAuth allows unlimited password attempts |
|  | [CVE-2026-65945](https://www.cve.org/CVERecord?id=CVE-2026-65945) | Ranger writes replayable JWT bearer tokens to logs |
| **Apache Airflow** | [CVE-2026-49487](https://www.cve.org/CVERecord?id=CVE-2026-49487) | Task-instance API exposes deferred trigger secrets |
|  | [CVE-2026-49486](https://www.cve.org/CVERecord?id=CVE-2026-49486) | **Airflow protects the FTPS login with TLS, then sends the file itself without encryption.** |
|  | [CVE-2026-65017](https://www.cve.org/CVERecord?id=CVE-2026-65017) | Config API exposes a team's Celery broker secret |
|  | [CVE-2026-68076](https://www.cve.org/CVERecord?id=CVE-2026-68076) | One team can make Airflow log in to another team's service with that team's password. |
|  | [CVE-2026-86467](https://www.cve.org/CVERecord?id=CVE-2026-86467) | AWS SAML login CSRF logs users into an attacker's account. |
|  | [CVE-2026-86843](https://www.cve.org/CVERecord?id=CVE-2026-86843) | The Teradata provider example DAG allows SQL injection |
|  | [GHSA-h6wx…3jg7](https://github.com/andreax79/airflow-code-editor/security/advisories/GHSA-h6wx-5586-3jg7) | Airflow Code Editor lets a read-only viewer upload Python that Airflow executes. |
| **Apache Hive** | [CVE-2026-53561](https://www.cve.org/CVERecord?id=CVE-2026-53561) | **A forged token with any username is enough to open a real Hive session.** |
| **Apache HBase** | [CVE-2026-49326](https://www.cve.org/CVERecord?id=CVE-2026-49326) | The Thrift service lets one user take over another user's scanner |
| **Apache Impala** | [CVE-2026-56207](https://www.cve.org/CVERecord?id=CVE-2026-56207) | **Impala accepts the wrong signature and logs the attacker in as any chosen user.** |
|  | [CVE-2026-57866](https://www.cve.org/CVERecord?id=CVE-2026-57866) | **A single SQL query can send Impala's cluster-managed AI API key to an attacker-controlled server.** |
|  | [CVE-2026-93684](https://www.cve.org/CVERecord?id=CVE-2026-93684) | **A table alias turns a SQL query into stored XSS in another user's browser.** |
|  | [CVE-2026-90466](https://www.cve.org/CVERecord?id=CVE-2026-90466) | JAR path traversal executes code outside the trusted folder. |
|  | [CVE-2026-97720](https://www.cve.org/CVERecord?id=CVE-2026-97720) | **A JWT with any username and any non-empty signature gets full access to the Impala executor Web UI.** |
| **FreeIPA** | [CVE-2026-14612](https://www.cve.org/CVERecord?id=CVE-2026-14612) | Off-by-one errors overflow buffers during OAuth2 device authorization |
|  | [CVE-2026-19550](https://www.cve.org/CVERecord?id=CVE-2026-19550) | The trust refresh operation allows unauthorized LDAP writes |
| **389 Directory Server** | [CVE-2026-14969](https://www.cve.org/CVERecord?id=CVE-2026-14969) | Attribute encryption uses a static initialization vector |
|  | [CVE-2026-15041](https://www.cve.org/CVERecord?id=CVE-2026-15041) | PBKDF2 password verification uses a non-constant-time comparison |
|  | [CVE-2026-18651](https://www.cve.org/CVERecord?id=CVE-2026-18651) | A failed SASL bind keeps a locked account logged in |
|  | [CVE-2026-19404](https://www.cve.org/CVERecord?id=CVE-2026-19404) | Anonymous LDAP clients can start or stop CleanAllRUV maintenance |
|  | [CVE-2026-19843](https://www.cve.org/CVERecord?id=CVE-2026-19843) | **A crafted LDAP entry name becomes a root command when an administrator opens it.** |

### Selected upstream fixes

| Project | Fix |
| :--- | :--- |
| Apache Airflow | [Prevent GCS-to-SFTP path traversal without blocking valid `../` destinations](https://github.com/apache/airflow/pull/74186) |
|  | [Keep sensitive edge worker workloads out of logs](https://github.com/apache/airflow/pull/68355) |
| Apache Hadoop / HDFS | [Mask delegation tokens in WebHDFS client logs](https://github.com/apache/hadoop/pull/8565) |
| 389 Directory Server | [Reject mismatched certificate names in dynamic certificate requests](https://github.com/389ds/389-ds-base/pull/7680) |
|  | [Check password history for every value in a multi-password change](https://github.com/389ds/389-ds-base/pull/7888) |

### Tools & methodology

- **[LLM Code Security Review](https://github.com/drewrukin/llm-code-security-review)** — a methodology for reviewing source code security with an LLM.
- **[Security Review MCP Server](https://github.com/drewrukin/llm-code-security-review-mcp)** — an MCP server for running LLM source code security reviews.
- **[Dependency-Track MCP](https://github.com/drewrukin/dtrack-mcp)** — vulnerability triage tooling with alias deduplication, cross-project discovery, and triage carry-over between versions.

---

Interested in application security research, source code review, or practical LLM audit workflows? Explore the projects above and their public discussions.

<sub>Selected public work · Updated October 2026</sub>
