# 📊 U4: Gerência de Desempenho e Tráfego

## 🎯 Objetivo
Monitorar métricas críticas de rede, como utilização do enlace e throughput real, analisando o impacto do fluxo de dados (ICMP e requisições HTTP) na infraestrutura.

## 🛠️ Topologia
O laboratório foi montado com uma arquitetura cliente-servidor:
* 3 Estações de Trabalho (PC0, PC1, PC2) na faixa `192.168.1.x`.
* 1 Servidor Web/Arquivo (Server0) no IP `192.168.1.100`.
* Análise de tráfego executada nas portas do Switch de agregação.

## 📝 Notas de Estudo (O que aprendi aqui)
* **Largura de Banda vs Throughput:** A largura de banda é apenas a capacidade teórica de um enlace. O throughput reflete o mundo real: é a taxa efetiva de bits transmitidos com sucesso, sofrendo impacto de latências e sobrecargas de protocolo.
* **Utilização da Rede:** É o percentual da capacidade do enlace que está ativamente consumida. É um indicador primário para o administrador detectar gargalos de tráfego.
* **Congestionamento:** Quando vários PCs requisitam dados pesados simultaneamente (ex: tráfego HTTP de download, a demanda excede a capacidade. Isso gera filas no switch, atrasos e redução imediata no throughput observado. A gerência de desempenho permite antecipar esses gargalos para manter a Qualidade de Serviço (QoS).
