# Mini Proyecto 1 - Plataforma de Virtualizacion con Proxmox VE

Este miniproyecto introduce y despliega un entorno de virtualización de alto rendimiento mediante **Proxmox VE**, un hipervisor de tipo 1 basado en Debian, altamente escalable y con soporte nativo para alta disponibilidad, gestión de VM/CT y almacenamiento distribuido.

## Objetivos

- Instalar y configurar Proxmox VE sobre una máquina física.
- Crear máquinas virtuales y contenedores con recursos optimizados.
- Teoría del sistema de redes (VLAN, bridges, bonding).

## Contenidos Clave

### 1. Instalacion de Proxmox
- Selección del disco adecuado para el sistema.
- Configuración de la IP de administración e interfaz web.

### 2. Creacion de maquinas virtuales
- Debian, win10, RHEL (y otros S.O.) con configuraciones optimizadas (vCPU, RAM, vGPU).
- Uso de VirtIO SCSI para mejorar el IO y reducir latencia.

### 3. Configuració de la Red
- Explicación teórica de Bridges y otros adaptadores de red.
- Teoría Bonding para mejorar ancho de banda y redundancia.
