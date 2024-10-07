
<div align="center">
  <img src="img/xygeni.logo.png" alt="xygeni logo" width="250"></img><br/>
  <i>End to End Software Supply Chain Security</i>
</div>

---

[![documentation](https://img.shields.io/badge/documentation-blue.svg)](https://docs.xygeni.io/) 
[![api documentation](https://img.shields.io/badge/api-reference-blue.svg)](https://api.xygeni.io/swagger-ui.html) 
[![version](https://img.shields.io/badge/version-4.33-blue.svg)]() 
[![xygeni.io](https://img.shields.io/badge/website-blue.svg)](https://xygeni.io/)

## Overview

Enhance your **Application Security Posture Management (ASPM)** through comprehensive risk assessment, strategic prioritization, 
and protection against attacks and malware infection throughout your Software Supply Chain.

**Xygeni** is a platform for improving the Software Supply Chain Security posture for organizations.

The platform protects the integrity and security of your software ecosystem throughout the entire SDLC
by providing the following products:

- **[Application Security Posture Management (ASPM)](https://docs.xygeni.io/xygeni-products/application-security-posture-management-aspm)** unifies risk management from code to the cloud, providing real-time visibility, prioritization, and remediation. Security findings are contextualized to facilitate security and risk assessment, ensuring that your applications are protected from development to deployment.

- **[Code Security](https://docs.xygeni.io/xygeni-products/code-security-cs)**, to protect critical code against malicious or unintended changes done without following a strict change review process. Vulnerabilities and malware in code are detected and prioritized. 

- **[Open Source Security](https://docs.xygeni.io/xygeni-products/open-source-security-oss)** offers real-time monitoring of your dependencies to detect and mitigate threats before they impact your software. Both vulnerable and malicious dependencies are identified, qualified according to factors like reachability and exploitability, and prioritized for remediation.

- **[Software Supply Chain Security (SSCS)](https://docs.xygeni.io/xygeni-products/software-supply-chain-security-sscs)** protects your CI/CD pipelines by scanning configuration files, build scripts, and CI job definitions. The software infrastructure, including code repositories, package managers, CI/CD systems and component registries, is scanned for misconfigurations to prevent potential supply chain attacks. It also evaluates compliance with existing SSCS standards, to enforce robust security practices.

- **[Build Security](https://docs.xygeni.io/xygeni-products/build-security)** protects the integrity of your software artifacts and build/deploy pipelines. Create and publish attestations, signed documents about a software artifact that contain an authenticated statement about its provenance and other properties. Consumers of the artifact can then verify the origin of the artifact, its integrity, and whether it conforms with a predefined policy. This could prevent a malicious actor from modifying the artifact or the build/deploy process, and state certain properties about the artifact at build time (such as the absence of known critical vulnerabilities).

- **[Secrets Security](https://docs.xygeni.io/xygeni-products/secrets-security)** provides a robust defense against secrets leakage within the software development lifecycle. It scans, detects, and blocks the release of sensitive information such as passwords, API keys, and tokens in real time. It also provides optional validation that the secret is currently active, and automated / guided remediation (where possible) or detailed instructions on how to remove / revoke any hardcoded secrets found.

- **[iac security](https://docs.xygeni.io/xygeni-products/iac-security)** in provisioning IT/Cloud templates, for the main IaC frameworks and configuration management tools. Common security flaws are reported before the assets are deployed at runtime, with detailed remediation instructions.

- **[Anomaly Detection](https://docs.xygeni.io/xygeni-products/anomaly-detection)** provides an additional layer of security by continuously monitoring and analyzing activity within your SCM and CI/CD infrastructure to quickly identify and respond to unusual behavior. Xygeni detects anomalies that indicate unauthorized changes, access, or exploits in real time. This proactive approach ensures that potential security breaches are addressed before they can escalate into serious threats.

## The platform components

The platform is a cloud-based service, accessible via REST API, that keeps findings and metadata from different sources.

![Platform components](img/platform.png)

**Scanner**: Xygeni provides a command-line interface (CLI) for running the scanner. The scanner can either run analysis commands separately, like detecting hardcoded secrets or misconfigurations, or run all the analyses at once.

**Sensor**: For capturing _unusual activity_, a monitoring component (_Sensor_) can be installed on target systems (typically SCM or CI/CD tools) for monitoring the user actions and detecting activity that may evidence a bad practice, or even an ongoing attack. In addition, the sensor may capture access control data for detecting accounts with excessive privileges, or 'stale' accounts.

**Dashboard**: The Dashboard is the web user interface for showing the results of the scans. The dashboard provides a summary security posture and the breakdown of security issues at the global, group or project levels; plus trends exploration, reporting, and platform administration, among other facilities.

**API**: The REST API is the central element in the platform. All elements in the platform use the API as a backbone for reporting findings and receiving the processed information for integration into Xygeni tools, third-party plugins and integrations, or any custom integration for organizations.

**Integrations**: Xygeni provides ready-made integrations for running scans in CI/CD systems or uploading security issues, performing administrative operations, or exporting findings to communication and reporting tools.

**Malware Early Warning, MEW**: Activity on public registries is monitored by Xygeni so potential attacks could be detected early. Publishing new packages in popular public repositories is an example of an activity that is monitored by Xygeni. In addition, security advisories are ingressed for modelling new threats and malicious activity on the wild. Xygeni customers may receive alerts when a security issue may affect them.

## Installation

For operating with the Xygeni platform, you must have a valid user account linked to your organization at Xygeni.

> **NOTE**: Your organization must have a valid subscription with Xygeni Security. Please proceed to [how to subscribe to Xygeni](https://xygeni.io/book-a-demo) for further details.

Follow the instructions provided in the [Getting Started](https://docs.xygeni.io/getting-started) section of the documentation.

## Current checksums

* `install.sh` (install script for Linux/macOS): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.sh.sha256)
https://github.com/xygeni/xygeni/blob/ec353d61e560fb031a5983ba5d57cab843833152/checksum/latest/install.sh.sha256?plain=1#L1

* `install.ps1` (install script for Windows): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.ps1.sha256)
https://github.com/xygeni/xygeni/blob/036472c2e102272f82360446ab51f1e9dee876e8/checksum/latest/install.ps1.sha256?plain=1#L1

* `xygeni-release.zip` (scanner): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/xygeni-release.zip.sha256)
https://github.com/xygeni/xygeni/blob/a1d55afd724e0e92adfa16d29d4ec032523728a9/checksum/latest/xygeni-release.zip.sha256?plain=1#L1

* `salt.zip` (build attestations): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/salt.zip.sha256)
https://github.com/xygeni/xygeni/blob/a1d55afd724e0e92adfa16d29d4ec032523728a9/checksum/latest/salt.zip.sha256?plain=1#L1

So you may verify the integrity of a downloaded artifact. For example, for install scripts:

* Under Linux / macOS:
```
# Download the install script from downloads area
curl -sLO https://get.xygeni.io/latest/scanner/install.sh

# Check the scanner checksum published in xygeni GitHub repo (separate environment)
checksum="$(curl -s https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.sh.sha256)"
echo "$checksum install.sh" | sha256sum --check
```

* Under Windows (PowerShell):
```
# Download the install script (via Invoke-WebRequest)
iwr https://get.xygeni.io/latest/scanner/install.ps1 -useb -OutFile install.ps1

# Check the scanner checksum
(Get-FileHash '.\install.ps1' -Algorithm SHA256).Hash -eq `
  (iwr https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.ps1.sha256)
```

