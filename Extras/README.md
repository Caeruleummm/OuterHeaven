# Recursos Adicionales – Capturas i Configuraciones

Este directorio contiene un conjunto de **capturas de pantalla y documentos graficos** utilitzats durant el desenvolupament, instal·lació i configuració de diferents serveis i entorns relacionats amb el projecte Outer Heaven. Es tracta d’informació complementària no inclosa en altres seccions principals, però que resulta útil com a **referència visual** i per validar la **traçabilitat del projecte**.

---

## Capturas de Configuracion de Servicios

Este apartado incluye pruebas y capturas relacionadas con:

- Configuración de servidores DHCP.
- Configuración de perfiles PPPoE.
- Pools de direcciones IP y gestión de VLANs.
- Conexión entre OLT y bridges.
- Servicios PPP Server, secrets, clientes y validación de conexiones.

Esta información es clave para entender cómo se implementó el provisioning de clientes y la segmentación de servicios dentro de la infraestructura de red.

---

## `chr-ont/` – Simulacion y gestion de la ONT/OLT

Capturas relacionadas con:

- Creación de bridges entre interfaces.
- Asignación de pools IP públicos.
- Perfiles de limitación de ancho de banda.
- Configuración del servidor PPPoE y secretos.
- Validación final de conexión desde el client.

Estas pruebas representan la parte más cercana al comportamiento real de un ISP, con una estructura modular y escalable para futuros clientes.

---

## `hotelejemplo/` – Ejemplo de un cliente Hotelero

Incluye capturas de configuración de red para un entorno hotelero:

- Creación de VLANs específicas.
- Pools DHCP para usuarios finales.
- Configuración de NAT (masquerading).
- Validación desde máquinas virtuales Windows.
- Asignación IP y visibilidad interna.

Serveix com a prova pilot de la segmentació d’un entorn hoteler típic dins la infraestructura simulada.

---

## `instalar proxmox/` – Instalacion de Proxmox VE

Capturas detalladas del proceso de instalación del hipervisor Proxmox VE:

- Elección de disco y sistema de archivos ZFS.
- Configuración inicial de la IP de gestión.
- Instalación GUI y acceso al nodo principal.

Este apartado ayuda a documentar el punto de partida para la virtualización del proyecto.

---

## `instalar truenas/` – Instalación de TrueNAS SCALE

Proceso completo de instalación de TrueNAS como sistema de almacenamiento:

- Creación del pool principal.
- Configuración de datasets y permisos.
- Activación de servicios NFS, SMB e iSCSI.
- Preparación de recursos compartidos para la infraestructura virtual.

Es el origen del sistema de archivos compartidos que alimenta Proxmox y otros servicios críticos.

---

## `RepararCluster.md`

Document amb instruccions pas a pas per a solucionar errors freqüents de sincronització i quorum dins el clúster de Proxmox. Inclou:

- Reinici de serveis.
- Comprovació de connexions Corosync.
- Reassignació de nodes i forçat de quorum.

Aquest fitxer és essencial per garantir la resiliència del clúster.

---

## Notes finals

Aquest apartat funciona com a **anex visual**, complementari a les fases principals del projecte, i reflecteix el procés real de desplegament.
Totes les captures tenen valor com a evidència de configuració i execució tècnica.

Aquesta seccio conte captures que es consideren importants, es per aixo que no es troba tot el annex complet, per visualitzar tota la instalacio, configuracio i demostracio tota la infraestructura
es recomena consultar el document final del projecte que recull tota aquesta informacio dels annexos.

S’hi pot accedir per consultar dubtes específics, comparar configuracions o reutilitzar estructures en futurs projectes.

