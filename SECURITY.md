# Security Policy

## Reporting Security Vulnerabilities

The Xygeni team takes security vulnerabilities seriously. We appreciate your efforts to responsibly disclose your findings and will make every effort to acknowledge your contributions.

### Preferred Method: Private Vulnerability Reporting

To report a security vulnerability affecting any Xygeni product or tool, please use GitHub's **Private Vulnerability Reporting** feature:

1. Navigate to the [**Security**](https://github.com/xygeni/xygeni/security) tab of this repository
2. Click on **"Report a vulnerability"**
3. Fill in the advisory details form with as much information as possible:
   - **Title**: A clear, concise description of the vulnerability
   - **Description**: Detailed information about the vulnerability
   - **Affected products/versions**: Which Xygeni tools or products are affected
   - **Severity**: Your assessment of the vulnerability's impact

You may add in the description additional sections, such as **Proof of Concept** with the steps to reproduce or demonstrate the vulnerability,
and even **Proposed fix or mitigation** if you have suggestions.

This creates a private security advisory that only the Xygeni security team can see, allowing for coordinated disclosure.

### Alternative Method: Email Reporting

If you prefer not to use GitHub's private reporting feature, or if you need to report a security incident rather than a vulnerability, you can email us directly at:

**security@xygeni.io**

When reporting via email, please include:

- A clear description of the vulnerability or incident
- The affected product(s) and version(s)
- Steps to reproduce the issue
- Any proof-of-concept code or evidence, such as IoCs
- Your contact information for follow-up
- Whether you would like to be credited for the discovery

Please use this email for:
- Security vulnerabilities in any Xygeni product
- Security incidents requiring immediate attention
- Sensitive security matters that require confidential communication

## What to Expect

After you submit a vulnerability report:

1. **Initial Response**: The Xygeni security team will acknowledge receipt of your report within **3 business days**
2. **Assessment**: We will investigate and validate the reported vulnerability
3. **Updates**: We will keep you informed of our progress toward a fix and full disclosure
4. **Resolution**: Once fixed, we will work with you on coordinated public disclosure
5. **Credit**: With your permission, we will credit you for the responsible disclosure

## Scope

This security policy covers vulnerabilities in:

- All Xygeni product tools and services
- Xygeni-maintained repositories (both public and private)
- Xygeni infrastructure that may affect product security
- Third-party dependencies bundled with Xygeni products

### Out of Scope

Please do **not** report:
- Security vulnerabilities in third-party libraries (report these to the library maintainers directly)
- Social engineering attacks
- Physical security issues
- Issues affecting only outdated/unsupported versions

## Security Best Practices for Xygeni Products

When using Xygeni products, we recommend:

- Always use the latest stable version
- Follow the principle of least privilege for access controls, such as api tokens
- Regularly review and rotate credentials
- Enable all available security features
- Monitor security advisories for updates
- Implement defense-in-depth security measures

## Disclosure Policy

- **Coordinated Disclosure**: We believe in coordinated vulnerability disclosure and will work with you to understand and fix the issue before public disclosure
- **Timeline**: We aim to resolve critical vulnerabilities within **90 days** of initial report
- **Public Disclosure**: After a fix is available, we will publish a security advisory crediting the reporter (unless you prefer to remain anonymous)
- **Embargo Period**: We request a reasonable embargo period to develop, test, and deploy fixes before public disclosure

## Security Advisories

Published security advisories for Xygeni products can be found in:
- The **Security** tab of this repository under **Advisories**
- Our security mailing list (contact security@xygeni.io to subscribe)
- Release notes for security patches

## Recognition and Rewards

<!-- Information about our bug bounty program (if applicable) can be found at [link to program details] or by contacting security@xygeni.io. -->
While we do not currently operate a formal bug bounty program, we deeply value the contributions of security researchers. 
We offer the following recognition and rewards for valid security vulnerability reports:

**Public Recognition**:
* Security Advisories: Credit in our published security advisories (with your permission)
<!-- * Hall of Fame: Recognition on our Security Researchers Hall of Fame page -->
* Social Media: Public acknowledgment on our official channels (Twitter, LinkedIn, blog)
* CVE Credit: Named credit in CVE entries for vulnerabilities you discover

**Severity-Based Recognition**:
The level of recognition and potential compensation depends on the vulnerability severity:

| Severity | Impact | Typical Recognition |
|----------|--------|---------------------|
| **Critical** | Complete system compromise, data breach, authentication bypass | Premium swag, prominent credit in advisories |
| **High** | Significant security impact, privilege escalation, data exposure | Swag package, extended product access, credit in advisories |
| **Medium** | Moderate security impact, limited data exposure | Standard swag, product access, public credit |
| **Low** | Minor security impact, low exploitability | Public credit, acknowledgment in release notes |

To discuss potential compensation for a specific finding, please contact security@xygeni.io after submitting your initial report.


## Contact

For any questions about this security policy or the responsible disclosure process:

- **Email**: security@xygeni.io
- **GitHub**: Use the "Report a vulnerability" feature in this repository's Security tab

Thank you for helping keep Xygeni and our users safe!
