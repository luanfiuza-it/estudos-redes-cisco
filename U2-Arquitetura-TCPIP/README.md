# 🖧 U2: Arquitetura TCP/IP

## 🎯 Objetivo
[cite_start]Criar uma topologia abrangendo duas sub-redes interconectadas por um roteador central, realizando a configuração de endereços IP e gateways para garantir a comunicação[cite: 156].

## 🛠️ Topologia e Endereçamento
[cite_start]O cenário conta com duas redes /24 ligadas a um Roteador (Router0)[cite: 158].
* [cite_start]**Sub-rede 1:** `192.168.1.0/24` (Gateway na GigabitEthernet 0/0: `192.168.1.1`)[cite: 159].
* [cite_start]**Sub-rede 2:** `192.168.2.0/24` (Gateway na GigabitEthernet 0/1: `192.168.2.1`)[cite: 159].

### Comandos Cisco IOS Utilizados no Roteador
```bash
enable
configure terminal
interface gigabitEthernet 0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
