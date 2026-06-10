
# Esquemas y Diagramas del Proyecto Outer Heaven

Este directorio contiene los **diagramas funcionales, lógicos y físicos** que representan la arquitectura, la virtualización, la infraestructura física, la automatización y el sistema de monitorización del proyecto Outer Heaven. Cada elemento gráfico ha sido elaborado para ofrecer una visión clara y detallada de los componentes clave del sistema, y se utiliza como referencia tanto para el despliegue como para la documentación.

---

## Infraestructura Física i CPD

### `Esquema_Racks_Frontal_OH.png`
Vista frontal de los racks del CPD, mostrando la distribución vertical de los equipos por función: servidores, switches, SAI y unidades de comunicación. Se diferencia claramente el rack de **procesamiento** y el de **comunicacion**.

### `diagramaFrontalCPD_OH_Bruto.png`  
Versión preliminar del frontal de racks, realizada para la planificación inicial. Muestra el etiquetado físico y el posicionamiento estimado de los componentes.

### `CPD_Clase_Diagrama_Bruto.drawio.png`
Esquema inicial del CPD creado durante las sesiones de planificación.

---

## Infraestructura Virtual y Proxmox

### `DiagramaInfraestructura_Virtual_Proxmox_OH.drawio`  
Archivos editables `.drawio` con la infraestructura virtual completa desplegada con Proxmox: nodos del clúster, interconexiones, Ceph y relaciones entre máquinas.

### `DiagramaInfraestructura_Virtual_Proxmox_OH.drawio.png`  
Versión exportada en imagen del diagrama anterior, pensada para ser incluida en documentación impresa o PDF.

### `ServerDiagramOH.png`  
Diagrama general de interconexión entre hipervisores, servicios esenciales, Docker Swarm, clientes y servicios de monitorización. Muestra tanto la conexión lógica como la asignación de roles por máquina.

---

## Arquitectura Global del Proyecto

### `Diagrama General OH - Página 1.png`
Esquema integrado de todo el proyecto: entorno virtual, CPD físico, servicios desplegados, canales de monitorización y flujos de datos. Es el diagrama de más alto nivel y resume Outer Heaven como infraestructura ISP simulada.

---

## Automatitzacion y Backups (Ansible)

### `ansible_copiasSeguretat_automatitzacio_OH.drawio`  
Diagrama del proceso de automatización de copias de seguridad con Ansible, mostrando los pasos de ejecución, validación, subida a la nube y borrado temporal local.

### `ansible_copiasSeguretat_automatitzacio_OH.drawio.png`  
Versión exportada del diagrama anterior en formato imagen.

---

## Monitorizacion y Alertas

### `diagramaMonitorizacion_OH.drawio`  
Arquitectura de monitorización con Zabbix, NetData y agentes. Se muestra cómo se distribuyen las funciones de monitorización, el flujo de datos hacia el servidor central y la jerarquía de triggers y alertas.

### `diagramaMonitorizacion_OH.drawio.png`  
Versión visual exportada del mismo esquema, para incluir en informes.

### `diagrama_alertas_notificacions_OH.drawio`  
Flujo de alertas y notificaciones. Muestra qué acciones se generan ante un evento y cómo se comunican (Telegram, Discord, correo) y si hay acción correctiva automática.

### `diagrama_alertas_notificacions_OH.drawio.png`  
Versión visual del flujo anterior.

---

## Provisionamiento y Gestion de Usuarios

### `PPPChart1.png`
Diagrama de flujo del servicio de provisioning PPPoE para clientes hoteleros, incluyendo conexión, autenticación, asignación de IP y control de ancho de banda.

---

## Formato y Edicion

- Los archivos `.drawio` han sido creados a traves de: [diagrams.net](https://www.diagrams.net/).

