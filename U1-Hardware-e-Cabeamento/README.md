# 🖥️ U1: Hardware e Cabeamento

## 🎯 Objetivo
[cite_start]Estabelecer e validar a comunicação entre dois computadores através de um switch [cite: 6][cite_start], compreendendo a configuração de endereços IPv4 e o funcionamento básico da camada de enlace[cite: 16].

## 🛠️ Topologia e Endereçamento
[cite_start]A rede foi configurada utilizando a sub-rede `192.168.1.0/24` [cite: 9, 10, 18][cite_start], com os hosts conectados a um switch via cabo de par trançado (Copper Straight-Through)[cite: 11].
* [cite_start]**PC0:** `192.168.1.1` [cite: 9]
* [cite_start]**PC1:** `192.168.1.2` [cite: 10]
* [cite_start]**Máscara de Sub-rede:** `255.255.255.0` [cite: 10]

## 📝 Notas de Estudo (O que aprendi aqui)
* [cite_start]**Tempo de Aprendizado do Switch:** Inicialmente, os pacotes de `ping` podem falhar[cite: 14]. [cite_start]Isso ocorre porque o switch opera na Camada 2 do modelo OSI e precisa de tempo para popular sua tabela MAC através do protocolo ARP, antes de conseguir encaminhar os primeiros pacotes corretamente[cite: 16].
* **Conflito de IP:** Endereços IP devem ser exclusivos. [cite_start]Um erro de IP duplicado na mesma rede lógica impede a comunicação e o roteamento dos pacotes[cite: 20, 21].
