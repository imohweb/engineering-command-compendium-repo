# Archiving and Compression

> **Section:** 8  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `tar -czf archive.tar.gz /path/to/directory` | Create a gzip-compressed tar archive. | Source |  |
| `tar -xzf archive.tar.gz` | Extract a gzip-compressed tar archive. | Source |  |
| `tar -cf archive.tar /path/to/directory` | Create an uncompressed tar archive. | Source |  |
| `tar -xf archive.tar` | Extract a tar archive. | Source |  |
| `zip` | Package and compress files into a ZIP archive. | Source |  |
| `unzip` | Extract a ZIP archive. | Source |  |
| `gzip` | Compress files using gzip. | Source |  |
| `gunzip` | Decompress gzip files. | Source |  |
| `bzip2` | Compress files using bzip2. | Source |  |
| `bunzip2` | Decompress bzip2 files. | Source |  |
| `xz` | Compress files using xz. | Source |  |
| `unxz` | Decompress xz files. | Source |  |
| `tar -caf archive.tar.xz PATH` | Create an archive and choose compression automatically from the suffix. | Added |  |
| `tar -taf archive.tar.gz` | List archive contents without extracting. | Added |  |
| `zip -r archive.zip DIRECTORY` | Recursively create a ZIP archive. | Added |  |
| `unzip -l archive.zip` | List ZIP contents without extracting. | Added |  |
| `zstd FILE` | Compress a file using Zstandard (when installed). | Added |  |
| `unzstd FILE.zst` | Decompress a Zstandard file. | Added |  |
| `7z a archive.7z PATH` | Create a 7z archive (7-Zip/p7zip when installed). | Added |  |
| `7z x archive.7z` | Extract a 7z archive. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
