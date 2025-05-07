# Outer Heaven - Infraestructura ISP Simulada

**Outer Heaven** és un projecte final que simula una infraestructura pròpia d’un ISP orientat al sector hoteler i residencial. El projecte integra tecnologies reals emprades a l’entorn professional per oferir serveis de connectivitat i virtualització amb alta disponibilitat, monitorització avançada i automatització completa.

## Objectius Principals

- Desplegar una infraestructura amb virtualització de tipus 1 amb **Proxmox VE** en clúster.
- Implementar **alta disponibilitat** (HA) de màquines virtuals (VM/CT) amb migracions en calent.
- Utilitzar **Ceph** com a clúster d’emmagatzematge compartit i balanceig de càrrega de discos.
- Automatitzar la configuració i gestió de serveis amb **Ansible**.
- Monitoritzar en temps real amb **Zabbix**, **NetData** i integració amb sistemes de notificació.
- Implementar serveis de **DNS intern en alta disponibilitat** amb Docker Swarm.
- Proveir un sistema funcional de **provisionament PPPoE**.
- Gestionar còpies de seguretat locals i en el núvol de forma automatitzada.

## Estructura del Repositori

- `/proxmox-cluster/` → Configuració del clúster de virtualització Proxmox VE amb alta disponibilitat.
- `/ceph-storage/` → Configuració detallada del clúster Ceph i emmagatzematge compartit.
- `/monitoring/` → Implementació de Zabbix, NetData i integració amb alertes.
- `/dns-ha/` → Clúster DNS en alta disponibilitat amb Docker Swarm.
- `/ansible/` → Playbooks i automatitzacions diverses amb Ansible.
- `/backups/` → Sistema de còpies de seguretat automatitzades amb Proxmox Backup Server i Rclone.
- `/cpd-design/` → Disseny físic i lògic del centre de processament de dades (CPD).

## Requisits

- Proxmox VE 8.x
- Ceph Octopus o posterior
- Ansible ≥ 2.9
- Docker Swarm
- Zabbix 6.x
- Accés a S3/OneDrive via Rclone

## Autors i Agraïments

Projecte desenvolupat per Unai Conus i Victor Redel, amb el suport de:

- Orvis360 i Pedro Corregidor (infraestructura i material tècnic)
- Víctor Redel i EquemmFoundation (hardware físic dedicat)

---
