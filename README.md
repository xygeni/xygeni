
<div align="center">
  <img src="img/xygeni.logo.text.png" alt="xygeni logo" width="450"></img><br/>
  <i>End to End Software Development and Delivery Security</i>
</div>

---

[![documentation](https://img.shields.io/badge/documentation-blue.svg)](https://docs.xygeni.io/) 
[![api documentation](https://img.shields.io/badge/api-reference-blue.svg)](https://api.xygeni.io/swagger-ui.html) 
[![version](https://img.shields.io/badge/version-3.2-blue.svg)]() 
[![xygeni.io](https://img.shields.io/badge/website-blue.svg)](https://xygeni.io/)

## Install

For operating with the Xygeni platform, you must have a valid user account linked to your organization at Xygeni.

> **NOTE**: Your organization must have a valid subscription with Xygeni Security. Please proceed to [how to subscribe to Xygeni](https://xygeni.io/book-a-demo) for further details.

Follow the instructions provided in the [Xygeni Quick Start](http://docs.xygeni.io/introduction/quick_start.htl) section of the documentation.

## Current checksums

* `install.sh` (install script for Linux/macOS): 

```
3069927267261d644a796fc65e912375f399df3ba3903d926d79a55b92476b5b

```
* `install.ps1` (install script for Windows):
```
f13defabd11da3c742acb46fbad8512e0e4ffca52b8359df07d9dbdb68b5688e
```
* `xygeni-release.zip` (scanner):
```
3b7dcae06f0968d20404eb06d5f779af1295de1ae9e6039e7f7df82bcec0e432
```

So you may verify the integrity of a downloaded artifact:

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

