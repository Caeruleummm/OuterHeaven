# Infraestructura de Xarxa - Empreses, Hotels i Provisioning

Aquesta secció cobreix el disseny i desplegament de la infraestructura de xarxa per a entorns **empresarials**, **residencials** (hotels), i el sistema de **provisionament dinàmic d'usuaris mitjançant PPPoE**. La xarxa de hotels esta segmentada amb VLANs.

## Objectius

- Dissenyar una xarxa flexible i escalable per a diferents segments de clients.
- Garantir separació lògica entre tràfic d’empresa, hotels i serveis interns.
- Implementar un sistema de provisioning d’IP i autenticació amb PPPoE.
- Proporcionar accés controlat a Internet i serveis locals.

---

## Arquitectura General

- Routing entre VLANs controlat via firewall per NAT i regles específiques.
- Accés a Internet controlat amb llistes d'accés i DNS intern.
- Cada servei i client està virtualitzat dins d'una VM/CT a Proxmox.

---

## Xarxa per a Hotels

- Accés només a Internet via PPPoE.
- Limitació de velocitat i trànsit per grup d’usuaris.
- Portal captiu (RADIUS) gestionat per futurs desenvolupaments.

---

## Sistema de Provisioning (PPPoE)

- - Limitació de velocitat i trànsit per grup d’usuaris.
- Assignació dinàmica d’IP i ample de banda per usuari.
- Accés només a Internet via PPPoE.

---

## Components Tècnics

| Component       | Funció                                     |
|------------------|---------------------------------------------|
| DHCP Server Mikrotik  | Assignació IP Local Hotels y Particulars           |
| PPPoE Server     | Provisionament per usuaris hotelers         |
| VLANs i Bridges  | Segmentació de la xarxa en Proxmox          |
| Firewall/NAT     | Control de trànsit entre segments i cap a Internet |
| DNS Intern       | Resolució de serveis interns                |

---

## Casos d’ús simulats

- **Client hoteler**: Només pot establir connexió PPPoE, obtenir IP i navegar per Internet.
- **Administració**: Pot monitoritzar tots els segments i gestionar usuaris des del node de control.

---

## Requisits previs

- Interfícies de xarxa virtualitzades amb suport per VLANs. // borrar inventada del chatgpt total
- Mòduls kernel activats per PPP i pppoe-server.
- Assignació correcta d’adreçament IP per segment.

---

## Consideracions de seguretat

- Totes les VLAN estan tallades per defecte.
- Accés a serveis interns només des de VLANs autoritzades.
- El trànsit PPPoE es filtra mitjançant regles de firewall amb NAT específic.

---

## Millores previstes

- Integració d’un portal web per gestionar usuaris i provisioning (radius + freeradius).
- Control de QoS dinàmic per usuaris PPPoE segons subscripció.
- Visualització gràfica de connexions actives dins Zabbix i scripts d’auditoria.
