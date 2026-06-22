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

Documento con instrucciones paso a paso para solucionar errores frecuentes de sincronización y quórum dentro del clúster de Proxmox. Incluye:

- Reinicio del servicio.
- Comprobación de conexiones Corosync.
- Reasignación de nodos y forzado de quórum.

Este archivo es esencial para garantizar la resiliencia del clúster.

---

## Notas finales

Este apartado funciona como **anexo visual**, complementario a las fases principales del proyecto, y refleja el proceso real de despliegue.
Todas las capturas tienen valor como evidencia de configuración y ejecución técnica.

Esta sección contiene capturas que se consideran importantes, es por esto que no se encuentra todo el anexo completo, para visualizar toda la instalación, configuración y demostración de toda la infraestructura
se recomienda consultar el documento final del proyecto que recoge toda esta información de los anexos.

Se puede acceder para consultar dudas específicas, comparar configuraciones o reutilizar estructuras en futuros proyectos.

