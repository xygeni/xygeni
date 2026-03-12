
<div align="center">
  <img src="img/xygeni.logo.text.png" alt="xygeni logo" width="450"></img><br/>
  <i>End to End Software Development and Delivery Security</i>
</div>

---

[![documentation](https://img.shields.io/badge/documentation-blue.svg)](https://docs.xygeni.io/) 
[![api documentation](https://img.shields.io/badge/api-reference-blue.svg)](https://api.xygeni.io/swagger-ui.html) 
[![version](https://img.shields.io/badge/version-3.2-blue.svg)]() 
[![xygeni.io](https://img.shields.io/badge/website-blue.svg)](https://xygeni.io/)

## Overview

Xygeni is a platform for improving the Software Supply Chain Security posture for organizations.

The platform protects the integrity and security of your software ecosystem throughout the entire DevOps

The platform features:

- **SDLC inventory**, which is automatically discovered from sources and configuration. The inventory enables us to know how assets in software infrastructure at the organization are related, for impact and risk propagation analysis: _"We can't protect what we don't know it exists."_

- **Code tampering prevention**, to protect critical code againt unintended changes done without following a strict change review process. 

- **Identify unusual activity**, anomalies in behaviour as evidence for a potential security breach, particularly when administering SDLC tools. Imagine a resource like a organization's private code repository: clones from unintended users or from anomalous geographic locations, adding-and-removing permissions in a short time period, deleting branch protection rules, or using admin rights to merge code without review or with failed status checks, are examples of such anomalies.

- **Software dependency analysis**, to control open source, proprietary and third-party components used throughout the software supply chain. This includes the discovery of components, detection of common attacks to the dependencies like typosquatting or dependency confusion, and extended SBOM management.

- **Detection of misconfigurations**, in source code managers, CI/CD pipelines and tools, build and deploy tools, artifact registries and package managers. Misconfigurations at these tools open the door to supply chain attacks, so a quick-and-easy detection capacity is necessary.   

- **Detection of Secret leaks** with optional validation that the secret is currently active and detailed instructions on how to remove / revoke the hardcoded secrets found.

- **Finding IaC flaws** in provisioning IT/Cloud templates, for the main IaC frameworks and configuration management tools. Common security flaws are reported before the assets are deployed at runtime.

- **Hardening build systems** with attestations on software provenance, chain of build steps and augmented SBOM, that could be validated and checked against deploy policies when the build artifact needs to be deployed or used by a client.

- **Compliance assessment** with common software supply chain standards and guidelines, like `Google SLSA`, `OpenSSF ScoreCard`, `CIS Software Supply Chain Security` benchmark, `OWASP Top-10 for CI/CD Security`, or the `ESF Securing SSC Guide for Developers`. Xygeni runs sort of automated audits on software projects for compliance assessment, were each standard is composed of a set of checkpoints to pass. The result tells us if the project complies with the standard, with a compliance level.

## The platform components

The platform is a cloud-based service, accessible via REST API, that keeps findings and metadata from different sources.

![Platform components](img/platform.png)

**Scanner**: Xygeni provides a command-line interface (CLI) for running the scanner. The scanner can either run analysis commands separately, like detecting hardcoded secrets or misconfigurations, or run all the analyses at once.

**Sensor**: For capturing _unusual activity_, a monitoring component (_Sensor_) can be installed on target systems (typically SCM or CI/CD tools) for monitoring the user actions and detecting activity that may evidence a bad practice, or even an ongoing attack. In addition, the sensor may capture access control data for detecting accounts with excessive privileges, or 'stale' accounts.

**Dashboard**: The Dashboard is the web user interface for showing the results of the scans. The dashboard provides a summary security posture and the breakdown of security issues at the global, group or project levels; plus trends exploration, reporting, and platform administration, among other facilities.

**API**: The REST API is the central element in the platform. All elements in the platform use the API as a backbone for reporting findings and receiving the processed information for integration into Xygeni tools, third-party plugins and integrations, or any custom integration for organizations.

**Integrations**: Xygeni provides ready-made integrations for running scans in CI/CD systems or uploading security issues, performing administrative operations, or exporting findings to communication and reporting tools.

**Watcher**: Activity on public registries is monitored by Xygeni so potential attacks could be detected early. Publishing new packages in popular public repositories is an example of an activity that is monitored by Xygeni. In addition, security advisories are ingressed for modelling new threats and malicious activity on the wild. Xygeni customers may receive alerts when a security issue may affect them.

## Installation

For operating with the Xygeni platform, you must have a valid user account linked to your organization at Xygeni.

> **NOTE**: Your organization must have a valid subscription with Xygeni Security. Please proceed to [how to subscribe to Xygeni](https://xygeni.io/book-a-demo) for further details.

Follow the instructions provided in the [Xygeni Quick Start](https://docs.xygeni.io/xydocs/introduction/quick_start.html) section of the documentation.

## Current checksums

See [checksum/CHECKSUMS.md](checksum/CHECKSUMS.md) for the full list of SHA-256 checksums and verification instructions for all downloadable artifacts (scanner, Salt CLI, bootstrap and install scripts).

