## Project Progression

This project was developed step-by-step to gradually build a complete multi-VM environment.

---

### Phase 1 – Initial Setup
- Single DB-VM with MariaDB  
- Basic system setup  
- Initial testing of database functionality  

---

### Phase 2 – Adding Clients
- Introduction of Worker VM 1  
- Client-to-database interaction  
- Basic access testing  

---

### Phase 3 – Multi-Client Environment
- Added Worker VM 2  
- Introduced separate user roles  
- Simulated multiple users in the system  

---

### Phase 4 – Shared Storage (NFS)
- Implemented NFS on DB-VM  
- Workers mounted shared folder  
- Centralized file access introduced  

---

### Phase 5 – Application Layer
- Introduced Web/App VM  
- Clients now interact through application layer  
- Removed direct database access from clients  

---

### Phase 6 – Security Testing (Kali VM)
- Added Kali VM for controlled testing  
- Performed basic enumeration and testing  
- Identified a SQL injection vulnerability caused by improper input handling  

---

### Phase 7 – Security Improvement
- Fixed the SQL injection vulnerability using prepared statements  
- Improved handling of user input  
- Reduced exposure to injection attacks  

---

### Phase 8 – Verification
- Re-tested the application after applying fixes  
- Confirmed that injection attempts no longer succeeded  
- Validated that the vulnerability was properly mitigated  
