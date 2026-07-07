# Tutorial: Provision Azure Database for MySQL with Premium SSD v2 (Private Preview)

## Goal
Provision a MySQL Flexible Server using Premium SSD v2 managed storage under Private Preview scope.

## Before you begin
- You have enrolled for the private preview of Azure Database for MySQL on Premium SSDv2 and are allowlisted.
- You have Azure subscription access with permission to create Azure Database for MySQL Server.

This tutorial describes the Azure portal flow used during Private Preview. Labels in the portal can change as the feature evolves.

## Inputs to decide upfront
- Server name
- Region
- MySQL version: 8.4
- Compute tier/SKU: V6 family in preview scope
- Storage type: Premium SSD v2
- Initial storage size (GiB)
- Target IOPS and throughput
- Networking mode: Public access + firewall or Private Link

## Step-by-step (Azure portal)

### Step 1: Start server creation
1. Open Azure portal.
2. Go to Azure Database for MySQL flexible server.
3. Select Advanced Create.

Screenshot placeholder: ./media/01-create-server-entry.png

### Step 2: Configure Storage and Compute
1. Choose subscription and resource group.
2. Enter server name.
3. Select a region approved for preview onboarding.
4. Select MySQL version 8.4.
5. Click on "Confugure Server" in Compute+Storage
6. In Storage, select Premium SSD v2.
5. Select supported V6 compute SKU.


Screenshot placeholder: ./media/02-storage-ssdv2-settings.png

### Step 3: Configure networking
1. Choose connectivity path: Public access + firewall rules, or Private Link
2. If public access is selected, add required client IP rules.


### Step 4: Review and create
1. Review all settings.
2. Select Create.


Note: Observed IOPS and throughput can vary by compute SKU, region, and workload profile.

## Related
- Announcement page: ./README.md
- Concepts and support matrix: ./concepts-managed-disks.md
