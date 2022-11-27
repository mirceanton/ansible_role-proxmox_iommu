Proxmox: IOMMU
==============

An Ansible role that enables IOMMU on a Proxmox VE host.

Requirements
------------

N/A.

Role Variables
--------------

|              Variable              |  Type  |                       Description                        |
| :--------------------------------: | :----: | :------------------------------------------------------: |
|  `proxmox_iommu_cmdline_override`  | string | Override the auto-generated cmdline with this variable.  |
| `proxmox_iommu_boot_type_override` | string | Override the auto-detected boot type with this variable. |

Dependencies
------------

N/A.

Example Playbook
----------------

``` yml
---
- name: Enable IOMMU on all PVE hosts
  hosts: pve
  remote_user: root

  roles:
    - role: mirceanton.proxmox_iommu
```

LICENSE
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
