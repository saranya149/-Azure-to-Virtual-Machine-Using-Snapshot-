# Azure VM Recovery Using Disk Snapshot

## Overview
This project demonstrates how to back up and recover a Microsoft Azure Virtual Machine using a managed disk snapshot. A snapshot is a read-only, point-in-time copy of a disk. It can be used to restore a VM after data loss, corruption, or a failed change.

## Objective
- Create a snapshot of the VM's OS disk
- Create a new managed disk from the snapshot
- Deploy a new VM using the restored disk
- Verify that the recovered VM runs correctly and the data is intact

## Architecture / Workflow

    Azure VM (OS Disk) → Snapshot → Managed Disk (from Snapshot) → Recovered VM

## Prerequisites
- An active Microsoft Azure subscription
- A running Azure Virtual Machine
- Access to the Azure Portal with permission to create disks and VMs

## Implementation Steps

### 1. Create a Snapshot
1. Open the Azure Portal and go to **Snapshots > Create**.
2. Select the subscription, resource group, and region.
3. Set the source type to **Disk** and select the VM's OS disk.
4. Choose the storage type and click **Review + create**.

### 2. Create a Managed Disk from the Snapshot
1. Open the snapshot and click **Create disk**.
2. Provide a disk name, resource group, and size.
3. Click **Review + create**.

### 3. Create a New VM from the Restored Disk
1. Open the new disk and click **Create VM**.
2. Configure the VM name, size, networking, and region.
3. Click **Review + create** and deploy.

### 4. Verify the Recovery
1. Connect to the new VM (SSH / RDP).
2. Confirm the OS boots and the data is intact.

## Use Cases
- Backup and recovery of Azure VMs
- Safe rollback before OS upgrades or configuration changes
- Cloning VMs for testing and development
- Moving VMs across regions or subscriptions

## Snapshot vs Azure Backup

| Feature | Snapshot | Azure Backup |
|---|---|---|
| Method | Manual, one-time | Automated, policy-based |
| Retention | Short-term | Long-term |
| Best for | Quick rollback | Production protection |

## Tools & Services Used
- Microsoft Azure Portal
- Azure Virtual Machines
- Azure Managed Disks
- Azure Snapshots

## Documentation
Step-by-step screenshots: [snap vm to recovery 1.pdf](./snap%20vm%20to%20recovery%201.pdf)

## Key Learnings
- Created and managed disk snapshots in Azure
- Restored a VM from a snapshot
- Understood the difference between snapshots and Azure Backup

## Author
**Saranya T**
GitHub: [saranya149](https://github.com/saranya149)
