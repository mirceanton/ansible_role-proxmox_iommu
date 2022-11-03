Proxmox: IOMMU
==============

An Ansible role that enables IOMMU on a Proxmox VE host.

Requirements
------------

N/A.

Role Variables
--------------

**Required Variables**:

|         Variable         |  Type   |          Default          |                                Description                                 |
| :----------------------: | :-----: | :-----------------------: | :------------------------------------------------------------------------: |
| `proxmox_iommu_cmdline`  | string  | `intel_iommu=on iommu=pt` |                       The actual cmdline to append.                        |
| `proxmox_iommu_zfs_boot` | boolean |          `true`           | Whether the PVE host boots off ZFS (systemd-boot) or anything else (grub). |

Dependencies
------------

N/A.

Example Playbook
----------------

``` yml
---
- hosts: all
  remote_user: root

  roles:
    - role: mirceanton.proxmox_iommu
      vars:
        proxmox_iommu_zfs_boot: true
        proxmox_iommu_cmdline: intel_iommu=on iommu=pt pcie_acs_override=downstream pcie_acs_override=multifunction nofb nomodeset video=vesafb:off video=efifb:off video=simplefb:off initcall_blacklist=sysfb_init vga=off
```

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
