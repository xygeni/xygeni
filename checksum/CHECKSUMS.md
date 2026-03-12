# Current checksums

SHA-256 checksums for the latest Xygeni downloadable artifacts, used for integrity verification.

## Scanner

* `get-xygeni.sh` (bootstrap script for Linux/macOS): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-xygeni.sh.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/get-xygeni.sh.sha256?plain=1#L1

* `get-xygeni.ps1` (bootstrap script for Windows): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-xygeni.ps1.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/get-xygeni.ps1.sha256?plain=1#L1

* `install.sh` (**deprecated** — use `get-xygeni.sh` instead): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.sh.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/install.sh.sha256?plain=1#L1

* `install.ps1` (**deprecated** — use `get-xygeni.ps1` instead): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/install.ps1.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/install.ps1.sha256?plain=1#L1

* `xygeni-release.zip` (scanner): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/xygeni-release.zip.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/xygeni-release.zip.sha256?plain=1#L1

## Salt CLI

* `get-salt.sh` (bootstrap script for Linux/macOS): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-salt.sh.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/get-salt.sh.sha256?plain=1#L1

* `get-salt.ps1` (bootstrap script for Windows): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-salt.ps1.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/get-salt.ps1.sha256?plain=1#L1

* `salt.zip` (build attestations): [checksum link](https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/salt.zip.sha256)
https://github.com/xygeni/xygeni/blob/main/checksum/latest/salt.zip.sha256?plain=1#L1

## Verification

You may verify the integrity of a downloaded artifact before execution.

### Linux / macOS

```bash
# Download and verify the bootstrap script
curl -sLO https://get.xygeni.io/latest/scanner/get-xygeni.sh
checksum="$(curl -s https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-xygeni.sh.sha256)"
echo "$checksum get-xygeni.sh" | sha256sum --check

# Same for Salt CLI
curl -sLO https://get.xygeni.io/latest/salt/get-salt.sh
checksum="$(curl -s https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-salt.sh.sha256)"
echo "$checksum get-salt.sh" | sha256sum --check
```

### Windows (PowerShell)

```powershell
# Download and verify the bootstrap script
iwr https://get.xygeni.io/latest/scanner/get-xygeni.ps1 -useb -OutFile get-xygeni.ps1
(Get-FileHash '.\get-xygeni.ps1' -Algorithm SHA256).Hash -eq `
  (iwr https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-xygeni.ps1.sha256)

# Same for Salt CLI
iwr https://get.xygeni.io/latest/salt/get-salt.ps1 -useb -OutFile get-salt.ps1
(Get-FileHash '.\get-salt.ps1' -Algorithm SHA256).Hash -eq `
  (iwr https://raw.githubusercontent.com/xygeni/xygeni/main/checksum/latest/get-salt.ps1.sha256)
```
