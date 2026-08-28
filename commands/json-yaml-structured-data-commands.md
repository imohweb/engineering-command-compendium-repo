# JSON, YAML and Structured Data

> **Section:** 26  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `jq '.' file.json` | Pretty-print and validate JSON with jq. | Added |  |
| `jq -r '.name' file.json` | Extract a string value without JSON quotes. | Added |  |
| `jq '.items[] &#124; {name: .metadata.name}' file.json` | Transform JSON arrays/objects. | Added |  |
| `curl -s URL &#124; jq '.'` | Pretty-print JSON returned by an HTTP endpoint. | Added |  |
| `python3 -m json.tool file.json` | Pretty-print and validate JSON using Python standard library. | Added |  |
| `yq '.metadata.name' file.yaml` | Read a YAML field with yq (syntax depends on yq implementation/version). | Added |  |
| `yq -o=json '.' file.yaml` | Convert YAML to JSON with Mike Farah yq. | Added |  |
| `base64 FILE` | Encode a file as Base64. | Added |  |
| `base64 -d FILE.b64` | Decode Base64 on GNU/Linux. | Added |  |
| `xmllint --format file.xml` | Pretty-print XML (libxml2 tools). | Added |  |
| `xmllint --xpath '//name/text()' file.xml` | Extract XML data with XPath. | Added |  |
| `column -s, -t file.csv` | Render simple CSV-like data as aligned columns. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
