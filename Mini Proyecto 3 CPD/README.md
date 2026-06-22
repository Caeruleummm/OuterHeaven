# Mini Proyecto 3 - Diseño y Infraestructura del Centro de Procesamiento de Datos (CPD)

Este miniproyecto describe el diseño físico y lógico del CPD del proyecto OuterHeaven, con el objetivo de garantizar **alta disponibilidad**, **redundància**, **seguridad física y logica**, y **eficiencia energetica**.

## Objetivos

- Diseñar un CPD escalable y modular con dos racks diferenciados.
- Aplicar mejores prácticas en refrigeración, alimentación y distribución de red.
- Simular un entorno profesional de telecomunicaciones con ISP doble, balanceo y redundancia completa.
- Definir una arquitectura de racks ordenada y funcional.

---

## Contenido Tecnico

###  Estructura General del CPD

- **Rack 1 (Procesamiento)**: Proxmox, TrueNAS, SAI.
- **Rack 2 (Comuniacion)**: Switchos, routers, ONU, fibra, passarel·les PPPoE.
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
