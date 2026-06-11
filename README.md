# Outer Heaven - Infraestructura ISP Simulada

**Outer Heaven** Es un proyecto que busca imitar una infraestructura propia de un ISP orientado al sector hotelero y residencial. El proyecto integra tecnologías reales empleadas en el entorno profesional para ofrecer servicios de conectividad manteniendo una infraestructura virtualizada con alta disponibilidad, monitorización avanzada y automatización completa. Este proyecto es muy escalable con un presupuesto adecuado para los servicios ofrecidos y desplegados.

## Objectivos Principales

- Desplegar una infraestructura con virtualización de tipo 1 con **Proxmox VE** en clúster.
- Implementar **alta disponibilidad** (HA) de máquinas virtuales (VM/CT) con migraciones en caliente.
- Utilizar **Ceph** como clúster de almacenamiento compartido y balanceo de carga de discos.
- Automatizar la configuración y gestión de servicios con **Ansible**.
- Monitorizar en tiempo real con **Zabbix**, **NetData** e integración con sistemas de notificación.
- Implementar servicios de **DNS interno en alta disponibilidad** con Docker Swarm.
- Proveer un sistema funcional de **aprovisionamiento PPPoE** para clientes particulares y hoteles simulados.
- Gestionar copias de seguridad locales y en la nube de forma automatizada y cambios de configuracion masivos (**Ansible**).
- Implementar un sistema **RADIUS** para Hoteles Simulados.
- Implementar un sistema de limitación de velocidad de ancho de banda imitando un ISP real.

## Estructura del Repositorio 

En este repositorio encontraras la siguiente estructura e informacion del proyecto.

- `/Demos/` → Todas las demostraciones de los servicios y configuraciones más importantes en vídeo.
- `/Diagrames/` → Todos los diagramas/esquemas del proyecto.
- `/Extra/` → Capturas de las configuraciones más importantes del proyecto y cómo reparar un clúster de Proxmox.
- `/Mini Projecte 1 Proxmox/` → Recursos e información sobre el mini proyecto de Proxmox.
- `/Mini Projecte 2 Monitoritatge de Xarxa/` → Recursos e información sobre el mini proyecto de Monitoritatge de Xarxa.
- `/Mini Projecte 3 CPD/` → Recursos e información sobre el mini proyecto de CPD.
- `/Projecte OuterHeaven/` → Recursos e información sobre todo el proyecto personal, diagramas, configuraciones, herramientas a utilizar, infraestructura de red y sistemas, etc.

## Principales Tecnologías Utilizadas

- **Proxmox VE** con clúster y migraciones en caliente
- **Ceph** como almacenamiento compartido con balanceo de carga
- **Zabbix + NetData** para monitorización activa
- **Ansible** para despliegues automatizados y backups
- **Docker Swarm** para servicios como DNS en alta disponibilidad
- **Rclone** para copias en la nube
- **Bash i Yml** Para scripts de sistema y de ansible
- **CPD disseñado con redundancia elèctrica y refrigeracion InRow**
- **LucidChart i DrawIo** Para la creación de diagramas y esquemas.
- **Cloudfare** Como proxy inverso y firewall
- **Mikrotik** Para la creación y configuración de hoteles, clientes particulares, PPPOE, perfiles de velocidad y Radius.
- **Wordpress i Ghost** Para páginas web de la empresa y de un hotel.
- **Trello** Para la gestión de tareas entre los miembros del grupo.
- **TailScale** Como VPN para acceder a Proxmox y la definición de ACL, firewall y subredes.

## Estructura del Proyecto

- `Mini Projecte 1 Proxmox`: Instalación, configuración y entorno de virtualización
- `Mini Projecte 2 Monitoratge de xarxa`: Monitorización con Zabbix, alertas, notificaciones a Telegram y correo y Gráficos.
- `Mini Projecte 3 CPD`: Infraestructura física, racks, refrigeración, diseño eléctrico, ISP
- `Projecte OuterHeaven`: Implementación final de los servicios en entorno virtualizado ( Infraestructura de sistemas y servicios, Seguridad y HA, Clústeres, balanceo de carga, infraestructura ISP e Infraestructura de Red general).

## Autores i Agradecimientos

Proyecto desarollado por Unai Conus i Victor Redel, con el soporte de:

- Orvis360 y Pedro Corregidor (infraestructura y material técnico)
- Víctor Redel y EquemmFoundation (hardware físico dedicado)

PD:

Queremos expresar nuestro sincero agradecimiento a Orvis360 y al señor Pedro Corregidor por su valiosa colaboración en la aportación de conocimientos de nuestro proyecto. Su ayuda en la propuesta y el diseño de la infraestructura de red, así como la cesión de materiales técnicos necesarios, ha sido esencial para alcanzar los objetivos marcados.

También queremos agradecer especialmente a Víctor Redel y a EquemmFoundation por haber patrocinado y facilitado un servidor físico dedicado, que nos ha permitido desplegar un entorno completo con Proxmox y llevar a cabo todo el desarrollo del proyecto dentro de un contexto realista y profesional.
Sin vuestro apoyo, este proyecto no habría sido posible en las mismas condiciones de calidad y aprendizaje.

---
