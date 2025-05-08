# Mini Projecte 2 - Monitorització de Xarxa amb Zabbix

Aquest mini projecte desplega un sistema complet de **monitorització activa i temps real** per a l’entorn OuterHeaven, fent servir la potència de **Zabbix**.

## Objectius

- Supervisar estat, rendiment i serveis dels nodes del clúster.
- Detectar anomalies i enviar alertes automàtiques.
- Visualitzar gràfiques detallades de rendiment per a cada dispositiu.
  
## Eines seleccionades

| Eina     | Funció principal                      |
|----------|----------------------------------------|
| Zabbix   | Monitorització per agents, SNMP i traps|
| Gmail    | Servidor de correu per rebre noticacions d'alertes   |
| Telegram | Canal de notificació via Webhooks      |

## Contingut Tècnic

### 1. Instal·lació de Zabbix
- Instal·lació de frontend, base de dades i servidor.
- Desplegament d’agents en nodes Linux i Windows.
- Afegiment semi manual de hosts. 

### 2. Llindars i Alertes
- Creacio de Grafics.
- Notificacions a Telegram i correu electrònic.
- Configuració de dependències i horaris d’actuació.

## Captures i Dashboards
Consulta el document final del projecte i les demos per veure taulers de control, proves de rendiment i captures reals d’anàlisi.

---

## 📎 Propostes de millora futura

- Integrar amb Prometheus + Grafana per escenaris empresarials.
- Utilitzar discovery amb Ansible per adaptar configuracions automàticament.
- Exportar informes de rendiment per setmana amb PDF automatitzat.
