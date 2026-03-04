# 📊 Log Centralizado com Loki + Grafana

Sistema completo de coleta, armazenamento e visualização de logs usando Loki e Grafana.

## ✨ Funcionalidades

- **Loki**: Log aggregation
- **Grafana**: Visualização e alertas
- **Promtail**: Coleta de logs
- **LogQL**: Query language para logs
- **Dashboard**: Análise em tempo real
- **Alertas**: Notificações automáticas

## 🛠️ Tecnologias

- **Grafana Loki**: Log storage
- **Promtail**: Log shipper
- **Docker Compose**: Orquestração
- **Prometheus**: Métricas

## 🚀 Como Executar

```bash
# Iniciar stack com Docker
docker-compose up -d

# Acessar Grafana
# http://localhost:3000

# Default credentials
# Username: admin
# Password: admin
```

## 📁 Estrutura

```
loki-grafana/
├── docker-compose.yml
├── loki-config.yaml
├── promtail-config.yaml
├── dashboards/
│   └── application-logs.json
├── alerts/
│   └── alert-rules.yaml
└── README.md
```

## 💡 LogQL Queries

```logql
{job="app"} | json | level="error"
{container="api"} !="health" | stats count() by status
rate({job="nginx"}[5m])
```

## 📈 Recursos

- Log aggregation e análise
- Alertas em tempo real
- Múltiplos datasources
- Query builder interativo

## 📝 Licença

MIT License

---

⭐ Se este projeto foi útil, deixe uma star!
