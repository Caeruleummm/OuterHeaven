
# Demos de Funcionament – Outer Heaven

Este directorio recoge una serie de vídeos demostrativos que validan funcionalidades clave del proyecto **Outer Heaven** en escenarios prácticos. Cada vídeo muestra acciones realizadas en tiempo real sobre la infraestructura simulada, con el objetivo de verificar la estabilidad, la automatización y la capacidad de recuperación del sistema.

---

## Indice de Demos

### Automatitzacion y Copias de Seguridad

- **CopiaSeguretatAutomatitzada.wmv**  
  Ejecución automatizada de una copia de seguridad local cada 3 días a las 3 am (ejemplo).

- **CrearCopiaSeguretat.wmv**  
  Realización semi-manual de una copia de seguridad a través de un script de ansible.

- **CrearSnapshot.wmv**  
  Generación de un snapshot instantáneo para una máquina virtual a través de un script de ansible.

- **RestauracioInstantanea.wmv**  
  Restauración inmediata de una VM a partir de un backup creado anteriormente.

- **RestauracionCopiaSeguridad.wmv**  
  Recuperación de un entorno completo después de hacer cambios a una VM (demostración).

---

### Alta Disponibilidad y Migraciones

- **MigracioCalent.wmv**  
  Migración en caliente de una máquina virtual entre dos nodos Proxmox, sin downtime ni interrupción del servicio.

- **MigracioVMCaidaNode.wmv**  
    Simulación de caída de un nodo y migración automática de la máquina hacia un nodo disponible mediante sistema HA.

---

### Monitoritzacion y Alertas

- **AlertaZabbix.wmv**  
  Recepción y gestión de una alerta generada por Zabbix en caso de caída de alguna VM de Proxmox y notificación por correo y Telegram.

- **SolucioAlertaZabbix.wmv**  
  Acción correctiva automatizada y resolución de la alerta generada anteriormente.

- **AlertaNetDataNode.wmv**  
  Detección en tiempo real de una caída de un nodo de Proxmox y la notificación por Discord.

- **RecuperacioAlertaNetData.wmv**  
  Normalización de los valores monitorizados y confirmación automática de la recuperación del estado del nodo.

- **AfegirClientZabbix.wmv**  
  Proceso completo para añadir un nuevo host al sistema de monitorización Zabbix, con asignación de plantilla y validación de estado.

---

## Finalitat de les Demos

Aquest conjunt de vídeos té com a objectiu demostrar que l’entorn Outer Heaven:
- Funciona com una infraestructura real d’un ISP.
- Respon correctament davant escenaris de fallida i recuperació.
- Automatitza processos clau com backups, migracions i notificacions.
- Garanteix un entorn monitoritzat i auto-recuperable.

Els vídeos constitueixen **proves d’acceptació** i serveixen de referència per avaluar el projecte des de la perspectiva de fiabilitat, manteniment i escalabilitat.

