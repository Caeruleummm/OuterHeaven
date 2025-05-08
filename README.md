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

En aquest repositori trovaras la seguent estructura e informacio del projecte.

- `/Demos/` → Totes les demostracions dels serveis i configuracions mes importants en video.
- `/Diagrames/` → Tots els diagrames/esquemas del projecte.
- `/Extra/` → Captures de les configuracions mes importants del projecte i com reparar un cluster de Proxmox.
- `/Mini Projecte 1 Proxmox/` → Recursos e informacio sobre el mini projecte de Proxmox .
- `/Mini Projecte 2 Monitoritatge de Xarxa/` → Recursos e informacio sobre el mini projecte de Monitoritatge de Xarxa.
- `/Mini Projecte 3 CPD/` → Recursos e informacio sobre el mini projecte de CPD.
- `/Projecte OuterHeaven/` → Recursos e informacio sobre tot el projecte personal, diagrames, configuracions, eines a servir, infraestructura de xarxa i sistemas etc.

## Principals Tecnologies Utilitzades

- **Proxmox VE** amb clúster i migracions en calent
- **Ceph** com a emmagatzematge compartit amb balanceig de càrrega
- **Zabbix + NetData** per monitorització activa
- **Ansible** per a desplegaments automatitzats i backups
- **Docker Swarm** per serveis com DNS en alta disponibilitat
- **Rclone** per còpies en núvol
- **Bash i Yml** Per a scripts de sistema i de ansible
- **CPD dissenyat amb redundància elèctrica i refrigeració InRow**
- **LucidChart i DrawIo** Per a la creacio de diagrames i esquemas.
- **Cloudfare** Com a proxy invers i firewall
- **Mikrotik** Per a la creacio i configuracio d'hotels, clients particulars , PPPOE, perfils de velocitat i Radius.
- **Wordpress i Ghost** Per a pagines web de l'empresa i d'un hotel.
- **Trello** Per la gestio de tasques entre els membres del grup.
- **TailScale** Com a VPN per accedir a Proxmox i la definicio d'Acl, firewall i subxarxes.

## Estructura del Projecte

- `Mini Projecte 1 Proxmox`: Instal·lació, configuració i entorn de virtualització
- `Mini Projecte 2 Monitoratge de xarxa`: Monitorització amb Zabbix, alertes, notificacions a Telegram i correu i Grafics.
- `Mini Projecte 3 CPD`: Infraestructura física, racks, refrigeració, disseny elèctric, ISP
- `Projecte OuterHeaven`: Implementació final dels serveis en entorn virtualitzat ( Infraestructura de sistemas i serveis, Seguretat y HA, Clusters,
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
