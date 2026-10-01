# monitoring

Metrics, dashboards and uptime alerting for the home lab.

| Service | Purpose | Port |
|---|---|---|
| Uptime Kuma | HTTP, ping and DNS checks for every service, with Discord alerts | 3001 |
| Prometheus | Collects metrics (30-day retention) | 9090 |
| node-exporter | Host CPU, RAM, disk and network metrics | 9100 |
| cAdvisor | Per-container resource usage | 8088 |
| Grafana | Dashboards (Node Exporter Full, cAdvisor) | 3000 |

## Setup

```bash
cp .env.example .env   # set GRAFANA_ADMIN_PASSWORD
docker compose up -d
```

## Alerting

- Uptime Kuma monitors each service and the TrueNAS and Pi-hole machines, and sends Down and Up messages to a Discord webhook.
- TrueNAS sends pool and drive alerts to the same Discord channel through its Slack-compatible alert service.
- Alerting was tested by stopping a container and confirming both the Down and recovery messages arrived.

## Not in this repo

Webhook URLs, the Uptime Kuma database (monitor list and notification settings) and Grafana's data. Re-create them through each web UI.
