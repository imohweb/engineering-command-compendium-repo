# Package Management (Depends on Distribution)

> **Section:** 9  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `apt-get install PACKAGE` | Install a package on Debian/Ubuntu. | Source |  |
| `apt-get update` | Update APT package indexes. | Source |  |
| `apt-get upgrade` | Upgrade installed packages. | Source |  |
| `apt-get remove PACKAGE` | Remove a package. | Source |  |
| `apt-cache search PACKAGE` | Search APT package metadata. | Source |  |
| `apt-cache show PACKAGE` | Show APT package details. | Source |  |
| `yum install PACKAGE` | Install an RPM package on yum-based systems. | Source |  |
| `yum update` | Update installed packages on yum-based systems. | Source |  |
| `yum remove PACKAGE` | Remove a package using yum. | Source |  |
| `dnf install PACKAGE` | Install a package on modern Fedora/RHEL-family systems. | Source |  |
| `dnf update` | Update installed packages using dnf. | Source |  |
| `dnf remove PACKAGE` | Remove a package using dnf. | Source |  |
| `rpm -i PACKAGE.rpm` | Install an RPM package directly. | Source |  |
| `rpm -e PACKAGE` | Remove an RPM package. | Source |  |
| `dpkg -i PACKAGE.deb` | Install a Debian package directly. | Source |  |
| `dpkg -r PACKAGE` | Remove a Debian package. | Source |  |
| `apt install PACKAGE` | Preferred interactive APT install command. | Added |  |
| `apt update && apt upgrade` | Refresh indexes and upgrade packages. | Added |  |
| `apt autoremove` | Remove automatically installed packages no longer needed. | Added |  |
| `apt search PATTERN` | Search packages. | Added |  |
| `dpkg -l` | List installed Debian packages. | Added |  |
| `dpkg -S PATH` | Find which installed package owns a path. | Added |  |
| `dnf search PATTERN` | Search dnf repositories. | Added |  |
| `dnf info PACKAGE` | Show package information. | Added |  |
| `rpm -qa` | List installed RPM packages. | Added |  |
| `rpm -qf PATH` | Find which installed RPM owns a file. | Added |  |
| `pacman -S PACKAGE` | Install a package on Arch Linux. | Added |  |
| `pacman -Syu` | Refresh package database and fully upgrade Arch Linux. | Added |  |
| `zypper install PACKAGE` | Install a package on openSUSE/SLES. | Added |  |
| `zypper update` | Update packages on openSUSE/SLES. | Added |  |
| `brew install PACKAGE` | Install a package using Homebrew on macOS/Linux. | Added |  |
| `brew update && brew upgrade` | Update Homebrew metadata and upgrade installed formulae. | Added |  |
| `brew services list` | List services managed by Homebrew. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
