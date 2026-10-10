# Download & Install PTTS Ping 1.3.0

PTTS Ping is available for **Microsoft Windows** and supported **Linux distributions**. Choose your operating system below for the recommended installation method.

- **Windows:** download and run the PTTS Ping installer from GitHub.
- **Linux:** installation from the signed PTTS Linux repository is recommended on supported distributions. Direct `.deb` and `.rpm` downloads remain available as an alternative.

For Linux command blocks, GitHub provides a **Copy** button. Open the section for your distribution, copy the commands, paste them into a terminal, and press **Enter**.

<details>
<summary><strong>Microsoft Windows 10 1809+ / Windows 11 x64</strong></summary>

**Recommended — Windows installer**

[**Download PTTS Ping 1.3.0 for Windows x64**](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-windows-x64-setup.exe) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-windows-x64-setup.exe.sha256)

One installer supports Windows 10 version 1809 or later and Windows 11 x64.

1. Download the installer.
2. Run the installer and complete setup.
3. Launch **PTTS Ping** from the Start menu.

The current Windows installer is unsigned, so Windows may display a trust or security prompt before installation.

</details>

<details>
<summary><strong>Ubuntu 24.04 Noble</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo apt update
sudo apt install -y curl gnupg ca-certificates
sudo install -d -m 0755 /etc/apt/keyrings
curl -fsSL https://repo.pttsllc.com/keys/ptts-linux-repo.asc | gpg --dearmor | sudo tee /etc/apt/keyrings/ptts-linux-repo.gpg >/dev/null
echo 'deb [arch=amd64 signed-by=/etc/apt/keyrings/ptts-linux-repo.gpg] https://repo.pttsllc.com/apt noble main' | sudo tee /etc/apt/sources.list.d/ptts.list >/dev/null
sudo apt update
sudo apt install ptts-ping
```

**Alternative:** [Download the `.deb` directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping_amd64.deb) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping_amd64.deb.sha256)

</details>

<details>
<summary><strong>Ubuntu 26.04 Resolute</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo apt update
sudo apt install -y curl gnupg ca-certificates
sudo install -d -m 0755 /etc/apt/keyrings
curl -fsSL https://repo.pttsllc.com/keys/ptts-linux-repo.asc | gpg --dearmor | sudo tee /etc/apt/keyrings/ptts-linux-repo.gpg >/dev/null
echo 'deb [arch=amd64 signed-by=/etc/apt/keyrings/ptts-linux-repo.gpg] https://repo.pttsllc.com/apt resolute main' | sudo tee /etc/apt/sources.list.d/ptts.list >/dev/null
sudo apt update
sudo apt install ptts-ping
```

**Alternative:** [Download the `.deb` directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping_amd64.deb) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping_amd64.deb.sha256)

</details>

<details>
<summary><strong>Fedora 43</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo tee /etc/yum.repos.d/ptts.repo >/dev/null <<'EOF'
[ptts]
name=PTTS LLC
baseurl=https://repo.pttsllc.com/rpm/fedora/43/x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=1
gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
metadata_expire=0
EOF
sudo dnf clean all
sudo dnf makecache --refresh
sudo dnf install ptts-ping
```

**Alternative:** [Download the Fedora 43 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.fc43.x86_64.rpm) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.fc43.x86_64.rpm.sha256)

</details>

<details>
<summary><strong>Fedora 44</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo tee /etc/yum.repos.d/ptts.repo >/dev/null <<'EOF'
[ptts]
name=PTTS LLC
baseurl=https://repo.pttsllc.com/rpm/fedora/44/x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=1
gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
metadata_expire=0
EOF
sudo dnf clean all
sudo dnf makecache --refresh
sudo dnf install ptts-ping
```

**Alternative:** [Download the Fedora 44 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.fc44.x86_64.rpm) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.fc44.x86_64.rpm.sha256)

</details>

<details>
<summary><strong>Rocky Linux 9 / AlmaLinux 9</strong></summary>

**Recommended — PTTS Linux repository.** EL9 also requires EPEL and CRB for PTTS Ping runtime dependencies.

```sh
sudo dnf install -y dnf-plugins-core epel-release
sudo dnf config-manager --set-enabled crb
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo tee /etc/yum.repos.d/ptts.repo >/dev/null <<'EOF'
[ptts]
name=PTTS LLC
baseurl=https://repo.pttsllc.com/rpm/el/9/x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=1
gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
metadata_expire=0
EOF
sudo dnf clean all
sudo dnf makecache --refresh
sudo dnf install ptts-ping
```

**Alternative:** [Download the EL9 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.el9.x86_64.rpm) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.el9.x86_64.rpm.sha256)

</details>

<details>
<summary><strong>Rocky Linux 10 / AlmaLinux 10</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo tee /etc/yum.repos.d/ptts.repo >/dev/null <<'EOF'
[ptts]
name=PTTS LLC
baseurl=https://repo.pttsllc.com/rpm/el/10/x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=1
gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
metadata_expire=0
EOF
sudo dnf clean all
sudo dnf makecache --refresh
sudo dnf install ptts-ping
```

**Alternative:** [Download the EL10 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.el10.x86_64.rpm) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.el10.x86_64.rpm.sha256)

</details>

<details>
<summary><strong>openSUSE Leap 16.0</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo zypper --non-interactive ar -f --gpgcheck-allow-unsigned-package https://repo.pttsllc.com/rpm/opensuse/leap/16.0/x86_64 ptts
sudo zypper refresh
sudo zypper install --from ptts ptts-ping
```

**Alternative:** [Download the Leap 16.0 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.lp160.x86_64.rpm) · [SHA256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.3.0/ptts-ping-1.3.0-1.lp160.x86_64.rpm.sha256)

</details>

<details>
<summary><strong>Other Linux / Debian</strong></summary>

Debian and other unlisted Linux distributions have not been validated. Use only a package intended for your system.

[View all PTTS Ping 1.3.0 release downloads](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/tag/v1.3.0)

</details>

## Linux repository trust

The following trust information applies to installation through the PTTS Linux repository.

Repository metadata is signed by **PTTS LLC Linux Software Signing**.

```text
C611 38A4 9D40 5036 D599 2E45 AEB9 E7DE 9F21 AE57
```

PTTS Ping 1.3.0 RPM package payloads predate package-level RPM signing. Repository metadata is signed and verified, while the current repository configuration allows these legacy unsigned package payloads. Future RPM releases are intended to use package-level signatures as well.

## Release resources

[PTTS Ping 1.3.0 release](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/tag/v1.3.0) · [Product website](https://pttsllc.com/software/ptts-ping/) · [Support](https://github.com/nproctor-dev/PTTS-Ping-Support/issues)
