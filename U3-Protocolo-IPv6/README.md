# 🌐 U3: Protocolo IPv6

## 🎯 Objetivo
Configurar uma infraestrutura de rede utilizando o novo padrão de endereçamento IPv6, garantindo o roteamento e a comunicação entre dispositivos de sub-redes distintas[cite: 351, 352].

## 🛠️ Topologia e Endereçamento
* **Sub-rede 1:** Prefixo `2001:DB8:1::/64` (Gateway: `2001:DB8:1::1`)[cite: 357].
* **Sub-rede 2:** Prefixo `2001:DB8:2::/64` (Gateway: `2001:DB8:2::1`)[cite: 357].

### Comandos de Roteamento IPv6
```bash
interface gigabitEthernet 0/0
ipv6 address 2001:DB8:1::1/64
no shutdown
exit
ipv6 unicast-routing
