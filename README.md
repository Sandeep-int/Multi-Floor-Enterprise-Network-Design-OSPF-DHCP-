## Project Title: Multi-Floor Enterprise Network Design (OSPF & DHCP)
# Objective
The primary objective was to architect a high-availability, multi-floor enterprise network utilizing a redundant "Triangle" core topology. The project focused on implementing dynamic routing for self-healing capabilities and centralized DHCP for automated infrastructure management across eight corporate departments.

## Laboratory Architecture
Core Layer: Deployed three Cisco 2911 Routers in a redundant serial mesh configuration to ensure 99.9% network uptime.
Access Layer: Utilized Cisco 2960 Switches distributed across three physical floors to manage local departmental traffic.
Segmentation: Established 8 distinct VLANs to isolate traffic for LOG, RECEPTION, STORE (Floor 1), FINANCE, HR, SALES (Floor 2), and IT/ADMIN (Floor 3).
Endpoints: Configured multiple Laptops and PCs to utilize automated IPv4 addressing.

# Technical Configuration
Dynamic Routing: Implemented OSPF Area 0 across all core routers, enabling automated route discovery and sub-second convergence.
Redundancy: Established high-speed Serial link connectivity between core nodes to eliminate single points of failure within the backbone.
Infrastructure Automation: Engineered centralized DHCP pools on core routers to manage complex multi-subnet IP distribution.
Management Security: Configured SSH for encrypted remote administrative access to all network infrastructure.
Address Optimization: Applied strategic IP Exclusions to protect gateway integrity and prevent address collisions within the DHCP pools.

#Testing & Validation
Routing Convergence: Verified full network synchronization by confirming OSPF "O" codes in the routing tables of all core nodes.
End-to-End Connectivity: Demonstrated a 100% success rate on ICMP pings for inter-floor communication, specifically from Floor 1 hosts to Floor 3 IT gateways.
Automation Verification: Validated successful DHCP lease assignments and correct subnet masking for all department endpoints.

# Technical Troubleshooting
OSPF Process Conflict: Diagnosed and resolved a dual-process ID mismatch (Process 1 vs. 10) on the Floor 3 router that was causing critical routing "blackouts".
Subnet Mask Triage: Identified and corrected a DHCP configuration error (Class B vs. Class C mask mismatch) that was inhibiting local gateway communication.
Conflict Mitigation: Resolved %DHCPD-4-PING_CONFLICT errors by re-evaluating and applying appropriate IP address exclusion ranges.

# SOC & Infrastructure Relevance
Business Continuity: Applied physical and logical redundancy concepts to ensure persistent network availability during simulated link failures.
Incident Response: Developed advanced CLI-based diagnostic and triage skills essential for rapid identification of network faults.
Security Architecture: Mastered VLAN isolation techniques fundamental to implementing modern Zero-Trust network security frameworks.
Enterprise Scalability: Practiced standardized, automated deployment workflows required for large-scale corporate infrastructure.
