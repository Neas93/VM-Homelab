## Virtual Machines

### Kali VM
Used for controlled testing and enumeration within the isolated lab environment.

- Scans services and open ports  
- Used to observe system exposure  
- Operates only inside the internal network  

---

### Web/App VM
Handles application logic and communication between clients and the database.

- Hosts web application (PHP / Docker-based setup)  
- Processes client requests  
- Sends queries to the database (DB-VM)  

---

### DB-VM
Acts as the central server in the environment.

- Hosts MariaDB database  
- Stores application data (users, accounts, transactions, etc.)  
- Hosts a shared folder accessible by worker machines  
- Exposes shared storage via NFS  
- Manages access and permissions  

This VM functions as both:

- database server  
- central storage server  

---

### Worker VM 1 (trainnet)
Acts in a dual role within the environment.

**System role:**
- Participates as part of the internal network  

**Client role:**
- Simulates a user accessing shared resources and services  
- Interacts with the web/app system  
- Uses credentials (intentionally stored insecurely for demonstration)  

This dual-role setup allows testing of both:

- system-level communication  
- user-level interaction  

---

### Worker VM 2
Simulates a separate client machine in the environment.

- Accesses shared folder on DB-VM via NFS  
- Operates with different user permissions than Worker VM 1  
- Represents a second user in the office setup  

---

## Summary
The environment consists of five virtual machines working together in an isolated network:

- 1 testing machine (Kali VM)  
- 1 application server (Web/App VM)  
- 1 central database and storage server (DB-VM)  
- 2 client machines with separate roles and permissions  

Shared resources are provided by the DB-VM and accessed remotely by worker machines using NFS.

This setup simulates a small office environment with centralized services, multiple users, and controlled testing conditions.
