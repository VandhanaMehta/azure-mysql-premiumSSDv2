# Azure Database for MySQL on Premium SSD v2 - Private Preview (July 2026)

## What is being announced
Azure Database for MySQL on Premium SSD v2 (Managed Disks) is now available in Private Preview.

This preview focuses on:
- Ability to provision a Azure MySQL server on Premium SSD v2 (Managed Disks)
- Better price/performance potential through tunable storage performance
- Improved write latency and higher IOPS ceiling for demanding workloads
- End-to-end server lifecycle and managed operations for both HA and Non-HA scenarios in preview scope

## Why this matters
Premium SSD v2 enables independent tuning of storage size, IOPS, and throughput, which can help align performance and cost with workload needs.

## Supported Features (Private Preview scope at a glance)
- Non-HA server: create/delete, CRUD workflows (compute/storage/backup), managed operations, parameter updates
- HA server: create/update, force failover, zone selection, password reset
- Networking: Private Link, firewall rules, public access enable/disable, VNet-injected create disabled in preview
- Backup/Restore: automatic backup/list, on-demand backup (create/delete/schedule), fast restore, PITR
  
## Supported Regions
- Australia East, Brazil South, Canada Central, Central India, Central US, East Asia, Germany West Central, Italy North, Japan East, Japan West, Korea Central, Poland Central, South Africa North, Southeast Asia, Sweden Central

## Who should sign up
- Customers with high I/O and latency-sensitive workloads
- Teams planning MySQL 8.4 rollout on V6 compute
- Teams evaluating cost/performance optimization with tunable managed storage

## How to sign up
1. Complete the preview request form: [enrolment form](https://aka.ms/mysql-premium-ssdv2)
2. Wait for onboarding confirmation and allowlist communication from the product team

## Important preview notes
- Private Preview scope is limited and can change before Public Preview or GA
- Regional availability is controlled during onboarding
- As per Azure Private Preview guidance, this feature carries no SLA or formal support commitment. The product team provides best-effort assistance only. Production use is at the customer's discretion and risk until the feature reaches GA.

## Related files
- [Concepts and scope details](concepts-managed-disks.md)
- [Provisioning walkthrough](tutorial-managed-disks.md)

## References
- [Premium SSD v2 public reference pattern](https://learn.microsoft.com/en-us/azure/virtual-machines/disks-types#premium-ssd-v2)
- [v6 compute (AMD)](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes/general-purpose/dadsv6-series?tabs=sizebasic)
- [v6 compute (Intel)](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes/general-purpose/ddsv6-series?tabs=sizebasic)
