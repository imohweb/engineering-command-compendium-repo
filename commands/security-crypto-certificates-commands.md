# Security, Cryptography and Certificates

> **Section:** 27  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `sha256sum FILE` | Calculate a SHA-256 checksum on Linux. | Added |  |
| `shasum -a 256 FILE` | Calculate a SHA-256 checksum on macOS and other systems with shasum. | Added |  |
| `md5sum FILE` | Calculate an MD5 checksum for non-security integrity comparisons. | Added | MD5 is cryptographically broken; do not use it for security assurances. |
| `openssl version -a` | Show OpenSSL version and build details. | Added |  |
| `openssl s_client -connect HOST:443 -servername HOST` | Inspect a TLS handshake, certificate chain and negotiated parameters. | Added |  |
| `openssl x509 -in cert.pem -noout -subject -issuer -dates` | Display certificate subject, issuer and validity dates. | Added |  |
| `openssl x509 -in cert.pem -text -noout` | Display full X.509 certificate details. | Added |  |
| `openssl req -new -newkey rsa:2048 -nodes -keyout key.pem -out request.csr` | Generate an RSA private key and CSR. | Added | Protect the generated private key. |
| `openssl rand -hex 32` | Generate 32 random bytes encoded as hexadecimal. | Added |  |
| `ssh-keygen -t ed25519 -C "COMMENT"` | Generate an Ed25519 SSH key pair. | Added |  |
| `ssh-keygen -lf ~/.ssh/id_ed25519.pub` | Show an SSH public-key fingerprint. | Added |  |
| `ssh-keyscan -H HOST >> ~/.ssh/known_hosts` | Fetch and append host keys. | Added | Verify fingerprints through a trusted channel before relying on them. |
| `gpg --list-keys` | List GPG public keys. | Added |  |
| `gpg --verify SIGNATURE FILE` | Verify a detached GPG signature. | Added |  |
| `getcap FILE` | Show Linux file capabilities. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
