# Arreglar Clusters
### Nosotros usaremos de ejemplo el 172.30.30.X/27
### Recomiendo si no eres tan experto usar el NANO

## Stop the cluster services
```bash
systemctl stop pve-cluster
systemctl stop corosync
```
## Mount the filesystem locally
```bash
pmxcfs -l
```
## Edit the network interfaces file to have the new IP information
## Be sure to replace both the address and gateway
```bash
vi /etc/network/interfaces
```
## Replace any host entries with the new IP addresses
```bash
vi /etc/hosts
```
## Change the DNS server as necessary
```bash
vi /etc/resolv.conf
```
## Edit the corosync file and replace the old IPs with the new IPs for all hosts
#### :%s/172\.30\.30\./172.30.30./g   <- vi command to replace all instances
## BE SURE TO INCREMENT THE config_version: x LINE BY ONE TO ENSURE THE CONFIG IS NOT OVERWRITTEN
```bash
vi /etc/pve/corosync.conf
```
## Edit the known hosts file to have the correct IPs
## :%s/172\.30\.30\./172.30.30./g   <- vi command to replace all instances
```bash
/etc/pve/priv/known_hosts   
```
## If using ceph, edit the ceph configuration file to reflect the new network
## (thanks u/FortunatelyLethal)
#### :%s/172\.30\.30\./172.30.30./g   <- vi command to replace all instances
```bash
vi /etc/ceph/ceph.conf
```
## If you want to be granular... fix the IP in /etc/issue
```bash
vi /etc/issue
```
## Verify there aren't any stragglers with the old IP hanging around
```bash
cd /etc
grep -R '172\.30\.30\.' *
cd /var
grep -R '172\.30\.30\.' *
```
## Reboot the system to cleanly restart all the networking and services
```bash
reboot
```
## Referenced pages:
## - https://forum.proxmox.com/threads/change-cluster-nodes-ip-addresses.33406/
## - https://pve.proxmox.com/wiki/Cluster_Manager##_remove_a_cluster_node


### Fuente:
## - https://bookstack.dismyserver.net/books/documentation/page/how-to-change-the-ip-address-of-a-proxmox-clustered-node
