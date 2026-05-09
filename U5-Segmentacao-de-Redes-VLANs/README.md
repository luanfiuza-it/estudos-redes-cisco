# 🛡️ U5: Segmentação de Redes com VLANs e Router-on-a-Stick

## 🎯 Objetivo
Implementar a segmentação lógica de uma rede corporativa utilizando VLANs (Virtual LANs) para isolar departamentos (RH e ADM) e configurar o roteamento inter-VLAN através de subinterfaces em um roteador Cisco.

## 🛠️ Topologia e Endereçamento
Neste cenário, utilizamos um único switch para ambos os departamentos, mas garantimos que um não "enxergue" o tráfego do outro na Camada 2.

* **VLAN 10 (RH):** Rede `192.168.10.0/24` | Gateway: `192.168.10.1`
* **VLAN 20 (ADM):** Rede `192.168.20.0/24` | Gateway: `192.168.20.1`

## 💻 Configurações Principais (Cisco IOS)

### No Switch (Camada 2)
Criação das fronteiras lógicas e configuração do tronco (Trunk) para o roteador:
```bash
vlan 10
 name RH
vlan 20
 name ADM
exit

interface range fa0/1 - 5
 switchport mode access
 switchport access vlan 10

interface Gig0/1
 switchport mode trunk
 description LINK_PARA_ROTEADOR
