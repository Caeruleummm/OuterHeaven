
# Esquemes i Diagrames del Projecte Outer Heaven

Aquest directori conté els **diagrames funcionals, lògics i físics** que representen l'arquitectura, la virtualització, la infraestructura física, l'automatització i el sistema de monitoratge del projecte Outer Heaven. Cada element gràfic ha estat elaborat per oferir una visió clara i detallada dels components clau del sistema, i s'utilitza com a referència tant per al desplegament com per a la documentació.

---

## Infraestructura Física i CPD

### `Esquema_Racks_Frontal_OH.png`
Vista frontal dels racks del CPD, mostrant la distribució vertical dels equips per funció: servidors, switchos, SAI i unitats de comunicació. Es diferencia clarament el rack de **processament** del de **comunicació**.

### `diagramaFrontalCPD_OH_Bruto.png`  
Versió preliminar del frontal de racks, feta per a planificació inicial. Mostra etiquetatge físic i posicionament estimat de components.

### `CPD_Clase_Diagrama_Bruto.drawio.png`
Esquema inicial del CPD creat durant les sessions de planificació.

---

## Infraestructura Virtual i Proxmox

### `DiagramaInfraestructura_Virtual_Proxmox_OH.drawio`  
Arxiu editables `.drawio` amb la infraestructura virtual completa desplegada amb Proxmox: nodes del clúster, interconnexions, Ceph i relacions entre màquines.

### `DiagramaInfraestructura_Virtual_Proxmox_OH.drawio.png`  
Versió exportada en imatge del diagrama anterior, pensada per a ser inclosa en documentació impresa o PDF.

### `ServerDiagramOH.png`  
Diagrama general d’interconnexió entre hipervisors, serveis essencials, docker Swarm, clients i serveis de monitoratge. Mostra tant la connexió lògica com l’assignació de rols per màquina.

---

## Arquitectura Global del Projecte

### `Diagrama General OH - Página 1.png`
Esquema integrat de tot el projecte: entorn virtual, CPD físic, serveis desplegats, canals de monitoratge i fluxos de dades. És el diagrama de més alt nivell i resumeix Outer Heaven com a infraestructura ISP simulada.

---

## Automatització i Backups (Ansible)

### `ansible_copiasSeguretat_automatitzacio_OH.drawio`  
Diagrama del procés d'automatització de còpies de seguretat amb Ansible, mostrant els passos d’execució, validació, pujada al núvol i esborrat temporal local.

### `ansible_copiasSeguretat_automatitzacio_OH.drawio.png`  
Versió exportada del diagrama anterior en format imatge.

---

## Monitoratge i Alertes

### `diagramaMonitorizacion_OH.drawio`  
Arquitectura de monitoratge amb Zabbix, NetData i agents. Es mostra com es distribueixen les funcions de monitoratge, el flux de dades cap al servidor central i la jerarquia de triggers i alertes.

### `diagramaMonitorizacion_OH.drawio.png`  
Versió visual exportada del mateix esquema, per incloure a informes.

### `diagrama_alertas_notificacions_OH.drawio`  
Flux d’alertes i notificacions. Mostra quines accions es generen davant d’un esdeveniment i  com es comuniquen (Telegram, Discord, correu) i si hi ha acció correctiva automàtica.

### `diagrama_alertas_notificacions_OH.drawio.png`  
Versió visual del flux anterior.

---

## Provisionament i Gestió d'Usuaris

### `PPPChart1.png`
Diagrama de flux del servei de provisioning PPPoE per a clients hotelers, incloent connexió, autenticació, assignació IP, i control d’ample de banda.

---

## Format i Edició

- Els fitxers `.drawio` han sigut creats a traves de: [diagrams.net](https://www.diagrams.net/).

