# Mini Projecte 1 - Plataforma de Virtualització amb Proxmox VE

Aquest mini projecte introdueix i desplega un entorn de virtualització d’alt rendiment mitjançant **Proxmox VE**, un hipervisor de tipus 1 basat en Debian,
altament escalable i amb suport nadiu per a alta disponibilitat, gestió de VM/CT i emmagatzematge distribuït.

## Objectius

- Instal·lar i configurar Proxmox VE sobre màquina física.
- Crear màquines virtuals i contenidors amb recursos optimitzats.
- Teoria del sistema de xarxes (VLAN, bridges, bonding).

## Continguts Clau

### 1. Instal·lació de Proxmox
- Selecció del disc adequat per al sistema.
- Configuració de la IP d’administració i interfície web.

### 2. Creació de màquines virtuals
- Ubuntu Desktop i Windows 10 amb configuracions optimitzades (vCPU, RAM, vGPU).
- Ús de VirtIO SCSI per millorar l’IO i reduir latència.

### 3. Configuració de Xarxa
- Explicacio Teorica de Bridges i altres adaptadors de xarxa
- Teoria Bonding per millorar ample de banda i redundància.

---

## 📎 Documents relacionats

- `instalar proxmox/`: Captures i processos d’instal·lació manual.
- `RepararCluster.md`: Resolució d’errors en Corosync o nodes no sincronitzats.
- `ProxmoxYTrueNAS/`: Configuració combinada de Proxmox i emmagatzematge TrueNAS.
