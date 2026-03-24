## Access Rights and Shared Resources

The homelab uses a centralized access model where the DB-VM provides shared resources and controls access for client machines.

---

### Shared Storage (NFS)

The DB-VM hosts a shared folder which is exposed to worker machines using NFS.

- Worker VM 1 and Worker VM 2 both have access to the shared storage  
- The shared folder is mounted remotely on each worker machine  
- Access is controlled through user permissions  

---

### User Roles

The environment simulates multiple users with different access levels.

#### Worker VM 1 (trainnet)
- Has access to shared storage via NFS  
- Acts both as a system participant and client  
- Uses credentials stored in plaintext (for demonstration purposes)  

#### Worker VM 2
- Has access to shared storage via NFS  
- Operates with different user permissions than Worker VM 1  
- Represents a separate user in the environment  

---

### Web Application Access

Both worker machines can access the web application.

- Access is performed through a login interface  
- Clients do not interact directly with the database  
- All database communication goes through the Web/App VM  

---

### Access Model Summary

- DB-VM controls data and shared storage  
- Worker machines access shared files via NFS  
- Clients access application services via Web/App VM  
- Direct access to the database is restricted  

---

### Purpose

This setup demonstrates:

- centralized resource management  
- separation of user roles  
- controlled access to shared data  
- indirect database interaction through an application layer  
