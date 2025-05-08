
# Demos de Funcionament – Outer Heaven

Aquest directori recull una sèrie de vídeos demostratius que validen funcionalitats clau del projecte **Outer Heaven** en escenaris pràctics. Cada vídeo mostra accions realitzades en temps real sobre la infraestructura simulada, amb l’objectiu de verificar l’estabilitat, l'automatització i la capacitat de recuperació del sistema.

---

## Índex de Demos

### Automatització i Còpies de Seguretat

- **CopiaSeguretatAutomatitzada.wmv**  
  Execució automatitzada d’una còpia de seguretat local cada 3 dies a las 3 am (exemple).

- **CrearCopiaSeguretat.wmv**  
  Realització semi-manual d’una còpia de seguretat a través d'un script d'ansible.

- **CrearSnapshot.wmv**  
  Generació d’un snapshot instantani per a una màquina virtual a traves d'un script d'ansible.

- **RestauracioInstantanea.wmv**  
  Restauració immediata d’una VM a partir d’un backup creat anteriorment.

- **RestauracionCopiaSeguridad.wmv**  
  Recuperació d’un entorn complet després de fer canvis a una VM (demostracio).

---

### Alta Disponibilitat i Migracions

- **MigracioCalent.wmv**  
  Migració en calent d’una màquina virtual entre dos nodes Proxmox, sense downtime ni aturacio del servei.

- **MigracioVMCaidaNode.wmv**  
  Simulació de caiguda d’un node i migració automàtica de la màquina cap a un node disponible mitjançant sistema HA.

---

### Monitorització i Alertes

- **AlertaZabbix.wmv**  
  Recepció i gestió d’una alerta generada per Zabbix en cas de caiguda d'alguna VM del Proxmox i notificacio per correu i telegram.

- **SolucioAlertaZabbix.wmv**  
  Acció correctiva automatitzada i resolució de l’alerta generada anteriorment.

- **AlertaNetDataNode.wmv**  
  Detectació en temps real d'una caiguda d'un node de proxmox i la notificacio per discord.

- **RecuperacioAlertaNetData.wmv**  
  Normalització dels valors monitoritzats i confirmació automàtica de la recuperació de l’estat del node.

- **AfegirClientZabbix.wmv**  
  Procés complet per afegir un nou host al sistema de monitoratge Zabbix, amb assignació de plantilla i validació d’estat.

---

## Finalitat de les Demos

Aquest conjunt de vídeos té com a objectiu demostrar que l’entorn Outer Heaven:
- Funciona com una infraestructura real d’un ISP.
- Respon correctament davant escenaris de fallida i recuperació.
- Automatitza processos clau com backups, migracions i notificacions.
- Garanteix un entorn monitoritzat i auto-recuperable.

Els vídeos constitueixen **proves d’acceptació** i serveixen de referència per avaluar el projecte des de la perspectiva de fiabilitat, manteniment i escalabilitat.

