# Mini Projecte 3 - Disseny i Infraestructura del Centre de Processament de Dades (CPD)

Aquest mini projecte descriu el disseny físic i lògic del CPD del projecte OuterHeaven, amb l’objectiu de garantir **alta disponibilitat**, **redundància**, **seguretat física i lògica**, i **eficiència energètica**.

## Objectius

- Dissenyar un CPD escalable i modular amb dos racks diferenciats.
- Aplicar millors pràctiques en refrigeració, alimentació i distribució de xarxa.
- Simular un entorn professional de telecomunicacions amb ISP doble, balanceig i redundància completa.
- Definir una arquitectura de racks ordenada i funcional.

---

## Contingut Tècnic

###  Estructura General del CPD

- **Rack 1 (Processament)**: Proxmox, TrueNAS, SAI.
- **Rack 2 (Comunicació)**: Switchos, routers, ONU, fibra, passarel·les PPPoE.
- **Separació funcional per evitar col·lapse tèrmic o elèctric.**

###  Sistema de Refrigeració

- Sistema **InRow** entre racks, amb distribució frontal i posterior.
- Arquitectura **Hot Aisle / Cold Aisle**.
- Sensorització en 3 nivells (superior, mig i base) per cada rack.
- Comparativa amb altres sistemes:
  - InRow: alta eficiència, fàcil manteniment.
  - Tradicional: menys control tèrmic.
  - CRAC: alt cost i baixa flexibilitat.
  - Refrigeració líquida: complexa i cara, poc recomanable per entorns petits.

###  Sistema Elèctric i Redundància

- Doble línia A/B alimentada per **SAI independents**.
- Sistema de **Transferència Estàtica (STS)** per triar font elèctrica més estable.
- Autonomia mínima de 10 minuts per apagada controlada (SCRAM).
- Supervisió i gestió SNMP via Zabbix.
- Comparativa d’equips:
  - Eaton 9PX, APC SRT, Riello Sentinel Pro.

###  Connexió a Internet

- **Doble ISP** amb 10Gb/s cadascun (Telefónica i Adamo/Orange).
- Load Balancing entre proveïdors mitjançant rutes diferenciades.
- Configuració de política de failover automàtic.
- Assignació d’IP públiques per a serveis diferenciats.
- Integració amb switch core i router de distribució.

---

## Subprojectes

Aquest directori inclou diferents àrees del disseny CPD:

- `Cablatge de Xarxa/` → Xarxa estructurada per VLAN i zones.
- `Sistema de Refrigeracion/` → Infraestructura tèrmica i sensors.
- `Sistema Electric i Redundancia/` → Doble línia i SAI + STS.
- `Distribucio dins dels racks/` → Posicionament físic dels equips.
- `Comunicacio de Racks i distribucio Horizontal/` → Distribució entre racks.
- `Esquema CPD i distribució/` → Plànol general i esquemes de flux.

---

## 📌 Consideracions finals

El CPD d’OuterHeaven reflecteix una infraestructura professional, amb criteris clars d’escalabilitat i manteniment, i facilita el desplegament de serveis en condicions reals i segures. Ha estat pensat com una prova pilot per simular el funcionament d’un ISP de mida mitjana.
