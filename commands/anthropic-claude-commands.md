# Anthropic Claude / Claude Code Commands

A quick-reference guide to key Anthropic Claude / Claude Code environment variables and practical shell usage.

> **Security:** Never commit API keys, bearer tokens, client certificates, or other secrets to Git. Prefer secret managers, CI/CD secret stores, or local environment files excluded by `.gitignore`.

---

## Key Environment Variables

| Variable | Category | What it does |
|---|---|---|
| `ANTHROPIC_API_KEY` | Auth | API key for authentication. Optional for interactive use when subscription login is available. Required for headless, CI, or API-key-only deployments. When set, it overrides subscription login. |
| `ANTHROPIC_AUTH_TOKEN` | Auth | Custom bearer token for the `Authorization` header. Often used with gateways, managed authentication, or externally provisioned credentials. Takes precedence over `ANTHROPIC_API_KEY`. |
| `ANTHROPIC_BASE_URL` | Deployment | Redirects Claude API traffic to an LLM gateway or corporate proxy. Point this at the gateway's Anthropic-compatible endpoint. |
| `CLAUDE_CODE_USE_BEDROCK` | Deployment | Routes model traffic through Amazon Bedrock instead of the Anthropic API. Set to `1` to enable. |
| `CLAUDE_CODE_USE_VERTEX` | Deployment | Routes model traffic through Google Vertex AI. Requires `ANTHROPIC_VERTEX_PROJECT_ID` and `CLOUD_ML_REGION`. |
| `ANTHROPIC_BEDROCK_BASE_URL` | Deployment | Overrides the Bedrock endpoint. Typically used to route Bedrock traffic through an LLM gateway. |
| `HTTPS_PROXY` / `HTTP_PROXY` | Network | Corporate proxy server URL. Use `HTTPS_PROXY` first and fall back to `HTTP_PROXY` if required. |
| `NO_PROXY` | Network | Comma-separated or space-separated hosts that should bypass the proxy. Set to `*` to bypass the proxy for all requests. |
| `NODE_EXTRA_CA_CERTS` | Network | Path to a custom CA certificate file. Useful when a corporate network uses a CA not present in the OS trust store. |
| `CLAUDE_CODE_CERT_STORE` | Network | Controls which CA certificate store Claude Code trusts. |
| `CLAUDE_CODE_CLIENT_CERT` | Network | Path to a client certificate for mTLS authentication. Pair with `CLAUDE_CODE_CLIENT_KEY`. |
| `DISABLE_TELEMETRY` | Governance | Disables telemetry reporting. Useful where outbound telemetry traffic is restricted by policy. |
| `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC` | Governance | Suppresses non-essential outbound traffic such as telemetry and changelog fetches. Useful for air-gapped or restricted-egress environments. |
| `DISABLE_AUTOUPDATER` | Governance | Prevents Claude Code from auto-updating. Useful where software versions are centrally managed or pinned for stability. |
| `CLAUDE_CODE_MAX_TURNS` | Behavior | Sets the maximum number of agentic turns before Claude Code stops and asks for confirmation. Useful for cost control and controlled pilots. |

---

## Authentication

### Set an Anthropic API key

```bash
export ANTHROPIC_API_KEY="<your-api-key>"
```

Check that the variable is set without printing the secret:

```bash
test -n "$ANTHROPIC_API_KEY" && echo "ANTHROPIC_API_KEY is set"
```

Remove it from the current shell session:

```bash
unset ANTHROPIC_API_KEY
```

### Use a custom bearer token

```bash
export ANTHROPIC_AUTH_TOKEN="<your-bearer-token>"
```

Remove it:

```bash
unset ANTHROPIC_AUTH_TOKEN
```

---

## Custom API Gateway / Corporate Endpoint

Point Claude traffic to an Anthropic-compatible gateway:

```bash
export ANTHROPIC_BASE_URL="https://gateway.example.com/anthropic"
```

Confirm the configured endpoint:

```bash
echo "$ANTHROPIC_BASE_URL"
```

Remove the override:

```bash
unset ANTHROPIC_BASE_URL
```

---

## Amazon Bedrock

Enable Claude Code through Amazon Bedrock:

```bash
export CLAUDE_CODE_USE_BEDROCK=1
```

