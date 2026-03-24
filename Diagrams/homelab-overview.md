## Homelab Overview

This diagram shows the structure of the homelab and how the different virtual machines interact.

The environment is built around a central DB-VM, which provides both database services (MariaDB) and shared storage via NFS to internal worker machines.

Client access is separated from direct database interaction by introducing a Web/App layer. Both worker machines can act as clients and access the system through the web application, which then communicates with the database.

Worker VM 1 (trainnet) operates in a dual role:
- as an internal worker accessing shared storage via NFS  
- as a client accessing the web application  

This setup demonstrates a clear separation between:
- client layer  
- application layer  
- database layer  

as well as centralized storage and role-based access within the system.
