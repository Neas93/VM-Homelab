## Network Setup

The homelab is built as an isolated multi-VM environment using an internal virtual network.

All virtual machines are connected to the same internal network, allowing them to communicate with each other while remaining separated from external networks.

---

### Network Characteristics

- Internal virtual network (no external exposure)  
- All VMs can communicate within the lab  
- No direct access from outside the environment  

This setup provides a safe environment for testing and experimentation.

---

### Communication Flow

The environment follows a structured communication model:

- Clients (Worker VMs) access the system through the Web/App VM  
- The Web/App VM communicates with the DB-VM  
- The DB-VM provides database services (MariaDB)  

Direct access from clients to the database is not used.

---

### Shared Storage (NFS)

The DB-VM exposes a shared folder via NFS.

- Worker VM 1 and Worker VM 2 mount the shared storage  
- File access is performed over the internal network  
- The Web/App VM is not involved in this process  

---

### Purpose

This network design allows:

- controlled communication between systems  
- separation between clients, application layer, and database  
- safe testing without affecting external systems  
