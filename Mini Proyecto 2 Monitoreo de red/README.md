# Mini Proyecto 2 - Monitorizacion de Red con Zabbix

Este miniproyecto despliega un sistema completo de **monitorizacion activo y en tiempo real** para el entorno OuterHeaven, utilizando la herramienta de **Zabbix y NetData**.

## Objetivos

- Supervisar estado, rendimiento y servicios de los nodos del clúster.
- Detectar anomalías y enviar alertas automáticas.
- Visualizar gráficas detalladas de rendimiento para cada dispositivo.
  
## Herramientas Seleccionadas

| Eina     | Funció principal                      |
|----------|----------------------------------------|
| Zabbix   | Monitorización por agentes, SNMP y traps|
| NetData  | Monitoritzacion del cluster de Proxmox|
| Gmail    | Servidor de correo para recibir notificaciones de alertas   |
| Telegram | Canal de notificación vía Webhooks.     |

## Contenido Tecnico

### 1. Instalacion de Zabbix
- Instalación de frontend, base de datos y servidor.
- Despliegue de agentes en nodos Linux y Windows.
- Añadido semimanual de hosts.

### 2. Umbrales y Alertas.
- Creacion de Graficos.
- Notificaciones en Telegram y correo electronico.
- Configuracion de dependencias y horarios de actuacion.

## Capturas y Dashboards
Consulte el documento final del proyecto y las demostraciones para visualizar los paneles de control, las pruebas de rendimiento y las capturas de análisis

---

## 📎 Propuestas de futuras mejoras

- Integrar con Prometheus + Grafana para escenarios empresariales.
- Utilizar discovery con Ansible para adaptar configuraciones automáticamente.
- Exportar informes de rendimiento semanales en PDF automatizado.
