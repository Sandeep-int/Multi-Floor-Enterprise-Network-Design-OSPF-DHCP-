## Multi-Floor Enterprise Network Design (OSPF & DHCP)

# Objective
- To architect and deploy a high-availability, multi-floor enterprise network featuring a redundant "Triangle" core topology. The project focuses on implementing dynamic routing for self-healing and centralized DHCP for automated infrastructure management across 8 departments.

# Lab Architecture
- 3x Cisco 2911 Routers (Redundant Serial Mesh)
- Cisco 2960 Switches (Floor Distribution)
- 8 Departments/VLANs (LOG, RECEPTION, STORE, FINANCE, HR, SALES, IT, ADMIN)
- Multiple Endpoints (Laptops & PCs)

# Configuration Performed
- Dynamic Routing: Implemented OSPF Area 0 for automated route discovery and fast convergence
- Redundancy: Established Serial link connectivity between core routers to eliminate single points of failure
- Infrastructure Automation: Engineered centralized DHCP pools on routers for multi-subnet IP management
- Management Security: Configured SSH for encrypted remote administrative access
- Address Optimization: Applied strategic IP Exclusions to prevent gateway address collisions

# Testing & Validation
- Verified full OSPF convergence through routing table inspection ("O" codes)
- Confirmed 100% ICMP success rate for inter-floor communication (e.g., Floor 1 to Floor 3)
- Validated successful DHCP lease assignments for departmental laptops

# Troubleshooting
- OSPF Conflict: Resolved dual-process ID mismatch on the Floor 3 router causing routing blackouts
- Subnet Mismatch: Identified and corrected DHCP configuration errors (Class B vs. Class C mask)
- IP Conflicts: Mitigated %DHCPD-4-PING_CONFLICT errors using appropriate exclusion ranges

# SOC & Infrastructure Relevance
- Business Continuity: Implemented redundancy to ensure persistent uptime during link failures
- Incident Response: Developed advanced CLI-based diagnostic skills for rapid network triage
- Segmentation: Mastered VLAN isolation techniques fundamental to Zero-Trust architectures
- Scalability: Practiced automated deployment workflows required for large-scale environments

# Evidence
- 