Optionally override the Bedrock endpoint:

```bash
export ANTHROPIC_BEDROCK_BASE_URL="https://bedrock-gateway.example.com"
```

Disable the Bedrock routing override:

```bash
unset CLAUDE_CODE_USE_BEDROCK
unset ANTHROPIC_BEDROCK_BASE_URL
```

---

## Google Vertex AI

Enable Claude Code through Google Vertex AI:

```bash
export CLAUDE_CODE_USE_VERTEX=1
```

Set the required project and region:

```bash
export ANTHROPIC_VERTEX_PROJECT_ID="<gcp-project-id>"
export CLOUD_ML_REGION="<gcp-region>"
```

Disable the Vertex routing override:

```bash
unset CLAUDE_CODE_USE_VERTEX
unset ANTHROPIC_VERTEX_PROJECT_ID
unset CLOUD_ML_REGION
```

---

## Proxy Configuration

Configure an HTTPS proxy:

```bash
export HTTPS_PROXY="http://proxy.example.com:8080"
```

Configure an HTTP proxy:

```bash
export HTTP_PROXY="http://proxy.example.com:8080"
```

Bypass the proxy for selected hosts:

```bash
export NO_PROXY="localhost,127.0.0.1,.example.internal"
```

Remove proxy settings:

```bash
unset HTTPS_PROXY
unset HTTP_PROXY
unset NO_PROXY
```

---

## Custom CA Certificates

Use an additional corporate CA certificate:

```bash
export NODE_EXTRA_CA_CERTS="/path/to/corporate-ca.pem"
```

Configure Claude Code certificate-store behavior:

```bash
export CLAUDE_CODE_CERT_STORE="system"
```

---

## Mutual TLS (mTLS)

Set the client certificate:

```bash
export CLAUDE_CODE_CLIENT_CERT="/path/to/client-cert.pem"
```

Set the matching private key:

```bash
export CLAUDE_CODE_CLIENT_KEY="/path/to/client-key.pem"
```

Restrict private-key permissions:

```bash
chmod 600 /path/to/client-key.pem
```

---

## Governance and Restricted-Egress Environments

Disable telemetry:

```bash
export DISABLE_TELEMETRY=1
```

Disable non-essential outbound traffic:

```bash
export CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1
```

Disable automatic updates:

```bash
export DISABLE_AUTOUPDATER=1
```

Remove the governance overrides:

```bash
unset DISABLE_TELEMETRY
unset CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC
unset DISABLE_AUTOUPDATER
```

---

## Limit Agentic Turns

Set a maximum number of agentic turns:

```bash
export CLAUDE_CODE_MAX_TURNS=10
```

Check the configured value:

```bash
echo "$CLAUDE_CODE_MAX_TURNS"
```

Remove the limit:

```bash
unset CLAUDE_CODE_MAX_TURNS
```

---

## Persist Variables in Your Shell

### Bash

```bash
echo 'export ANTHROPIC_BASE_URL="https://gateway.example.com/anthropic"' >> ~/.bashrc
source ~/.bashrc
```

### Zsh

```bash
echo 'export ANTHROPIC_BASE_URL="https://gateway.example.com/anthropic"' >> ~/.zshrc
source ~/.zshrc
```

> Avoid storing secrets such as `ANTHROPIC_API_KEY` directly in shell startup files on shared or managed systems.

---

## Inspect Claude-Related Environment Variables

List relevant variables:

```bash
env | grep -E '^(ANTHROPIC|CLAUDE_CODE|DISABLE_|NODE_EXTRA_CA_CERTS|HTTPS_PROXY|HTTP_PROXY|NO_PROXY)='
```

List only variable names while avoiding accidental secret disclosure:

```bash
env | cut -d= -f1 | grep -E '^(ANTHROPIC|CLAUDE_CODE|DISABLE_|NODE_EXTRA_CA_CERTS|HTTPS_PROXY|HTTP_PROXY|NO_PROXY)$'
```

---

## Recommended `.gitignore` Entries

```gitignore
.env
.env.*
*.pem
*.key
secrets/
```

---

## Reference

The source screenshot points to the Claude Code environment variable reference:

`code.claude.com/docs/en/env-vars`
