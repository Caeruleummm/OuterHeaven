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
- **Rack 2 (Comunicacion)**: Switches, routers, ONU, fibra, pasarelas PPPoE.
- **Separacion funcional para evitar colapso termico o electrico.**

###  Sistema de Refrigeracion

- Sistema **InRow** entre racks, con distribución frontal y posterior.
- Arquitectura **Hot Aisle / Cold Aisle**.
- Sensorizacion en 3 niveles (superior, medio y base) por cada rack.
- Comparativa con otros sistemas:
  - InRow: alta eficiencia, facil mantenimento.
  - Tradicional: menos control termico.
  - CRAC: alto coste y baja flexibilidad.
  - Refrigeracion líquida: compleja y cara, poco recomanable para entornos pequeños.

###  Sistema Electrico y Redundancia

- Doble línia A/B alimentada por **SAI independientes**.
- Sistema de **Transferència Estàtica (STS)** para escoger la fuente electrica mas estable.
- Autonomia minima de 10 minutos para un apagado controlado (SCRAM).
- Supervision y gestion SNMP via Zabbix.
- Comparativa de equipos:
  - Eaton 9PX, APC SRT, Riello Sentinel Pro.

###  Connexion a Internet

- **Doble ISP** con 10Gb/s cada uno (Telefónica i Adamo/Orange).
- Load Balancing entre proveedores mediante rutas diferenciadas.
- Configuracion de politicas de failover automaticas.
- Asignacion de IP publicas para servicios diferenciados.
- Integracion con switch core y router de distribucion.

---

## Subproyectos

Este directorio incluye diferentes areas del diseño del CPD:

- `Cablatge de Xarxa/` → Red estructurada por VLAN y zonas.
- `Sistema de Refrigeracion/` → Infraestructura tèrmica y sensores.
- `Sistema Electric i Redundancia/` → Doble línia y SAI + STS.
- `Distribucio dins dels racks/` → Posicionamiento físico de los equipos.
- `Comunicacio de Racks i distribucio Horizontal/` → Distribucion entre racks.
- `Esquema CPD i distribució/` → Plano general y esquemas de flujos.

---

## 📌 Consideracions finals

El CPD d’OuterHeaven reflecteix una infraestructura professional, amb criteris clars d’escalabilitat i manteniment, i facilita el desplegament de serveis en condicions reals i segures. Ha estat pensat com una prova pilot per simular el funcionament d’un ISP de mida mitjana.
