# OSPF Multi-Area Lab — Cisco Packet Tracer

## 🎯 Objetivo
Implementar OSPF multiárea para simular expansão de rede corporativa,
com backbone Area 0 e filiais nas Areas 1 e 2.

## 🧠 Conceitos Aplicados
- OSPF Single Area
- OSPF Multi-Area
- Area Border Router (ABR)
- Router ID manual
- Passive Interfaces
- Métrica OSPF (Cost)
- Inter-area routing (O IA)

## 🗺️ Topologia
### Logical Topology
![Topology](topology.png)

## 🌐 Plano de Endereçamento
| Segmento | Rede |
|---------|------|
| LAN A | 192.168.10.0/24 |
| LAN B | 192.168.20.0/24 |
| LAN C | 192.168.30.0/24 |
| LAN D | 192.168.40.0/24 |
| R1–R2 | 10.0.0.0/30 |
| R2–R3 | 10.0.0.4/30 |
| R1–R4 | 10.0.0.8/30 |

## ⚙️ Configuração dos Roteadores
Arquivos disponíveis em `/configs`

## 🔍 Validação
Arquivos disponíveis em `/validation`

## ✅ Resultados
- Todas as áreas formaram adjacência FULL
- Rotas intra-área e inter-área propagadas
- Conectividade fim-a-fim validada

## 🧪 Ambiente de Simulação
Simulado no Cisco Packet Tracer

## 🏢 Aplicação no Mundo Real
Cenário semelhante a:
- Expansão de filiais corporativas
- Redes campus multiárea
- Backbone empresarial
