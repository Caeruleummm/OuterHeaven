# DNS Intern en Alta Disponibilitat amb Docker Swarm

Aquest directori documenta la implementació d’un servei **DNS intern** amb **alta disponibilitat (HA)** desplegat mitjançant
**Docker Swarm**, utilitzant com a resolutor **Bind9** aplicada al ISP simulat.

## Objectius

- Garantir la resolució de noms interna per a serveis i clients dins l’infraestructura.
- Implementar alta disponibilitat per evitar punts únics de fallida.
- Permetre l’autogestió de zones DNS per escenaris hotelers i residencials.

---

## Arquitectura

- **3 nodes Docker Swarm** desplegats com a clúster.
- **1 instàncies DNS activa** (Bind9).
- Zones DNS delegades a Bind9.
- Possibilitat de migració a **Unbound + RPZ** o **Knot Resolver** per a escenaris empresarials reals.

---

## Funcionalitats Implementades

- Zona DNS per serveis de Proxmox, Zabbix, Wordpress, Ghost etc.
- Zones reverses per resolució IP → nom.

---

## Eines i components

| Component         | Funció                            |
|-------------------|------------------------------------|
| Bind9             | Autoritatiu de zones internes      |
| Docker Swarm      | Orquestració i alta disponibilitat |

---

## Requisits previs

- Docker + Docker Compose instal·lat en tots els nodes.
- Port 53 (UDP/TCP) obert i no usat per altres serveis.
- Sistema de resolució per defecte redirigit als servidors DNS interns.

---

## Scripts i configuracions

- `bind9/named.conf.local`: Configuració de zones internes
- `pi-hole/docker-compose.yml`: Definició de servei replicat
- `failover.sh`: Script per controlar DNS actiu

---

## Notes finals

Aquesta arquitectura permet garantir resolució interna de serveis encara que falli un node, i es pot escalar fàcilment per a múltiples zones (empreses, hotels, serveis). És un component crític per garantir l’estabilitat de serveis com Proxmox, monitorització o serveis web interns.
