# Recursos Addicionals – Captures i Configuracions

Aquest directori conté un conjunt de **captures de pantalla i documents gràfics** utilitzats durant el desenvolupament, instal·lació i configuració de diferents serveis i entorns relacionats amb el projecte Outer Heaven. Es tracta d’informació complementària no inclosa en altres seccions principals, però que resulta útil com a **referència visual** i per validar la **traçabilitat del projecte**.

---

## Captures de Configuració de Serveis

Aquest apartat inclou proves i captures relacionades amb:

- Configuració de servidors DHCP.
- Configuració de perfils PPPoE.
- Pools d’adreces IP i gestió de VLANs.
- Connexió entre OLT i bridges.
- Serveis PPP Server, secrets, clients i validació de connexions.

Aquesta informació és clau per entendre com es va implementar el provisioning de clients i la segmentació de serveis dins la infraestructura de xarxa.

---

## `chr-ont/` – Simulació i gestió de l’ONT/OLT

Captures relacionades amb:

- Creació de bridges entre interfícies.
- Assignació de pools IP públics.
- Perfils de limitació d’ample de banda.
- Configuració del servidor PPPoE i secrets.
- Validació final de connexió des del client.

Aquestes proves representen la part més propera al comportament real d’un ISP, amb una estructura modular i escalable per a futurs clients.

---

## `hotelejemplo/` – Exemple de client hoteler

Inclou captures de configuració de xarxa per a un entorn hoteler:

- Creació de VLANs específiques.
- Pools DHCP per a usuaris finals.
- Configuració de NAT (masquerading).
- Validació des de màquines virtuals Windows.
- Assignació IP i visibilitat interna.

Serveix com a prova pilot de la segmentació d’un entorn hoteler típic dins la infraestructura simulada.

---

## `instalar proxmox/` – Instal·lació de Proxmox VE

Captures detallades del procés d’instal·lació del hipervisor Proxmox VE:

- Elecció de disc i sistema de fitxers ZFS.
- Configuració inicial de la IP de gestió.
- Instal·lació GUI i accés al node principal.

Aquest apartat ajuda a documentar el punt de partida per a la virtualització del projecte.

---

## `instalar truenas/` – Instal·lació de TrueNAS SCALE

Procés complet d’instal·lació de TrueNAS com a sistema d’emmagatzematge:

- Creació del pool principal.
- Configuració de datasets i permisos.
- Activació de serveis NFS, SMB i iSCSI.
- Preparació de recursos compartits per a la infraestructura virtual.

És l’origen del sistema de fitxers compartits que alimenta Proxmox i altres serveis crítics.

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

