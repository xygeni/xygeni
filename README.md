
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

* `install.sh` (install script for Linux/macOS): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.sh.sha256)
https://github.com/xygeni/xygeni/blob/a36ca1f19e8b820b78716f9ff04645e369f57693/checksum/latest/install.sh.sha256?plain=1#L1

* `install.ps1` (install script for Windows): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.ps1.sha256)
https://github.com/xygeni/xygeni/blob/a36ca1f19e8b820b78716f9ff04645e369f57693/checksum/latest/install.ps1.sha256?plain=1#L1

* `xygeni-release.zip` (scanner): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/xygeni-release.zip.sha256)
https://github.com/xygeni/xygeni/blob/a36ca1f19e8b820b78716f9ff04645e369f57693/checksum/latest/xygeni-release.zip.sha256?plain=1#L1

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

