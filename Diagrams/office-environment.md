## Office Environment

The setup consists of two worker machines connected to a central DB-VM, which provides shared storage via NFS.

Both worker machines access the same shared resources, but operate with different user permissions. This allows simulation of a small office environment where multiple users interact with centralized systems while maintaining separate access rights.

Worker VM 1 (trainnet) operates in a dual role:
- as part of the internal system (worker)
- as a client accessing services and shared resources  

Worker VM 2 represents a separate user with different permissions, allowing testing of role-based access and user separation.

The DB-VM acts as the central point for:
- shared storage (via NFS)  
- access control and permissions  

This setup demonstrates:
- centralized resource management  
- remote access to shared data  
- separation of user roles  
- realistic multi-user interaction within a controlled environment
