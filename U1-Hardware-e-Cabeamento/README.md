# 🖥️ U1: Hardware e Cabeamento

## 🎯 Objetivo
Estabelecer e validar a comunicação entre dois computadores através de um switch, compreendendo a configuração de endereços IPv4 e o funcionamento básico da camada de enlace.

## 🛠️ Topologia e Endereçamento
A rede foi configurada utilizando a sub-rede `192.168.1.0/24`, com os hosts conectados a um switch via cabo de par trançado (Copper Straight-Through).
**PC0:** `192.168.1.1`
**PC1:** `192.168.1.2`
**Máscara de Sub-rede:** `255.255.255.0`

## 📝 Notas de Estudo (O que aprendi aqui)
**Tempo de Aprendizado do Switch:** Inicialmente, os pacotes de `ping` podem falhar. Isso ocorre porque o switch opera na Camada 2 do modelo OSI e precisa de tempo para popular sua tabela MAC através do protocolo ARP, antes de conseguir encaminhar os primeiros pacotes corretamente.
**Conflito de IP:** Endereços IP devem ser exclusivos. Um erro de IP duplicado na mesma rede lógica impede a comunicação e o roteamento dos pacotes.
