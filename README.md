# Outer Heaven - Infraestructura ISP Simulada

**Outer Heaven** és un projecte final que simula una infraestructura pròpia d’un ISP orientat al sector hoteler i residencial. El projecte integra tecnologies reals empleades a l’entorn professional per oferir serveis de connectivitat mantenint una virtualització amb alta disponibilitat, monitorització avançada i automatització completa (simulacio). Aquest projecte es molt escalable amb un presupost adecuat per als serveis oferits y desplegats ( en aquest cast el presupost d'aquest projecte a sigut nul).

## Objectius Principals

- Desplegar una infraestructura amb virtualització de tipus 1 amb **Proxmox VE** en clúster.
- Implementar **alta disponibilitat** (HA) de màquines virtuals (VM/CT) amb migracions en calent.
- Utilitzar **Ceph** com a clúster d’emmagatzematge compartit i balanceig de càrrega de discos.
- Automatitzar la configuració i gestió de serveis amb **Ansible**.
- Monitoritzar en temps real amb **Zabbix**, **NetData** i integració amb sistemes de notificació.
- Implementar serveis de **DNS intern en alta disponibilitat** amb Docker Swarm.
- Proveir un sistema funcional de **provisionament PPPoE** a clients particulars i hotels simulats.
- Gestionar còpies de seguretat locals i en el núvol de forma automatitzada (Ansible).
- Implementar un sistema **RADIUS** per a Hotels Simulats.
- Implementar un sistema de limitacio de velocitat d'amplada de banda imitant un ISP real.

## Estructura del Repositori

- `/proxmox-cluster/` → Configuració del clúster de virtualització Proxmox VE amb alta disponibilitat.
- `/ceph-storage/` → Configuració detallada del clúster Ceph i emmagatzematge compartit.
- `/monitoring/` → Implementació de Zabbix, NetData i integració amb alertes.
- `/dns-ha/` → Clúster DNS en alta disponibilitat amb Docker Swarm.
- `/ansible/` → Playbooks i automatitzacions diverses amb Ansible.
- `/backups/` → Sistema de còpies de seguretat automatitzades amb Proxmox Backup Server i Rclone.
- `/cpd-design/` → Disseny físic i lògic del centre de processament de dades (CPD).

## Principals Tecnologies Utilitzades

- **Proxmox VE** amb clúster i migracions en calent
- **Ceph** com a emmagatzematge compartit amb balanceig de càrrega
- **Zabbix + NetData** per monitorització activa
- **Ansible** per a desplegaments automatitzats i backups
- **Docker Swarm** per serveis com DNS en alta disponibilitat
- **Rclone** per còpies en núvol
- **CPD dissenyat amb redundància elèctrica i refrigeració InRow**

## Estructura del Projecte

- `Mini Projecte 1 Proxmox`: Instal·lació, configuració i entorn de virtualització
- `Mini Projecte 2 Monitoratge de xarxa`: Monitorització amb Zabbix
- `Mini Projecte 3 CPD`: Infraestructura física, racks, refrigeració, disseny elèctric, ISP
- `Projecte OuterHeaven`: Implementació final dels serveis en entorn realista ( Infraestructura de sistemas i serveis, Seguretat y HA, Clusters,
balanceig de carrega, infraestructura ISP i Infraestructura de Xarxa general).

## Autors i Agraïments

Projecte desenvolupat per Unai Conus i Victor Redel, amb el suport de:

- Orvis360 i Pedro Corregidor (infraestructura i material tècnic)
- Víctor Redel i EquemmFoundation (hardware físic dedicat)

PD:

Volem expressar el nostre sincer agraïment a Orvis360 i al senyor Pedro Corregidor per la seva valuosa col·laboració en el aportament de coneixements del nostre projecte. La seva ajuda en la proposta i el disseny de la infraestructura de xarxa, així com la cessió de materials tècnics necessaris, ha estat essencial per assolir els objectius marcats.
També volem agrair especialment a Víctor Redel i a EquemmFoundation per haver patrocinat i facilitat un servidor físic dedicat, que ens ha permès desplegar un entorn complert amb Proxmox i dur a terme tot el desenvolupament del projecte dins d’un context realista i professional.
Sense el vostre suport, aquest projecte no hauria estat possible en les mateixes condicions de qualitat i aprenentatge.

---
