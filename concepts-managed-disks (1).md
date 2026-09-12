# Concepts: Managed Disks (Premium SSD v2) for Azure Database for MySQL

## Overview
Azure Database for MySQL Flexible Server Private Preview (July 2026) introduces Premium SSD v2 based managed storage. Premium SSD v2 enables independent configuration of storage capacity, IOPS, and throughput, allowing you to optimize storage performance based on your workload requirements.

Premium SSD v2 allows granular and independent tuning of:
- Storage capacity
- IOPS
- Throughput

This flexibility allows storage performance to scale independently of storage capacity, helping optimize both performance and cost as workload requirements evolve.

### Premium SSD v2 reference model (service pattern)
- Storage capacity range: 1 GiB to 32 TiB
- IOPS range: 3,000 - 12,000 (depending on storage size and compute selected)
- Throughput range: 125 MB/s - 1200 MB/s (depending on storage size and compute selected)

## What is supported in this Private Preview

### 1) Non-HA server
- Provision an Azure Database for MySQL 8.4 server using a v6 compute SKU and SSDv2 storage.
- Delete the server.
- Update compute, storage, and backup configurations.
- Perform managed operations, including start, stop, restart, and administrator password reset.
- Modify supported server parameters.

### 2) HA server
- Create a Zone-Redundant HA server using MySQL 8.4 and a v6 compute SKU.
- Create a Same-Zone (Local Redundant) HA server using MySQL 8.4 and a v6 compute SKU.
- Perform a manual failover between primary and standby nodes.
- Configure availability zones using either explicit zone selection or automatic placement.
- Reset the server administrator password.

### 3) Networking
- Public access with firewall rules.
- Private access with Private link for HA and non-HA server.
- Enable or disable public network access using Private Link.

### 4) Backup and Restore
- Automatic backup and backup listing
- Restore a server using Fast Restore.
- Configure backup retention days
- Restore a server to a specific point in time (PITR).

## Limitations and considerations (Private Preview)

### General Limitations
- Enabling or disabling high availability (HA) after server creation.
- Private link for HA servers is not supported.
- Some server parameter modifications are not supported. Only a subset of exposed server parameters can be modified during the preview.
- Restarting, compute scaling and private link for HA servers.
- Read replicas
- Fabric Mirroring
- Customer-managed keys (CMK)
- Geo-redundant backups amd storage auto-grow

### Maintenance Limitations
- Planned maintenance operations.
- Maintenance window configuration (Virtual Canary, SMW, CMW).
- Maintenance reschedule and reschedule-now operations.

### Monitoring and Diagnostic Limitations
- General metrics for HA and non-HA servers.
- Premium SSD v2 performance metrics (IOPS, throughput, storage capacity, etc.).
- Slow query and error logs via Server Logs.
- Slow query and error logs via Diagnostic Settings (Log Analytics, Storage Account, and Event Hub).
- Azure Monitor workbooks.


## Related
- [Announcement Page](README.md)
- [Provisioning tutorial](tutorial-managed-disks.md)

