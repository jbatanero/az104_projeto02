# Log Analytics

## O que é?

Serviço usado para coletar e consultar logs de diagnóstico e telemetria de recursos no Azure.

## Como configurar:

1. Criar um Workspace do Log Analytics.
2. Associar a VM ao workspace.
3. Habilitar coleta de logs e métricas.
4. Acessar o Log Analytics e usar consultas (KQL).

## Exemplo de consulta:
```kql
Heartbeat
| summarize Count() by Computer, bin(TimeGenerated, 1h)
