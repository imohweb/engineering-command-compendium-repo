# Logging and Monitoring

> **Section:** 23  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `prometheus` | Start the Prometheus server binary. | Source |  |
| `prometheus --config.file=CONFIG_FILE` | Start Prometheus with a specific configuration file. | Source |  |
| `grafana-cli plugins install PLUGIN_NAME` | Install a Grafana plugin using the legacy grafana-cli entry point. | Source |  |
| `curl -XGET 'localhost:9200/_cluster/health?pretty'` | Get Elasticsearch cluster health. | Source |  |
| `logstash -f CONFIG_FILE` | Run Logstash with a configuration file. | Source |  |
| `http://localhost:5601` | Typical local Kibana web endpoint. | Source | URL, not a shell command. |
| `promtool check config prometheus.yml` | Validate Prometheus configuration. | Added |  |
| `promtool check rules rules.yml` | Validate Prometheus rule files. | Added |  |
| `promtool query instant http://localhost:9090 'up'` | Run an instant PromQL query from the CLI. | Added |  |
| `curl -fsS http://localhost:9090/-/healthy` | Check Prometheus health endpoint. | Added |  |
| `grafana-cli plugins ls` | List installed Grafana plugins on installations that provide grafana-cli. | Added |  |
| `curl -s 'localhost:9200/_cat/indices?v'` | List Elasticsearch indices. | Added |  |
| `curl -s 'localhost:9200/_cat/nodes?v'` | List Elasticsearch nodes. | Added |  |
| `curl -s -H 'Content-Type: application/json' localhost:9200/INDEX/_search -d '{"query":{"match_all":{}}}'` | Run a basic Elasticsearch search request. | Added |  |
| `logstash -t -f CONFIG_FILE` | Test Logstash configuration syntax. | Added |  |
| `journalctl -f` | Follow the systemd journal. | Added |  |
| `journalctl -u SERVICE --since today` | Show service logs since the start of today. | Added |  |
| `tail -F /var/log/FILE` | Follow a log file across rotations/replacements. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
