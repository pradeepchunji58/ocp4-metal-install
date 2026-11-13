Backup and Restore of ETCD/Cluster State







\## 📌 Question



When you install RHCOS on these physical servers and configure their MAC addresses and IP addresses, how does OpenShift ensure that the correct server receives the correct Ignition configuration and becomes a Bootstrap, Control Plane, or Worker node?





\## 📜 Explain the complete flow:



MAC Address → DHCP/PXE/Provisioning → IP Address → RHCOS → Ignition → Node Role



Also explain whether the Ignition file itself identifies the MAC address and decides whether the server is a Control Plane or Worker, or whether another component is responsible for mapping the physical server to the appropriate Ignition file.





bootstrap.ign

master.ign

worker.ign









incase the above didnt work -- Follow this



CubenSquare Lab Access - VMware ESXi

&#x20;

Lab time: 13 Nov 2026, 10:00 AM to 13 Nov 2026, 02:00 PM IST. Access stops automatically at the end time.

&#x20;

1\. Open: https://esxi.cubensquare.com (Chrome incognito recommended)

2\. Login email: pradeepchunji58@gmail.com -> a one-time PIN is sent to this email

3\. ESXi login: username pradip password LabTxwclFrY975!

&#x20;

Lab rules:

\- Name every VM you create starting with 'pradip-' (e.g. pradip-bastion)

\- ISOs: datastore1 -> ISO/

\- VM Network = internet (DHCP only, never set a static IP on it)

\- Do not touch VMs that are not yours

\- Your VMs are powered off automatically at the end time

username Pradip

LabTxwclFrY975!



root

Admin@123



useradd admin

passwd admin@123





usermod -aG wheel username



su - admin



sudo whoami



##### openshift-4.22.X       -1.99  - bast



**openshift-install-linux**

https://mirror.openshift.com/pub/openshift-v4/x86\_64/clients/ocp/stable/openshift-install-linux.tar.gz



&#x20;     

**openshift-client-linux**



https://mirror.openshift.com/pub/openshift-v4/x86\_64/clients/ocp/stable/openshift-client-linux.tar.gz





**rhcos-4.22.21-x86\_64-metal**



https://mirror.openshift.com/pub/openshift-v4/x86\_64/dependencies/rhcos/latest/rhcos-4.22.21-x86\_64-metal.x86\_64.raw.gz



https://github.com/cubensquare/ocp4-metal-install.git



ens34- 192.16.1.99

ens35- 192.16.22.95     - > 192.16.22.1  - > intenal ip / no internet zone within the port 



boot	00:0c:29:49:af:b3

contpl   00:0c:29:a2:75:1e

work     00:0c:29:34:a2:04



