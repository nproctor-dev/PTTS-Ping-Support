# Download & Install PTTS Ping 1.4.0

PTTS Ping is available for **Microsoft Windows** and supported **Linux distributions**. Choose your operating system below for the recommended installation method.

- **Windows:** download and run the PTTS Ping installer from GitHub.
- **Linux:** installation from the signed PTTS Linux repository is recommended on supported distributions. Direct `.deb` and `.rpm` downloads remain available as an alternative; their hashes are published in the signed aggregate `SHA256SUMS` manifest.

**Simple install:** expand the section for your distribution, click GitHub's **Copy** control on the command block, paste into a terminal, and run. The commands configure the signed PTTS Linux repository and install PTTS Ping. After setup, updates arrive through your normal package manager; existing users do not need to repeat repository configuration.

<details>
<summary><strong>Windows x64</strong></summary>

**Recommended — Windows x64 ZIP**

[**Download PTTS Ping 1.4.0 for Windows x64 (ZIP)**](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-windows-x64.zip) · [ZIP SHA-256](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-windows-x64.zip.sha256)

1. Download the ZIP and extract it.
2. Run `ptts-ping-1.4.0-windows-x64-setup.exe` from the extracted folder and follow setup.
3. Launch **PTTS Ping** from the Start menu.

The ZIP contains the installer and its `.sha256` checksum. The [standalone installer EXE](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-windows-x64-setup.exe) remains available for PTTS Ping's built-in update link. Windows x64 support covers Windows 10 version 1809 or later and Windows 11.

The current Windows installer is unsigned, so Windows may display a trust or security prompt before installation.

</details>

<details>
<summary><strong>Ubuntu 24.04 Noble / Linux Mint 22.3 Zena</strong></summary>

Linux Mint 22.3 Zena is based on Ubuntu 24.04 Noble and uses the **same Noble APT repository**. PTTS Ping 1.4.0-2 passed real-machine installation, ICMP, and reboot-persistence tests on Mint 22.3. Other Mint 22.x releases have not been separately qualified.

**Recommended — PTTS Linux repository**

```sh
sudo apt update && sudo apt install -y curl ca-certificates
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://repo.pttsllc.com/keys/ptts-linux-repo.asc -o /etc/apt/keyrings/ptts-linux-repo.asc
echo 'deb [arch=amd64 signed-by=/etc/apt/keyrings/ptts-linux-repo.asc] https://repo.pttsllc.com/apt noble main' | sudo tee /etc/apt/sources.list.d/ptts.list >/dev/null
sudo apt update && sudo apt install -y ptts-ping
```

**Alternative:** [Download the `.deb` directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping_1.4.0-2_amd64.deb) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Ubuntu 26.04 Resolute</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo apt update && sudo apt install -y curl ca-certificates
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://repo.pttsllc.com/keys/ptts-linux-repo.asc -o /etc/apt/keyrings/ptts-linux-repo.asc
echo 'deb [arch=amd64 signed-by=/etc/apt/keyrings/ptts-linux-repo.asc] https://repo.pttsllc.com/apt resolute main' | sudo tee /etc/apt/sources.list.d/ptts.list >/dev/null
sudo apt update && sudo apt install -y ptts-ping
```

**Alternative:** [Download the `.deb` directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping_1.4.0-2_amd64.deb) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Fedora 43</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf config-manager addrepo --id=ptts --set=baseurl=https://repo.pttsllc.com/rpm/fedora/43/x86_64 --set=enabled=1 --set=gpgcheck=1 --set=repo_gpgcheck=1 --set=gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf install -y ptts-ping
```

**Alternative:** [Download the Fedora 43 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-2.fc43.x86_64.rpm) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Fedora 44</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf config-manager addrepo --id=ptts --set=baseurl=https://repo.pttsllc.com/rpm/fedora/44/x86_64 --set=enabled=1 --set=gpgcheck=1 --set=repo_gpgcheck=1 --set=gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf install -y ptts-ping
```

**Alternative:** [Download the Fedora 44 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-2.fc44.x86_64.rpm) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Fedora 45</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf config-manager addrepo --id=ptts --set=baseurl=https://repo.pttsllc.com/rpm/fedora/45/x86_64 --set=enabled=1 --set=gpgcheck=1 --set=repo_gpgcheck=1 --set=gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf install -y ptts-ping
```

**Alternative:** [Download the Fedora 45 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-3.fc45.x86_64.rpm) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Rocky Linux 9 / AlmaLinux 9</strong></summary>

**Recommended — PTTS Linux repository.** EL9 also requires EPEL and CRB for PTTS Ping runtime dependencies.

```sh
sudo dnf install -y dnf-plugins-core epel-release
sudo dnf config-manager --set-enabled crb
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo tee /etc/yum.repos.d/ptts.repo >/dev/null <<'EOF_REPO'
[ptts]
name=PTTS LLC
baseurl=https://repo.pttsllc.com/rpm/el/9/x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
EOF_REPO
sudo dnf install -y ptts-ping
```

**Alternative:** [Download the EL9 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-2.el9.x86_64.rpm) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Rocky Linux 10 / AlmaLinux 10</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf config-manager addrepo --id=ptts --set=baseurl=https://repo.pttsllc.com/rpm/el/10/x86_64 --set=enabled=1 --set=gpgcheck=1 --set=repo_gpgcheck=1 --set=gpgkey=https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo dnf install -y ptts-ping
```

**Alternative:** [Download the EL10 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-2.el10.x86_64.rpm) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>openSUSE Leap 16.0</strong></summary>

**Recommended — PTTS Linux repository**

```sh
sudo rpm --import https://repo.pttsllc.com/keys/ptts-linux-repo.asc
sudo zypper --non-interactive ar -f https://repo.pttsllc.com/rpm/opensuse/leap/16.0/x86_64 ptts
sudo zypper refresh
sudo zypper install --from ptts ptts-ping
```

**Alternative:** [Download the Leap 16.0 RPM directly from GitHub](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/ptts-ping-1.4.0-2.lp160.x86_64.rpm) · [Linux SHA256SUMS](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) · [signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc)

</details>

<details>
<summary><strong>Other Linux / Debian</strong></summary>

Debian and other unlisted Linux distributions have not been validated. Use only a package intended for your system.

[View all PTTS Ping 1.4.0 release downloads](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/tag/v1.4.0)

</details>

## Linux repository trust

The following trust information applies to installation through the PTTS Linux repository.

Repository metadata is signed by **PTTS LLC Linux Software Signing**.

```text
C611 38A4 9D40 5036 D599 2E45 AEB9 E7DE 9F21 AE57
```

**Current Linux package revisions: `1.4.0-2` for Ubuntu, Fedora 43/44, EL9/10 and Leap; `1.4.0-3.fc45` for Fedora 45.** PTTS Ping installs `/usr/lib/sysctl.d/50-ptts-ping.conf` to permit native unprivileged IPv4 ICMP on systems where restrictive `net.ipv4.ping_group_range` defaults would otherwise interfere. Administrator overrides take precedence. The signed PTTS APT/RPM repository is the recommended installation and upgrade method. All six RPM packages have individual PTTS package signatures, and repository metadata is signed separately.

Direct Linux 1.4.0 downloads use the signed aggregate [`SHA256SUMS`](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS) manifest and its [detached signature](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/download/v1.4.0/SHA256SUMS.asc).

## Release resources

[PTTS Ping 1.4.0 release](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/tag/v1.4.0) · [Product website](https://pttsllc.com/software/ptts-ping/) · [Support](https://github.com/nproctor-dev/PTTS-Ping-Support/issues)
