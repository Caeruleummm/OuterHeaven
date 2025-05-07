# Infraestructura de Xarxa - Empreses, Hotels i Provisioning

Aquesta secció cobreix el disseny i desplegament de la infraestructura de xarxa per a entorns **empresarials**, **residencials** (hotels), i el sistema de **provisionament dinàmic d'usuaris mitjançant PPPoE**. La xarxa ha estat segmentada amb VLANs, control de trànsit i alta disponibilitat.

## Objectius

- Dissenyar una xarxa flexible i escalable per a diferents segments de clients.
- Garantir separació lògica entre tràfic d’empresa, hotels i serveis interns.
- Implementar un sistema de provisioning d’IP i autenticació amb PPPoE.
- Proporcionar accés controlat a Internet i serveis locals.

---

## Arquitectura General

- Segmentació mitjançant VLANs:
  - VLAN 10: Gestió interna
  - VLAN 20: Serveis interns (DNS, Zabbix, NFS, etc.)
  - VLAN 30: Xarxa d’empreses
  - VLAN 40: Xarxa d’hotels
  - VLAN 50: Provisioning i tràfic PPPoE
- Routing entre VLANs controlat via firewall per NAT i regles específiques.
- Accés a Internet controlat amb llistes d'accés i DNS intern.
- Cada servei i client està virtualitzat dins d'una VM/CT a Proxmox.

---

## Xarxa per a Empreses

- Assignació d’IP per DHCP gestionat per servidor central.
- Accés a recursos compartits (TrueNAS, carpetes compartides, DNS intern).
- Segmentació per departaments dins de la VLAN empresarial.
- Polítiques de tallafoc més permissives per a serveis administratius.

---

## Xarxa per a Hotels

- Entorns aïllats per client final amb microsegmentació.
- Accés només a Internet via PPPoE.
- Limitació de velocitat i trànsit per grup d’usuaris.
- Portal captiu gestionat per futurs desenvolupaments.

---

## Sistema de Provisioning (PPPoE)

- Servei desplegat en contenidor amb autenticació local (fitxer o base de dades).
- Assignació dinàmica d’IP i ample de banda per usuari.
- Integració amb scripts de Zabbix per controlar autenticació.
- Simula l’entorn d’un ISP real, permetent gestió i control del servei per usuari.

---

## Components Tècnics

| Component       | Funció                                     |
|------------------|---------------------------------------------|
| ISC DHCP Server  | Assignació IP per VLAN empreses             |
| PPPoE Server     | Provisionament per usuaris hotelers         |
| VLANs i Bridges  | Segmentació de la xarxa en Proxmox          |
| Firewall/NAT     | Control de trànsit entre segments i cap a Internet |
| DNS Intern       | Resolució de serveis interns                |
| Switchs VLAN-aware | Suport per etiquetatge de trànsit         |

---

## Casos d’ús simulats

- **Client empresa**: Accedeix a serveis interns, carpetes compartides i Internet.
- **Client hoteler**: Només pot establir connexió PPPoE, obtenir IP i navegar per Internet.
- **Administració**: Pot monitoritzar tots els segments i gestionar usuaris des del node de control.

---

## Requisits previs

- Interfícies de xarxa virtualitzades amb suport per VLANs.
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
